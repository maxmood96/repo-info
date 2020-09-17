## `buildpack-deps:xenial-curl`

```console
$ docker pull buildpack-deps@sha256:d132c679536dad08609bd4ab65030fc02460853373edd5cb2dfd17c92692a098
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
$ docker pull buildpack-deps@sha256:afa3f79337aa6c126c30b8fbaef8b32a0eb0e9d7453e7a4b8bb2ce34590e510a
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.7 MB (51735157 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0afdbf7199c49762d70c000509a56294571db31223cdd846155bf529cc69778`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 19 Aug 2020 21:16:18 GMT
ADD file:144835a276ed2d8eaf6e893d5560444fe0d6a6f9b9bdadec1eb56e7bd9814427 in / 
# Wed, 19 Aug 2020 21:16:19 GMT
RUN rm -rf /var/lib/apt/lists/*
# Wed, 19 Aug 2020 21:16:21 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 19 Aug 2020 21:16:22 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 19 Aug 2020 21:16:22 GMT
CMD ["/bin/bash"]
# Wed, 19 Aug 2020 22:30:41 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 19 Aug 2020 22:30:42 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:8e097b52bfb8e743e52ccd2dfbd5a0363e48a00b06cdd3728a6fd4d1f3a34280`  
		Last Modified: Sat, 08 Aug 2020 13:20:06 GMT  
		Size: 44.4 MB (44447543 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a613a9b4553ca86fac22546f2f79e2ff3d17d8d6aeea8b97d67862a5a40ad8ec`  
		Last Modified: Wed, 19 Aug 2020 21:17:23 GMT  
		Size: 529.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acc000f015361df35e770a910ce03d30691e35aa10d52f4a4f432f183a6c03db`  
		Last Modified: Wed, 19 Aug 2020 21:17:23 GMT  
		Size: 853.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73eef93b7466c41f22f32d28aae5eb87e1ebc0c4d232c5f5e68c955d0e798dca`  
		Last Modified: Wed, 19 Aug 2020 21:17:23 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:529cf66b51f093e1e8b42b336d1a1a49b0ad49267fb4db1e2b2a809ce9552333`  
		Last Modified: Wed, 19 Aug 2020 22:37:08 GMT  
		Size: 7.3 MB (7286062 bytes)  
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
$ docker pull buildpack-deps@sha256:8304783b6b2216403c944105bbba936b5d9ec9de3e1c084a87169dbed18f79b1
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.4 MB (46417922 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57707b901716aa21e9684cae59d069c76a1f4d790f4cd05a197162d4f2c30e71`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 19 Aug 2020 21:31:42 GMT
ADD file:20ffb81d6b7edd3826c028369ed1774914394328d1ccef79ecee109f5cfbcc5f in / 
# Wed, 19 Aug 2020 21:31:45 GMT
RUN rm -rf /var/lib/apt/lists/*
# Wed, 19 Aug 2020 21:31:49 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 19 Aug 2020 21:31:51 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 19 Aug 2020 21:31:52 GMT
CMD ["/bin/bash"]
# Wed, 19 Aug 2020 22:08:53 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 19 Aug 2020 22:08:55 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:3266c9b0302777bdc8ccdffab895ef058fb0777dc7600b0fe0b6c80dd3e71f9b`  
		Last Modified: Sat, 08 Aug 2020 00:25:28 GMT  
		Size: 40.1 MB (40073893 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a5240d1a89e17ed7dda51e3b38d3749e4ab3fb2fc2433de69ea23a838bb00c7`  
		Last Modified: Wed, 19 Aug 2020 21:33:04 GMT  
		Size: 469.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be065fa7bcd4d9f2540e1fec00c455a04755974444b17fb108b73cd4b15963a1`  
		Last Modified: Wed, 19 Aug 2020 21:33:04 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75305dc60d93c15276fd1b3dc21a09ef1ce9c248393c85eb1a5caf2be6e02671`  
		Last Modified: Wed, 19 Aug 2020 21:33:04 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e288aeb73e29da96c2ea0672cfd89b1288eea9baf1d6c849014ec5432f3a18d`  
		Last Modified: Wed, 19 Aug 2020 22:15:59 GMT  
		Size: 6.3 MB (6342541 bytes)  
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
