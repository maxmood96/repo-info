## `buildpack-deps:xenial-curl`

```console
$ docker pull buildpack-deps@sha256:2570a8ba7fded5ced537fb482d30f1dafd62ade0a04f0be96f1f80c1c8c1e31d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `buildpack-deps:xenial-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:c40ddf96e758956ac565948df5dd20f58d6a8a6613478076361ce1323352a9c5
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.8 MB (51778008 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91da9dbfb0587f2db6895d0ecece4d01e98eae60b0c5c90a63fcefbbe0f19c7e`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 16 Sep 2020 22:22:41 GMT
ADD file:22e6fa4e90b4c26ba962a4fe57e5784d8923885e6eb39435cb121c716c42f7ff in / 
# Wed, 16 Sep 2020 22:22:42 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 16 Sep 2020 22:22:43 GMT
RUN rm -rf /var/lib/apt/lists/*
# Wed, 16 Sep 2020 22:22:44 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 16 Sep 2020 22:22:44 GMT
CMD ["/bin/bash"]
# Thu, 17 Sep 2020 00:13:04 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Thu, 17 Sep 2020 00:13:05 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:001ecc9468da6632359722ccefa732463486659ee07daacd31602ec3bf4d862f`  
		Last Modified: Fri, 04 Sep 2020 13:20:12 GMT  
		Size: 44.5 MB (44490811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2b9667498691604756cf3601ba44360f2b1f6ba8b5745eee963847d2a4ea736`  
		Last Modified: Wed, 16 Sep 2020 22:23:34 GMT  
		Size: 849.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abe474042557a4bffb655cd6079656d79e2ecfb0d0fad367c610ca1ec65d0e86`  
		Last Modified: Wed, 16 Sep 2020 22:23:34 GMT  
		Size: 528.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1bf2fb0fbbc55e614a3391455d772eae373e0136b7cba4d79dd72f28fb347f0`  
		Last Modified: Wed, 16 Sep 2020 22:23:34 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b4491051bbbcd0f439ec6924eb70a37e56be53460610c5474ab3825793c77da`  
		Last Modified: Thu, 17 Sep 2020 00:19:16 GMT  
		Size: 7.3 MB (7285650 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:xenial-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:d066800d132c205e349f277e3369c931a6ba1cce435d79a22b25f579f8c0876f
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.2 MB (45211957 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6259e1fd8bdb7b629990ca59e2e67a745cad30540d87adccd019106080df07e`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 16 Sep 2020 22:30:05 GMT
ADD file:38aaa478c79aa248bad103715a39948793d797d37812d22469c22ee5d851ae7d in / 
# Wed, 16 Sep 2020 22:30:09 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 16 Sep 2020 22:30:11 GMT
RUN rm -rf /var/lib/apt/lists/*
# Wed, 16 Sep 2020 22:30:13 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 16 Sep 2020 22:30:14 GMT
CMD ["/bin/bash"]
# Wed, 16 Sep 2020 23:12:39 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 16 Sep 2020 23:12:42 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:13ff11dca1d6052e4025732a8fa027aecbd6e55b19a6b9ad7b324d0ad5b188be`  
		Last Modified: Mon, 07 Sep 2020 15:58:48 GMT  
		Size: 39.1 MB (39075749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:724bf755e43234a743c552c2b8d8b994728e9584ef07a48b3409fbd838d112f2`  
		Last Modified: Wed, 16 Sep 2020 22:31:23 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81bc444073b632a9a70a0c9afdeb3b85fd5825c467bd64b3e3e345634a1633be`  
		Last Modified: Wed, 16 Sep 2020 22:31:23 GMT  
		Size: 512.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d2c632cb71c9b8f4e9c5e410f5d672570841e16446869dc106b325d823a27b0`  
		Last Modified: Wed, 16 Sep 2020 22:31:23 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb723685f0aa7808fc41837564153a82a1a4686232c5fddaeab786005355acea`  
		Last Modified: Wed, 16 Sep 2020 23:20:15 GMT  
		Size: 6.1 MB (6134674 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:xenial-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:dc9d633d52a3a937b69ab12454299fd4803c711caad4dbfc585436fd00ecdb8c
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.4 MB (46440091 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14795034df1a3efb8eb5a9141a10c8f35c61c4c8cddc809ce5add2fb121e3bc8`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 16 Sep 2020 23:17:57 GMT
ADD file:07638f480082d3760a79e7f8ab797a506252cc2233f89865558b0b5e0220a4d3 in / 
# Wed, 16 Sep 2020 23:18:00 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 16 Sep 2020 23:18:02 GMT
RUN rm -rf /var/lib/apt/lists/*
# Wed, 16 Sep 2020 23:18:04 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 16 Sep 2020 23:18:05 GMT
CMD ["/bin/bash"]
# Thu, 17 Sep 2020 00:21:47 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Thu, 17 Sep 2020 00:21:49 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:72fb9e9daf6916d23d5ddb9755e3ab864abfa8ba4f352549179782677ea68012`  
		Last Modified: Fri, 04 Sep 2020 00:25:27 GMT  
		Size: 40.1 MB (40096941 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:899cdab0a82a447b311cc0646f11453c021df6968deccedf1187f915f1e8053b`  
		Last Modified: Wed, 16 Sep 2020 23:19:18 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:016b9151e276d67695313eeb9bce429497ee8ab86848317064a39e8a8666c87a`  
		Last Modified: Wed, 16 Sep 2020 23:19:18 GMT  
		Size: 471.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:727158034d7c22989558e6c5c700ff8c0e20942f6d4296293e5fd59e47f0cdc9`  
		Last Modified: Wed, 16 Sep 2020 23:19:18 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3442c5ffebf7b34be70c0b87967194f572d1f07bd2587c3a59933d4c52f3bab`  
		Last Modified: Thu, 17 Sep 2020 00:29:25 GMT  
		Size: 6.3 MB (6341656 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:xenial-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:dd5afc5a23db2cd91e6b925c3cada518ee091cce86e52026d2a246ccdcbc1f72
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.8 MB (51799798 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef71e6924e8de4ccda959bd94a43a4bcd665b7708016403550f06bafe1e2bca0`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 16 Sep 2020 22:45:43 GMT
ADD file:d90eb653b3417fbde02f7460ab205b837e65f3e0e6026fd6f75d5b139a05851b in / 
# Wed, 16 Sep 2020 22:45:44 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 16 Sep 2020 22:45:45 GMT
RUN rm -rf /var/lib/apt/lists/*
# Wed, 16 Sep 2020 22:45:46 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 16 Sep 2020 22:45:46 GMT
CMD ["/bin/bash"]
# Wed, 16 Sep 2020 23:10:29 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 16 Sep 2020 23:10:30 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:fdeaa309388081a95677bf7967b1ef042bc0ea9d9ca3d4427de8deebc6243094`  
		Last Modified: Mon, 07 Sep 2020 15:58:35 GMT  
		Size: 44.4 MB (44369052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bca931ce181954c97bd00eca89335fb2a6505fccc8314e2862ba86e32936a4d`  
		Last Modified: Wed, 16 Sep 2020 22:46:11 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5f56edaa73ba2096f1a9f17c5174343b724c5b55c624658e4d779a7b9350c0c`  
		Last Modified: Wed, 16 Sep 2020 22:46:11 GMT  
		Size: 515.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da32f43170d941b881385b491f4217eb7ba6e9d9c27f5b5ebe657b186ec7e102`  
		Last Modified: Wed, 16 Sep 2020 22:46:11 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93edb47fa19944fb3a89b16c34d3d32655abd3623524a8431fa806ad243626aa`  
		Last Modified: Wed, 16 Sep 2020 23:15:02 GMT  
		Size: 7.4 MB (7429210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:xenial-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:4e8a9e408dda1ba11f9fcf24859b26432613e24c3fb7c8373b7ba759d1517884
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.4 MB (53423281 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc2b21d56ea072f06297d0a7d2b9e187d5079f489f3ff911fdafc77e26bd4ef2`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 19 Aug 2020 21:17:33 GMT
ADD file:def338dba259759f1f7bae334be1365a9ca730faf2901580bb9afc0532722307 in / 
# Wed, 19 Aug 2020 21:17:49 GMT
RUN rm -rf /var/lib/apt/lists/*
# Wed, 19 Aug 2020 21:18:03 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 19 Aug 2020 21:18:10 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 19 Aug 2020 21:18:13 GMT
CMD ["/bin/bash"]
# Thu, 20 Aug 2020 00:46:04 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Thu, 20 Aug 2020 00:46:16 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:1a5b802f69ab6e348addfa9dd5d0977a580fcf97cfd6d4a984b9357b40d0db34`  
		Last Modified: Mon, 10 Aug 2020 15:58:22 GMT  
		Size: 46.2 MB (46235755 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ba0a75c6c5e4d73ba6d6c874a8701f2b43fb11a2b82f301c316ecce97cbd6ad`  
		Last Modified: Wed, 19 Aug 2020 21:19:57 GMT  
		Size: 472.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e50c3d6d8b5278095a86769892e36dea6113572333d6cfe64a1d01a119aa482`  
		Last Modified: Wed, 19 Aug 2020 21:19:57 GMT  
		Size: 854.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad004884663aebec1d2d5990fe8005198223ce4cc403e4bb7fc582ad10b93ec1`  
		Last Modified: Wed, 19 Aug 2020 21:19:57 GMT  
		Size: 168.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25cba080960d441c8726bcfdfd05a1d646228e939ba1f0f787e2e4878f5276af`  
		Last Modified: Thu, 20 Aug 2020 01:07:39 GMT  
		Size: 7.2 MB (7186032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:xenial-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:18a569bed6b94cce4253cd312e7936d78574bc16048afa935992dcb899d51aa8
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.0 MB (49995491 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a34f814fa1bfcc680491902a1112a3521f81957a82b80563df9f5a672cb14f6a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 16 Sep 2020 22:52:06 GMT
ADD file:57376209e203a40d3e96a99d817a6de79cb30f16682cdaf77cf49cb181682b82 in / 
# Wed, 16 Sep 2020 22:52:09 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 16 Sep 2020 22:52:10 GMT
RUN rm -rf /var/lib/apt/lists/*
# Wed, 16 Sep 2020 22:52:10 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 16 Sep 2020 22:52:11 GMT
CMD ["/bin/bash"]
# Wed, 16 Sep 2020 23:29:27 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 16 Sep 2020 23:29:28 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:552fdf6ac8a13e7f08b94bb31e859fc1ef8424b33f7913515f42ff94fb37977f`  
		Last Modified: Mon, 07 Sep 2020 15:59:45 GMT  
		Size: 43.0 MB (42974094 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e23be6d2eb5db8ff902fc835b162e5c259893419d71723d4e34b2f53bc95da7`  
		Last Modified: Wed, 16 Sep 2020 22:52:55 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ac97abd09e577cc24b80c7b3a7a2949e667501df080571248973c283f4ec761`  
		Last Modified: Wed, 16 Sep 2020 22:52:55 GMT  
		Size: 468.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42a45dfc6bd75a3304b5951c283befe7503729c10ebfa2ae306d7446ba12dd4b`  
		Last Modified: Wed, 16 Sep 2020 22:52:55 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:161c090a307fa6123f7b524c9976c6cb5aa45a0128782039816abc3eb3b71a37`  
		Last Modified: Wed, 16 Sep 2020 23:33:22 GMT  
		Size: 7.0 MB (7019908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
