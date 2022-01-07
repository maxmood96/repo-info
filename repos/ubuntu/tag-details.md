<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `ubuntu`

-	[`ubuntu:14.04`](#ubuntu1404)
-	[`ubuntu:16.04`](#ubuntu1604)
-	[`ubuntu:18.04`](#ubuntu1804)
-	[`ubuntu:20.04`](#ubuntu2004)
-	[`ubuntu:21.04`](#ubuntu2104)
-	[`ubuntu:21.10`](#ubuntu2110)
-	[`ubuntu:22.04`](#ubuntu2204)
-	[`ubuntu:bionic`](#ubuntubionic)
-	[`ubuntu:bionic-20220105`](#ubuntubionic-20220105)
-	[`ubuntu:devel`](#ubuntudevel)
-	[`ubuntu:focal`](#ubuntufocal)
-	[`ubuntu:focal-20220105`](#ubuntufocal-20220105)
-	[`ubuntu:hirsute`](#ubuntuhirsute)
-	[`ubuntu:hirsute-20211208`](#ubuntuhirsute-20211208)
-	[`ubuntu:impish`](#ubuntuimpish)
-	[`ubuntu:impish-20220105`](#ubuntuimpish-20220105)
-	[`ubuntu:jammy`](#ubuntujammy)
-	[`ubuntu:jammy-20220101`](#ubuntujammy-20220101)
-	[`ubuntu:latest`](#ubuntulatest)
-	[`ubuntu:rolling`](#ubunturolling)
-	[`ubuntu:trusty`](#ubuntutrusty)
-	[`ubuntu:trusty-20191217`](#ubuntutrusty-20191217)
-	[`ubuntu:xenial`](#ubuntuxenial)
-	[`ubuntu:xenial-20210804`](#ubuntuxenial-20210804)

## `ubuntu:14.04`

```console
$ docker pull ubuntu@sha256:60840958b25b5947b11d7a274274dc48ab32a2f5d18527f5dae2962b64269a3a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le

### `ubuntu:14.04` - linux; amd64

```console
$ docker pull ubuntu@sha256:881afbae521c910f764f7187dbfbca3cc10c26f8bafa458c76dda009a901c29d
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.8 MB (70764430 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13b66b487594a1f2b75396013bc05d29d9f527852d96c5577cc4f187559875d0`
-	Default Command: `["\/bin\/bash"]`

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

### `ubuntu:14.04` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:534255069ef3adf1c7a555fd9f614845ab66c61ef9846e438d86e12ae8c89b88
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.7 MB (64700978 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2cd03315989aa8326f2c276922d3969994c1304b1310d2e0d33a26d94dd68ea`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 13 Jul 2021 23:23:03 GMT
ADD file:e9d55e059869915743a8ca8e64582d23c48fe7e90e439daccd56d3e08e8673b4 in / 
# Tue, 13 Jul 2021 23:23:06 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Tue, 13 Jul 2021 23:23:07 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Tue, 13 Jul 2021 23:23:09 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Tue, 13 Jul 2021 23:23:10 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:0db3a87a3d7959895fd860c8b924980adda6e77f5d315b6676a4ac0e12518978`  
		Last Modified: Thu, 19 Dec 2019 06:16:01 GMT  
		Size: 64.6 MB (64624015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0c5cd1be699257153c2a6de85968c2d9c413d87470dc4f540c5c3decbca8e47`  
		Last Modified: Tue, 13 Jul 2021 23:28:27 GMT  
		Size: 76.8 KB (76774 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecbf1c32ebce749806713a088af6ff1cbf7c75a8132d310ff391948e3e611ef6`  
		Last Modified: Tue, 13 Jul 2021 23:28:26 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:14.04` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:5dc82d0f897a1bfd6a68db5b2c3692d81e5ea04e31a09664edc420689f8b450c
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.5 MB (66525481 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7304c635fe5273ccdfbc8a38e839c9089350fc8e80daf57394d1f7a9c5a70c86`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 16 Oct 2021 01:48:09 GMT
ADD file:b0eb0db52e323748ea9b8d7f8aecbc523a747619cd08663bab0fe60ab59bc60e in / 
# Sat, 16 Oct 2021 01:48:12 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Sat, 16 Oct 2021 01:48:13 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Sat, 16 Oct 2021 01:48:14 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Sat, 16 Oct 2021 01:48:14 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:d1a5a1e51f251c3431dec02e2cc8d157e92d1b46913708ce9e600747a6274977`  
		Last Modified: Thu, 19 Dec 2019 03:57:08 GMT  
		Size: 66.5 MB (66466219 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5fc464c2dc9f9ce8d7fe9ccd36f4e746ce32b39f19590f519a8cd3dd76827f8`  
		Last Modified: Sat, 16 Oct 2021 01:50:15 GMT  
		Size: 59.1 KB (59100 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:561f253b7549524704fe8cc1da5ebd27d77bc1a1424b0632b683d90eb58e73d3`  
		Last Modified: Sat, 16 Oct 2021 01:50:15 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:14.04` - linux; 386

```console
$ docker pull ubuntu@sha256:88152195106ff09bade23cb5aacfd26c381a8835c9d42124b4cba1dc3c2475e4
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.4 MB (68445499 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f18ba408bae1426c4f394e045b16a140bc555e520d5eaacc97ac60ac5f298313`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 25 Mar 2021 22:57:06 GMT
ADD file:e034601a525da53b0f39bb04d6e2264e2a592d0ae7c21e00697b9b62ca1efec9 in / 
# Thu, 25 Mar 2021 22:57:08 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 25 Mar 2021 22:57:10 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 25 Mar 2021 22:57:12 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 25 Mar 2021 22:57:12 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:630712fe5783a35ad52a7026002143cb4f8fe65d34097dcaa4c4331b1b059a17`  
		Last Modified: Thu, 19 Dec 2019 04:44:02 GMT  
		Size: 68.4 MB (68380440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ea2d50b5278097c6d027fc9fc0caf006649fcd94f094dde6ce578abe865ff21`  
		Last Modified: Thu, 25 Mar 2021 22:58:27 GMT  
		Size: 64.9 KB (64870 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5795a499c24598e294527992a703053ab615879af048f3b809a3ad86141684d`  
		Last Modified: Thu, 25 Mar 2021 22:58:27 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:14.04` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:12d9fa858f255e4b70827aff83e8ce37b6fcaddaf6732276aa1f0763402f4fdc
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.4 MB (73443156 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02949c650aebaafb917ebe6bfd55a42505e22b38e8370878164051da4ae1bcc3`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 13 Jul 2021 23:24:04 GMT
ADD file:581665e92c72c8638b40fe509de6479dc1a5d7b5ffe8d6706006178c406e35e2 in / 
# Tue, 13 Jul 2021 23:24:24 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Tue, 13 Jul 2021 23:24:33 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Tue, 13 Jul 2021 23:24:42 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Tue, 13 Jul 2021 23:24:45 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:bed4146d918c6c9a57bc3a8bf829e702975b0e53c7f25920fe9435b58ed6b64f`  
		Last Modified: Thu, 19 Dec 2019 04:26:52 GMT  
		Size: 73.4 MB (73379539 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12aab203a69be44b1617f0da6b00b670e9016c3b00ab311b384ac3f859e86613`  
		Last Modified: Tue, 13 Jul 2021 23:29:07 GMT  
		Size: 63.4 KB (63430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1576c78d220b27404b5d0c3d635c36524229553e3ccf3b9a5ad4ca93c216c6c6`  
		Last Modified: Tue, 13 Jul 2021 23:29:07 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ubuntu:16.04`

```console
$ docker pull ubuntu@sha256:0f71fa8d4d2d4292c3c617fda2b36f6dabe5c8b6e34c3dc5b0d17d4e704bd39c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `ubuntu:16.04` - linux; amd64

```console
$ docker pull ubuntu@sha256:a3785f78ab8547ae2710c89e627783cfa7ee7824d3468cae6835c9f4eae23ff7
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.5 MB (46499103 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6f50765242581c887ff1acc2511fa2d885c52d8fb3ac8c4bba131fd86567f2e`
-	Default Command: `["\/bin\/bash"]`

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

### `ubuntu:16.04` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:b722e2654241f9681f4719dce7aa16a2f0c35769e17a636f5b39a33967d1aeb8
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.3 MB (40313783 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:033c410d53efaab9e847168b94fea14d551788200a15f4d2424c84e4cd2ab8a2`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 31 Aug 2021 01:42:28 GMT
ADD file:294a94a081de785c730003a440a0530a85add2bcb60c0f5bc4ce7ee17867ac4e in / 
# Tue, 31 Aug 2021 01:42:30 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Tue, 31 Aug 2021 01:42:31 GMT
RUN rm -rf /var/lib/apt/lists/*
# Tue, 31 Aug 2021 01:42:33 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Tue, 31 Aug 2021 01:42:33 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:b95ba076a26b98e98eac4b43596b59c20d1e61a36bcaf2afae3aeebadc8844cf`  
		Last Modified: Sun, 08 Aug 2021 01:00:22 GMT  
		Size: 40.3 MB (40312250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48547e29bdd75abab2cbd318d0739f4092117ce9d04e7b8f20c36674abd65e59`  
		Last Modified: Tue, 31 Aug 2021 01:46:36 GMT  
		Size: 851.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ebef378167277f2a504e20691b3f74632e59e23c5761cb5e602a634aa32b1b9`  
		Last Modified: Tue, 31 Aug 2021 01:46:37 GMT  
		Size: 511.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f97155dfcb43995751a1533d2e37802f3b35f78bd9b0eaf5049f79f56199ac90`  
		Last Modified: Tue, 31 Aug 2021 01:46:36 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:16.04` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:70fa660340a344b46cc56b3606dc8abd3bf48b5cbce13d01c720e9793a6bc3c0
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.2 MB (41240746 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe3b34cb9255c8dd390f85c8fe37e6fbe6ac555f86c7e8944cd68da2de2f7633`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 16 Oct 2021 01:48:22 GMT
ADD file:3c6dc937cb7b4c81b42126f377d23320ec1d0a8ca34d38e7c45871f1d08dac43 in / 
# Sat, 16 Oct 2021 01:48:22 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Sat, 16 Oct 2021 01:48:23 GMT
RUN rm -rf /var/lib/apt/lists/*
# Sat, 16 Oct 2021 01:48:24 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Sat, 16 Oct 2021 01:48:25 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:828b35a09f0b2f3d1dead43aa2468ff5eba6c463423b3fff7ee6d150f6fd1b6b`  
		Last Modified: Thu, 05 Aug 2021 00:25:09 GMT  
		Size: 41.2 MB (41239253 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:238e9b8fdf46981043813ae269c4420735959dd01d4d15c420b66448523e9adc`  
		Last Modified: Sat, 16 Oct 2021 01:50:40 GMT  
		Size: 848.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d5b1b49195905e9415adfe3583301316ef591d794fcfd12b5cd29103fa7ee6b`  
		Last Modified: Sat, 16 Oct 2021 01:50:40 GMT  
		Size: 473.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:269a6c6175ba12a0fd708883c2625167711f111f24ce2bb79221fda132487e57`  
		Last Modified: Sat, 16 Oct 2021 01:50:40 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:16.04` - linux; 386

```console
$ docker pull ubuntu@sha256:4a6759446930ee402a2091605c0911f237ad18b5c250a535d11563d9402eb15a
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.8 MB (45817719 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac20e7c3411697a4a85c1cb30850f77b8238e0a0ef0e176ca8f0e763066eed4b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 31 Aug 2021 01:39:31 GMT
ADD file:a4ae521feddf8357667e9361bdd972a69ed945f3857cc8c534652592e432575d in / 
# Tue, 31 Aug 2021 01:39:32 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Tue, 31 Aug 2021 01:39:33 GMT
RUN rm -rf /var/lib/apt/lists/*
# Tue, 31 Aug 2021 01:39:34 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Tue, 31 Aug 2021 01:39:34 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:1335d7ebdbbb7325d434cf945bcb54cb20f7288e1ca2a1cf140ae02b324646e6`  
		Last Modified: Sun, 08 Aug 2021 01:00:22 GMT  
		Size: 45.8 MB (45816182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c250dcd0b24a66322cdee2165435035a76e5b72085df234bfcdc340c5321c74d`  
		Last Modified: Tue, 31 Aug 2021 01:40:23 GMT  
		Size: 851.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df3c7bbf9087c9dae9eb48a2b2a913146a0705560689407ee02802ff92408abf`  
		Last Modified: Tue, 31 Aug 2021 01:40:23 GMT  
		Size: 514.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ea45938bfbd7dd3f314ea2ad08a94370db722a20c33d6407c8eaeaf906b40c5`  
		Last Modified: Tue, 31 Aug 2021 01:40:23 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:16.04` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:cf25d111d193288d47d20a4e5d42a68dc2af24bb962853b067752eca3914355e
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.5 MB (47523633 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:914466c340b7c02825333f4de2597bcd673f18eb0cec83840b13a3cc68338937`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 31 Aug 2021 02:12:03 GMT
ADD file:c84969ed4d4e336ec5996e26e35261f683b36f1af7a978df587296ef5e7a2627 in / 
# Tue, 31 Aug 2021 02:12:21 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Tue, 31 Aug 2021 02:12:31 GMT
RUN rm -rf /var/lib/apt/lists/*
# Tue, 31 Aug 2021 02:12:46 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Tue, 31 Aug 2021 02:12:49 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:5057452c10cfe2216f39949f909f3cd83002d256d1bbd564ae242352a5460fe2`  
		Last Modified: Sun, 08 Aug 2021 01:00:30 GMT  
		Size: 47.5 MB (47522137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c76cb7ccfe1638448c02d9e8f51fae873202f130515c9fb7a791038a2bd9586`  
		Last Modified: Tue, 31 Aug 2021 02:15:30 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22a12ad70abdfd318d55001c9a70e7eccffb1f5ece5eee88d8e4e549083928a9`  
		Last Modified: Tue, 31 Aug 2021 02:15:30 GMT  
		Size: 474.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4e2d97c60bc4668c8613c3ef5ffe0205d9be50368dfe09cb0859beb030ed103`  
		Last Modified: Tue, 31 Aug 2021 02:15:30 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:16.04` - linux; s390x

```console
$ docker pull ubuntu@sha256:5fea5a070916f61785140faa8e16fa8bf7ca3f152ceed9c48154f8aca4c3667e
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.1 MB (44089219 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bdb8683432fbdd1ec03145305370c4ec7079b01e22fcc47dd4df1aa862463474`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 31 Aug 2021 01:43:07 GMT
ADD file:8719dec76e2491e6bcc4cba5072d8123bd3472e72108280ea29f6a34761adbeb in / 
# Tue, 31 Aug 2021 01:43:10 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Tue, 31 Aug 2021 01:43:11 GMT
RUN rm -rf /var/lib/apt/lists/*
# Tue, 31 Aug 2021 01:43:11 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Tue, 31 Aug 2021 01:43:11 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:80d499f9d46bfeec5260ce5a395259ab5e54118e786a0e9023d6550a57730bd4`  
		Last Modified: Tue, 31 Aug 2021 01:45:04 GMT  
		Size: 44.1 MB (44087722 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:883d7cfe3e67b3dd7ffd87697a9050dfad287116e1f38ed165b815d7285a7d70`  
		Last Modified: Tue, 31 Aug 2021 01:44:59 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05e68cf162fecf9f82ab0d540cd0f3af1a4a74defc8ba9434379cbae3a09b30c`  
		Last Modified: Tue, 31 Aug 2021 01:44:59 GMT  
		Size: 478.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bfcc45f37d760e154b69274e44e31fd64b8537f3cb1cba39203b537246bc891`  
		Last Modified: Tue, 31 Aug 2021 01:44:59 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ubuntu:18.04`

```console
$ docker pull ubuntu@sha256:37b7471c1945a2a12e5a57488ee4e3e216a8369d0b9ee1ec2e41db9c2c1e3d22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `ubuntu:18.04` - linux; amd64

```console
$ docker pull ubuntu@sha256:81d5a9161533bba27b2fcc6475228ff2348c82f7bb610bcd97880a100f8e4d5c
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.7 MB (26705027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:886eca19e6118615a5089b4f60f614d2e2b49afdfbde2e43438de15bbaefe23f`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 07 Jan 2022 02:25:21 GMT
ADD file:2aa3e79e3cff3c048612744ac310cf86bc27de3433d420711bafc6612445befc in / 
# Fri, 07 Jan 2022 02:25:21 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:2f94e549220aea96f00cae7eb95f401e61b41a16cc5eb0b4ea592d0ce871930a`  
		Last Modified: Thu, 06 Jan 2022 23:50:21 GMT  
		Size: 26.7 MB (26705027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:18.04` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:c81b7fc895f08fbd59c9130ebc8d7b70842d4ca2a00ab2f8c16e09ee40caa874
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.3 MB (22303634 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d352c919ae0ee17c392eebda5c54380a346a875bd17b84f3e6b1854c43980f48`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 07 Jan 2022 02:26:03 GMT
ADD file:04c050ae3b998115f9e3f0da295a93a62bdff5d2efc3c37e792665d263cbf804 in / 
# Fri, 07 Jan 2022 02:26:04 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:db4feefed17933b9e08cd0d0fd6c63db5c115552848576f2bc2062c8c5f69628`  
		Last Modified: Fri, 07 Jan 2022 02:30:10 GMT  
		Size: 22.3 MB (22303634 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:18.04` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:963f8ca4f8dcda72717dfbe53617aa2a705dc8ebf01abe9d9922f4bedb4825b0
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.7 MB (23726915 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df8edc186894d22d1f425f0a490b3a5c3a2af96f27f836f4dad58274cbbbbe15`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 07 Jan 2022 01:53:37 GMT
ADD file:def71737de83b2ed2d5ddb5520331ef14ccd496fc11b4f830b79318dd65164a3 in / 
# Fri, 07 Jan 2022 01:53:38 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:976e4515cbe3bb05d3eaff6aa830f00c2593211ff7600840d5e9a030c803bbee`  
		Last Modified: Fri, 07 Jan 2022 01:55:15 GMT  
		Size: 23.7 MB (23726915 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:18.04` - linux; 386

```console
$ docker pull ubuntu@sha256:4a2efd378fc094a2b78f4478d88d8c02a828bb3adf551b903cdfe24ac0ea852f
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.2 MB (27156435 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a311310981abfb6655a8639d5b28c7f149338d659d0ee503784328f23030ec6`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 07 Jan 2022 01:39:03 GMT
ADD file:4992040d291a9a6b53435279ff532c15e004fd7c7b35aa4783850a06ccff0694 in / 
# Fri, 07 Jan 2022 01:39:04 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:cd8c855b84a6297384d4a364fec672137f3aef84749b319ee5158b568545eb0f`  
		Last Modified: Fri, 07 Jan 2022 01:39:50 GMT  
		Size: 27.2 MB (27156435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:18.04` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:3523581fac0c7d6872d26685f85d723311eda60630badaaada600acae20e5c02
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.4 MB (30432347 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:850f01bec948177956a3fc87e23c6884fecb0e78f4e094812156b92918e546bc`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 07 Jan 2022 02:19:52 GMT
ADD file:e29b7078eb9c78ec6f3931c4beea820e4b7fe5d0d02e02e220c083dcd603aad1 in / 
# Fri, 07 Jan 2022 02:19:55 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:f130035f6453da800db2a1c34f617d35285297b1e549cc5fe138db9ecb704f0b`  
		Last Modified: Fri, 07 Jan 2022 02:22:21 GMT  
		Size: 30.4 MB (30432347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:18.04` - linux; s390x

```console
$ docker pull ubuntu@sha256:391c3aa91581859dab57e004603ed2d040d30d64a13adfc65cfc31f7d0bc1818
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.4 MB (25362136 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6572fc6b779b474dbe4d0f2ba7cc6850855ae2c2a4f5a20cbf721b82e93e5b2e`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 07 Jan 2022 01:42:09 GMT
ADD file:caefb9be68fabe0b9b7dba683dabb869e5165a5a13534742d73a489a3712d9a9 in / 
# Fri, 07 Jan 2022 01:42:12 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:7587f9252eef493a02840102ba78c74de317d3d47f6d568af5602ff6c1c54a20`  
		Last Modified: Fri, 07 Jan 2022 01:43:57 GMT  
		Size: 25.4 MB (25362136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ubuntu:20.04`

```console
$ docker pull ubuntu@sha256:b5a61709a9a44284d88fb12e5c48db0409cfad5b69d4ff8224077c57302df9cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; riscv64
	-	linux; s390x

### `ubuntu:20.04` - linux; amd64

```console
$ docker pull ubuntu@sha256:57df66b9fc9ce2947e434b4aa02dbe16f6685e20db0c170917d4a1962a5fe6a9
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.6 MB (28566425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d13c942271d66cb0954c3ba93e143cd253421fe0772b8bed32c4c0077a546d4d`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 07 Jan 2022 02:25:29 GMT
ADD file:122ad323412c2e70b3138d8eb62648c4692989de91be1ffb6b4bf086c8311b62 in / 
# Fri, 07 Jan 2022 02:25:30 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:ea362f368469f909a95f9a6e54ebe0121ce0a8e3c30583dd9c5fb35b14544dec`  
		Last Modified: Thu, 06 Jan 2022 15:07:12 GMT  
		Size: 28.6 MB (28566425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:20.04` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:06bd529675558f58ea2aa4bb0f2442a073750e5d3b8c6d1f7e180b59b056f238
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.1 MB (24064434 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4273349cd30895098e846fcd0b542d97732d2c33a433267e48634fa5aa45fc9`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 07 Jan 2022 02:26:25 GMT
ADD file:ac83e0dc7e48a0dc1805c0fd7b71b8eb119b3eeafd1fdcab93e11fbc9c0bcda0 in / 
# Fri, 07 Jan 2022 02:26:26 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:9b8080fa0945580f29aa3abed4664f8ab849229eca04510b5d259a9e29616064`  
		Last Modified: Fri, 07 Jan 2022 02:30:39 GMT  
		Size: 24.1 MB (24064434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:20.04` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:64162ac111b666daf1305de1888eb67a3033f62000f5ff781fe529aff8f88b09
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.2 MB (27171074 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f4877540c734dfd8ee2e523b1487788f871e64a4f3137797d33e5971ac9adde`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 07 Jan 2022 01:53:45 GMT
ADD file:521a8ada4ac06e6f7720904486d481d216a8c3e08c0c7db1376c39a33e709668 in / 
# Fri, 07 Jan 2022 01:53:45 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:5f3d23ccb99f6c9462a15efcf35aef0863858073a06d56df671d0e791b26222a`  
		Last Modified: Fri, 07 Jan 2022 01:55:32 GMT  
		Size: 27.2 MB (27171074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:20.04` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:edb1aa0254b14fd8d321fc5b8b2ccf73cea79bd8c18d690bc52f1e4a810ac409
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.3 MB (33286892 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a4c29dc93ac6b035392b13201bdf0e145386248a5473522dba4c2ee619ff32f`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 07 Jan 2022 02:20:15 GMT
ADD file:014236839eaee978894ae0bd6aecc246177a0a2c11af73f86d9cfafe5478ce18 in / 
# Fri, 07 Jan 2022 02:20:19 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:e6e6dea5a8cc4bdc9e5e51e2bfa948159b69d5fbc2dca99bc41776fb04dab967`  
		Last Modified: Fri, 07 Jan 2022 02:22:43 GMT  
		Size: 33.3 MB (33286892 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:20.04` - linux; riscv64

```console
$ docker pull ubuntu@sha256:bc700522fdbb6d8fa43a6800954e3f12c6990df7e344649c05eafac375aa4dcf
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.2 MB (24226982 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3459adb1e25a18e53fc9834550294901f7461cb2dec65efbaeff4bf5c9737cc`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 07 Jan 2022 02:16:06 GMT
ADD file:8c67f745313efae2d5d96d237357fdd8bd6ea54c3f198c07010bf1bce663d48c in / 
# Fri, 07 Jan 2022 02:16:08 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:8c703baf60b6c639070fea2dcfc339570983cdb4555d172e28f82e765410e364`  
		Last Modified: Fri, 07 Jan 2022 02:34:37 GMT  
		Size: 24.2 MB (24226982 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:20.04` - linux; s390x

```console
$ docker pull ubuntu@sha256:0081dfc53722a9cf4be7067ef069d102889dea63ed7536ddef1f6d2666fd1de0
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.1 MB (27120999 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:851f3d9fd80317037249fb42643a20742a38a8112130ff428e48c1c914d5ee9b`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 07 Jan 2022 01:42:20 GMT
ADD file:b6119f4fcd6a113749f515278b315ffd96aecce7006f086acb060f981e5c59db in / 
# Fri, 07 Jan 2022 01:42:22 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:6d200361446626b53394c2a1a520a74a1221795562eac9b318c58e0abe147e23`  
		Last Modified: Fri, 07 Jan 2022 01:44:09 GMT  
		Size: 27.1 MB (27120999 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ubuntu:21.04`

```console
$ docker pull ubuntu@sha256:041767af88d66339ef063abfecb0e8052f776460325b8a2b91f5394938d27281
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; riscv64
	-	linux; s390x

### `ubuntu:21.04` - linux; amd64

```console
$ docker pull ubuntu@sha256:fd367579637b6c083eaddb9a21ac4a2f63d1e02a4ca2671d7e57c24ee3764deb
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.7 MB (31703311 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64cdc469caaa7cee68b06410692f436ff4a1d8b314577a83f4e6400cc2dfc1ff`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 07 Jan 2022 02:25:37 GMT
ADD file:cfcb96e25bf4af2949d0c04953666b16dca08216ded8040ddfeedd0e782c6ddc in / 
# Fri, 07 Jan 2022 02:25:38 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:318226705d6bf4f94a70707b917c9bea2190a83f512b1c257dffbb691859831e`  
		Last Modified: Tue, 14 Dec 2021 13:10:17 GMT  
		Size: 31.7 MB (31703311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:21.04` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:e0e5f03210d623b83cd8fc30d4f9e4099c6e541e4a44ef04f47cbbffa76d18d3
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.9 MB (26860386 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7b078fa17f59892eaf4ffe618fa9cf8774564f764cd9f5011534613b0996e73`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 07 Jan 2022 02:26:48 GMT
ADD file:b5bafdb9006674a167988c876664fe5c9986ad3472147327f21401be96959a6c in / 
# Fri, 07 Jan 2022 02:26:48 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:f72a97c294933ef5ddaab06415361fb5ebd9a11c5a2652c06e97c5c7e6ebefaa`  
		Last Modified: Tue, 14 Dec 2021 13:11:38 GMT  
		Size: 26.9 MB (26860386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:21.04` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:70493c1293aac4d5e1b49284cd4a82ebf64634892875f5b564ceda827f76d4f3
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.2 MB (30175274 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f17f05e89a1671c20c8d32c69a6b323973fbc471a8a45ff6b7e3c6e756e3ebe`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 07 Jan 2022 01:53:53 GMT
ADD file:53760a4a864d7c22beaf50ceaaceb7114cf6e4d285c9c4e41bddcb4ee83a71cd in / 
# Fri, 07 Jan 2022 01:53:53 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:a2edff5d3cccb200e40a203e356b5409a32f6982fc3cb50d5dfa39ecb3402d0f`  
		Last Modified: Tue, 14 Dec 2021 13:11:05 GMT  
		Size: 30.2 MB (30175274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:21.04` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:73ec4cde47ba5a97eee6cf67594b1e2477da3c22a1afbc6677dc5687b51e6df2
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.3 MB (37256256 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb1722ce1cf10ab1ddf29417410556bcb48908dfe1de137b6e0dccbe2014375a`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 07 Jan 2022 02:20:30 GMT
ADD file:9356fd6fd5fe8e2698a7935a4f9e731784a123135fbbac56c0a64aba4ff055d8 in / 
# Fri, 07 Jan 2022 02:20:34 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:9e0f94572fe4babd7bb8b4026de5bab1243bfc425d3ef7113aab8ad7c891c73f`  
		Last Modified: Tue, 14 Dec 2021 13:12:16 GMT  
		Size: 37.3 MB (37256256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:21.04` - linux; riscv64

```console
$ docker pull ubuntu@sha256:24d503e08f07e16761b7e6a3046a03b90e303a0a93292868cb14a234ceabd477
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.1 MB (27142124 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f55f171d7b38cdde4cce8bf874a39bfbe1c432746aeeef80514ee5a3c5b9732`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 07 Jan 2022 02:18:08 GMT
ADD file:88bfbe1378489e66f6bc7226898a5fbf2fa4921a2a9f8368035d39f3f9e7879e in / 
# Fri, 07 Jan 2022 02:18:09 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:a42cee3150e09146966460b6ef66d449ef9ab179df8c79c79444cbf84185ca45`  
		Last Modified: Tue, 14 Dec 2021 13:12:53 GMT  
		Size: 27.1 MB (27142124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:21.04` - linux; s390x

```console
$ docker pull ubuntu@sha256:9967da8c3c3248fc78eab07882cbf502b8007eaf347027519dbc926997358493
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.5 MB (32506835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c28770469e05cdf7ac3d0b8be3b4c1ae8c993ca1c283603db1520c208baa8250`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 07 Jan 2022 01:42:31 GMT
ADD file:0ab8d0c606111287c48ef013f6e2c33f36b1f35018d55a975462a5bd8a3ba1d7 in / 
# Fri, 07 Jan 2022 01:42:33 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:d7416c72715444586e1570693d4643393f777728e1eebec0c79ccefc15b81acc`  
		Last Modified: Tue, 14 Dec 2021 13:13:27 GMT  
		Size: 32.5 MB (32506835 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ubuntu:21.10`

```console
$ docker pull ubuntu@sha256:cfc189b67f53b322b0ceaabacfc9e2414c63435f362348807fe960d0fbce5ada
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; riscv64
	-	linux; s390x

### `ubuntu:21.10` - linux; amd64

```console
$ docker pull ubuntu@sha256:28941e0c8e9be8c6aa586be8c7ae3074c81ed915cb5b5836853985d756fb46e2
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.4 MB (30377796 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64c59b1065b1ea628a7253ea0e5e87234e764fe3612ced48c495bb0f2de60a85`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 07 Jan 2022 02:25:45 GMT
ADD file:f8a2d8d5948f5e12d6d04bf3b60fdbe16956e3a0d5486994c3088f3c9ddfe3b6 in / 
# Fri, 07 Jan 2022 02:25:45 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:688b037d2a94faed4d0a662851a3612e2a23a9e0e2636b9fc84be4f45a05f698`  
		Last Modified: Fri, 07 Jan 2022 02:27:28 GMT  
		Size: 30.4 MB (30377796 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:21.10` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:33965bb123b32366424d2f837f48e7793d4c879e0157b2a886c3a59b05180529
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.9 MB (26918664 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c5bd2c1ab61832ce70760e1f1aadd4099dccd69084b3d20db7538a20c77d2c6`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 07 Jan 2022 02:27:09 GMT
ADD file:1943eb8161d1853aa98adec6971ce80e67c5ef8deafcefaa8809addbc3eee806 in / 
# Fri, 07 Jan 2022 02:27:10 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:2d5d37c142fbf68de0a42ff73e6ce8a0826e64699a992a9f245b81d99456b441`  
		Last Modified: Fri, 07 Jan 2022 02:31:42 GMT  
		Size: 26.9 MB (26918664 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:21.10` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:cd8c34bca231c3bc85141170cde83763cb6cbf1ceb74550178e549125f2bbad9
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.0 MB (29026221 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a5119fc922bda6dc97dd851b40203a71403c35765b2413bf16187d5f369d339`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 07 Jan 2022 01:54:01 GMT
ADD file:313dff926c3a3dbea803ddccb86e973465260b7b2618bcbe33892115f68a773b in / 
# Fri, 07 Jan 2022 01:54:01 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:f0ffaea8604435228e4901f528ec20078ee34a6050875405766fd95208f0c31f`  
		Last Modified: Fri, 07 Jan 2022 01:56:10 GMT  
		Size: 29.0 MB (29026221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:21.10` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:5a7abe42cbb7b56ef2b7033c970cdb2561c888e6b56855be3f8eb6a0fd2420e2
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.2 MB (36174729 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7dc8aa3f2f3bb8749e361794f031649f81c39a898c749e3f05f2680cea407a7`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 07 Jan 2022 02:20:45 GMT
ADD file:6c52e72233bc011d6cc1943cc59283ed3def1a426a7cf3b9b8a03320a1de85ac in / 
# Fri, 07 Jan 2022 02:20:48 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:5e28f686135f4d211abc5a5fe924bd23a6fee36d43e23d37529639850f708a22`  
		Last Modified: Fri, 07 Jan 2022 02:23:31 GMT  
		Size: 36.2 MB (36174729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:21.10` - linux; riscv64

```console
$ docker pull ubuntu@sha256:f754ba1e1c296e6c2829454e7b6dee03bea619db93de1a9daf79a035445e92f5
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.2 MB (27207318 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e45ed113f979ce70402d70dcbe4d2cf0d583d04d5c4658a39dd5455bf71b476`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 07 Jan 2022 02:19:54 GMT
ADD file:80d7cfc8a88ccc3ac0dd24dfba95a65c7e24cc96f880a61736d5ab358db84912 in / 
# Fri, 07 Jan 2022 02:19:56 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:41481709d1b8a29bbdd69a8df35aeab07866245eed21a54aa5f2d183351e4569`  
		Last Modified: Fri, 07 Jan 2022 02:39:10 GMT  
		Size: 27.2 MB (27207318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:21.10` - linux; s390x

```console
$ docker pull ubuntu@sha256:4c5b76c0baf3a991fd734c73ed6d0d40787dbf24afcf60aaf9962ab1f62654f0
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.5 MB (30526144 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b2af0eb503e8f19260c6db71780890dc9a7164118f04a8581f23c4dd5c29901`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 07 Jan 2022 01:42:43 GMT
ADD file:d2d689ec5bbbbec520f5fc8ea75e1d642f177a30c5937027ca800b3a9ccf5b83 in / 
# Fri, 07 Jan 2022 01:42:45 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:77bd6b10105ec281aabfad8249bf82b48478e0eac3503dccd5d75db49b1dd586`  
		Last Modified: Fri, 07 Jan 2022 01:44:35 GMT  
		Size: 30.5 MB (30526144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ubuntu:22.04`

```console
$ docker pull ubuntu@sha256:0ad36748089181d832164977bdeb56d08672e352173127d8bfcd9aa4f7b3bd41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; riscv64
	-	linux; s390x

### `ubuntu:22.04` - linux; amd64

```console
$ docker pull ubuntu@sha256:74075bbbd941a1766a0db1d66e617a0ab82ab54dd23e0b55bebd7e62d9e9b7be
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.5 MB (30501041 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c68f8d0eb3f063896e40d4ef7652b2901eeb2d35281104a4d2132d8df4ba9e34`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 07 Jan 2022 02:25:53 GMT
ADD file:7fa9713fdcdef2552cd85dc53d57c2f444a09798fd2254d68f2f955cc1114ab7 in / 
# Fri, 07 Jan 2022 02:25:53 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:25f4cd1d54a5120c409f812234ad6f2266a5ae22fe0cf58c3ffab80bedc4368c`  
		Last Modified: Fri, 07 Jan 2022 02:27:47 GMT  
		Size: 30.5 MB (30501041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:22.04` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:572beed80a67a6184fade4720c815f1d72242a6474a6ed88c0fdcbe3863f29d2
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.6 MB (27564608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eafb6ceae367630169b067d6ff2eaaa704ea2dc470b63e765448fc1c7548b27c`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 07 Jan 2022 02:27:32 GMT
ADD file:8718f314f447f7d0c389825500d5ceb026028c337363ef130cdcf6125750046e in / 
# Fri, 07 Jan 2022 02:27:33 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:152d82d6f338fbb1e956a78af2d045c6fc15f4c5352ab546d88118f037a1a4e5`  
		Last Modified: Fri, 07 Jan 2022 02:32:16 GMT  
		Size: 27.6 MB (27564608 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:22.04` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:073e060cec31fed4a86fcd45ad6f80b1f135109ac2c0b57272f01909c9626486
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.9 MB (28921769 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63a4636836063b8f0d2297a5df988c114bed06c3989c4585630f1f808271451c`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 07 Jan 2022 01:54:09 GMT
ADD file:d75d592836ef38b5620858a3eb1666af50f390695066b7b3432f365e1cc3a56b in / 
# Fri, 07 Jan 2022 01:54:10 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:a9ca93140713b0208e2ea5b1925e67a506893717f9d1ff5aa2097ad25d2ffd59`  
		Last Modified: Fri, 07 Jan 2022 01:56:30 GMT  
		Size: 28.9 MB (28921769 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:22.04` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:910a9c3d7b81e15b0b4e07c1bb6153c00b5609a383c8940ebf51a653d115230d
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.3 MB (36323413 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27d6b27e00447e7b536d840bdeaede3e641f6cf351c0688b9cb2ba4327a5fbde`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 07 Jan 2022 02:21:00 GMT
ADD file:ee7ea12d6a8f311929a29ce03c167071ec7ae0e38a90c35118926fa9ee0881a6 in / 
# Fri, 07 Jan 2022 02:21:04 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:d7e91abaf3158b413cf53113f304d05a30a09d1920db39a3eaa08c8c5da337fd`  
		Last Modified: Fri, 07 Jan 2022 02:23:54 GMT  
		Size: 36.3 MB (36323413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:22.04` - linux; riscv64

```console
$ docker pull ubuntu@sha256:afc637a71adf6e5324b37ad3a1f005e2c28703ddaec376581103df6c2e86805b
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.2 MB (28205700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2555b7864f3f9d8a4ef30c58887ac62eea38960574da93eb4ea03c9699e0d349`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 07 Jan 2022 02:21:55 GMT
ADD file:fb3b5a3e5efdc1d60cfffdd3cff88b09a96f8d9c5fd22023cfa826992be407da in / 
# Fri, 07 Jan 2022 02:21:57 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:939152979f37020f3d9c4352564dab069f4ae0c7d16abbe222f7721f7f9543ef`  
		Last Modified: Fri, 07 Jan 2022 02:41:41 GMT  
		Size: 28.2 MB (28205700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:22.04` - linux; s390x

```console
$ docker pull ubuntu@sha256:d6c91889a7d4e92152af9aa33e8a8902ad37b05a287f8744b9c21bcfe85f11fd
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.4 MB (29387057 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74956f997a30cfd4b88964886f260e9751c5fde79ec202f151f31d8275378f85`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 07 Jan 2022 01:42:53 GMT
ADD file:63122dcff09feadc66081fd2b45b3e3de924cf0f111e8515c56594154aabde6e in / 
# Fri, 07 Jan 2022 01:42:56 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:a0ea954c58d9a01dec91e416a4d333a9fcdca5f2b6512986d1201c7c1763d0b2`  
		Last Modified: Fri, 07 Jan 2022 01:44:50 GMT  
		Size: 29.4 MB (29387057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ubuntu:bionic`

```console
$ docker pull ubuntu@sha256:37b7471c1945a2a12e5a57488ee4e3e216a8369d0b9ee1ec2e41db9c2c1e3d22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `ubuntu:bionic` - linux; amd64

```console
$ docker pull ubuntu@sha256:81d5a9161533bba27b2fcc6475228ff2348c82f7bb610bcd97880a100f8e4d5c
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.7 MB (26705027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:886eca19e6118615a5089b4f60f614d2e2b49afdfbde2e43438de15bbaefe23f`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 07 Jan 2022 02:25:21 GMT
ADD file:2aa3e79e3cff3c048612744ac310cf86bc27de3433d420711bafc6612445befc in / 
# Fri, 07 Jan 2022 02:25:21 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:2f94e549220aea96f00cae7eb95f401e61b41a16cc5eb0b4ea592d0ce871930a`  
		Last Modified: Thu, 06 Jan 2022 23:50:21 GMT  
		Size: 26.7 MB (26705027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:bionic` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:c81b7fc895f08fbd59c9130ebc8d7b70842d4ca2a00ab2f8c16e09ee40caa874
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.3 MB (22303634 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d352c919ae0ee17c392eebda5c54380a346a875bd17b84f3e6b1854c43980f48`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 07 Jan 2022 02:26:03 GMT
ADD file:04c050ae3b998115f9e3f0da295a93a62bdff5d2efc3c37e792665d263cbf804 in / 
# Fri, 07 Jan 2022 02:26:04 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:db4feefed17933b9e08cd0d0fd6c63db5c115552848576f2bc2062c8c5f69628`  
		Last Modified: Fri, 07 Jan 2022 02:30:10 GMT  
		Size: 22.3 MB (22303634 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:bionic` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:963f8ca4f8dcda72717dfbe53617aa2a705dc8ebf01abe9d9922f4bedb4825b0
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.7 MB (23726915 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df8edc186894d22d1f425f0a490b3a5c3a2af96f27f836f4dad58274cbbbbe15`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 07 Jan 2022 01:53:37 GMT
ADD file:def71737de83b2ed2d5ddb5520331ef14ccd496fc11b4f830b79318dd65164a3 in / 
# Fri, 07 Jan 2022 01:53:38 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:976e4515cbe3bb05d3eaff6aa830f00c2593211ff7600840d5e9a030c803bbee`  
		Last Modified: Fri, 07 Jan 2022 01:55:15 GMT  
		Size: 23.7 MB (23726915 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:bionic` - linux; 386

```console
$ docker pull ubuntu@sha256:4a2efd378fc094a2b78f4478d88d8c02a828bb3adf551b903cdfe24ac0ea852f
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.2 MB (27156435 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a311310981abfb6655a8639d5b28c7f149338d659d0ee503784328f23030ec6`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 07 Jan 2022 01:39:03 GMT
ADD file:4992040d291a9a6b53435279ff532c15e004fd7c7b35aa4783850a06ccff0694 in / 
# Fri, 07 Jan 2022 01:39:04 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:cd8c855b84a6297384d4a364fec672137f3aef84749b319ee5158b568545eb0f`  
		Last Modified: Fri, 07 Jan 2022 01:39:50 GMT  
		Size: 27.2 MB (27156435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:bionic` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:3523581fac0c7d6872d26685f85d723311eda60630badaaada600acae20e5c02
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.4 MB (30432347 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:850f01bec948177956a3fc87e23c6884fecb0e78f4e094812156b92918e546bc`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 07 Jan 2022 02:19:52 GMT
ADD file:e29b7078eb9c78ec6f3931c4beea820e4b7fe5d0d02e02e220c083dcd603aad1 in / 
# Fri, 07 Jan 2022 02:19:55 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:f130035f6453da800db2a1c34f617d35285297b1e549cc5fe138db9ecb704f0b`  
		Last Modified: Fri, 07 Jan 2022 02:22:21 GMT  
		Size: 30.4 MB (30432347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:bionic` - linux; s390x

```console
$ docker pull ubuntu@sha256:391c3aa91581859dab57e004603ed2d040d30d64a13adfc65cfc31f7d0bc1818
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.4 MB (25362136 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6572fc6b779b474dbe4d0f2ba7cc6850855ae2c2a4f5a20cbf721b82e93e5b2e`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 07 Jan 2022 01:42:09 GMT
ADD file:caefb9be68fabe0b9b7dba683dabb869e5165a5a13534742d73a489a3712d9a9 in / 
# Fri, 07 Jan 2022 01:42:12 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:7587f9252eef493a02840102ba78c74de317d3d47f6d568af5602ff6c1c54a20`  
		Last Modified: Fri, 07 Jan 2022 01:43:57 GMT  
		Size: 25.4 MB (25362136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ubuntu:bionic-20220105`

```console
$ docker pull ubuntu@sha256:37b7471c1945a2a12e5a57488ee4e3e216a8369d0b9ee1ec2e41db9c2c1e3d22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `ubuntu:bionic-20220105` - linux; amd64

```console
$ docker pull ubuntu@sha256:81d5a9161533bba27b2fcc6475228ff2348c82f7bb610bcd97880a100f8e4d5c
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.7 MB (26705027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:886eca19e6118615a5089b4f60f614d2e2b49afdfbde2e43438de15bbaefe23f`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 07 Jan 2022 02:25:21 GMT
ADD file:2aa3e79e3cff3c048612744ac310cf86bc27de3433d420711bafc6612445befc in / 
# Fri, 07 Jan 2022 02:25:21 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:2f94e549220aea96f00cae7eb95f401e61b41a16cc5eb0b4ea592d0ce871930a`  
		Last Modified: Thu, 06 Jan 2022 23:50:21 GMT  
		Size: 26.7 MB (26705027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:bionic-20220105` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:c81b7fc895f08fbd59c9130ebc8d7b70842d4ca2a00ab2f8c16e09ee40caa874
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.3 MB (22303634 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d352c919ae0ee17c392eebda5c54380a346a875bd17b84f3e6b1854c43980f48`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 07 Jan 2022 02:26:03 GMT
ADD file:04c050ae3b998115f9e3f0da295a93a62bdff5d2efc3c37e792665d263cbf804 in / 
# Fri, 07 Jan 2022 02:26:04 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:db4feefed17933b9e08cd0d0fd6c63db5c115552848576f2bc2062c8c5f69628`  
		Last Modified: Fri, 07 Jan 2022 02:30:10 GMT  
		Size: 22.3 MB (22303634 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:bionic-20220105` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:963f8ca4f8dcda72717dfbe53617aa2a705dc8ebf01abe9d9922f4bedb4825b0
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.7 MB (23726915 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df8edc186894d22d1f425f0a490b3a5c3a2af96f27f836f4dad58274cbbbbe15`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 07 Jan 2022 01:53:37 GMT
ADD file:def71737de83b2ed2d5ddb5520331ef14ccd496fc11b4f830b79318dd65164a3 in / 
# Fri, 07 Jan 2022 01:53:38 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:976e4515cbe3bb05d3eaff6aa830f00c2593211ff7600840d5e9a030c803bbee`  
		Last Modified: Fri, 07 Jan 2022 01:55:15 GMT  
		Size: 23.7 MB (23726915 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:bionic-20220105` - linux; 386

```console
$ docker pull ubuntu@sha256:4a2efd378fc094a2b78f4478d88d8c02a828bb3adf551b903cdfe24ac0ea852f
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.2 MB (27156435 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a311310981abfb6655a8639d5b28c7f149338d659d0ee503784328f23030ec6`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 07 Jan 2022 01:39:03 GMT
ADD file:4992040d291a9a6b53435279ff532c15e004fd7c7b35aa4783850a06ccff0694 in / 
# Fri, 07 Jan 2022 01:39:04 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:cd8c855b84a6297384d4a364fec672137f3aef84749b319ee5158b568545eb0f`  
		Last Modified: Fri, 07 Jan 2022 01:39:50 GMT  
		Size: 27.2 MB (27156435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:bionic-20220105` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:3523581fac0c7d6872d26685f85d723311eda60630badaaada600acae20e5c02
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.4 MB (30432347 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:850f01bec948177956a3fc87e23c6884fecb0e78f4e094812156b92918e546bc`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 07 Jan 2022 02:19:52 GMT
ADD file:e29b7078eb9c78ec6f3931c4beea820e4b7fe5d0d02e02e220c083dcd603aad1 in / 
# Fri, 07 Jan 2022 02:19:55 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:f130035f6453da800db2a1c34f617d35285297b1e549cc5fe138db9ecb704f0b`  
		Last Modified: Fri, 07 Jan 2022 02:22:21 GMT  
		Size: 30.4 MB (30432347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:bionic-20220105` - linux; s390x

```console
$ docker pull ubuntu@sha256:391c3aa91581859dab57e004603ed2d040d30d64a13adfc65cfc31f7d0bc1818
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.4 MB (25362136 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6572fc6b779b474dbe4d0f2ba7cc6850855ae2c2a4f5a20cbf721b82e93e5b2e`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 07 Jan 2022 01:42:09 GMT
ADD file:caefb9be68fabe0b9b7dba683dabb869e5165a5a13534742d73a489a3712d9a9 in / 
# Fri, 07 Jan 2022 01:42:12 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:7587f9252eef493a02840102ba78c74de317d3d47f6d568af5602ff6c1c54a20`  
		Last Modified: Fri, 07 Jan 2022 01:43:57 GMT  
		Size: 25.4 MB (25362136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ubuntu:devel`

```console
$ docker pull ubuntu@sha256:0ad36748089181d832164977bdeb56d08672e352173127d8bfcd9aa4f7b3bd41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; riscv64
	-	linux; s390x

### `ubuntu:devel` - linux; amd64

```console
$ docker pull ubuntu@sha256:74075bbbd941a1766a0db1d66e617a0ab82ab54dd23e0b55bebd7e62d9e9b7be
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.5 MB (30501041 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c68f8d0eb3f063896e40d4ef7652b2901eeb2d35281104a4d2132d8df4ba9e34`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 07 Jan 2022 02:25:53 GMT
ADD file:7fa9713fdcdef2552cd85dc53d57c2f444a09798fd2254d68f2f955cc1114ab7 in / 
# Fri, 07 Jan 2022 02:25:53 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:25f4cd1d54a5120c409f812234ad6f2266a5ae22fe0cf58c3ffab80bedc4368c`  
		Last Modified: Fri, 07 Jan 2022 02:27:47 GMT  
		Size: 30.5 MB (30501041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:devel` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:572beed80a67a6184fade4720c815f1d72242a6474a6ed88c0fdcbe3863f29d2
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.6 MB (27564608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eafb6ceae367630169b067d6ff2eaaa704ea2dc470b63e765448fc1c7548b27c`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 07 Jan 2022 02:27:32 GMT
ADD file:8718f314f447f7d0c389825500d5ceb026028c337363ef130cdcf6125750046e in / 
# Fri, 07 Jan 2022 02:27:33 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:152d82d6f338fbb1e956a78af2d045c6fc15f4c5352ab546d88118f037a1a4e5`  
		Last Modified: Fri, 07 Jan 2022 02:32:16 GMT  
		Size: 27.6 MB (27564608 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:devel` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:073e060cec31fed4a86fcd45ad6f80b1f135109ac2c0b57272f01909c9626486
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.9 MB (28921769 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63a4636836063b8f0d2297a5df988c114bed06c3989c4585630f1f808271451c`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 07 Jan 2022 01:54:09 GMT
ADD file:d75d592836ef38b5620858a3eb1666af50f390695066b7b3432f365e1cc3a56b in / 
# Fri, 07 Jan 2022 01:54:10 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:a9ca93140713b0208e2ea5b1925e67a506893717f9d1ff5aa2097ad25d2ffd59`  
		Last Modified: Fri, 07 Jan 2022 01:56:30 GMT  
		Size: 28.9 MB (28921769 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:devel` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:910a9c3d7b81e15b0b4e07c1bb6153c00b5609a383c8940ebf51a653d115230d
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.3 MB (36323413 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27d6b27e00447e7b536d840bdeaede3e641f6cf351c0688b9cb2ba4327a5fbde`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 07 Jan 2022 02:21:00 GMT
ADD file:ee7ea12d6a8f311929a29ce03c167071ec7ae0e38a90c35118926fa9ee0881a6 in / 
# Fri, 07 Jan 2022 02:21:04 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:d7e91abaf3158b413cf53113f304d05a30a09d1920db39a3eaa08c8c5da337fd`  
		Last Modified: Fri, 07 Jan 2022 02:23:54 GMT  
		Size: 36.3 MB (36323413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:devel` - linux; riscv64

```console
$ docker pull ubuntu@sha256:afc637a71adf6e5324b37ad3a1f005e2c28703ddaec376581103df6c2e86805b
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.2 MB (28205700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2555b7864f3f9d8a4ef30c58887ac62eea38960574da93eb4ea03c9699e0d349`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 07 Jan 2022 02:21:55 GMT
ADD file:fb3b5a3e5efdc1d60cfffdd3cff88b09a96f8d9c5fd22023cfa826992be407da in / 
# Fri, 07 Jan 2022 02:21:57 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:939152979f37020f3d9c4352564dab069f4ae0c7d16abbe222f7721f7f9543ef`  
		Last Modified: Fri, 07 Jan 2022 02:41:41 GMT  
		Size: 28.2 MB (28205700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:devel` - linux; s390x

```console
$ docker pull ubuntu@sha256:d6c91889a7d4e92152af9aa33e8a8902ad37b05a287f8744b9c21bcfe85f11fd
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.4 MB (29387057 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74956f997a30cfd4b88964886f260e9751c5fde79ec202f151f31d8275378f85`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 07 Jan 2022 01:42:53 GMT
ADD file:63122dcff09feadc66081fd2b45b3e3de924cf0f111e8515c56594154aabde6e in / 
# Fri, 07 Jan 2022 01:42:56 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:a0ea954c58d9a01dec91e416a4d333a9fcdca5f2b6512986d1201c7c1763d0b2`  
		Last Modified: Fri, 07 Jan 2022 01:44:50 GMT  
		Size: 29.4 MB (29387057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ubuntu:focal`

```console
$ docker pull ubuntu@sha256:b5a61709a9a44284d88fb12e5c48db0409cfad5b69d4ff8224077c57302df9cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; riscv64
	-	linux; s390x

### `ubuntu:focal` - linux; amd64

```console
$ docker pull ubuntu@sha256:57df66b9fc9ce2947e434b4aa02dbe16f6685e20db0c170917d4a1962a5fe6a9
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.6 MB (28566425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d13c942271d66cb0954c3ba93e143cd253421fe0772b8bed32c4c0077a546d4d`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 07 Jan 2022 02:25:29 GMT
ADD file:122ad323412c2e70b3138d8eb62648c4692989de91be1ffb6b4bf086c8311b62 in / 
# Fri, 07 Jan 2022 02:25:30 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:ea362f368469f909a95f9a6e54ebe0121ce0a8e3c30583dd9c5fb35b14544dec`  
		Last Modified: Thu, 06 Jan 2022 15:07:12 GMT  
		Size: 28.6 MB (28566425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:focal` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:06bd529675558f58ea2aa4bb0f2442a073750e5d3b8c6d1f7e180b59b056f238
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.1 MB (24064434 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4273349cd30895098e846fcd0b542d97732d2c33a433267e48634fa5aa45fc9`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 07 Jan 2022 02:26:25 GMT
ADD file:ac83e0dc7e48a0dc1805c0fd7b71b8eb119b3eeafd1fdcab93e11fbc9c0bcda0 in / 
# Fri, 07 Jan 2022 02:26:26 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:9b8080fa0945580f29aa3abed4664f8ab849229eca04510b5d259a9e29616064`  
		Last Modified: Fri, 07 Jan 2022 02:30:39 GMT  
		Size: 24.1 MB (24064434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:focal` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:64162ac111b666daf1305de1888eb67a3033f62000f5ff781fe529aff8f88b09
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.2 MB (27171074 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f4877540c734dfd8ee2e523b1487788f871e64a4f3137797d33e5971ac9adde`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 07 Jan 2022 01:53:45 GMT
ADD file:521a8ada4ac06e6f7720904486d481d216a8c3e08c0c7db1376c39a33e709668 in / 
# Fri, 07 Jan 2022 01:53:45 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:5f3d23ccb99f6c9462a15efcf35aef0863858073a06d56df671d0e791b26222a`  
		Last Modified: Fri, 07 Jan 2022 01:55:32 GMT  
		Size: 27.2 MB (27171074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:focal` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:edb1aa0254b14fd8d321fc5b8b2ccf73cea79bd8c18d690bc52f1e4a810ac409
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.3 MB (33286892 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a4c29dc93ac6b035392b13201bdf0e145386248a5473522dba4c2ee619ff32f`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 07 Jan 2022 02:20:15 GMT
ADD file:014236839eaee978894ae0bd6aecc246177a0a2c11af73f86d9cfafe5478ce18 in / 
# Fri, 07 Jan 2022 02:20:19 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:e6e6dea5a8cc4bdc9e5e51e2bfa948159b69d5fbc2dca99bc41776fb04dab967`  
		Last Modified: Fri, 07 Jan 2022 02:22:43 GMT  
		Size: 33.3 MB (33286892 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:focal` - linux; riscv64

```console
$ docker pull ubuntu@sha256:bc700522fdbb6d8fa43a6800954e3f12c6990df7e344649c05eafac375aa4dcf
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.2 MB (24226982 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3459adb1e25a18e53fc9834550294901f7461cb2dec65efbaeff4bf5c9737cc`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 07 Jan 2022 02:16:06 GMT
ADD file:8c67f745313efae2d5d96d237357fdd8bd6ea54c3f198c07010bf1bce663d48c in / 
# Fri, 07 Jan 2022 02:16:08 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:8c703baf60b6c639070fea2dcfc339570983cdb4555d172e28f82e765410e364`  
		Last Modified: Fri, 07 Jan 2022 02:34:37 GMT  
		Size: 24.2 MB (24226982 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:focal` - linux; s390x

```console
$ docker pull ubuntu@sha256:0081dfc53722a9cf4be7067ef069d102889dea63ed7536ddef1f6d2666fd1de0
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.1 MB (27120999 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:851f3d9fd80317037249fb42643a20742a38a8112130ff428e48c1c914d5ee9b`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 07 Jan 2022 01:42:20 GMT
ADD file:b6119f4fcd6a113749f515278b315ffd96aecce7006f086acb060f981e5c59db in / 
# Fri, 07 Jan 2022 01:42:22 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:6d200361446626b53394c2a1a520a74a1221795562eac9b318c58e0abe147e23`  
		Last Modified: Fri, 07 Jan 2022 01:44:09 GMT  
		Size: 27.1 MB (27120999 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ubuntu:focal-20220105`

```console
$ docker pull ubuntu@sha256:b5a61709a9a44284d88fb12e5c48db0409cfad5b69d4ff8224077c57302df9cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; riscv64
	-	linux; s390x

### `ubuntu:focal-20220105` - linux; amd64

```console
$ docker pull ubuntu@sha256:57df66b9fc9ce2947e434b4aa02dbe16f6685e20db0c170917d4a1962a5fe6a9
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.6 MB (28566425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d13c942271d66cb0954c3ba93e143cd253421fe0772b8bed32c4c0077a546d4d`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 07 Jan 2022 02:25:29 GMT
ADD file:122ad323412c2e70b3138d8eb62648c4692989de91be1ffb6b4bf086c8311b62 in / 
# Fri, 07 Jan 2022 02:25:30 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:ea362f368469f909a95f9a6e54ebe0121ce0a8e3c30583dd9c5fb35b14544dec`  
		Last Modified: Thu, 06 Jan 2022 15:07:12 GMT  
		Size: 28.6 MB (28566425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:focal-20220105` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:06bd529675558f58ea2aa4bb0f2442a073750e5d3b8c6d1f7e180b59b056f238
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.1 MB (24064434 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4273349cd30895098e846fcd0b542d97732d2c33a433267e48634fa5aa45fc9`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 07 Jan 2022 02:26:25 GMT
ADD file:ac83e0dc7e48a0dc1805c0fd7b71b8eb119b3eeafd1fdcab93e11fbc9c0bcda0 in / 
# Fri, 07 Jan 2022 02:26:26 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:9b8080fa0945580f29aa3abed4664f8ab849229eca04510b5d259a9e29616064`  
		Last Modified: Fri, 07 Jan 2022 02:30:39 GMT  
		Size: 24.1 MB (24064434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:focal-20220105` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:64162ac111b666daf1305de1888eb67a3033f62000f5ff781fe529aff8f88b09
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.2 MB (27171074 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f4877540c734dfd8ee2e523b1487788f871e64a4f3137797d33e5971ac9adde`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 07 Jan 2022 01:53:45 GMT
ADD file:521a8ada4ac06e6f7720904486d481d216a8c3e08c0c7db1376c39a33e709668 in / 
# Fri, 07 Jan 2022 01:53:45 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:5f3d23ccb99f6c9462a15efcf35aef0863858073a06d56df671d0e791b26222a`  
		Last Modified: Fri, 07 Jan 2022 01:55:32 GMT  
		Size: 27.2 MB (27171074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:focal-20220105` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:edb1aa0254b14fd8d321fc5b8b2ccf73cea79bd8c18d690bc52f1e4a810ac409
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.3 MB (33286892 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a4c29dc93ac6b035392b13201bdf0e145386248a5473522dba4c2ee619ff32f`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 07 Jan 2022 02:20:15 GMT
ADD file:014236839eaee978894ae0bd6aecc246177a0a2c11af73f86d9cfafe5478ce18 in / 
# Fri, 07 Jan 2022 02:20:19 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:e6e6dea5a8cc4bdc9e5e51e2bfa948159b69d5fbc2dca99bc41776fb04dab967`  
		Last Modified: Fri, 07 Jan 2022 02:22:43 GMT  
		Size: 33.3 MB (33286892 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:focal-20220105` - linux; riscv64

```console
$ docker pull ubuntu@sha256:bc700522fdbb6d8fa43a6800954e3f12c6990df7e344649c05eafac375aa4dcf
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.2 MB (24226982 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3459adb1e25a18e53fc9834550294901f7461cb2dec65efbaeff4bf5c9737cc`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 07 Jan 2022 02:16:06 GMT
ADD file:8c67f745313efae2d5d96d237357fdd8bd6ea54c3f198c07010bf1bce663d48c in / 
# Fri, 07 Jan 2022 02:16:08 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:8c703baf60b6c639070fea2dcfc339570983cdb4555d172e28f82e765410e364`  
		Last Modified: Fri, 07 Jan 2022 02:34:37 GMT  
		Size: 24.2 MB (24226982 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:focal-20220105` - linux; s390x

```console
$ docker pull ubuntu@sha256:0081dfc53722a9cf4be7067ef069d102889dea63ed7536ddef1f6d2666fd1de0
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.1 MB (27120999 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:851f3d9fd80317037249fb42643a20742a38a8112130ff428e48c1c914d5ee9b`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 07 Jan 2022 01:42:20 GMT
ADD file:b6119f4fcd6a113749f515278b315ffd96aecce7006f086acb060f981e5c59db in / 
# Fri, 07 Jan 2022 01:42:22 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:6d200361446626b53394c2a1a520a74a1221795562eac9b318c58e0abe147e23`  
		Last Modified: Fri, 07 Jan 2022 01:44:09 GMT  
		Size: 27.1 MB (27120999 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ubuntu:hirsute`

```console
$ docker pull ubuntu@sha256:041767af88d66339ef063abfecb0e8052f776460325b8a2b91f5394938d27281
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; riscv64
	-	linux; s390x

### `ubuntu:hirsute` - linux; amd64

```console
$ docker pull ubuntu@sha256:fd367579637b6c083eaddb9a21ac4a2f63d1e02a4ca2671d7e57c24ee3764deb
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.7 MB (31703311 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64cdc469caaa7cee68b06410692f436ff4a1d8b314577a83f4e6400cc2dfc1ff`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 07 Jan 2022 02:25:37 GMT
ADD file:cfcb96e25bf4af2949d0c04953666b16dca08216ded8040ddfeedd0e782c6ddc in / 
# Fri, 07 Jan 2022 02:25:38 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:318226705d6bf4f94a70707b917c9bea2190a83f512b1c257dffbb691859831e`  
		Last Modified: Tue, 14 Dec 2021 13:10:17 GMT  
		Size: 31.7 MB (31703311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:hirsute` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:e0e5f03210d623b83cd8fc30d4f9e4099c6e541e4a44ef04f47cbbffa76d18d3
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.9 MB (26860386 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7b078fa17f59892eaf4ffe618fa9cf8774564f764cd9f5011534613b0996e73`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 07 Jan 2022 02:26:48 GMT
ADD file:b5bafdb9006674a167988c876664fe5c9986ad3472147327f21401be96959a6c in / 
# Fri, 07 Jan 2022 02:26:48 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:f72a97c294933ef5ddaab06415361fb5ebd9a11c5a2652c06e97c5c7e6ebefaa`  
		Last Modified: Tue, 14 Dec 2021 13:11:38 GMT  
		Size: 26.9 MB (26860386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:hirsute` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:70493c1293aac4d5e1b49284cd4a82ebf64634892875f5b564ceda827f76d4f3
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.2 MB (30175274 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f17f05e89a1671c20c8d32c69a6b323973fbc471a8a45ff6b7e3c6e756e3ebe`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 07 Jan 2022 01:53:53 GMT
ADD file:53760a4a864d7c22beaf50ceaaceb7114cf6e4d285c9c4e41bddcb4ee83a71cd in / 
# Fri, 07 Jan 2022 01:53:53 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:a2edff5d3cccb200e40a203e356b5409a32f6982fc3cb50d5dfa39ecb3402d0f`  
		Last Modified: Tue, 14 Dec 2021 13:11:05 GMT  
		Size: 30.2 MB (30175274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:hirsute` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:73ec4cde47ba5a97eee6cf67594b1e2477da3c22a1afbc6677dc5687b51e6df2
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.3 MB (37256256 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb1722ce1cf10ab1ddf29417410556bcb48908dfe1de137b6e0dccbe2014375a`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 07 Jan 2022 02:20:30 GMT
ADD file:9356fd6fd5fe8e2698a7935a4f9e731784a123135fbbac56c0a64aba4ff055d8 in / 
# Fri, 07 Jan 2022 02:20:34 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:9e0f94572fe4babd7bb8b4026de5bab1243bfc425d3ef7113aab8ad7c891c73f`  
		Last Modified: Tue, 14 Dec 2021 13:12:16 GMT  
		Size: 37.3 MB (37256256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:hirsute` - linux; riscv64

```console
$ docker pull ubuntu@sha256:24d503e08f07e16761b7e6a3046a03b90e303a0a93292868cb14a234ceabd477
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.1 MB (27142124 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f55f171d7b38cdde4cce8bf874a39bfbe1c432746aeeef80514ee5a3c5b9732`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 07 Jan 2022 02:18:08 GMT
ADD file:88bfbe1378489e66f6bc7226898a5fbf2fa4921a2a9f8368035d39f3f9e7879e in / 
# Fri, 07 Jan 2022 02:18:09 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:a42cee3150e09146966460b6ef66d449ef9ab179df8c79c79444cbf84185ca45`  
		Last Modified: Tue, 14 Dec 2021 13:12:53 GMT  
		Size: 27.1 MB (27142124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:hirsute` - linux; s390x

```console
$ docker pull ubuntu@sha256:9967da8c3c3248fc78eab07882cbf502b8007eaf347027519dbc926997358493
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.5 MB (32506835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c28770469e05cdf7ac3d0b8be3b4c1ae8c993ca1c283603db1520c208baa8250`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 07 Jan 2022 01:42:31 GMT
ADD file:0ab8d0c606111287c48ef013f6e2c33f36b1f35018d55a975462a5bd8a3ba1d7 in / 
# Fri, 07 Jan 2022 01:42:33 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:d7416c72715444586e1570693d4643393f777728e1eebec0c79ccefc15b81acc`  
		Last Modified: Tue, 14 Dec 2021 13:13:27 GMT  
		Size: 32.5 MB (32506835 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ubuntu:hirsute-20211208`

```console
$ docker pull ubuntu@sha256:041767af88d66339ef063abfecb0e8052f776460325b8a2b91f5394938d27281
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; riscv64
	-	linux; s390x

### `ubuntu:hirsute-20211208` - linux; amd64

```console
$ docker pull ubuntu@sha256:fd367579637b6c083eaddb9a21ac4a2f63d1e02a4ca2671d7e57c24ee3764deb
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.7 MB (31703311 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64cdc469caaa7cee68b06410692f436ff4a1d8b314577a83f4e6400cc2dfc1ff`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 07 Jan 2022 02:25:37 GMT
ADD file:cfcb96e25bf4af2949d0c04953666b16dca08216ded8040ddfeedd0e782c6ddc in / 
# Fri, 07 Jan 2022 02:25:38 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:318226705d6bf4f94a70707b917c9bea2190a83f512b1c257dffbb691859831e`  
		Last Modified: Tue, 14 Dec 2021 13:10:17 GMT  
		Size: 31.7 MB (31703311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:hirsute-20211208` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:e0e5f03210d623b83cd8fc30d4f9e4099c6e541e4a44ef04f47cbbffa76d18d3
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.9 MB (26860386 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7b078fa17f59892eaf4ffe618fa9cf8774564f764cd9f5011534613b0996e73`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 07 Jan 2022 02:26:48 GMT
ADD file:b5bafdb9006674a167988c876664fe5c9986ad3472147327f21401be96959a6c in / 
# Fri, 07 Jan 2022 02:26:48 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:f72a97c294933ef5ddaab06415361fb5ebd9a11c5a2652c06e97c5c7e6ebefaa`  
		Last Modified: Tue, 14 Dec 2021 13:11:38 GMT  
		Size: 26.9 MB (26860386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:hirsute-20211208` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:70493c1293aac4d5e1b49284cd4a82ebf64634892875f5b564ceda827f76d4f3
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.2 MB (30175274 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f17f05e89a1671c20c8d32c69a6b323973fbc471a8a45ff6b7e3c6e756e3ebe`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 07 Jan 2022 01:53:53 GMT
ADD file:53760a4a864d7c22beaf50ceaaceb7114cf6e4d285c9c4e41bddcb4ee83a71cd in / 
# Fri, 07 Jan 2022 01:53:53 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:a2edff5d3cccb200e40a203e356b5409a32f6982fc3cb50d5dfa39ecb3402d0f`  
		Last Modified: Tue, 14 Dec 2021 13:11:05 GMT  
		Size: 30.2 MB (30175274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:hirsute-20211208` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:73ec4cde47ba5a97eee6cf67594b1e2477da3c22a1afbc6677dc5687b51e6df2
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.3 MB (37256256 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb1722ce1cf10ab1ddf29417410556bcb48908dfe1de137b6e0dccbe2014375a`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 07 Jan 2022 02:20:30 GMT
ADD file:9356fd6fd5fe8e2698a7935a4f9e731784a123135fbbac56c0a64aba4ff055d8 in / 
# Fri, 07 Jan 2022 02:20:34 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:9e0f94572fe4babd7bb8b4026de5bab1243bfc425d3ef7113aab8ad7c891c73f`  
		Last Modified: Tue, 14 Dec 2021 13:12:16 GMT  
		Size: 37.3 MB (37256256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:hirsute-20211208` - linux; riscv64

```console
$ docker pull ubuntu@sha256:24d503e08f07e16761b7e6a3046a03b90e303a0a93292868cb14a234ceabd477
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.1 MB (27142124 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f55f171d7b38cdde4cce8bf874a39bfbe1c432746aeeef80514ee5a3c5b9732`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 07 Jan 2022 02:18:08 GMT
ADD file:88bfbe1378489e66f6bc7226898a5fbf2fa4921a2a9f8368035d39f3f9e7879e in / 
# Fri, 07 Jan 2022 02:18:09 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:a42cee3150e09146966460b6ef66d449ef9ab179df8c79c79444cbf84185ca45`  
		Last Modified: Tue, 14 Dec 2021 13:12:53 GMT  
		Size: 27.1 MB (27142124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:hirsute-20211208` - linux; s390x

```console
$ docker pull ubuntu@sha256:9967da8c3c3248fc78eab07882cbf502b8007eaf347027519dbc926997358493
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.5 MB (32506835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c28770469e05cdf7ac3d0b8be3b4c1ae8c993ca1c283603db1520c208baa8250`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 07 Jan 2022 01:42:31 GMT
ADD file:0ab8d0c606111287c48ef013f6e2c33f36b1f35018d55a975462a5bd8a3ba1d7 in / 
# Fri, 07 Jan 2022 01:42:33 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:d7416c72715444586e1570693d4643393f777728e1eebec0c79ccefc15b81acc`  
		Last Modified: Tue, 14 Dec 2021 13:13:27 GMT  
		Size: 32.5 MB (32506835 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ubuntu:impish`

```console
$ docker pull ubuntu@sha256:cfc189b67f53b322b0ceaabacfc9e2414c63435f362348807fe960d0fbce5ada
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; riscv64
	-	linux; s390x

### `ubuntu:impish` - linux; amd64

```console
$ docker pull ubuntu@sha256:28941e0c8e9be8c6aa586be8c7ae3074c81ed915cb5b5836853985d756fb46e2
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.4 MB (30377796 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64c59b1065b1ea628a7253ea0e5e87234e764fe3612ced48c495bb0f2de60a85`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 07 Jan 2022 02:25:45 GMT
ADD file:f8a2d8d5948f5e12d6d04bf3b60fdbe16956e3a0d5486994c3088f3c9ddfe3b6 in / 
# Fri, 07 Jan 2022 02:25:45 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:688b037d2a94faed4d0a662851a3612e2a23a9e0e2636b9fc84be4f45a05f698`  
		Last Modified: Fri, 07 Jan 2022 02:27:28 GMT  
		Size: 30.4 MB (30377796 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:impish` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:33965bb123b32366424d2f837f48e7793d4c879e0157b2a886c3a59b05180529
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.9 MB (26918664 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c5bd2c1ab61832ce70760e1f1aadd4099dccd69084b3d20db7538a20c77d2c6`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 07 Jan 2022 02:27:09 GMT
ADD file:1943eb8161d1853aa98adec6971ce80e67c5ef8deafcefaa8809addbc3eee806 in / 
# Fri, 07 Jan 2022 02:27:10 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:2d5d37c142fbf68de0a42ff73e6ce8a0826e64699a992a9f245b81d99456b441`  
		Last Modified: Fri, 07 Jan 2022 02:31:42 GMT  
		Size: 26.9 MB (26918664 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:impish` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:cd8c34bca231c3bc85141170cde83763cb6cbf1ceb74550178e549125f2bbad9
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.0 MB (29026221 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a5119fc922bda6dc97dd851b40203a71403c35765b2413bf16187d5f369d339`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 07 Jan 2022 01:54:01 GMT
ADD file:313dff926c3a3dbea803ddccb86e973465260b7b2618bcbe33892115f68a773b in / 
# Fri, 07 Jan 2022 01:54:01 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:f0ffaea8604435228e4901f528ec20078ee34a6050875405766fd95208f0c31f`  
		Last Modified: Fri, 07 Jan 2022 01:56:10 GMT  
		Size: 29.0 MB (29026221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:impish` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:5a7abe42cbb7b56ef2b7033c970cdb2561c888e6b56855be3f8eb6a0fd2420e2
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.2 MB (36174729 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7dc8aa3f2f3bb8749e361794f031649f81c39a898c749e3f05f2680cea407a7`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 07 Jan 2022 02:20:45 GMT
ADD file:6c52e72233bc011d6cc1943cc59283ed3def1a426a7cf3b9b8a03320a1de85ac in / 
# Fri, 07 Jan 2022 02:20:48 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:5e28f686135f4d211abc5a5fe924bd23a6fee36d43e23d37529639850f708a22`  
		Last Modified: Fri, 07 Jan 2022 02:23:31 GMT  
		Size: 36.2 MB (36174729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:impish` - linux; riscv64

```console
$ docker pull ubuntu@sha256:f754ba1e1c296e6c2829454e7b6dee03bea619db93de1a9daf79a035445e92f5
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.2 MB (27207318 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e45ed113f979ce70402d70dcbe4d2cf0d583d04d5c4658a39dd5455bf71b476`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 07 Jan 2022 02:19:54 GMT
ADD file:80d7cfc8a88ccc3ac0dd24dfba95a65c7e24cc96f880a61736d5ab358db84912 in / 
# Fri, 07 Jan 2022 02:19:56 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:41481709d1b8a29bbdd69a8df35aeab07866245eed21a54aa5f2d183351e4569`  
		Last Modified: Fri, 07 Jan 2022 02:39:10 GMT  
		Size: 27.2 MB (27207318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:impish` - linux; s390x

```console
$ docker pull ubuntu@sha256:4c5b76c0baf3a991fd734c73ed6d0d40787dbf24afcf60aaf9962ab1f62654f0
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.5 MB (30526144 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b2af0eb503e8f19260c6db71780890dc9a7164118f04a8581f23c4dd5c29901`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 07 Jan 2022 01:42:43 GMT
ADD file:d2d689ec5bbbbec520f5fc8ea75e1d642f177a30c5937027ca800b3a9ccf5b83 in / 
# Fri, 07 Jan 2022 01:42:45 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:77bd6b10105ec281aabfad8249bf82b48478e0eac3503dccd5d75db49b1dd586`  
		Last Modified: Fri, 07 Jan 2022 01:44:35 GMT  
		Size: 30.5 MB (30526144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ubuntu:impish-20220105`

```console
$ docker pull ubuntu@sha256:cfc189b67f53b322b0ceaabacfc9e2414c63435f362348807fe960d0fbce5ada
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; riscv64
	-	linux; s390x

### `ubuntu:impish-20220105` - linux; amd64

```console
$ docker pull ubuntu@sha256:28941e0c8e9be8c6aa586be8c7ae3074c81ed915cb5b5836853985d756fb46e2
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.4 MB (30377796 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64c59b1065b1ea628a7253ea0e5e87234e764fe3612ced48c495bb0f2de60a85`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 07 Jan 2022 02:25:45 GMT
ADD file:f8a2d8d5948f5e12d6d04bf3b60fdbe16956e3a0d5486994c3088f3c9ddfe3b6 in / 
# Fri, 07 Jan 2022 02:25:45 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:688b037d2a94faed4d0a662851a3612e2a23a9e0e2636b9fc84be4f45a05f698`  
		Last Modified: Fri, 07 Jan 2022 02:27:28 GMT  
		Size: 30.4 MB (30377796 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:impish-20220105` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:33965bb123b32366424d2f837f48e7793d4c879e0157b2a886c3a59b05180529
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.9 MB (26918664 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c5bd2c1ab61832ce70760e1f1aadd4099dccd69084b3d20db7538a20c77d2c6`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 07 Jan 2022 02:27:09 GMT
ADD file:1943eb8161d1853aa98adec6971ce80e67c5ef8deafcefaa8809addbc3eee806 in / 
# Fri, 07 Jan 2022 02:27:10 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:2d5d37c142fbf68de0a42ff73e6ce8a0826e64699a992a9f245b81d99456b441`  
		Last Modified: Fri, 07 Jan 2022 02:31:42 GMT  
		Size: 26.9 MB (26918664 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:impish-20220105` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:cd8c34bca231c3bc85141170cde83763cb6cbf1ceb74550178e549125f2bbad9
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.0 MB (29026221 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a5119fc922bda6dc97dd851b40203a71403c35765b2413bf16187d5f369d339`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 07 Jan 2022 01:54:01 GMT
ADD file:313dff926c3a3dbea803ddccb86e973465260b7b2618bcbe33892115f68a773b in / 
# Fri, 07 Jan 2022 01:54:01 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:f0ffaea8604435228e4901f528ec20078ee34a6050875405766fd95208f0c31f`  
		Last Modified: Fri, 07 Jan 2022 01:56:10 GMT  
		Size: 29.0 MB (29026221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:impish-20220105` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:5a7abe42cbb7b56ef2b7033c970cdb2561c888e6b56855be3f8eb6a0fd2420e2
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.2 MB (36174729 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7dc8aa3f2f3bb8749e361794f031649f81c39a898c749e3f05f2680cea407a7`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 07 Jan 2022 02:20:45 GMT
ADD file:6c52e72233bc011d6cc1943cc59283ed3def1a426a7cf3b9b8a03320a1de85ac in / 
# Fri, 07 Jan 2022 02:20:48 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:5e28f686135f4d211abc5a5fe924bd23a6fee36d43e23d37529639850f708a22`  
		Last Modified: Fri, 07 Jan 2022 02:23:31 GMT  
		Size: 36.2 MB (36174729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:impish-20220105` - linux; riscv64

```console
$ docker pull ubuntu@sha256:f754ba1e1c296e6c2829454e7b6dee03bea619db93de1a9daf79a035445e92f5
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.2 MB (27207318 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e45ed113f979ce70402d70dcbe4d2cf0d583d04d5c4658a39dd5455bf71b476`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 07 Jan 2022 02:19:54 GMT
ADD file:80d7cfc8a88ccc3ac0dd24dfba95a65c7e24cc96f880a61736d5ab358db84912 in / 
# Fri, 07 Jan 2022 02:19:56 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:41481709d1b8a29bbdd69a8df35aeab07866245eed21a54aa5f2d183351e4569`  
		Last Modified: Fri, 07 Jan 2022 02:39:10 GMT  
		Size: 27.2 MB (27207318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:impish-20220105` - linux; s390x

```console
$ docker pull ubuntu@sha256:4c5b76c0baf3a991fd734c73ed6d0d40787dbf24afcf60aaf9962ab1f62654f0
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.5 MB (30526144 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b2af0eb503e8f19260c6db71780890dc9a7164118f04a8581f23c4dd5c29901`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 07 Jan 2022 01:42:43 GMT
ADD file:d2d689ec5bbbbec520f5fc8ea75e1d642f177a30c5937027ca800b3a9ccf5b83 in / 
# Fri, 07 Jan 2022 01:42:45 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:77bd6b10105ec281aabfad8249bf82b48478e0eac3503dccd5d75db49b1dd586`  
		Last Modified: Fri, 07 Jan 2022 01:44:35 GMT  
		Size: 30.5 MB (30526144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ubuntu:jammy`

```console
$ docker pull ubuntu@sha256:0ad36748089181d832164977bdeb56d08672e352173127d8bfcd9aa4f7b3bd41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; riscv64
	-	linux; s390x

### `ubuntu:jammy` - linux; amd64

```console
$ docker pull ubuntu@sha256:74075bbbd941a1766a0db1d66e617a0ab82ab54dd23e0b55bebd7e62d9e9b7be
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.5 MB (30501041 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c68f8d0eb3f063896e40d4ef7652b2901eeb2d35281104a4d2132d8df4ba9e34`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 07 Jan 2022 02:25:53 GMT
ADD file:7fa9713fdcdef2552cd85dc53d57c2f444a09798fd2254d68f2f955cc1114ab7 in / 
# Fri, 07 Jan 2022 02:25:53 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:25f4cd1d54a5120c409f812234ad6f2266a5ae22fe0cf58c3ffab80bedc4368c`  
		Last Modified: Fri, 07 Jan 2022 02:27:47 GMT  
		Size: 30.5 MB (30501041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:jammy` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:572beed80a67a6184fade4720c815f1d72242a6474a6ed88c0fdcbe3863f29d2
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.6 MB (27564608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eafb6ceae367630169b067d6ff2eaaa704ea2dc470b63e765448fc1c7548b27c`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 07 Jan 2022 02:27:32 GMT
ADD file:8718f314f447f7d0c389825500d5ceb026028c337363ef130cdcf6125750046e in / 
# Fri, 07 Jan 2022 02:27:33 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:152d82d6f338fbb1e956a78af2d045c6fc15f4c5352ab546d88118f037a1a4e5`  
		Last Modified: Fri, 07 Jan 2022 02:32:16 GMT  
		Size: 27.6 MB (27564608 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:jammy` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:073e060cec31fed4a86fcd45ad6f80b1f135109ac2c0b57272f01909c9626486
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.9 MB (28921769 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63a4636836063b8f0d2297a5df988c114bed06c3989c4585630f1f808271451c`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 07 Jan 2022 01:54:09 GMT
ADD file:d75d592836ef38b5620858a3eb1666af50f390695066b7b3432f365e1cc3a56b in / 
# Fri, 07 Jan 2022 01:54:10 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:a9ca93140713b0208e2ea5b1925e67a506893717f9d1ff5aa2097ad25d2ffd59`  
		Last Modified: Fri, 07 Jan 2022 01:56:30 GMT  
		Size: 28.9 MB (28921769 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:jammy` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:910a9c3d7b81e15b0b4e07c1bb6153c00b5609a383c8940ebf51a653d115230d
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.3 MB (36323413 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27d6b27e00447e7b536d840bdeaede3e641f6cf351c0688b9cb2ba4327a5fbde`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 07 Jan 2022 02:21:00 GMT
ADD file:ee7ea12d6a8f311929a29ce03c167071ec7ae0e38a90c35118926fa9ee0881a6 in / 
# Fri, 07 Jan 2022 02:21:04 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:d7e91abaf3158b413cf53113f304d05a30a09d1920db39a3eaa08c8c5da337fd`  
		Last Modified: Fri, 07 Jan 2022 02:23:54 GMT  
		Size: 36.3 MB (36323413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:jammy` - linux; riscv64

```console
$ docker pull ubuntu@sha256:afc637a71adf6e5324b37ad3a1f005e2c28703ddaec376581103df6c2e86805b
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.2 MB (28205700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2555b7864f3f9d8a4ef30c58887ac62eea38960574da93eb4ea03c9699e0d349`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 07 Jan 2022 02:21:55 GMT
ADD file:fb3b5a3e5efdc1d60cfffdd3cff88b09a96f8d9c5fd22023cfa826992be407da in / 
# Fri, 07 Jan 2022 02:21:57 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:939152979f37020f3d9c4352564dab069f4ae0c7d16abbe222f7721f7f9543ef`  
		Last Modified: Fri, 07 Jan 2022 02:41:41 GMT  
		Size: 28.2 MB (28205700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:jammy` - linux; s390x

```console
$ docker pull ubuntu@sha256:d6c91889a7d4e92152af9aa33e8a8902ad37b05a287f8744b9c21bcfe85f11fd
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.4 MB (29387057 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74956f997a30cfd4b88964886f260e9751c5fde79ec202f151f31d8275378f85`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 07 Jan 2022 01:42:53 GMT
ADD file:63122dcff09feadc66081fd2b45b3e3de924cf0f111e8515c56594154aabde6e in / 
# Fri, 07 Jan 2022 01:42:56 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:a0ea954c58d9a01dec91e416a4d333a9fcdca5f2b6512986d1201c7c1763d0b2`  
		Last Modified: Fri, 07 Jan 2022 01:44:50 GMT  
		Size: 29.4 MB (29387057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ubuntu:jammy-20220101`

```console
$ docker pull ubuntu@sha256:0ad36748089181d832164977bdeb56d08672e352173127d8bfcd9aa4f7b3bd41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; riscv64
	-	linux; s390x

### `ubuntu:jammy-20220101` - linux; amd64

```console
$ docker pull ubuntu@sha256:74075bbbd941a1766a0db1d66e617a0ab82ab54dd23e0b55bebd7e62d9e9b7be
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.5 MB (30501041 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c68f8d0eb3f063896e40d4ef7652b2901eeb2d35281104a4d2132d8df4ba9e34`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 07 Jan 2022 02:25:53 GMT
ADD file:7fa9713fdcdef2552cd85dc53d57c2f444a09798fd2254d68f2f955cc1114ab7 in / 
# Fri, 07 Jan 2022 02:25:53 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:25f4cd1d54a5120c409f812234ad6f2266a5ae22fe0cf58c3ffab80bedc4368c`  
		Last Modified: Fri, 07 Jan 2022 02:27:47 GMT  
		Size: 30.5 MB (30501041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:jammy-20220101` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:572beed80a67a6184fade4720c815f1d72242a6474a6ed88c0fdcbe3863f29d2
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.6 MB (27564608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eafb6ceae367630169b067d6ff2eaaa704ea2dc470b63e765448fc1c7548b27c`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 07 Jan 2022 02:27:32 GMT
ADD file:8718f314f447f7d0c389825500d5ceb026028c337363ef130cdcf6125750046e in / 
# Fri, 07 Jan 2022 02:27:33 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:152d82d6f338fbb1e956a78af2d045c6fc15f4c5352ab546d88118f037a1a4e5`  
		Last Modified: Fri, 07 Jan 2022 02:32:16 GMT  
		Size: 27.6 MB (27564608 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:jammy-20220101` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:073e060cec31fed4a86fcd45ad6f80b1f135109ac2c0b57272f01909c9626486
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.9 MB (28921769 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63a4636836063b8f0d2297a5df988c114bed06c3989c4585630f1f808271451c`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 07 Jan 2022 01:54:09 GMT
ADD file:d75d592836ef38b5620858a3eb1666af50f390695066b7b3432f365e1cc3a56b in / 
# Fri, 07 Jan 2022 01:54:10 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:a9ca93140713b0208e2ea5b1925e67a506893717f9d1ff5aa2097ad25d2ffd59`  
		Last Modified: Fri, 07 Jan 2022 01:56:30 GMT  
		Size: 28.9 MB (28921769 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:jammy-20220101` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:910a9c3d7b81e15b0b4e07c1bb6153c00b5609a383c8940ebf51a653d115230d
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.3 MB (36323413 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27d6b27e00447e7b536d840bdeaede3e641f6cf351c0688b9cb2ba4327a5fbde`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 07 Jan 2022 02:21:00 GMT
ADD file:ee7ea12d6a8f311929a29ce03c167071ec7ae0e38a90c35118926fa9ee0881a6 in / 
# Fri, 07 Jan 2022 02:21:04 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:d7e91abaf3158b413cf53113f304d05a30a09d1920db39a3eaa08c8c5da337fd`  
		Last Modified: Fri, 07 Jan 2022 02:23:54 GMT  
		Size: 36.3 MB (36323413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:jammy-20220101` - linux; riscv64

```console
$ docker pull ubuntu@sha256:afc637a71adf6e5324b37ad3a1f005e2c28703ddaec376581103df6c2e86805b
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.2 MB (28205700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2555b7864f3f9d8a4ef30c58887ac62eea38960574da93eb4ea03c9699e0d349`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 07 Jan 2022 02:21:55 GMT
ADD file:fb3b5a3e5efdc1d60cfffdd3cff88b09a96f8d9c5fd22023cfa826992be407da in / 
# Fri, 07 Jan 2022 02:21:57 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:939152979f37020f3d9c4352564dab069f4ae0c7d16abbe222f7721f7f9543ef`  
		Last Modified: Fri, 07 Jan 2022 02:41:41 GMT  
		Size: 28.2 MB (28205700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:jammy-20220101` - linux; s390x

```console
$ docker pull ubuntu@sha256:d6c91889a7d4e92152af9aa33e8a8902ad37b05a287f8744b9c21bcfe85f11fd
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.4 MB (29387057 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74956f997a30cfd4b88964886f260e9751c5fde79ec202f151f31d8275378f85`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 07 Jan 2022 01:42:53 GMT
ADD file:63122dcff09feadc66081fd2b45b3e3de924cf0f111e8515c56594154aabde6e in / 
# Fri, 07 Jan 2022 01:42:56 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:a0ea954c58d9a01dec91e416a4d333a9fcdca5f2b6512986d1201c7c1763d0b2`  
		Last Modified: Fri, 07 Jan 2022 01:44:50 GMT  
		Size: 29.4 MB (29387057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ubuntu:latest`

```console
$ docker pull ubuntu@sha256:b5a61709a9a44284d88fb12e5c48db0409cfad5b69d4ff8224077c57302df9cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; riscv64
	-	linux; s390x

### `ubuntu:latest` - linux; amd64

```console
$ docker pull ubuntu@sha256:57df66b9fc9ce2947e434b4aa02dbe16f6685e20db0c170917d4a1962a5fe6a9
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.6 MB (28566425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d13c942271d66cb0954c3ba93e143cd253421fe0772b8bed32c4c0077a546d4d`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 07 Jan 2022 02:25:29 GMT
ADD file:122ad323412c2e70b3138d8eb62648c4692989de91be1ffb6b4bf086c8311b62 in / 
# Fri, 07 Jan 2022 02:25:30 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:ea362f368469f909a95f9a6e54ebe0121ce0a8e3c30583dd9c5fb35b14544dec`  
		Last Modified: Thu, 06 Jan 2022 15:07:12 GMT  
		Size: 28.6 MB (28566425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:latest` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:06bd529675558f58ea2aa4bb0f2442a073750e5d3b8c6d1f7e180b59b056f238
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.1 MB (24064434 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4273349cd30895098e846fcd0b542d97732d2c33a433267e48634fa5aa45fc9`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 07 Jan 2022 02:26:25 GMT
ADD file:ac83e0dc7e48a0dc1805c0fd7b71b8eb119b3eeafd1fdcab93e11fbc9c0bcda0 in / 
# Fri, 07 Jan 2022 02:26:26 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:9b8080fa0945580f29aa3abed4664f8ab849229eca04510b5d259a9e29616064`  
		Last Modified: Fri, 07 Jan 2022 02:30:39 GMT  
		Size: 24.1 MB (24064434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:latest` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:64162ac111b666daf1305de1888eb67a3033f62000f5ff781fe529aff8f88b09
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.2 MB (27171074 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f4877540c734dfd8ee2e523b1487788f871e64a4f3137797d33e5971ac9adde`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 07 Jan 2022 01:53:45 GMT
ADD file:521a8ada4ac06e6f7720904486d481d216a8c3e08c0c7db1376c39a33e709668 in / 
# Fri, 07 Jan 2022 01:53:45 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:5f3d23ccb99f6c9462a15efcf35aef0863858073a06d56df671d0e791b26222a`  
		Last Modified: Fri, 07 Jan 2022 01:55:32 GMT  
		Size: 27.2 MB (27171074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:latest` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:edb1aa0254b14fd8d321fc5b8b2ccf73cea79bd8c18d690bc52f1e4a810ac409
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.3 MB (33286892 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a4c29dc93ac6b035392b13201bdf0e145386248a5473522dba4c2ee619ff32f`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 07 Jan 2022 02:20:15 GMT
ADD file:014236839eaee978894ae0bd6aecc246177a0a2c11af73f86d9cfafe5478ce18 in / 
# Fri, 07 Jan 2022 02:20:19 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:e6e6dea5a8cc4bdc9e5e51e2bfa948159b69d5fbc2dca99bc41776fb04dab967`  
		Last Modified: Fri, 07 Jan 2022 02:22:43 GMT  
		Size: 33.3 MB (33286892 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:latest` - linux; riscv64

```console
$ docker pull ubuntu@sha256:bc700522fdbb6d8fa43a6800954e3f12c6990df7e344649c05eafac375aa4dcf
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.2 MB (24226982 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3459adb1e25a18e53fc9834550294901f7461cb2dec65efbaeff4bf5c9737cc`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 07 Jan 2022 02:16:06 GMT
ADD file:8c67f745313efae2d5d96d237357fdd8bd6ea54c3f198c07010bf1bce663d48c in / 
# Fri, 07 Jan 2022 02:16:08 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:8c703baf60b6c639070fea2dcfc339570983cdb4555d172e28f82e765410e364`  
		Last Modified: Fri, 07 Jan 2022 02:34:37 GMT  
		Size: 24.2 MB (24226982 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:latest` - linux; s390x

```console
$ docker pull ubuntu@sha256:0081dfc53722a9cf4be7067ef069d102889dea63ed7536ddef1f6d2666fd1de0
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.1 MB (27120999 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:851f3d9fd80317037249fb42643a20742a38a8112130ff428e48c1c914d5ee9b`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 07 Jan 2022 01:42:20 GMT
ADD file:b6119f4fcd6a113749f515278b315ffd96aecce7006f086acb060f981e5c59db in / 
# Fri, 07 Jan 2022 01:42:22 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:6d200361446626b53394c2a1a520a74a1221795562eac9b318c58e0abe147e23`  
		Last Modified: Fri, 07 Jan 2022 01:44:09 GMT  
		Size: 27.1 MB (27120999 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ubuntu:rolling`

```console
$ docker pull ubuntu@sha256:cfc189b67f53b322b0ceaabacfc9e2414c63435f362348807fe960d0fbce5ada
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; riscv64
	-	linux; s390x

### `ubuntu:rolling` - linux; amd64

```console
$ docker pull ubuntu@sha256:28941e0c8e9be8c6aa586be8c7ae3074c81ed915cb5b5836853985d756fb46e2
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.4 MB (30377796 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64c59b1065b1ea628a7253ea0e5e87234e764fe3612ced48c495bb0f2de60a85`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 07 Jan 2022 02:25:45 GMT
ADD file:f8a2d8d5948f5e12d6d04bf3b60fdbe16956e3a0d5486994c3088f3c9ddfe3b6 in / 
# Fri, 07 Jan 2022 02:25:45 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:688b037d2a94faed4d0a662851a3612e2a23a9e0e2636b9fc84be4f45a05f698`  
		Last Modified: Fri, 07 Jan 2022 02:27:28 GMT  
		Size: 30.4 MB (30377796 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:rolling` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:33965bb123b32366424d2f837f48e7793d4c879e0157b2a886c3a59b05180529
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.9 MB (26918664 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c5bd2c1ab61832ce70760e1f1aadd4099dccd69084b3d20db7538a20c77d2c6`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 07 Jan 2022 02:27:09 GMT
ADD file:1943eb8161d1853aa98adec6971ce80e67c5ef8deafcefaa8809addbc3eee806 in / 
# Fri, 07 Jan 2022 02:27:10 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:2d5d37c142fbf68de0a42ff73e6ce8a0826e64699a992a9f245b81d99456b441`  
		Last Modified: Fri, 07 Jan 2022 02:31:42 GMT  
		Size: 26.9 MB (26918664 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:rolling` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:cd8c34bca231c3bc85141170cde83763cb6cbf1ceb74550178e549125f2bbad9
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.0 MB (29026221 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a5119fc922bda6dc97dd851b40203a71403c35765b2413bf16187d5f369d339`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 07 Jan 2022 01:54:01 GMT
ADD file:313dff926c3a3dbea803ddccb86e973465260b7b2618bcbe33892115f68a773b in / 
# Fri, 07 Jan 2022 01:54:01 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:f0ffaea8604435228e4901f528ec20078ee34a6050875405766fd95208f0c31f`  
		Last Modified: Fri, 07 Jan 2022 01:56:10 GMT  
		Size: 29.0 MB (29026221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:rolling` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:5a7abe42cbb7b56ef2b7033c970cdb2561c888e6b56855be3f8eb6a0fd2420e2
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.2 MB (36174729 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7dc8aa3f2f3bb8749e361794f031649f81c39a898c749e3f05f2680cea407a7`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 07 Jan 2022 02:20:45 GMT
ADD file:6c52e72233bc011d6cc1943cc59283ed3def1a426a7cf3b9b8a03320a1de85ac in / 
# Fri, 07 Jan 2022 02:20:48 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:5e28f686135f4d211abc5a5fe924bd23a6fee36d43e23d37529639850f708a22`  
		Last Modified: Fri, 07 Jan 2022 02:23:31 GMT  
		Size: 36.2 MB (36174729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:rolling` - linux; riscv64

```console
$ docker pull ubuntu@sha256:f754ba1e1c296e6c2829454e7b6dee03bea619db93de1a9daf79a035445e92f5
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.2 MB (27207318 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e45ed113f979ce70402d70dcbe4d2cf0d583d04d5c4658a39dd5455bf71b476`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 07 Jan 2022 02:19:54 GMT
ADD file:80d7cfc8a88ccc3ac0dd24dfba95a65c7e24cc96f880a61736d5ab358db84912 in / 
# Fri, 07 Jan 2022 02:19:56 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:41481709d1b8a29bbdd69a8df35aeab07866245eed21a54aa5f2d183351e4569`  
		Last Modified: Fri, 07 Jan 2022 02:39:10 GMT  
		Size: 27.2 MB (27207318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:rolling` - linux; s390x

```console
$ docker pull ubuntu@sha256:4c5b76c0baf3a991fd734c73ed6d0d40787dbf24afcf60aaf9962ab1f62654f0
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.5 MB (30526144 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b2af0eb503e8f19260c6db71780890dc9a7164118f04a8581f23c4dd5c29901`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 07 Jan 2022 01:42:43 GMT
ADD file:d2d689ec5bbbbec520f5fc8ea75e1d642f177a30c5937027ca800b3a9ccf5b83 in / 
# Fri, 07 Jan 2022 01:42:45 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:77bd6b10105ec281aabfad8249bf82b48478e0eac3503dccd5d75db49b1dd586`  
		Last Modified: Fri, 07 Jan 2022 01:44:35 GMT  
		Size: 30.5 MB (30526144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ubuntu:trusty`

```console
$ docker pull ubuntu@sha256:60840958b25b5947b11d7a274274dc48ab32a2f5d18527f5dae2962b64269a3a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le

### `ubuntu:trusty` - linux; amd64

```console
$ docker pull ubuntu@sha256:881afbae521c910f764f7187dbfbca3cc10c26f8bafa458c76dda009a901c29d
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.8 MB (70764430 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13b66b487594a1f2b75396013bc05d29d9f527852d96c5577cc4f187559875d0`
-	Default Command: `["\/bin\/bash"]`

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

### `ubuntu:trusty` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:534255069ef3adf1c7a555fd9f614845ab66c61ef9846e438d86e12ae8c89b88
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.7 MB (64700978 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2cd03315989aa8326f2c276922d3969994c1304b1310d2e0d33a26d94dd68ea`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 13 Jul 2021 23:23:03 GMT
ADD file:e9d55e059869915743a8ca8e64582d23c48fe7e90e439daccd56d3e08e8673b4 in / 
# Tue, 13 Jul 2021 23:23:06 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Tue, 13 Jul 2021 23:23:07 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Tue, 13 Jul 2021 23:23:09 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Tue, 13 Jul 2021 23:23:10 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:0db3a87a3d7959895fd860c8b924980adda6e77f5d315b6676a4ac0e12518978`  
		Last Modified: Thu, 19 Dec 2019 06:16:01 GMT  
		Size: 64.6 MB (64624015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0c5cd1be699257153c2a6de85968c2d9c413d87470dc4f540c5c3decbca8e47`  
		Last Modified: Tue, 13 Jul 2021 23:28:27 GMT  
		Size: 76.8 KB (76774 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecbf1c32ebce749806713a088af6ff1cbf7c75a8132d310ff391948e3e611ef6`  
		Last Modified: Tue, 13 Jul 2021 23:28:26 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:trusty` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:5dc82d0f897a1bfd6a68db5b2c3692d81e5ea04e31a09664edc420689f8b450c
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.5 MB (66525481 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7304c635fe5273ccdfbc8a38e839c9089350fc8e80daf57394d1f7a9c5a70c86`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 16 Oct 2021 01:48:09 GMT
ADD file:b0eb0db52e323748ea9b8d7f8aecbc523a747619cd08663bab0fe60ab59bc60e in / 
# Sat, 16 Oct 2021 01:48:12 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Sat, 16 Oct 2021 01:48:13 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Sat, 16 Oct 2021 01:48:14 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Sat, 16 Oct 2021 01:48:14 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:d1a5a1e51f251c3431dec02e2cc8d157e92d1b46913708ce9e600747a6274977`  
		Last Modified: Thu, 19 Dec 2019 03:57:08 GMT  
		Size: 66.5 MB (66466219 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5fc464c2dc9f9ce8d7fe9ccd36f4e746ce32b39f19590f519a8cd3dd76827f8`  
		Last Modified: Sat, 16 Oct 2021 01:50:15 GMT  
		Size: 59.1 KB (59100 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:561f253b7549524704fe8cc1da5ebd27d77bc1a1424b0632b683d90eb58e73d3`  
		Last Modified: Sat, 16 Oct 2021 01:50:15 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:trusty` - linux; 386

```console
$ docker pull ubuntu@sha256:88152195106ff09bade23cb5aacfd26c381a8835c9d42124b4cba1dc3c2475e4
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.4 MB (68445499 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f18ba408bae1426c4f394e045b16a140bc555e520d5eaacc97ac60ac5f298313`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 25 Mar 2021 22:57:06 GMT
ADD file:e034601a525da53b0f39bb04d6e2264e2a592d0ae7c21e00697b9b62ca1efec9 in / 
# Thu, 25 Mar 2021 22:57:08 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 25 Mar 2021 22:57:10 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 25 Mar 2021 22:57:12 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 25 Mar 2021 22:57:12 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:630712fe5783a35ad52a7026002143cb4f8fe65d34097dcaa4c4331b1b059a17`  
		Last Modified: Thu, 19 Dec 2019 04:44:02 GMT  
		Size: 68.4 MB (68380440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ea2d50b5278097c6d027fc9fc0caf006649fcd94f094dde6ce578abe865ff21`  
		Last Modified: Thu, 25 Mar 2021 22:58:27 GMT  
		Size: 64.9 KB (64870 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5795a499c24598e294527992a703053ab615879af048f3b809a3ad86141684d`  
		Last Modified: Thu, 25 Mar 2021 22:58:27 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:trusty` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:12d9fa858f255e4b70827aff83e8ce37b6fcaddaf6732276aa1f0763402f4fdc
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.4 MB (73443156 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02949c650aebaafb917ebe6bfd55a42505e22b38e8370878164051da4ae1bcc3`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 13 Jul 2021 23:24:04 GMT
ADD file:581665e92c72c8638b40fe509de6479dc1a5d7b5ffe8d6706006178c406e35e2 in / 
# Tue, 13 Jul 2021 23:24:24 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Tue, 13 Jul 2021 23:24:33 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Tue, 13 Jul 2021 23:24:42 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Tue, 13 Jul 2021 23:24:45 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:bed4146d918c6c9a57bc3a8bf829e702975b0e53c7f25920fe9435b58ed6b64f`  
		Last Modified: Thu, 19 Dec 2019 04:26:52 GMT  
		Size: 73.4 MB (73379539 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12aab203a69be44b1617f0da6b00b670e9016c3b00ab311b384ac3f859e86613`  
		Last Modified: Tue, 13 Jul 2021 23:29:07 GMT  
		Size: 63.4 KB (63430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1576c78d220b27404b5d0c3d635c36524229553e3ccf3b9a5ad4ca93c216c6c6`  
		Last Modified: Tue, 13 Jul 2021 23:29:07 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ubuntu:trusty-20191217`

```console
$ docker pull ubuntu@sha256:60840958b25b5947b11d7a274274dc48ab32a2f5d18527f5dae2962b64269a3a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le

### `ubuntu:trusty-20191217` - linux; amd64

```console
$ docker pull ubuntu@sha256:881afbae521c910f764f7187dbfbca3cc10c26f8bafa458c76dda009a901c29d
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.8 MB (70764430 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13b66b487594a1f2b75396013bc05d29d9f527852d96c5577cc4f187559875d0`
-	Default Command: `["\/bin\/bash"]`

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

### `ubuntu:trusty-20191217` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:534255069ef3adf1c7a555fd9f614845ab66c61ef9846e438d86e12ae8c89b88
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.7 MB (64700978 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2cd03315989aa8326f2c276922d3969994c1304b1310d2e0d33a26d94dd68ea`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 13 Jul 2021 23:23:03 GMT
ADD file:e9d55e059869915743a8ca8e64582d23c48fe7e90e439daccd56d3e08e8673b4 in / 
# Tue, 13 Jul 2021 23:23:06 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Tue, 13 Jul 2021 23:23:07 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Tue, 13 Jul 2021 23:23:09 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Tue, 13 Jul 2021 23:23:10 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:0db3a87a3d7959895fd860c8b924980adda6e77f5d315b6676a4ac0e12518978`  
		Last Modified: Thu, 19 Dec 2019 06:16:01 GMT  
		Size: 64.6 MB (64624015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0c5cd1be699257153c2a6de85968c2d9c413d87470dc4f540c5c3decbca8e47`  
		Last Modified: Tue, 13 Jul 2021 23:28:27 GMT  
		Size: 76.8 KB (76774 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecbf1c32ebce749806713a088af6ff1cbf7c75a8132d310ff391948e3e611ef6`  
		Last Modified: Tue, 13 Jul 2021 23:28:26 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:trusty-20191217` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:5dc82d0f897a1bfd6a68db5b2c3692d81e5ea04e31a09664edc420689f8b450c
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.5 MB (66525481 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7304c635fe5273ccdfbc8a38e839c9089350fc8e80daf57394d1f7a9c5a70c86`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 16 Oct 2021 01:48:09 GMT
ADD file:b0eb0db52e323748ea9b8d7f8aecbc523a747619cd08663bab0fe60ab59bc60e in / 
# Sat, 16 Oct 2021 01:48:12 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Sat, 16 Oct 2021 01:48:13 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Sat, 16 Oct 2021 01:48:14 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Sat, 16 Oct 2021 01:48:14 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:d1a5a1e51f251c3431dec02e2cc8d157e92d1b46913708ce9e600747a6274977`  
		Last Modified: Thu, 19 Dec 2019 03:57:08 GMT  
		Size: 66.5 MB (66466219 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5fc464c2dc9f9ce8d7fe9ccd36f4e746ce32b39f19590f519a8cd3dd76827f8`  
		Last Modified: Sat, 16 Oct 2021 01:50:15 GMT  
		Size: 59.1 KB (59100 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:561f253b7549524704fe8cc1da5ebd27d77bc1a1424b0632b683d90eb58e73d3`  
		Last Modified: Sat, 16 Oct 2021 01:50:15 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:trusty-20191217` - linux; 386

```console
$ docker pull ubuntu@sha256:88152195106ff09bade23cb5aacfd26c381a8835c9d42124b4cba1dc3c2475e4
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.4 MB (68445499 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f18ba408bae1426c4f394e045b16a140bc555e520d5eaacc97ac60ac5f298313`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 25 Mar 2021 22:57:06 GMT
ADD file:e034601a525da53b0f39bb04d6e2264e2a592d0ae7c21e00697b9b62ca1efec9 in / 
# Thu, 25 Mar 2021 22:57:08 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 25 Mar 2021 22:57:10 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 25 Mar 2021 22:57:12 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 25 Mar 2021 22:57:12 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:630712fe5783a35ad52a7026002143cb4f8fe65d34097dcaa4c4331b1b059a17`  
		Last Modified: Thu, 19 Dec 2019 04:44:02 GMT  
		Size: 68.4 MB (68380440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ea2d50b5278097c6d027fc9fc0caf006649fcd94f094dde6ce578abe865ff21`  
		Last Modified: Thu, 25 Mar 2021 22:58:27 GMT  
		Size: 64.9 KB (64870 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5795a499c24598e294527992a703053ab615879af048f3b809a3ad86141684d`  
		Last Modified: Thu, 25 Mar 2021 22:58:27 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:trusty-20191217` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:12d9fa858f255e4b70827aff83e8ce37b6fcaddaf6732276aa1f0763402f4fdc
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.4 MB (73443156 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02949c650aebaafb917ebe6bfd55a42505e22b38e8370878164051da4ae1bcc3`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 13 Jul 2021 23:24:04 GMT
ADD file:581665e92c72c8638b40fe509de6479dc1a5d7b5ffe8d6706006178c406e35e2 in / 
# Tue, 13 Jul 2021 23:24:24 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Tue, 13 Jul 2021 23:24:33 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Tue, 13 Jul 2021 23:24:42 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Tue, 13 Jul 2021 23:24:45 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:bed4146d918c6c9a57bc3a8bf829e702975b0e53c7f25920fe9435b58ed6b64f`  
		Last Modified: Thu, 19 Dec 2019 04:26:52 GMT  
		Size: 73.4 MB (73379539 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12aab203a69be44b1617f0da6b00b670e9016c3b00ab311b384ac3f859e86613`  
		Last Modified: Tue, 13 Jul 2021 23:29:07 GMT  
		Size: 63.4 KB (63430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1576c78d220b27404b5d0c3d635c36524229553e3ccf3b9a5ad4ca93c216c6c6`  
		Last Modified: Tue, 13 Jul 2021 23:29:07 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ubuntu:xenial`

```console
$ docker pull ubuntu@sha256:0f71fa8d4d2d4292c3c617fda2b36f6dabe5c8b6e34c3dc5b0d17d4e704bd39c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `ubuntu:xenial` - linux; amd64

```console
$ docker pull ubuntu@sha256:a3785f78ab8547ae2710c89e627783cfa7ee7824d3468cae6835c9f4eae23ff7
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.5 MB (46499103 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6f50765242581c887ff1acc2511fa2d885c52d8fb3ac8c4bba131fd86567f2e`
-	Default Command: `["\/bin\/bash"]`

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

### `ubuntu:xenial` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:b722e2654241f9681f4719dce7aa16a2f0c35769e17a636f5b39a33967d1aeb8
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.3 MB (40313783 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:033c410d53efaab9e847168b94fea14d551788200a15f4d2424c84e4cd2ab8a2`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 31 Aug 2021 01:42:28 GMT
ADD file:294a94a081de785c730003a440a0530a85add2bcb60c0f5bc4ce7ee17867ac4e in / 
# Tue, 31 Aug 2021 01:42:30 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Tue, 31 Aug 2021 01:42:31 GMT
RUN rm -rf /var/lib/apt/lists/*
# Tue, 31 Aug 2021 01:42:33 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Tue, 31 Aug 2021 01:42:33 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:b95ba076a26b98e98eac4b43596b59c20d1e61a36bcaf2afae3aeebadc8844cf`  
		Last Modified: Sun, 08 Aug 2021 01:00:22 GMT  
		Size: 40.3 MB (40312250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48547e29bdd75abab2cbd318d0739f4092117ce9d04e7b8f20c36674abd65e59`  
		Last Modified: Tue, 31 Aug 2021 01:46:36 GMT  
		Size: 851.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ebef378167277f2a504e20691b3f74632e59e23c5761cb5e602a634aa32b1b9`  
		Last Modified: Tue, 31 Aug 2021 01:46:37 GMT  
		Size: 511.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f97155dfcb43995751a1533d2e37802f3b35f78bd9b0eaf5049f79f56199ac90`  
		Last Modified: Tue, 31 Aug 2021 01:46:36 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:xenial` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:70fa660340a344b46cc56b3606dc8abd3bf48b5cbce13d01c720e9793a6bc3c0
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.2 MB (41240746 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe3b34cb9255c8dd390f85c8fe37e6fbe6ac555f86c7e8944cd68da2de2f7633`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 16 Oct 2021 01:48:22 GMT
ADD file:3c6dc937cb7b4c81b42126f377d23320ec1d0a8ca34d38e7c45871f1d08dac43 in / 
# Sat, 16 Oct 2021 01:48:22 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Sat, 16 Oct 2021 01:48:23 GMT
RUN rm -rf /var/lib/apt/lists/*
# Sat, 16 Oct 2021 01:48:24 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Sat, 16 Oct 2021 01:48:25 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:828b35a09f0b2f3d1dead43aa2468ff5eba6c463423b3fff7ee6d150f6fd1b6b`  
		Last Modified: Thu, 05 Aug 2021 00:25:09 GMT  
		Size: 41.2 MB (41239253 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:238e9b8fdf46981043813ae269c4420735959dd01d4d15c420b66448523e9adc`  
		Last Modified: Sat, 16 Oct 2021 01:50:40 GMT  
		Size: 848.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d5b1b49195905e9415adfe3583301316ef591d794fcfd12b5cd29103fa7ee6b`  
		Last Modified: Sat, 16 Oct 2021 01:50:40 GMT  
		Size: 473.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:269a6c6175ba12a0fd708883c2625167711f111f24ce2bb79221fda132487e57`  
		Last Modified: Sat, 16 Oct 2021 01:50:40 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:xenial` - linux; 386

```console
$ docker pull ubuntu@sha256:4a6759446930ee402a2091605c0911f237ad18b5c250a535d11563d9402eb15a
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.8 MB (45817719 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac20e7c3411697a4a85c1cb30850f77b8238e0a0ef0e176ca8f0e763066eed4b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 31 Aug 2021 01:39:31 GMT
ADD file:a4ae521feddf8357667e9361bdd972a69ed945f3857cc8c534652592e432575d in / 
# Tue, 31 Aug 2021 01:39:32 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Tue, 31 Aug 2021 01:39:33 GMT
RUN rm -rf /var/lib/apt/lists/*
# Tue, 31 Aug 2021 01:39:34 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Tue, 31 Aug 2021 01:39:34 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:1335d7ebdbbb7325d434cf945bcb54cb20f7288e1ca2a1cf140ae02b324646e6`  
		Last Modified: Sun, 08 Aug 2021 01:00:22 GMT  
		Size: 45.8 MB (45816182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c250dcd0b24a66322cdee2165435035a76e5b72085df234bfcdc340c5321c74d`  
		Last Modified: Tue, 31 Aug 2021 01:40:23 GMT  
		Size: 851.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df3c7bbf9087c9dae9eb48a2b2a913146a0705560689407ee02802ff92408abf`  
		Last Modified: Tue, 31 Aug 2021 01:40:23 GMT  
		Size: 514.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ea45938bfbd7dd3f314ea2ad08a94370db722a20c33d6407c8eaeaf906b40c5`  
		Last Modified: Tue, 31 Aug 2021 01:40:23 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:xenial` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:cf25d111d193288d47d20a4e5d42a68dc2af24bb962853b067752eca3914355e
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.5 MB (47523633 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:914466c340b7c02825333f4de2597bcd673f18eb0cec83840b13a3cc68338937`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 31 Aug 2021 02:12:03 GMT
ADD file:c84969ed4d4e336ec5996e26e35261f683b36f1af7a978df587296ef5e7a2627 in / 
# Tue, 31 Aug 2021 02:12:21 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Tue, 31 Aug 2021 02:12:31 GMT
RUN rm -rf /var/lib/apt/lists/*
# Tue, 31 Aug 2021 02:12:46 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Tue, 31 Aug 2021 02:12:49 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:5057452c10cfe2216f39949f909f3cd83002d256d1bbd564ae242352a5460fe2`  
		Last Modified: Sun, 08 Aug 2021 01:00:30 GMT  
		Size: 47.5 MB (47522137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c76cb7ccfe1638448c02d9e8f51fae873202f130515c9fb7a791038a2bd9586`  
		Last Modified: Tue, 31 Aug 2021 02:15:30 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22a12ad70abdfd318d55001c9a70e7eccffb1f5ece5eee88d8e4e549083928a9`  
		Last Modified: Tue, 31 Aug 2021 02:15:30 GMT  
		Size: 474.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4e2d97c60bc4668c8613c3ef5ffe0205d9be50368dfe09cb0859beb030ed103`  
		Last Modified: Tue, 31 Aug 2021 02:15:30 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:xenial` - linux; s390x

```console
$ docker pull ubuntu@sha256:5fea5a070916f61785140faa8e16fa8bf7ca3f152ceed9c48154f8aca4c3667e
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.1 MB (44089219 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bdb8683432fbdd1ec03145305370c4ec7079b01e22fcc47dd4df1aa862463474`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 31 Aug 2021 01:43:07 GMT
ADD file:8719dec76e2491e6bcc4cba5072d8123bd3472e72108280ea29f6a34761adbeb in / 
# Tue, 31 Aug 2021 01:43:10 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Tue, 31 Aug 2021 01:43:11 GMT
RUN rm -rf /var/lib/apt/lists/*
# Tue, 31 Aug 2021 01:43:11 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Tue, 31 Aug 2021 01:43:11 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:80d499f9d46bfeec5260ce5a395259ab5e54118e786a0e9023d6550a57730bd4`  
		Last Modified: Tue, 31 Aug 2021 01:45:04 GMT  
		Size: 44.1 MB (44087722 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:883d7cfe3e67b3dd7ffd87697a9050dfad287116e1f38ed165b815d7285a7d70`  
		Last Modified: Tue, 31 Aug 2021 01:44:59 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05e68cf162fecf9f82ab0d540cd0f3af1a4a74defc8ba9434379cbae3a09b30c`  
		Last Modified: Tue, 31 Aug 2021 01:44:59 GMT  
		Size: 478.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bfcc45f37d760e154b69274e44e31fd64b8537f3cb1cba39203b537246bc891`  
		Last Modified: Tue, 31 Aug 2021 01:44:59 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ubuntu:xenial-20210804`

```console
$ docker pull ubuntu@sha256:0f71fa8d4d2d4292c3c617fda2b36f6dabe5c8b6e34c3dc5b0d17d4e704bd39c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `ubuntu:xenial-20210804` - linux; amd64

```console
$ docker pull ubuntu@sha256:a3785f78ab8547ae2710c89e627783cfa7ee7824d3468cae6835c9f4eae23ff7
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.5 MB (46499103 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6f50765242581c887ff1acc2511fa2d885c52d8fb3ac8c4bba131fd86567f2e`
-	Default Command: `["\/bin\/bash"]`

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

### `ubuntu:xenial-20210804` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:b722e2654241f9681f4719dce7aa16a2f0c35769e17a636f5b39a33967d1aeb8
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.3 MB (40313783 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:033c410d53efaab9e847168b94fea14d551788200a15f4d2424c84e4cd2ab8a2`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 31 Aug 2021 01:42:28 GMT
ADD file:294a94a081de785c730003a440a0530a85add2bcb60c0f5bc4ce7ee17867ac4e in / 
# Tue, 31 Aug 2021 01:42:30 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Tue, 31 Aug 2021 01:42:31 GMT
RUN rm -rf /var/lib/apt/lists/*
# Tue, 31 Aug 2021 01:42:33 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Tue, 31 Aug 2021 01:42:33 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:b95ba076a26b98e98eac4b43596b59c20d1e61a36bcaf2afae3aeebadc8844cf`  
		Last Modified: Sun, 08 Aug 2021 01:00:22 GMT  
		Size: 40.3 MB (40312250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48547e29bdd75abab2cbd318d0739f4092117ce9d04e7b8f20c36674abd65e59`  
		Last Modified: Tue, 31 Aug 2021 01:46:36 GMT  
		Size: 851.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ebef378167277f2a504e20691b3f74632e59e23c5761cb5e602a634aa32b1b9`  
		Last Modified: Tue, 31 Aug 2021 01:46:37 GMT  
		Size: 511.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f97155dfcb43995751a1533d2e37802f3b35f78bd9b0eaf5049f79f56199ac90`  
		Last Modified: Tue, 31 Aug 2021 01:46:36 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:xenial-20210804` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:70fa660340a344b46cc56b3606dc8abd3bf48b5cbce13d01c720e9793a6bc3c0
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.2 MB (41240746 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe3b34cb9255c8dd390f85c8fe37e6fbe6ac555f86c7e8944cd68da2de2f7633`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 16 Oct 2021 01:48:22 GMT
ADD file:3c6dc937cb7b4c81b42126f377d23320ec1d0a8ca34d38e7c45871f1d08dac43 in / 
# Sat, 16 Oct 2021 01:48:22 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Sat, 16 Oct 2021 01:48:23 GMT
RUN rm -rf /var/lib/apt/lists/*
# Sat, 16 Oct 2021 01:48:24 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Sat, 16 Oct 2021 01:48:25 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:828b35a09f0b2f3d1dead43aa2468ff5eba6c463423b3fff7ee6d150f6fd1b6b`  
		Last Modified: Thu, 05 Aug 2021 00:25:09 GMT  
		Size: 41.2 MB (41239253 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:238e9b8fdf46981043813ae269c4420735959dd01d4d15c420b66448523e9adc`  
		Last Modified: Sat, 16 Oct 2021 01:50:40 GMT  
		Size: 848.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d5b1b49195905e9415adfe3583301316ef591d794fcfd12b5cd29103fa7ee6b`  
		Last Modified: Sat, 16 Oct 2021 01:50:40 GMT  
		Size: 473.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:269a6c6175ba12a0fd708883c2625167711f111f24ce2bb79221fda132487e57`  
		Last Modified: Sat, 16 Oct 2021 01:50:40 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:xenial-20210804` - linux; 386

```console
$ docker pull ubuntu@sha256:4a6759446930ee402a2091605c0911f237ad18b5c250a535d11563d9402eb15a
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.8 MB (45817719 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac20e7c3411697a4a85c1cb30850f77b8238e0a0ef0e176ca8f0e763066eed4b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 31 Aug 2021 01:39:31 GMT
ADD file:a4ae521feddf8357667e9361bdd972a69ed945f3857cc8c534652592e432575d in / 
# Tue, 31 Aug 2021 01:39:32 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Tue, 31 Aug 2021 01:39:33 GMT
RUN rm -rf /var/lib/apt/lists/*
# Tue, 31 Aug 2021 01:39:34 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Tue, 31 Aug 2021 01:39:34 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:1335d7ebdbbb7325d434cf945bcb54cb20f7288e1ca2a1cf140ae02b324646e6`  
		Last Modified: Sun, 08 Aug 2021 01:00:22 GMT  
		Size: 45.8 MB (45816182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c250dcd0b24a66322cdee2165435035a76e5b72085df234bfcdc340c5321c74d`  
		Last Modified: Tue, 31 Aug 2021 01:40:23 GMT  
		Size: 851.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df3c7bbf9087c9dae9eb48a2b2a913146a0705560689407ee02802ff92408abf`  
		Last Modified: Tue, 31 Aug 2021 01:40:23 GMT  
		Size: 514.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ea45938bfbd7dd3f314ea2ad08a94370db722a20c33d6407c8eaeaf906b40c5`  
		Last Modified: Tue, 31 Aug 2021 01:40:23 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:xenial-20210804` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:cf25d111d193288d47d20a4e5d42a68dc2af24bb962853b067752eca3914355e
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.5 MB (47523633 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:914466c340b7c02825333f4de2597bcd673f18eb0cec83840b13a3cc68338937`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 31 Aug 2021 02:12:03 GMT
ADD file:c84969ed4d4e336ec5996e26e35261f683b36f1af7a978df587296ef5e7a2627 in / 
# Tue, 31 Aug 2021 02:12:21 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Tue, 31 Aug 2021 02:12:31 GMT
RUN rm -rf /var/lib/apt/lists/*
# Tue, 31 Aug 2021 02:12:46 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Tue, 31 Aug 2021 02:12:49 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:5057452c10cfe2216f39949f909f3cd83002d256d1bbd564ae242352a5460fe2`  
		Last Modified: Sun, 08 Aug 2021 01:00:30 GMT  
		Size: 47.5 MB (47522137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c76cb7ccfe1638448c02d9e8f51fae873202f130515c9fb7a791038a2bd9586`  
		Last Modified: Tue, 31 Aug 2021 02:15:30 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22a12ad70abdfd318d55001c9a70e7eccffb1f5ece5eee88d8e4e549083928a9`  
		Last Modified: Tue, 31 Aug 2021 02:15:30 GMT  
		Size: 474.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4e2d97c60bc4668c8613c3ef5ffe0205d9be50368dfe09cb0859beb030ed103`  
		Last Modified: Tue, 31 Aug 2021 02:15:30 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:xenial-20210804` - linux; s390x

```console
$ docker pull ubuntu@sha256:5fea5a070916f61785140faa8e16fa8bf7ca3f152ceed9c48154f8aca4c3667e
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.1 MB (44089219 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bdb8683432fbdd1ec03145305370c4ec7079b01e22fcc47dd4df1aa862463474`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 31 Aug 2021 01:43:07 GMT
ADD file:8719dec76e2491e6bcc4cba5072d8123bd3472e72108280ea29f6a34761adbeb in / 
# Tue, 31 Aug 2021 01:43:10 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Tue, 31 Aug 2021 01:43:11 GMT
RUN rm -rf /var/lib/apt/lists/*
# Tue, 31 Aug 2021 01:43:11 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Tue, 31 Aug 2021 01:43:11 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:80d499f9d46bfeec5260ce5a395259ab5e54118e786a0e9023d6550a57730bd4`  
		Last Modified: Tue, 31 Aug 2021 01:45:04 GMT  
		Size: 44.1 MB (44087722 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:883d7cfe3e67b3dd7ffd87697a9050dfad287116e1f38ed165b815d7285a7d70`  
		Last Modified: Tue, 31 Aug 2021 01:44:59 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05e68cf162fecf9f82ab0d540cd0f3af1a4a74defc8ba9434379cbae3a09b30c`  
		Last Modified: Tue, 31 Aug 2021 01:44:59 GMT  
		Size: 478.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bfcc45f37d760e154b69274e44e31fd64b8537f3cb1cba39203b537246bc891`  
		Last Modified: Tue, 31 Aug 2021 01:44:59 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
