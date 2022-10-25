<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `ubuntu`

-	[`ubuntu:14.04`](#ubuntu1404)
-	[`ubuntu:16.04`](#ubuntu1604)
-	[`ubuntu:18.04`](#ubuntu1804)
-	[`ubuntu:20.04`](#ubuntu2004)
-	[`ubuntu:22.04`](#ubuntu2204)
-	[`ubuntu:22.10`](#ubuntu2210)
-	[`ubuntu:bionic`](#ubuntubionic)
-	[`ubuntu:bionic-20221019`](#ubuntubionic-20221019)
-	[`ubuntu:focal`](#ubuntufocal)
-	[`ubuntu:focal-20221019`](#ubuntufocal-20221019)
-	[`ubuntu:jammy`](#ubuntujammy)
-	[`ubuntu:jammy-20221020`](#ubuntujammy-20221020)
-	[`ubuntu:kinetic`](#ubuntukinetic)
-	[`ubuntu:kinetic-20221024`](#ubuntukinetic-20221024)
-	[`ubuntu:latest`](#ubuntulatest)
-	[`ubuntu:rolling`](#ubunturolling)
-	[`ubuntu:trusty`](#ubuntutrusty)
-	[`ubuntu:trusty-20191217`](#ubuntutrusty-20191217)
-	[`ubuntu:xenial`](#ubuntuxenial)
-	[`ubuntu:xenial-20210804`](#ubuntuxenial-20210804)

## `ubuntu:14.04`

```console
$ docker pull ubuntu@sha256:d7a459ecd77ebb09525584f2c3e1bb7f6a2879d90df8a3523c1b899dfc2a226f
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
$ docker pull ubuntu@sha256:d34202d0ce9f1a55b9fffa1d69af2821dcf9645cc655e96a5b168c2a9265d5db
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.7 MB (64700984 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8a7f3400ca032052bf769658a0a6f7562e441504c7da16527defa818a24fcf0`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 02 Aug 2022 01:41:30 GMT
ADD file:e9d55e059869915743a8ca8e64582d23c48fe7e90e439daccd56d3e08e8673b4 in / 
# Tue, 02 Aug 2022 01:41:31 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Tue, 02 Aug 2022 01:41:32 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Tue, 02 Aug 2022 01:41:32 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Tue, 02 Aug 2022 01:41:33 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:0db3a87a3d7959895fd860c8b924980adda6e77f5d315b6676a4ac0e12518978`  
		Last Modified: Thu, 19 Dec 2019 06:16:01 GMT  
		Size: 64.6 MB (64624015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a430e3e7a1afcac7bf89d27c42804489d76ac8775a945924494e9e5794f0ce6`  
		Last Modified: Tue, 02 Aug 2022 01:44:15 GMT  
		Size: 76.8 KB (76779 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb8c3e99facaf81b42b2e4e24792e7254297607e2273054e5f729712163cafc2`  
		Last Modified: Tue, 02 Aug 2022 01:44:15 GMT  
		Size: 190.0 B  
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
$ docker pull ubuntu@sha256:c97d63976268e6c2f3764be91e59f82009b2883d22c3dc6ff1f63e3ad6abdb05
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.4 MB (68445472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8a7710ba73fd21ad01442fe2b079693c60a5b77b18403d56e5da5448e325d06`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 05 Apr 2022 22:39:14 GMT
ADD file:e034601a525da53b0f39bb04d6e2264e2a592d0ae7c21e00697b9b62ca1efec9 in / 
# Tue, 05 Apr 2022 22:39:15 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Tue, 05 Apr 2022 22:39:16 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Tue, 05 Apr 2022 22:39:17 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Tue, 05 Apr 2022 22:39:18 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:630712fe5783a35ad52a7026002143cb4f8fe65d34097dcaa4c4331b1b059a17`  
		Last Modified: Thu, 19 Dec 2019 04:44:02 GMT  
		Size: 68.4 MB (68380440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03124bfb4886d9ba012a00a087fb41b4cc7e99517b3e2a2e6fd1e2ad327af191`  
		Last Modified: Tue, 05 Apr 2022 22:40:17 GMT  
		Size: 64.9 KB (64870 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22b953ad705784700c1611b7258f6c783a34b06bf27ed3efbd9acc7be80ba991`  
		Last Modified: Tue, 05 Apr 2022 22:40:17 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:14.04` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:209f78eaf05254c51cff7676b913bcb70c1da54e58ae728a592ea58f3b5552b4
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.4 MB (73443164 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd23a098588cb567106c63829bf08759e87f4235bbd4c90168e6b065420ac853`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 02 Aug 2022 01:31:42 GMT
ADD file:581665e92c72c8638b40fe509de6479dc1a5d7b5ffe8d6706006178c406e35e2 in / 
# Tue, 02 Aug 2022 01:31:47 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Tue, 02 Aug 2022 01:31:48 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Tue, 02 Aug 2022 01:31:50 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Tue, 02 Aug 2022 01:31:50 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:bed4146d918c6c9a57bc3a8bf829e702975b0e53c7f25920fe9435b58ed6b64f`  
		Last Modified: Thu, 19 Dec 2019 04:26:52 GMT  
		Size: 73.4 MB (73379539 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:736dbcbc0bcb73948970c71c59c6fc5662698a0cdca10a232da87ede89aabeef`  
		Last Modified: Tue, 02 Aug 2022 01:35:21 GMT  
		Size: 63.4 KB (63436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:376b7bbeb4d42e6e9b75e9ad5bd043790235c8963cac05a03bc5400002ae965b`  
		Last Modified: Tue, 02 Aug 2022 01:35:21 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ubuntu:16.04`

```console
$ docker pull ubuntu@sha256:91bd29a464fdabfcf44e29e1f2a5f213c6dfa750b6290e40dd6998ac79da3c41
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
$ docker pull ubuntu@sha256:696252dd941a9a0ca7db7ca8d9fbb91d838cc9bfb27403219953af6750a89111
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.3 MB (40313786 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20832692ca6e913217051aa57084ec76c076987a63cd497100d754b27097fa33`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 02 Aug 2022 01:41:46 GMT
ADD file:294a94a081de785c730003a440a0530a85add2bcb60c0f5bc4ce7ee17867ac4e in / 
# Tue, 02 Aug 2022 01:41:47 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Tue, 02 Aug 2022 01:41:48 GMT
RUN rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 01:41:49 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Tue, 02 Aug 2022 01:41:49 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:b95ba076a26b98e98eac4b43596b59c20d1e61a36bcaf2afae3aeebadc8844cf`  
		Last Modified: Sun, 08 Aug 2021 01:00:22 GMT  
		Size: 40.3 MB (40312250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32c9df55506368eeeb59c5f56bf5d6f9ef4476a6b1e43154eebe32e436e60d7a`  
		Last Modified: Tue, 02 Aug 2022 01:44:42 GMT  
		Size: 849.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60aa30d82c4849b80da22554e0006d9c23c68a807fcb795b2f35ac6c02549eca`  
		Last Modified: Tue, 02 Aug 2022 01:44:42 GMT  
		Size: 515.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e61b5d5a768deb5e021d74947bacf44422a006a3495d70395a7d745e07fab3f3`  
		Last Modified: Tue, 02 Aug 2022 01:44:42 GMT  
		Size: 172.0 B  
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
$ docker pull ubuntu@sha256:bcb8397f1390f4f0757ca06ce184f05c8ce0c7a4b5ff93f9ab029a581192917b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.8 MB (45817719 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:276b5b6b7721e99481801a9aaf21a4d2bf6ba6f6676f720f6f4e0da40a71fb19`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 05 Apr 2022 22:39:28 GMT
ADD file:a4ae521feddf8357667e9361bdd972a69ed945f3857cc8c534652592e432575d in / 
# Tue, 05 Apr 2022 22:39:29 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Tue, 05 Apr 2022 22:39:30 GMT
RUN rm -rf /var/lib/apt/lists/*
# Tue, 05 Apr 2022 22:39:31 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Tue, 05 Apr 2022 22:39:32 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:1335d7ebdbbb7325d434cf945bcb54cb20f7288e1ca2a1cf140ae02b324646e6`  
		Last Modified: Sun, 08 Aug 2021 01:00:22 GMT  
		Size: 45.8 MB (45816182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffa6a227af79fa98ebbd1d2da516e2b7ce1cea5519a760cd0f6688738fbdb951`  
		Last Modified: Tue, 05 Apr 2022 22:40:40 GMT  
		Size: 851.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab3928723c2c34ecd7264ce4e195ddda11403213b1c93d02e8efcd11de4b07a1`  
		Last Modified: Tue, 05 Apr 2022 22:40:40 GMT  
		Size: 514.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e468001dd2f338d54f47d062d65db61c754f09897744d97084afa15cee021200`  
		Last Modified: Tue, 05 Apr 2022 22:40:40 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:16.04` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:4ef33ed6b1af10706727d280de436bced5e9413cba7992d6126c866efd79cacd
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.5 MB (47523643 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17fb9d3bc97649795df6522739036df75814819b4b48997a6e05345dcd5e6845`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 02 Aug 2022 01:32:03 GMT
ADD file:c84969ed4d4e336ec5996e26e35261f683b36f1af7a978df587296ef5e7a2627 in / 
# Tue, 02 Aug 2022 01:32:06 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Tue, 02 Aug 2022 01:32:07 GMT
RUN rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 01:32:08 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Tue, 02 Aug 2022 01:32:08 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:5057452c10cfe2216f39949f909f3cd83002d256d1bbd564ae242352a5460fe2`  
		Last Modified: Sun, 08 Aug 2021 01:00:30 GMT  
		Size: 47.5 MB (47522137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72bced789eccb5759f541a5b15b9a3031c06cc54bdbff1a553cc0ef29ddad2bc`  
		Last Modified: Tue, 02 Aug 2022 01:36:22 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a11a61259761ffe18601a628413443ccb5dee06a185a81c902220dfc070801c3`  
		Last Modified: Tue, 02 Aug 2022 01:35:56 GMT  
		Size: 483.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3272460dff18ff8fd96d33337b0ff5cc5d9d2e7f158c662273e1bb760c7f9722`  
		Last Modified: Tue, 02 Aug 2022 01:36:06 GMT  
		Size: 171.0 B  
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
$ docker pull ubuntu@sha256:b0f7a97d9f116e7d5fe3b7f3675abbf75eed0454b6f1d415ccad79e03bc33f5c
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
$ docker pull ubuntu@sha256:cd9842111e50ca15135bd04bccfeed4e1e63006ee7d2210927fc8f49bacb4ee8
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.7 MB (26712500 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71eaf13299f415122ad887b4592146a6b6f5e80cd69e0cd4650102fa3a99972c`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 25 Oct 2022 01:53:28 GMT
ADD file:fc5d658c47ede58827812b75a311353be776e41e2dd339b8906839527c9b5247 in / 
# Tue, 25 Oct 2022 01:53:28 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:a404e54162968593b8d92b571f3cdd673e4c9eab5d9be28d7c494595c0aa6682`  
		Last Modified: Wed, 19 Oct 2022 22:03:02 GMT  
		Size: 26.7 MB (26712500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:18.04` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:4f8597f98459cabb2836f2c7feb17be1b402b6c2acb3fae245410f085f6d652e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.3 MB (22305721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfbba71faceed324ade917d45f467b6d30aca84d64a9ab26371026aa09a51b53`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 05 Oct 2022 00:13:31 GMT
ADD file:20e0d71059d38b1e18636b9db71f534d7297c3f571d73d45a75b4b8d3cac86c7 in / 
# Wed, 05 Oct 2022 00:13:32 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:91bb9a9844d67fd31f07ebd74dc8a4f4f18e2f959d3aa2166aca86ae57f353c6`  
		Last Modified: Wed, 05 Oct 2022 00:15:26 GMT  
		Size: 22.3 MB (22305721 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:18.04` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:354437aa4d06f7d91cf3ddcd97efac9d9cf746c8b9b0071acf2b4b06d5c72414
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.7 MB (23734594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7613777544784a5c0496fb94beaa478ca1de1ea80605e5e59fb43691bd2743b1`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 05 Oct 2022 00:02:02 GMT
ADD file:4beae13e1fd7bb92776c08a5cd95feb81b8b3c80522ed8513f2441adfb1661ac in / 
# Wed, 05 Oct 2022 00:02:02 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:0e9b69cf8198dafe5b7db1eee7b96b96238f8346ec641dd44f961f7996c2c152`  
		Last Modified: Wed, 05 Oct 2022 00:03:33 GMT  
		Size: 23.7 MB (23734594 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:18.04` - linux; 386

```console
$ docker pull ubuntu@sha256:d10b3e9a7d97e55aca798cac25df0d5181dfcbdf99b47a78c808b94b04e2e48d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.2 MB (27165243 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:787cfa9c6e1ba4e1bef087fd4fb71a2a8b8544237cc6d5f32bcb54b55e15e7eb`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 04 Oct 2022 23:51:15 GMT
ADD file:ee35e95b906b98c2d7493d8c365bf5aaf351251abce763f9be2d9fa6cc541aaf in / 
# Tue, 04 Oct 2022 23:51:15 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:6d1a231d13b300fc73c20f074f3accd74dcff41afd006c272719fdf8cf9be075`  
		Last Modified: Tue, 04 Oct 2022 23:52:01 GMT  
		Size: 27.2 MB (27165243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:18.04` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:f1ab5016e8faefa337896082ba69be60dfc7e3a6dd1f34f1fe3b08505599942b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.4 MB (30442565 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a815daf6860c7a9ad0aba8a52304a0137bdc07841495c412c27ea3e10a809199`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 05 Oct 2022 10:51:52 GMT
ADD file:d93b8e74342ae6048a42c90c30192dd384e92b697ad4d8d5944868e03325820c in / 
# Wed, 05 Oct 2022 10:51:54 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:faece833463c99bd10748da29171f2d588a627912f7bbb982b3ca4512dd39eed`  
		Last Modified: Wed, 05 Oct 2022 10:54:03 GMT  
		Size: 30.4 MB (30442565 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:18.04` - linux; s390x

```console
$ docker pull ubuntu@sha256:e8b5b1b0fd8023b3a13efc5ad58e7768520fe114448ebc800d4b68983886b8f2
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.4 MB (25371461 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f7c1da1bebf686edaa4ffa3b904cacd16d80b9ed086f550069be9eef0e09d11`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 25 Oct 2022 01:23:02 GMT
ADD file:0843e89b8865a30626cece7a42cf27708a86422aadb28029168b2f159a8768fa in / 
# Tue, 25 Oct 2022 01:23:03 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:4cd692a206d359f66e10c4f4f2a37009c4162f022df78a9bb8e8c24def290167`  
		Last Modified: Tue, 25 Oct 2022 01:24:23 GMT  
		Size: 25.4 MB (25371461 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ubuntu:20.04`

```console
$ docker pull ubuntu@sha256:90aa2a38a4e0a2450d0046fc827eef8c88aa866fd334478d15a3f2c432e66826
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
$ docker pull ubuntu@sha256:b25ef49a40b7797937d0d23eca3b0a41701af6757afca23d504d50826f0b37ce
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.6 MB (28577834 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:680e5dfb52c74a1fbc99c2922c8e25b5736e6cd1a3d9430890d52a4f8f44087a`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 25 Oct 2022 01:53:34 GMT
ADD file:7633003155a1059419aa1a6756fafb6e4f419d65bff7feb7c945de1e29dccb1e in / 
# Tue, 25 Oct 2022 01:53:35 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:eaead16dc43bb8811d4ff450935d607f9ba4baffda4fc110cc402fa43f601d83`  
		Last Modified: Fri, 21 Oct 2022 03:03:39 GMT  
		Size: 28.6 MB (28577834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:20.04` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:e5a044019a4cde9840aca3ed43534d096e1b6f0c035f7780a2da41827d25986f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.6 MB (24590092 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f43fba273ad6a0820c488b21308a878f86cde06700761ee0159e8924ee65f4db`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 05 Oct 2022 00:13:44 GMT
ADD file:75870468a948359044fa3df6c07c80badfea3dcde4823d41a19285436c40cf76 in / 
# Wed, 05 Oct 2022 00:13:44 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:e679d63f382033c15f8f921851bd71fb8a85a432c0a7a612bbef16e989075145`  
		Last Modified: Wed, 05 Oct 2022 00:15:44 GMT  
		Size: 24.6 MB (24590092 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:20.04` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:9488eba63bece0e05cd2cd84ce4dbe2710c8666f10259bbb9ebe55c4ff4f5704
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.2 MB (27191622 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f12f227aa3fdd90f0418130698b75f1eeb68f885f0760866a7801fa3877df26a`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 05 Oct 2022 00:02:10 GMT
ADD file:30b589901d2a6b82d0b7271487bdaf37514649a798cc13a17f74394321bdd051 in / 
# Wed, 05 Oct 2022 00:02:11 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:514fa78e57ce0d9437bc984cc36ab780c24b69da2b922bfff16737072e3e7de2`  
		Last Modified: Wed, 05 Oct 2022 00:03:51 GMT  
		Size: 27.2 MB (27191622 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:20.04` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:00f813cc648193e6c81b8afe75c7b7252287dcad966c6857934d9449d4397470
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.3 MB (33296076 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fde6bd3e00a511ec2c1633fdbfd4bc0cdd963e577d1b88762b889904020171e5`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 05 Oct 2022 10:52:08 GMT
ADD file:75224b75d955b3021df8214497d6835e1aff42b5ce83f96b779b63c4a8e15faf in / 
# Wed, 05 Oct 2022 10:52:10 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:ecaa0fe591301d50850e37b61a6fac5429c04a3c39272da2f7b748eaed7f5c52`  
		Last Modified: Wed, 05 Oct 2022 10:54:26 GMT  
		Size: 33.3 MB (33296076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:20.04` - linux; riscv64

```console
$ docker pull ubuntu@sha256:fc82f4ab16ae703eaa7668641f603989d88f6d6cc2c8f829668841ea8b9ff57b
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.2 MB (24242839 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:718ca6f5fba830fb1b140b0e64b7932c9c76bd695e6d7c5d5cb29f6a5af22f05`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 05 Oct 2022 00:12:13 GMT
ADD file:8c408c11e1eeed71fdd784404ddf9ac52b700161e6187e2313c2751d756e3442 in / 
# Wed, 05 Oct 2022 00:12:14 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:edcdeceb0859700b9f2e87516c30c0049092e29666696c30e6b862e0df3d4961`  
		Last Modified: Wed, 05 Oct 2022 00:29:16 GMT  
		Size: 24.2 MB (24242839 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:20.04` - linux; s390x

```console
$ docker pull ubuntu@sha256:3d2f0fd07dc2d5099f0fb58083ba3bcb9c1daf2225f7205cb8b1ddc7bfab3f24
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.0 MB (27016028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:702f00d888407e4809f313324d91de5d4b8d00bcfb8172ef98fb5bf4b36d87ff`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 25 Oct 2022 01:23:11 GMT
ADD file:c657b467ecb15f1f4a49a5f04a525f38924750c8187c9ef9f0b886d0264e21f1 in / 
# Tue, 25 Oct 2022 01:23:12 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:a63328f08dbd14148b5ffe154c18846ead48e759779d007b78ec3fb19f5f43a5`  
		Last Modified: Tue, 25 Oct 2022 01:24:36 GMT  
		Size: 27.0 MB (27016028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ubuntu:22.04`

```console
$ docker pull ubuntu@sha256:2ec38e3c5c9e889445516d2b044d061c23dc23d321e4e1508957997f4001dc1d
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
$ docker pull ubuntu@sha256:dda6886d8d153a2d86f046c9335123c6151d83fd63e446b752ed8d9da261205d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.4 MB (30426374 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cdb68b455a141ed921945f6d39a8c0694a7e21a37b2b030488d73e38875a26cc`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 25 Oct 2022 01:53:41 GMT
ADD file:ba96f963bbfd429a0839c40603fdd7829eaca58f20adfa0d15e6beae8244bc08 in / 
# Tue, 25 Oct 2022 01:53:41 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:301a8b74f71f85f3a31e9c7e7fedd5b001ead5bcf895bc2911c1d260e06bd987`  
		Last Modified: Fri, 21 Oct 2022 03:03:39 GMT  
		Size: 30.4 MB (30426374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:22.04` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:60c321f2700325103a0c185adeadfd5a93dbb3cd67dfbdd5b79a8aafa38325c2
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.0 MB (27018632 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:938dcade566893210cea0198ac17b9bd44033d0ac2376015cd86bf4d7b27b125`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 05 Oct 2022 00:13:57 GMT
ADD file:11e25fc4812528219464289700bb0495bf9298918899103c33d7ef9022690eb0 in / 
# Wed, 05 Oct 2022 00:13:57 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:99b9c73338a7c0dbe41f9fc543fae706650a616453e1e330f870e20916c18a11`  
		Last Modified: Wed, 05 Oct 2022 00:16:02 GMT  
		Size: 27.0 MB (27018632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:22.04` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:82aee33baa9ffa1accfc1c5e9865aa59b94ec289441894ddb8acad412e16168d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.4 MB (28382255 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d63f752103bb93d846e17fa9996d3e708717c51b106382fe84d8527ee47a3547`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 05 Oct 2022 00:02:19 GMT
ADD file:fd8103ca1472a4f51eeff3e22fbd1dfd61a3d22c34f16a61ef1ba016352e3629 in / 
# Wed, 05 Oct 2022 00:02:20 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:d6cb415e2683249f7884ee5367306b023c72f907afeca2a30ca19c8de5f4f7d9`  
		Last Modified: Tue, 04 Oct 2022 15:08:22 GMT  
		Size: 28.4 MB (28382255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:22.04` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:d80c03cea627ee3ceba6eaa9f0b168060923f6150b167c99ed446fa234863bcd
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.7 MB (35709341 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6670c4b363d0702a3dbcad7092e05567079bbede0e17609aa8d8612e936acab`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 05 Oct 2022 10:52:24 GMT
ADD file:5f3953a21754ce756642c9ddcf521f2cfe220a5fe988ccec51085bd074fbe46e in / 
# Wed, 05 Oct 2022 10:52:26 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:5053ecffedc109608feacf4836ad15e0f7b2f6a411250a41574342de479c4760`  
		Last Modified: Wed, 05 Oct 2022 10:54:49 GMT  
		Size: 35.7 MB (35709341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:22.04` - linux; riscv64

```console
$ docker pull ubuntu@sha256:8b497a96364d0dcb3dc7f4f237dbce73958bae2aa2d2989c920467f028c49534
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.7 MB (27747416 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c808209261fc55418f60b818c8e1af2266b637a0d290cd1f65aa1d24ba55bf31`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 05 Oct 2022 00:14:15 GMT
ADD file:e1fa146cf8e97dd6a2f3ebb2dacba539556ef4a1e87dc53bd745a3cf0ba10aef in / 
# Wed, 05 Oct 2022 00:14:16 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:cbeff255552ba792be63b343113968df42de6f599d1372edd4c7346d08dfeace`  
		Last Modified: Wed, 05 Oct 2022 00:31:39 GMT  
		Size: 27.7 MB (27747416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:22.04` - linux; s390x

```console
$ docker pull ubuntu@sha256:0a00cd261964effe192c08403af7c075c8713ead4e0729cb9794e5514ab6310b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.6 MB (28641668 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b87637e0f0a74618b572a61c6e411c31b1073d97c4ef7ac36986eaa55bc31deb`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 25 Oct 2022 01:23:21 GMT
ADD file:d9af7670f58e9478e400dac85a0fcb07a4209846dbd1ea560fdc6de6e2cb5e4e in / 
# Tue, 25 Oct 2022 01:23:22 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:9aed974aece14dd3aed00810d58a89e87eb5be9ad1c6fbb1ed077dc3f145dccc`  
		Last Modified: Tue, 25 Oct 2022 01:24:48 GMT  
		Size: 28.6 MB (28641668 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ubuntu:22.10`

```console
$ docker pull ubuntu@sha256:53d8acab9c74357830f822f89ecaf95a6a4a59aff9d3d6e74d8e842b4ecbeb31
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; riscv64
	-	linux; s390x

### `ubuntu:22.10` - linux; amd64

```console
$ docker pull ubuntu@sha256:17e4f3973ec125dcb7b97ed18da394a348b5ed7c1753d68fe6d20996184c198a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.5 MB (27457582 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f175c10c2b410262bdbcb91b176a308d15dd1f77a80f00b8488fe84a9cabf7e`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 25 Oct 2022 01:53:48 GMT
ADD file:610b4bc612cfad108d07bf023abb796fe6c02a4b6305d824d5d556b7dc85aa89 in / 
# Tue, 25 Oct 2022 01:53:48 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:bcd446fbf8a137bbf135b63332ebcd0c3e9880060bc5b41962fbbb07e94062b7`  
		Last Modified: Tue, 25 Oct 2022 01:55:07 GMT  
		Size: 27.5 MB (27457582 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:22.10` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:b6a6cc304b464d9730ab10c79c3c2b8ad9d92a86269b4f8808e7d9b17deb46a5
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.9 MB (25873193 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c738aa721c7c4e87815e177cae4e37893e3282c0b2ce6512d0a2b41192cec59`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 05 Oct 2022 00:14:09 GMT
ADD file:4b538f2c7b46aa601d747159ce9e8c2c7a99b2b6e09e4efe1073ca58e47fbeed in / 
# Wed, 05 Oct 2022 00:14:09 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:788f7bb1e1d719f6a9a9b3b1530cc5bbe5b808a2ad77a65f23e2c6d15b8ae546`  
		Last Modified: Wed, 05 Oct 2022 00:16:28 GMT  
		Size: 25.9 MB (25873193 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:22.10` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:6717e9297a44d81ab1b68a47aacce1eb9032a827e5550df658d2fbd646a3e8ee
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.7 MB (26690398 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39f5d02545a9b390e470a566bc049fcd716dcc3fdf7c7202202701c8fc188935`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 05 Oct 2022 00:02:29 GMT
ADD file:2496d47197031551828443c95a5e1dc6bb6dc7855695a8470f3ec96e8441e76b in / 
# Wed, 05 Oct 2022 00:02:30 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:9a768b6c77af7a723d25d349fe4a633e82e8ad41fae270b2bbee8849bb840009`  
		Last Modified: Wed, 05 Oct 2022 00:04:31 GMT  
		Size: 26.7 MB (26690398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:22.10` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:a7cd81b3fac5c8771e9924dc9dd6dc12c2eead4ea98d5383c8fdce13d828ca47
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.1 MB (32115528 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d7dcae3381fd5e36b661f8eed3ec64dcdd6144c4833dc0cc152bbb672f15557`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 05 Oct 2022 10:52:41 GMT
ADD file:88a1f03ef21cfaa40a714986930314d37550633cb8512f4b6f8f181d8578923a in / 
# Wed, 05 Oct 2022 10:52:43 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:21fc6649e0514e6dd480d6ec510ee3e255e841bc45eac6d3089ae5a1b109f126`  
		Last Modified: Wed, 05 Oct 2022 10:55:19 GMT  
		Size: 32.1 MB (32115528 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:22.10` - linux; riscv64

```console
$ docker pull ubuntu@sha256:014b7c9f2e08f240bd7611ecd2c207db6917e237b15bd4dd80bb19b4afc761bc
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.6 MB (25618700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6eeea9f38c5cada2aa1969a46596b8afb51fcbbc4b23abd3e166c7f26ebda815`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 05 Oct 2022 00:16:49 GMT
ADD file:2d01ff45e6105658cf6791d4ade5cc3168c7d455422fc973a54a795907023c4e in / 
# Wed, 05 Oct 2022 00:16:51 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:69c33ccbf3d1b09c78fae3f88deb756ae33a9e4610a01fc9ab8b457ee6107d7f`  
		Last Modified: Wed, 05 Oct 2022 00:35:11 GMT  
		Size: 25.6 MB (25618700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:22.10` - linux; s390x

```console
$ docker pull ubuntu@sha256:85bc42d3f6b0dd83e6a765456a47791f52f1d97f19cbbd494bce7e67fad51e47
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.0 MB (26022178 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08293ad2ee54d23056e5c346d001d71399750d119e0a686166fa2d160ff18f77`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 25 Oct 2022 01:23:31 GMT
ADD file:9c0c4172b14f0d37b0b074729a4738aeb165efe5c83e2d9bfefc5b39e4a4fe0b in / 
# Tue, 25 Oct 2022 01:23:32 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:cf61a33f110308ce64c1dd7a5dddf2a5587ee1c8ab2351219b925428957cbc10`  
		Last Modified: Tue, 25 Oct 2022 01:25:01 GMT  
		Size: 26.0 MB (26022178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ubuntu:bionic`

```console
$ docker pull ubuntu@sha256:b0f7a97d9f116e7d5fe3b7f3675abbf75eed0454b6f1d415ccad79e03bc33f5c
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
$ docker pull ubuntu@sha256:cd9842111e50ca15135bd04bccfeed4e1e63006ee7d2210927fc8f49bacb4ee8
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.7 MB (26712500 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71eaf13299f415122ad887b4592146a6b6f5e80cd69e0cd4650102fa3a99972c`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 25 Oct 2022 01:53:28 GMT
ADD file:fc5d658c47ede58827812b75a311353be776e41e2dd339b8906839527c9b5247 in / 
# Tue, 25 Oct 2022 01:53:28 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:a404e54162968593b8d92b571f3cdd673e4c9eab5d9be28d7c494595c0aa6682`  
		Last Modified: Wed, 19 Oct 2022 22:03:02 GMT  
		Size: 26.7 MB (26712500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:bionic` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:4f8597f98459cabb2836f2c7feb17be1b402b6c2acb3fae245410f085f6d652e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.3 MB (22305721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfbba71faceed324ade917d45f467b6d30aca84d64a9ab26371026aa09a51b53`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 05 Oct 2022 00:13:31 GMT
ADD file:20e0d71059d38b1e18636b9db71f534d7297c3f571d73d45a75b4b8d3cac86c7 in / 
# Wed, 05 Oct 2022 00:13:32 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:91bb9a9844d67fd31f07ebd74dc8a4f4f18e2f959d3aa2166aca86ae57f353c6`  
		Last Modified: Wed, 05 Oct 2022 00:15:26 GMT  
		Size: 22.3 MB (22305721 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:bionic` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:354437aa4d06f7d91cf3ddcd97efac9d9cf746c8b9b0071acf2b4b06d5c72414
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.7 MB (23734594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7613777544784a5c0496fb94beaa478ca1de1ea80605e5e59fb43691bd2743b1`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 05 Oct 2022 00:02:02 GMT
ADD file:4beae13e1fd7bb92776c08a5cd95feb81b8b3c80522ed8513f2441adfb1661ac in / 
# Wed, 05 Oct 2022 00:02:02 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:0e9b69cf8198dafe5b7db1eee7b96b96238f8346ec641dd44f961f7996c2c152`  
		Last Modified: Wed, 05 Oct 2022 00:03:33 GMT  
		Size: 23.7 MB (23734594 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:bionic` - linux; 386

```console
$ docker pull ubuntu@sha256:d10b3e9a7d97e55aca798cac25df0d5181dfcbdf99b47a78c808b94b04e2e48d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.2 MB (27165243 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:787cfa9c6e1ba4e1bef087fd4fb71a2a8b8544237cc6d5f32bcb54b55e15e7eb`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 04 Oct 2022 23:51:15 GMT
ADD file:ee35e95b906b98c2d7493d8c365bf5aaf351251abce763f9be2d9fa6cc541aaf in / 
# Tue, 04 Oct 2022 23:51:15 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:6d1a231d13b300fc73c20f074f3accd74dcff41afd006c272719fdf8cf9be075`  
		Last Modified: Tue, 04 Oct 2022 23:52:01 GMT  
		Size: 27.2 MB (27165243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:bionic` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:f1ab5016e8faefa337896082ba69be60dfc7e3a6dd1f34f1fe3b08505599942b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.4 MB (30442565 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a815daf6860c7a9ad0aba8a52304a0137bdc07841495c412c27ea3e10a809199`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 05 Oct 2022 10:51:52 GMT
ADD file:d93b8e74342ae6048a42c90c30192dd384e92b697ad4d8d5944868e03325820c in / 
# Wed, 05 Oct 2022 10:51:54 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:faece833463c99bd10748da29171f2d588a627912f7bbb982b3ca4512dd39eed`  
		Last Modified: Wed, 05 Oct 2022 10:54:03 GMT  
		Size: 30.4 MB (30442565 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:bionic` - linux; s390x

```console
$ docker pull ubuntu@sha256:e8b5b1b0fd8023b3a13efc5ad58e7768520fe114448ebc800d4b68983886b8f2
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.4 MB (25371461 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f7c1da1bebf686edaa4ffa3b904cacd16d80b9ed086f550069be9eef0e09d11`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 25 Oct 2022 01:23:02 GMT
ADD file:0843e89b8865a30626cece7a42cf27708a86422aadb28029168b2f159a8768fa in / 
# Tue, 25 Oct 2022 01:23:03 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:4cd692a206d359f66e10c4f4f2a37009c4162f022df78a9bb8e8c24def290167`  
		Last Modified: Tue, 25 Oct 2022 01:24:23 GMT  
		Size: 25.4 MB (25371461 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ubuntu:bionic-20221019`

```console
$ docker pull ubuntu@sha256:d01d31c50b7ca8397b001b3ef36d8b4f5468104aaf86890c881fdfe21c8ee6df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; s390x

### `ubuntu:bionic-20221019` - linux; amd64

```console
$ docker pull ubuntu@sha256:cd9842111e50ca15135bd04bccfeed4e1e63006ee7d2210927fc8f49bacb4ee8
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.7 MB (26712500 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71eaf13299f415122ad887b4592146a6b6f5e80cd69e0cd4650102fa3a99972c`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 25 Oct 2022 01:53:28 GMT
ADD file:fc5d658c47ede58827812b75a311353be776e41e2dd339b8906839527c9b5247 in / 
# Tue, 25 Oct 2022 01:53:28 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:a404e54162968593b8d92b571f3cdd673e4c9eab5d9be28d7c494595c0aa6682`  
		Last Modified: Wed, 19 Oct 2022 22:03:02 GMT  
		Size: 26.7 MB (26712500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:bionic-20221019` - linux; s390x

```console
$ docker pull ubuntu@sha256:e8b5b1b0fd8023b3a13efc5ad58e7768520fe114448ebc800d4b68983886b8f2
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.4 MB (25371461 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f7c1da1bebf686edaa4ffa3b904cacd16d80b9ed086f550069be9eef0e09d11`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 25 Oct 2022 01:23:02 GMT
ADD file:0843e89b8865a30626cece7a42cf27708a86422aadb28029168b2f159a8768fa in / 
# Tue, 25 Oct 2022 01:23:03 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:4cd692a206d359f66e10c4f4f2a37009c4162f022df78a9bb8e8c24def290167`  
		Last Modified: Tue, 25 Oct 2022 01:24:23 GMT  
		Size: 25.4 MB (25371461 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ubuntu:focal`

```console
$ docker pull ubuntu@sha256:90aa2a38a4e0a2450d0046fc827eef8c88aa866fd334478d15a3f2c432e66826
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
$ docker pull ubuntu@sha256:b25ef49a40b7797937d0d23eca3b0a41701af6757afca23d504d50826f0b37ce
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.6 MB (28577834 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:680e5dfb52c74a1fbc99c2922c8e25b5736e6cd1a3d9430890d52a4f8f44087a`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 25 Oct 2022 01:53:34 GMT
ADD file:7633003155a1059419aa1a6756fafb6e4f419d65bff7feb7c945de1e29dccb1e in / 
# Tue, 25 Oct 2022 01:53:35 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:eaead16dc43bb8811d4ff450935d607f9ba4baffda4fc110cc402fa43f601d83`  
		Last Modified: Fri, 21 Oct 2022 03:03:39 GMT  
		Size: 28.6 MB (28577834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:focal` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:e5a044019a4cde9840aca3ed43534d096e1b6f0c035f7780a2da41827d25986f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.6 MB (24590092 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f43fba273ad6a0820c488b21308a878f86cde06700761ee0159e8924ee65f4db`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 05 Oct 2022 00:13:44 GMT
ADD file:75870468a948359044fa3df6c07c80badfea3dcde4823d41a19285436c40cf76 in / 
# Wed, 05 Oct 2022 00:13:44 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:e679d63f382033c15f8f921851bd71fb8a85a432c0a7a612bbef16e989075145`  
		Last Modified: Wed, 05 Oct 2022 00:15:44 GMT  
		Size: 24.6 MB (24590092 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:focal` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:9488eba63bece0e05cd2cd84ce4dbe2710c8666f10259bbb9ebe55c4ff4f5704
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.2 MB (27191622 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f12f227aa3fdd90f0418130698b75f1eeb68f885f0760866a7801fa3877df26a`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 05 Oct 2022 00:02:10 GMT
ADD file:30b589901d2a6b82d0b7271487bdaf37514649a798cc13a17f74394321bdd051 in / 
# Wed, 05 Oct 2022 00:02:11 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:514fa78e57ce0d9437bc984cc36ab780c24b69da2b922bfff16737072e3e7de2`  
		Last Modified: Wed, 05 Oct 2022 00:03:51 GMT  
		Size: 27.2 MB (27191622 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:focal` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:00f813cc648193e6c81b8afe75c7b7252287dcad966c6857934d9449d4397470
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.3 MB (33296076 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fde6bd3e00a511ec2c1633fdbfd4bc0cdd963e577d1b88762b889904020171e5`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 05 Oct 2022 10:52:08 GMT
ADD file:75224b75d955b3021df8214497d6835e1aff42b5ce83f96b779b63c4a8e15faf in / 
# Wed, 05 Oct 2022 10:52:10 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:ecaa0fe591301d50850e37b61a6fac5429c04a3c39272da2f7b748eaed7f5c52`  
		Last Modified: Wed, 05 Oct 2022 10:54:26 GMT  
		Size: 33.3 MB (33296076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:focal` - linux; riscv64

```console
$ docker pull ubuntu@sha256:fc82f4ab16ae703eaa7668641f603989d88f6d6cc2c8f829668841ea8b9ff57b
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.2 MB (24242839 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:718ca6f5fba830fb1b140b0e64b7932c9c76bd695e6d7c5d5cb29f6a5af22f05`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 05 Oct 2022 00:12:13 GMT
ADD file:8c408c11e1eeed71fdd784404ddf9ac52b700161e6187e2313c2751d756e3442 in / 
# Wed, 05 Oct 2022 00:12:14 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:edcdeceb0859700b9f2e87516c30c0049092e29666696c30e6b862e0df3d4961`  
		Last Modified: Wed, 05 Oct 2022 00:29:16 GMT  
		Size: 24.2 MB (24242839 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:focal` - linux; s390x

```console
$ docker pull ubuntu@sha256:3d2f0fd07dc2d5099f0fb58083ba3bcb9c1daf2225f7205cb8b1ddc7bfab3f24
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.0 MB (27016028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:702f00d888407e4809f313324d91de5d4b8d00bcfb8172ef98fb5bf4b36d87ff`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 25 Oct 2022 01:23:11 GMT
ADD file:c657b467ecb15f1f4a49a5f04a525f38924750c8187c9ef9f0b886d0264e21f1 in / 
# Tue, 25 Oct 2022 01:23:12 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:a63328f08dbd14148b5ffe154c18846ead48e759779d007b78ec3fb19f5f43a5`  
		Last Modified: Tue, 25 Oct 2022 01:24:36 GMT  
		Size: 27.0 MB (27016028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ubuntu:focal-20221019`

```console
$ docker pull ubuntu@sha256:d8e0ffedfde257b543fa3d392254d05178e9190d25fcd655e5b78de6ae237974
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; s390x

### `ubuntu:focal-20221019` - linux; amd64

```console
$ docker pull ubuntu@sha256:b25ef49a40b7797937d0d23eca3b0a41701af6757afca23d504d50826f0b37ce
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.6 MB (28577834 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:680e5dfb52c74a1fbc99c2922c8e25b5736e6cd1a3d9430890d52a4f8f44087a`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 25 Oct 2022 01:53:34 GMT
ADD file:7633003155a1059419aa1a6756fafb6e4f419d65bff7feb7c945de1e29dccb1e in / 
# Tue, 25 Oct 2022 01:53:35 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:eaead16dc43bb8811d4ff450935d607f9ba4baffda4fc110cc402fa43f601d83`  
		Last Modified: Fri, 21 Oct 2022 03:03:39 GMT  
		Size: 28.6 MB (28577834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:focal-20221019` - linux; s390x

```console
$ docker pull ubuntu@sha256:3d2f0fd07dc2d5099f0fb58083ba3bcb9c1daf2225f7205cb8b1ddc7bfab3f24
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.0 MB (27016028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:702f00d888407e4809f313324d91de5d4b8d00bcfb8172ef98fb5bf4b36d87ff`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 25 Oct 2022 01:23:11 GMT
ADD file:c657b467ecb15f1f4a49a5f04a525f38924750c8187c9ef9f0b886d0264e21f1 in / 
# Tue, 25 Oct 2022 01:23:12 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:a63328f08dbd14148b5ffe154c18846ead48e759779d007b78ec3fb19f5f43a5`  
		Last Modified: Tue, 25 Oct 2022 01:24:36 GMT  
		Size: 27.0 MB (27016028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ubuntu:jammy`

```console
$ docker pull ubuntu@sha256:2ec38e3c5c9e889445516d2b044d061c23dc23d321e4e1508957997f4001dc1d
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
$ docker pull ubuntu@sha256:dda6886d8d153a2d86f046c9335123c6151d83fd63e446b752ed8d9da261205d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.4 MB (30426374 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cdb68b455a141ed921945f6d39a8c0694a7e21a37b2b030488d73e38875a26cc`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 25 Oct 2022 01:53:41 GMT
ADD file:ba96f963bbfd429a0839c40603fdd7829eaca58f20adfa0d15e6beae8244bc08 in / 
# Tue, 25 Oct 2022 01:53:41 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:301a8b74f71f85f3a31e9c7e7fedd5b001ead5bcf895bc2911c1d260e06bd987`  
		Last Modified: Fri, 21 Oct 2022 03:03:39 GMT  
		Size: 30.4 MB (30426374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:jammy` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:60c321f2700325103a0c185adeadfd5a93dbb3cd67dfbdd5b79a8aafa38325c2
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.0 MB (27018632 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:938dcade566893210cea0198ac17b9bd44033d0ac2376015cd86bf4d7b27b125`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 05 Oct 2022 00:13:57 GMT
ADD file:11e25fc4812528219464289700bb0495bf9298918899103c33d7ef9022690eb0 in / 
# Wed, 05 Oct 2022 00:13:57 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:99b9c73338a7c0dbe41f9fc543fae706650a616453e1e330f870e20916c18a11`  
		Last Modified: Wed, 05 Oct 2022 00:16:02 GMT  
		Size: 27.0 MB (27018632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:jammy` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:82aee33baa9ffa1accfc1c5e9865aa59b94ec289441894ddb8acad412e16168d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.4 MB (28382255 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d63f752103bb93d846e17fa9996d3e708717c51b106382fe84d8527ee47a3547`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 05 Oct 2022 00:02:19 GMT
ADD file:fd8103ca1472a4f51eeff3e22fbd1dfd61a3d22c34f16a61ef1ba016352e3629 in / 
# Wed, 05 Oct 2022 00:02:20 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:d6cb415e2683249f7884ee5367306b023c72f907afeca2a30ca19c8de5f4f7d9`  
		Last Modified: Tue, 04 Oct 2022 15:08:22 GMT  
		Size: 28.4 MB (28382255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:jammy` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:d80c03cea627ee3ceba6eaa9f0b168060923f6150b167c99ed446fa234863bcd
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.7 MB (35709341 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6670c4b363d0702a3dbcad7092e05567079bbede0e17609aa8d8612e936acab`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 05 Oct 2022 10:52:24 GMT
ADD file:5f3953a21754ce756642c9ddcf521f2cfe220a5fe988ccec51085bd074fbe46e in / 
# Wed, 05 Oct 2022 10:52:26 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:5053ecffedc109608feacf4836ad15e0f7b2f6a411250a41574342de479c4760`  
		Last Modified: Wed, 05 Oct 2022 10:54:49 GMT  
		Size: 35.7 MB (35709341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:jammy` - linux; riscv64

```console
$ docker pull ubuntu@sha256:8b497a96364d0dcb3dc7f4f237dbce73958bae2aa2d2989c920467f028c49534
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.7 MB (27747416 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c808209261fc55418f60b818c8e1af2266b637a0d290cd1f65aa1d24ba55bf31`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 05 Oct 2022 00:14:15 GMT
ADD file:e1fa146cf8e97dd6a2f3ebb2dacba539556ef4a1e87dc53bd745a3cf0ba10aef in / 
# Wed, 05 Oct 2022 00:14:16 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:cbeff255552ba792be63b343113968df42de6f599d1372edd4c7346d08dfeace`  
		Last Modified: Wed, 05 Oct 2022 00:31:39 GMT  
		Size: 27.7 MB (27747416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:jammy` - linux; s390x

```console
$ docker pull ubuntu@sha256:0a00cd261964effe192c08403af7c075c8713ead4e0729cb9794e5514ab6310b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.6 MB (28641668 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b87637e0f0a74618b572a61c6e411c31b1073d97c4ef7ac36986eaa55bc31deb`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 25 Oct 2022 01:23:21 GMT
ADD file:d9af7670f58e9478e400dac85a0fcb07a4209846dbd1ea560fdc6de6e2cb5e4e in / 
# Tue, 25 Oct 2022 01:23:22 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:9aed974aece14dd3aed00810d58a89e87eb5be9ad1c6fbb1ed077dc3f145dccc`  
		Last Modified: Tue, 25 Oct 2022 01:24:48 GMT  
		Size: 28.6 MB (28641668 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ubuntu:jammy-20221020`

```console
$ docker pull ubuntu@sha256:ae591625e17c46a7303ff76bd44ed98ea96b0a36596cdf3735f473a4306b135d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; s390x

### `ubuntu:jammy-20221020` - linux; amd64

```console
$ docker pull ubuntu@sha256:dda6886d8d153a2d86f046c9335123c6151d83fd63e446b752ed8d9da261205d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.4 MB (30426374 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cdb68b455a141ed921945f6d39a8c0694a7e21a37b2b030488d73e38875a26cc`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 25 Oct 2022 01:53:41 GMT
ADD file:ba96f963bbfd429a0839c40603fdd7829eaca58f20adfa0d15e6beae8244bc08 in / 
# Tue, 25 Oct 2022 01:53:41 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:301a8b74f71f85f3a31e9c7e7fedd5b001ead5bcf895bc2911c1d260e06bd987`  
		Last Modified: Fri, 21 Oct 2022 03:03:39 GMT  
		Size: 30.4 MB (30426374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:jammy-20221020` - linux; s390x

```console
$ docker pull ubuntu@sha256:0a00cd261964effe192c08403af7c075c8713ead4e0729cb9794e5514ab6310b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.6 MB (28641668 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b87637e0f0a74618b572a61c6e411c31b1073d97c4ef7ac36986eaa55bc31deb`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 25 Oct 2022 01:23:21 GMT
ADD file:d9af7670f58e9478e400dac85a0fcb07a4209846dbd1ea560fdc6de6e2cb5e4e in / 
# Tue, 25 Oct 2022 01:23:22 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:9aed974aece14dd3aed00810d58a89e87eb5be9ad1c6fbb1ed077dc3f145dccc`  
		Last Modified: Tue, 25 Oct 2022 01:24:48 GMT  
		Size: 28.6 MB (28641668 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ubuntu:kinetic`

```console
$ docker pull ubuntu@sha256:53d8acab9c74357830f822f89ecaf95a6a4a59aff9d3d6e74d8e842b4ecbeb31
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; riscv64
	-	linux; s390x

### `ubuntu:kinetic` - linux; amd64

```console
$ docker pull ubuntu@sha256:17e4f3973ec125dcb7b97ed18da394a348b5ed7c1753d68fe6d20996184c198a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.5 MB (27457582 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f175c10c2b410262bdbcb91b176a308d15dd1f77a80f00b8488fe84a9cabf7e`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 25 Oct 2022 01:53:48 GMT
ADD file:610b4bc612cfad108d07bf023abb796fe6c02a4b6305d824d5d556b7dc85aa89 in / 
# Tue, 25 Oct 2022 01:53:48 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:bcd446fbf8a137bbf135b63332ebcd0c3e9880060bc5b41962fbbb07e94062b7`  
		Last Modified: Tue, 25 Oct 2022 01:55:07 GMT  
		Size: 27.5 MB (27457582 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:kinetic` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:b6a6cc304b464d9730ab10c79c3c2b8ad9d92a86269b4f8808e7d9b17deb46a5
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.9 MB (25873193 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c738aa721c7c4e87815e177cae4e37893e3282c0b2ce6512d0a2b41192cec59`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 05 Oct 2022 00:14:09 GMT
ADD file:4b538f2c7b46aa601d747159ce9e8c2c7a99b2b6e09e4efe1073ca58e47fbeed in / 
# Wed, 05 Oct 2022 00:14:09 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:788f7bb1e1d719f6a9a9b3b1530cc5bbe5b808a2ad77a65f23e2c6d15b8ae546`  
		Last Modified: Wed, 05 Oct 2022 00:16:28 GMT  
		Size: 25.9 MB (25873193 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:kinetic` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:6717e9297a44d81ab1b68a47aacce1eb9032a827e5550df658d2fbd646a3e8ee
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.7 MB (26690398 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39f5d02545a9b390e470a566bc049fcd716dcc3fdf7c7202202701c8fc188935`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 05 Oct 2022 00:02:29 GMT
ADD file:2496d47197031551828443c95a5e1dc6bb6dc7855695a8470f3ec96e8441e76b in / 
# Wed, 05 Oct 2022 00:02:30 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:9a768b6c77af7a723d25d349fe4a633e82e8ad41fae270b2bbee8849bb840009`  
		Last Modified: Wed, 05 Oct 2022 00:04:31 GMT  
		Size: 26.7 MB (26690398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:kinetic` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:a7cd81b3fac5c8771e9924dc9dd6dc12c2eead4ea98d5383c8fdce13d828ca47
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.1 MB (32115528 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d7dcae3381fd5e36b661f8eed3ec64dcdd6144c4833dc0cc152bbb672f15557`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 05 Oct 2022 10:52:41 GMT
ADD file:88a1f03ef21cfaa40a714986930314d37550633cb8512f4b6f8f181d8578923a in / 
# Wed, 05 Oct 2022 10:52:43 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:21fc6649e0514e6dd480d6ec510ee3e255e841bc45eac6d3089ae5a1b109f126`  
		Last Modified: Wed, 05 Oct 2022 10:55:19 GMT  
		Size: 32.1 MB (32115528 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:kinetic` - linux; riscv64

```console
$ docker pull ubuntu@sha256:014b7c9f2e08f240bd7611ecd2c207db6917e237b15bd4dd80bb19b4afc761bc
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.6 MB (25618700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6eeea9f38c5cada2aa1969a46596b8afb51fcbbc4b23abd3e166c7f26ebda815`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 05 Oct 2022 00:16:49 GMT
ADD file:2d01ff45e6105658cf6791d4ade5cc3168c7d455422fc973a54a795907023c4e in / 
# Wed, 05 Oct 2022 00:16:51 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:69c33ccbf3d1b09c78fae3f88deb756ae33a9e4610a01fc9ab8b457ee6107d7f`  
		Last Modified: Wed, 05 Oct 2022 00:35:11 GMT  
		Size: 25.6 MB (25618700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:kinetic` - linux; s390x

```console
$ docker pull ubuntu@sha256:85bc42d3f6b0dd83e6a765456a47791f52f1d97f19cbbd494bce7e67fad51e47
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.0 MB (26022178 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08293ad2ee54d23056e5c346d001d71399750d119e0a686166fa2d160ff18f77`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 25 Oct 2022 01:23:31 GMT
ADD file:9c0c4172b14f0d37b0b074729a4738aeb165efe5c83e2d9bfefc5b39e4a4fe0b in / 
# Tue, 25 Oct 2022 01:23:32 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:cf61a33f110308ce64c1dd7a5dddf2a5587ee1c8ab2351219b925428957cbc10`  
		Last Modified: Tue, 25 Oct 2022 01:25:01 GMT  
		Size: 26.0 MB (26022178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ubuntu:kinetic-20221024`

```console
$ docker pull ubuntu@sha256:ee75a29177d196673dac07bcbc1ea4f22742217b66933d92b73dd6cab3bbb1ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; s390x

### `ubuntu:kinetic-20221024` - linux; amd64

```console
$ docker pull ubuntu@sha256:17e4f3973ec125dcb7b97ed18da394a348b5ed7c1753d68fe6d20996184c198a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.5 MB (27457582 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f175c10c2b410262bdbcb91b176a308d15dd1f77a80f00b8488fe84a9cabf7e`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 25 Oct 2022 01:53:48 GMT
ADD file:610b4bc612cfad108d07bf023abb796fe6c02a4b6305d824d5d556b7dc85aa89 in / 
# Tue, 25 Oct 2022 01:53:48 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:bcd446fbf8a137bbf135b63332ebcd0c3e9880060bc5b41962fbbb07e94062b7`  
		Last Modified: Tue, 25 Oct 2022 01:55:07 GMT  
		Size: 27.5 MB (27457582 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:kinetic-20221024` - linux; s390x

```console
$ docker pull ubuntu@sha256:85bc42d3f6b0dd83e6a765456a47791f52f1d97f19cbbd494bce7e67fad51e47
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.0 MB (26022178 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08293ad2ee54d23056e5c346d001d71399750d119e0a686166fa2d160ff18f77`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 25 Oct 2022 01:23:31 GMT
ADD file:9c0c4172b14f0d37b0b074729a4738aeb165efe5c83e2d9bfefc5b39e4a4fe0b in / 
# Tue, 25 Oct 2022 01:23:32 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:cf61a33f110308ce64c1dd7a5dddf2a5587ee1c8ab2351219b925428957cbc10`  
		Last Modified: Tue, 25 Oct 2022 01:25:01 GMT  
		Size: 26.0 MB (26022178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ubuntu:latest`

```console
$ docker pull ubuntu@sha256:2ec38e3c5c9e889445516d2b044d061c23dc23d321e4e1508957997f4001dc1d
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
$ docker pull ubuntu@sha256:dda6886d8d153a2d86f046c9335123c6151d83fd63e446b752ed8d9da261205d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.4 MB (30426374 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cdb68b455a141ed921945f6d39a8c0694a7e21a37b2b030488d73e38875a26cc`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 25 Oct 2022 01:53:41 GMT
ADD file:ba96f963bbfd429a0839c40603fdd7829eaca58f20adfa0d15e6beae8244bc08 in / 
# Tue, 25 Oct 2022 01:53:41 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:301a8b74f71f85f3a31e9c7e7fedd5b001ead5bcf895bc2911c1d260e06bd987`  
		Last Modified: Fri, 21 Oct 2022 03:03:39 GMT  
		Size: 30.4 MB (30426374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:latest` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:60c321f2700325103a0c185adeadfd5a93dbb3cd67dfbdd5b79a8aafa38325c2
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.0 MB (27018632 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:938dcade566893210cea0198ac17b9bd44033d0ac2376015cd86bf4d7b27b125`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 05 Oct 2022 00:13:57 GMT
ADD file:11e25fc4812528219464289700bb0495bf9298918899103c33d7ef9022690eb0 in / 
# Wed, 05 Oct 2022 00:13:57 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:99b9c73338a7c0dbe41f9fc543fae706650a616453e1e330f870e20916c18a11`  
		Last Modified: Wed, 05 Oct 2022 00:16:02 GMT  
		Size: 27.0 MB (27018632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:latest` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:82aee33baa9ffa1accfc1c5e9865aa59b94ec289441894ddb8acad412e16168d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.4 MB (28382255 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d63f752103bb93d846e17fa9996d3e708717c51b106382fe84d8527ee47a3547`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 05 Oct 2022 00:02:19 GMT
ADD file:fd8103ca1472a4f51eeff3e22fbd1dfd61a3d22c34f16a61ef1ba016352e3629 in / 
# Wed, 05 Oct 2022 00:02:20 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:d6cb415e2683249f7884ee5367306b023c72f907afeca2a30ca19c8de5f4f7d9`  
		Last Modified: Tue, 04 Oct 2022 15:08:22 GMT  
		Size: 28.4 MB (28382255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:latest` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:d80c03cea627ee3ceba6eaa9f0b168060923f6150b167c99ed446fa234863bcd
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.7 MB (35709341 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6670c4b363d0702a3dbcad7092e05567079bbede0e17609aa8d8612e936acab`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 05 Oct 2022 10:52:24 GMT
ADD file:5f3953a21754ce756642c9ddcf521f2cfe220a5fe988ccec51085bd074fbe46e in / 
# Wed, 05 Oct 2022 10:52:26 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:5053ecffedc109608feacf4836ad15e0f7b2f6a411250a41574342de479c4760`  
		Last Modified: Wed, 05 Oct 2022 10:54:49 GMT  
		Size: 35.7 MB (35709341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:latest` - linux; riscv64

```console
$ docker pull ubuntu@sha256:8b497a96364d0dcb3dc7f4f237dbce73958bae2aa2d2989c920467f028c49534
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.7 MB (27747416 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c808209261fc55418f60b818c8e1af2266b637a0d290cd1f65aa1d24ba55bf31`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 05 Oct 2022 00:14:15 GMT
ADD file:e1fa146cf8e97dd6a2f3ebb2dacba539556ef4a1e87dc53bd745a3cf0ba10aef in / 
# Wed, 05 Oct 2022 00:14:16 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:cbeff255552ba792be63b343113968df42de6f599d1372edd4c7346d08dfeace`  
		Last Modified: Wed, 05 Oct 2022 00:31:39 GMT  
		Size: 27.7 MB (27747416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:latest` - linux; s390x

```console
$ docker pull ubuntu@sha256:0a00cd261964effe192c08403af7c075c8713ead4e0729cb9794e5514ab6310b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.6 MB (28641668 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b87637e0f0a74618b572a61c6e411c31b1073d97c4ef7ac36986eaa55bc31deb`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 25 Oct 2022 01:23:21 GMT
ADD file:d9af7670f58e9478e400dac85a0fcb07a4209846dbd1ea560fdc6de6e2cb5e4e in / 
# Tue, 25 Oct 2022 01:23:22 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:9aed974aece14dd3aed00810d58a89e87eb5be9ad1c6fbb1ed077dc3f145dccc`  
		Last Modified: Tue, 25 Oct 2022 01:24:48 GMT  
		Size: 28.6 MB (28641668 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ubuntu:rolling`

```console
$ docker pull ubuntu@sha256:3884aff9a90445684c1cd225116537f610c2223208b08d792f30db20e1e642cf
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
$ docker pull ubuntu@sha256:17e4f3973ec125dcb7b97ed18da394a348b5ed7c1753d68fe6d20996184c198a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.5 MB (27457582 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f175c10c2b410262bdbcb91b176a308d15dd1f77a80f00b8488fe84a9cabf7e`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 25 Oct 2022 01:53:48 GMT
ADD file:610b4bc612cfad108d07bf023abb796fe6c02a4b6305d824d5d556b7dc85aa89 in / 
# Tue, 25 Oct 2022 01:53:48 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:bcd446fbf8a137bbf135b63332ebcd0c3e9880060bc5b41962fbbb07e94062b7`  
		Last Modified: Tue, 25 Oct 2022 01:55:07 GMT  
		Size: 27.5 MB (27457582 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:rolling` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:60c321f2700325103a0c185adeadfd5a93dbb3cd67dfbdd5b79a8aafa38325c2
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.0 MB (27018632 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:938dcade566893210cea0198ac17b9bd44033d0ac2376015cd86bf4d7b27b125`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 05 Oct 2022 00:13:57 GMT
ADD file:11e25fc4812528219464289700bb0495bf9298918899103c33d7ef9022690eb0 in / 
# Wed, 05 Oct 2022 00:13:57 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:99b9c73338a7c0dbe41f9fc543fae706650a616453e1e330f870e20916c18a11`  
		Last Modified: Wed, 05 Oct 2022 00:16:02 GMT  
		Size: 27.0 MB (27018632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:rolling` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:82aee33baa9ffa1accfc1c5e9865aa59b94ec289441894ddb8acad412e16168d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.4 MB (28382255 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d63f752103bb93d846e17fa9996d3e708717c51b106382fe84d8527ee47a3547`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 05 Oct 2022 00:02:19 GMT
ADD file:fd8103ca1472a4f51eeff3e22fbd1dfd61a3d22c34f16a61ef1ba016352e3629 in / 
# Wed, 05 Oct 2022 00:02:20 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:d6cb415e2683249f7884ee5367306b023c72f907afeca2a30ca19c8de5f4f7d9`  
		Last Modified: Tue, 04 Oct 2022 15:08:22 GMT  
		Size: 28.4 MB (28382255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:rolling` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:d80c03cea627ee3ceba6eaa9f0b168060923f6150b167c99ed446fa234863bcd
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.7 MB (35709341 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6670c4b363d0702a3dbcad7092e05567079bbede0e17609aa8d8612e936acab`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 05 Oct 2022 10:52:24 GMT
ADD file:5f3953a21754ce756642c9ddcf521f2cfe220a5fe988ccec51085bd074fbe46e in / 
# Wed, 05 Oct 2022 10:52:26 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:5053ecffedc109608feacf4836ad15e0f7b2f6a411250a41574342de479c4760`  
		Last Modified: Wed, 05 Oct 2022 10:54:49 GMT  
		Size: 35.7 MB (35709341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:rolling` - linux; riscv64

```console
$ docker pull ubuntu@sha256:8b497a96364d0dcb3dc7f4f237dbce73958bae2aa2d2989c920467f028c49534
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.7 MB (27747416 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c808209261fc55418f60b818c8e1af2266b637a0d290cd1f65aa1d24ba55bf31`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 05 Oct 2022 00:14:15 GMT
ADD file:e1fa146cf8e97dd6a2f3ebb2dacba539556ef4a1e87dc53bd745a3cf0ba10aef in / 
# Wed, 05 Oct 2022 00:14:16 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:cbeff255552ba792be63b343113968df42de6f599d1372edd4c7346d08dfeace`  
		Last Modified: Wed, 05 Oct 2022 00:31:39 GMT  
		Size: 27.7 MB (27747416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:rolling` - linux; s390x

```console
$ docker pull ubuntu@sha256:85bc42d3f6b0dd83e6a765456a47791f52f1d97f19cbbd494bce7e67fad51e47
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.0 MB (26022178 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08293ad2ee54d23056e5c346d001d71399750d119e0a686166fa2d160ff18f77`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 25 Oct 2022 01:23:31 GMT
ADD file:9c0c4172b14f0d37b0b074729a4738aeb165efe5c83e2d9bfefc5b39e4a4fe0b in / 
# Tue, 25 Oct 2022 01:23:32 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:cf61a33f110308ce64c1dd7a5dddf2a5587ee1c8ab2351219b925428957cbc10`  
		Last Modified: Tue, 25 Oct 2022 01:25:01 GMT  
		Size: 26.0 MB (26022178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ubuntu:trusty`

```console
$ docker pull ubuntu@sha256:d7a459ecd77ebb09525584f2c3e1bb7f6a2879d90df8a3523c1b899dfc2a226f
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
$ docker pull ubuntu@sha256:d34202d0ce9f1a55b9fffa1d69af2821dcf9645cc655e96a5b168c2a9265d5db
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.7 MB (64700984 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8a7f3400ca032052bf769658a0a6f7562e441504c7da16527defa818a24fcf0`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 02 Aug 2022 01:41:30 GMT
ADD file:e9d55e059869915743a8ca8e64582d23c48fe7e90e439daccd56d3e08e8673b4 in / 
# Tue, 02 Aug 2022 01:41:31 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Tue, 02 Aug 2022 01:41:32 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Tue, 02 Aug 2022 01:41:32 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Tue, 02 Aug 2022 01:41:33 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:0db3a87a3d7959895fd860c8b924980adda6e77f5d315b6676a4ac0e12518978`  
		Last Modified: Thu, 19 Dec 2019 06:16:01 GMT  
		Size: 64.6 MB (64624015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a430e3e7a1afcac7bf89d27c42804489d76ac8775a945924494e9e5794f0ce6`  
		Last Modified: Tue, 02 Aug 2022 01:44:15 GMT  
		Size: 76.8 KB (76779 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb8c3e99facaf81b42b2e4e24792e7254297607e2273054e5f729712163cafc2`  
		Last Modified: Tue, 02 Aug 2022 01:44:15 GMT  
		Size: 190.0 B  
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
$ docker pull ubuntu@sha256:c97d63976268e6c2f3764be91e59f82009b2883d22c3dc6ff1f63e3ad6abdb05
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.4 MB (68445472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8a7710ba73fd21ad01442fe2b079693c60a5b77b18403d56e5da5448e325d06`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 05 Apr 2022 22:39:14 GMT
ADD file:e034601a525da53b0f39bb04d6e2264e2a592d0ae7c21e00697b9b62ca1efec9 in / 
# Tue, 05 Apr 2022 22:39:15 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Tue, 05 Apr 2022 22:39:16 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Tue, 05 Apr 2022 22:39:17 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Tue, 05 Apr 2022 22:39:18 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:630712fe5783a35ad52a7026002143cb4f8fe65d34097dcaa4c4331b1b059a17`  
		Last Modified: Thu, 19 Dec 2019 04:44:02 GMT  
		Size: 68.4 MB (68380440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03124bfb4886d9ba012a00a087fb41b4cc7e99517b3e2a2e6fd1e2ad327af191`  
		Last Modified: Tue, 05 Apr 2022 22:40:17 GMT  
		Size: 64.9 KB (64870 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22b953ad705784700c1611b7258f6c783a34b06bf27ed3efbd9acc7be80ba991`  
		Last Modified: Tue, 05 Apr 2022 22:40:17 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:trusty` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:209f78eaf05254c51cff7676b913bcb70c1da54e58ae728a592ea58f3b5552b4
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.4 MB (73443164 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd23a098588cb567106c63829bf08759e87f4235bbd4c90168e6b065420ac853`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 02 Aug 2022 01:31:42 GMT
ADD file:581665e92c72c8638b40fe509de6479dc1a5d7b5ffe8d6706006178c406e35e2 in / 
# Tue, 02 Aug 2022 01:31:47 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Tue, 02 Aug 2022 01:31:48 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Tue, 02 Aug 2022 01:31:50 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Tue, 02 Aug 2022 01:31:50 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:bed4146d918c6c9a57bc3a8bf829e702975b0e53c7f25920fe9435b58ed6b64f`  
		Last Modified: Thu, 19 Dec 2019 04:26:52 GMT  
		Size: 73.4 MB (73379539 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:736dbcbc0bcb73948970c71c59c6fc5662698a0cdca10a232da87ede89aabeef`  
		Last Modified: Tue, 02 Aug 2022 01:35:21 GMT  
		Size: 63.4 KB (63436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:376b7bbeb4d42e6e9b75e9ad5bd043790235c8963cac05a03bc5400002ae965b`  
		Last Modified: Tue, 02 Aug 2022 01:35:21 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ubuntu:trusty-20191217`

```console
$ docker pull ubuntu@sha256:d7a459ecd77ebb09525584f2c3e1bb7f6a2879d90df8a3523c1b899dfc2a226f
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
$ docker pull ubuntu@sha256:d34202d0ce9f1a55b9fffa1d69af2821dcf9645cc655e96a5b168c2a9265d5db
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.7 MB (64700984 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8a7f3400ca032052bf769658a0a6f7562e441504c7da16527defa818a24fcf0`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 02 Aug 2022 01:41:30 GMT
ADD file:e9d55e059869915743a8ca8e64582d23c48fe7e90e439daccd56d3e08e8673b4 in / 
# Tue, 02 Aug 2022 01:41:31 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Tue, 02 Aug 2022 01:41:32 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Tue, 02 Aug 2022 01:41:32 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Tue, 02 Aug 2022 01:41:33 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:0db3a87a3d7959895fd860c8b924980adda6e77f5d315b6676a4ac0e12518978`  
		Last Modified: Thu, 19 Dec 2019 06:16:01 GMT  
		Size: 64.6 MB (64624015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a430e3e7a1afcac7bf89d27c42804489d76ac8775a945924494e9e5794f0ce6`  
		Last Modified: Tue, 02 Aug 2022 01:44:15 GMT  
		Size: 76.8 KB (76779 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb8c3e99facaf81b42b2e4e24792e7254297607e2273054e5f729712163cafc2`  
		Last Modified: Tue, 02 Aug 2022 01:44:15 GMT  
		Size: 190.0 B  
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
$ docker pull ubuntu@sha256:c97d63976268e6c2f3764be91e59f82009b2883d22c3dc6ff1f63e3ad6abdb05
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.4 MB (68445472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8a7710ba73fd21ad01442fe2b079693c60a5b77b18403d56e5da5448e325d06`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 05 Apr 2022 22:39:14 GMT
ADD file:e034601a525da53b0f39bb04d6e2264e2a592d0ae7c21e00697b9b62ca1efec9 in / 
# Tue, 05 Apr 2022 22:39:15 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Tue, 05 Apr 2022 22:39:16 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Tue, 05 Apr 2022 22:39:17 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Tue, 05 Apr 2022 22:39:18 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:630712fe5783a35ad52a7026002143cb4f8fe65d34097dcaa4c4331b1b059a17`  
		Last Modified: Thu, 19 Dec 2019 04:44:02 GMT  
		Size: 68.4 MB (68380440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03124bfb4886d9ba012a00a087fb41b4cc7e99517b3e2a2e6fd1e2ad327af191`  
		Last Modified: Tue, 05 Apr 2022 22:40:17 GMT  
		Size: 64.9 KB (64870 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22b953ad705784700c1611b7258f6c783a34b06bf27ed3efbd9acc7be80ba991`  
		Last Modified: Tue, 05 Apr 2022 22:40:17 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:trusty-20191217` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:209f78eaf05254c51cff7676b913bcb70c1da54e58ae728a592ea58f3b5552b4
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.4 MB (73443164 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd23a098588cb567106c63829bf08759e87f4235bbd4c90168e6b065420ac853`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 02 Aug 2022 01:31:42 GMT
ADD file:581665e92c72c8638b40fe509de6479dc1a5d7b5ffe8d6706006178c406e35e2 in / 
# Tue, 02 Aug 2022 01:31:47 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Tue, 02 Aug 2022 01:31:48 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Tue, 02 Aug 2022 01:31:50 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Tue, 02 Aug 2022 01:31:50 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:bed4146d918c6c9a57bc3a8bf829e702975b0e53c7f25920fe9435b58ed6b64f`  
		Last Modified: Thu, 19 Dec 2019 04:26:52 GMT  
		Size: 73.4 MB (73379539 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:736dbcbc0bcb73948970c71c59c6fc5662698a0cdca10a232da87ede89aabeef`  
		Last Modified: Tue, 02 Aug 2022 01:35:21 GMT  
		Size: 63.4 KB (63436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:376b7bbeb4d42e6e9b75e9ad5bd043790235c8963cac05a03bc5400002ae965b`  
		Last Modified: Tue, 02 Aug 2022 01:35:21 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ubuntu:xenial`

```console
$ docker pull ubuntu@sha256:91bd29a464fdabfcf44e29e1f2a5f213c6dfa750b6290e40dd6998ac79da3c41
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
$ docker pull ubuntu@sha256:696252dd941a9a0ca7db7ca8d9fbb91d838cc9bfb27403219953af6750a89111
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.3 MB (40313786 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20832692ca6e913217051aa57084ec76c076987a63cd497100d754b27097fa33`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 02 Aug 2022 01:41:46 GMT
ADD file:294a94a081de785c730003a440a0530a85add2bcb60c0f5bc4ce7ee17867ac4e in / 
# Tue, 02 Aug 2022 01:41:47 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Tue, 02 Aug 2022 01:41:48 GMT
RUN rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 01:41:49 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Tue, 02 Aug 2022 01:41:49 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:b95ba076a26b98e98eac4b43596b59c20d1e61a36bcaf2afae3aeebadc8844cf`  
		Last Modified: Sun, 08 Aug 2021 01:00:22 GMT  
		Size: 40.3 MB (40312250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32c9df55506368eeeb59c5f56bf5d6f9ef4476a6b1e43154eebe32e436e60d7a`  
		Last Modified: Tue, 02 Aug 2022 01:44:42 GMT  
		Size: 849.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60aa30d82c4849b80da22554e0006d9c23c68a807fcb795b2f35ac6c02549eca`  
		Last Modified: Tue, 02 Aug 2022 01:44:42 GMT  
		Size: 515.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e61b5d5a768deb5e021d74947bacf44422a006a3495d70395a7d745e07fab3f3`  
		Last Modified: Tue, 02 Aug 2022 01:44:42 GMT  
		Size: 172.0 B  
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
$ docker pull ubuntu@sha256:bcb8397f1390f4f0757ca06ce184f05c8ce0c7a4b5ff93f9ab029a581192917b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.8 MB (45817719 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:276b5b6b7721e99481801a9aaf21a4d2bf6ba6f6676f720f6f4e0da40a71fb19`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 05 Apr 2022 22:39:28 GMT
ADD file:a4ae521feddf8357667e9361bdd972a69ed945f3857cc8c534652592e432575d in / 
# Tue, 05 Apr 2022 22:39:29 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Tue, 05 Apr 2022 22:39:30 GMT
RUN rm -rf /var/lib/apt/lists/*
# Tue, 05 Apr 2022 22:39:31 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Tue, 05 Apr 2022 22:39:32 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:1335d7ebdbbb7325d434cf945bcb54cb20f7288e1ca2a1cf140ae02b324646e6`  
		Last Modified: Sun, 08 Aug 2021 01:00:22 GMT  
		Size: 45.8 MB (45816182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffa6a227af79fa98ebbd1d2da516e2b7ce1cea5519a760cd0f6688738fbdb951`  
		Last Modified: Tue, 05 Apr 2022 22:40:40 GMT  
		Size: 851.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab3928723c2c34ecd7264ce4e195ddda11403213b1c93d02e8efcd11de4b07a1`  
		Last Modified: Tue, 05 Apr 2022 22:40:40 GMT  
		Size: 514.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e468001dd2f338d54f47d062d65db61c754f09897744d97084afa15cee021200`  
		Last Modified: Tue, 05 Apr 2022 22:40:40 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:xenial` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:4ef33ed6b1af10706727d280de436bced5e9413cba7992d6126c866efd79cacd
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.5 MB (47523643 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17fb9d3bc97649795df6522739036df75814819b4b48997a6e05345dcd5e6845`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 02 Aug 2022 01:32:03 GMT
ADD file:c84969ed4d4e336ec5996e26e35261f683b36f1af7a978df587296ef5e7a2627 in / 
# Tue, 02 Aug 2022 01:32:06 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Tue, 02 Aug 2022 01:32:07 GMT
RUN rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 01:32:08 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Tue, 02 Aug 2022 01:32:08 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:5057452c10cfe2216f39949f909f3cd83002d256d1bbd564ae242352a5460fe2`  
		Last Modified: Sun, 08 Aug 2021 01:00:30 GMT  
		Size: 47.5 MB (47522137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72bced789eccb5759f541a5b15b9a3031c06cc54bdbff1a553cc0ef29ddad2bc`  
		Last Modified: Tue, 02 Aug 2022 01:36:22 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a11a61259761ffe18601a628413443ccb5dee06a185a81c902220dfc070801c3`  
		Last Modified: Tue, 02 Aug 2022 01:35:56 GMT  
		Size: 483.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3272460dff18ff8fd96d33337b0ff5cc5d9d2e7f158c662273e1bb760c7f9722`  
		Last Modified: Tue, 02 Aug 2022 01:36:06 GMT  
		Size: 171.0 B  
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
$ docker pull ubuntu@sha256:91bd29a464fdabfcf44e29e1f2a5f213c6dfa750b6290e40dd6998ac79da3c41
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
$ docker pull ubuntu@sha256:696252dd941a9a0ca7db7ca8d9fbb91d838cc9bfb27403219953af6750a89111
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.3 MB (40313786 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20832692ca6e913217051aa57084ec76c076987a63cd497100d754b27097fa33`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 02 Aug 2022 01:41:46 GMT
ADD file:294a94a081de785c730003a440a0530a85add2bcb60c0f5bc4ce7ee17867ac4e in / 
# Tue, 02 Aug 2022 01:41:47 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Tue, 02 Aug 2022 01:41:48 GMT
RUN rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 01:41:49 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Tue, 02 Aug 2022 01:41:49 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:b95ba076a26b98e98eac4b43596b59c20d1e61a36bcaf2afae3aeebadc8844cf`  
		Last Modified: Sun, 08 Aug 2021 01:00:22 GMT  
		Size: 40.3 MB (40312250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32c9df55506368eeeb59c5f56bf5d6f9ef4476a6b1e43154eebe32e436e60d7a`  
		Last Modified: Tue, 02 Aug 2022 01:44:42 GMT  
		Size: 849.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60aa30d82c4849b80da22554e0006d9c23c68a807fcb795b2f35ac6c02549eca`  
		Last Modified: Tue, 02 Aug 2022 01:44:42 GMT  
		Size: 515.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e61b5d5a768deb5e021d74947bacf44422a006a3495d70395a7d745e07fab3f3`  
		Last Modified: Tue, 02 Aug 2022 01:44:42 GMT  
		Size: 172.0 B  
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
$ docker pull ubuntu@sha256:bcb8397f1390f4f0757ca06ce184f05c8ce0c7a4b5ff93f9ab029a581192917b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.8 MB (45817719 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:276b5b6b7721e99481801a9aaf21a4d2bf6ba6f6676f720f6f4e0da40a71fb19`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 05 Apr 2022 22:39:28 GMT
ADD file:a4ae521feddf8357667e9361bdd972a69ed945f3857cc8c534652592e432575d in / 
# Tue, 05 Apr 2022 22:39:29 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Tue, 05 Apr 2022 22:39:30 GMT
RUN rm -rf /var/lib/apt/lists/*
# Tue, 05 Apr 2022 22:39:31 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Tue, 05 Apr 2022 22:39:32 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:1335d7ebdbbb7325d434cf945bcb54cb20f7288e1ca2a1cf140ae02b324646e6`  
		Last Modified: Sun, 08 Aug 2021 01:00:22 GMT  
		Size: 45.8 MB (45816182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffa6a227af79fa98ebbd1d2da516e2b7ce1cea5519a760cd0f6688738fbdb951`  
		Last Modified: Tue, 05 Apr 2022 22:40:40 GMT  
		Size: 851.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab3928723c2c34ecd7264ce4e195ddda11403213b1c93d02e8efcd11de4b07a1`  
		Last Modified: Tue, 05 Apr 2022 22:40:40 GMT  
		Size: 514.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e468001dd2f338d54f47d062d65db61c754f09897744d97084afa15cee021200`  
		Last Modified: Tue, 05 Apr 2022 22:40:40 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:xenial-20210804` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:4ef33ed6b1af10706727d280de436bced5e9413cba7992d6126c866efd79cacd
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.5 MB (47523643 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17fb9d3bc97649795df6522739036df75814819b4b48997a6e05345dcd5e6845`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 02 Aug 2022 01:32:03 GMT
ADD file:c84969ed4d4e336ec5996e26e35261f683b36f1af7a978df587296ef5e7a2627 in / 
# Tue, 02 Aug 2022 01:32:06 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Tue, 02 Aug 2022 01:32:07 GMT
RUN rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 01:32:08 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Tue, 02 Aug 2022 01:32:08 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:5057452c10cfe2216f39949f909f3cd83002d256d1bbd564ae242352a5460fe2`  
		Last Modified: Sun, 08 Aug 2021 01:00:30 GMT  
		Size: 47.5 MB (47522137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72bced789eccb5759f541a5b15b9a3031c06cc54bdbff1a553cc0ef29ddad2bc`  
		Last Modified: Tue, 02 Aug 2022 01:36:22 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a11a61259761ffe18601a628413443ccb5dee06a185a81c902220dfc070801c3`  
		Last Modified: Tue, 02 Aug 2022 01:35:56 GMT  
		Size: 483.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3272460dff18ff8fd96d33337b0ff5cc5d9d2e7f158c662273e1bb760c7f9722`  
		Last Modified: Tue, 02 Aug 2022 01:36:06 GMT  
		Size: 171.0 B  
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
