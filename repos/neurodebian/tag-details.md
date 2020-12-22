<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `neurodebian`

-	[`neurodebian:bionic`](#neurodebianbionic)
-	[`neurodebian:bionic-non-free`](#neurodebianbionic-non-free)
-	[`neurodebian:bullseye`](#neurodebianbullseye)
-	[`neurodebian:bullseye-non-free`](#neurodebianbullseye-non-free)
-	[`neurodebian:buster`](#neurodebianbuster)
-	[`neurodebian:buster-non-free`](#neurodebianbuster-non-free)
-	[`neurodebian:focal`](#neurodebianfocal)
-	[`neurodebian:focal-non-free`](#neurodebianfocal-non-free)
-	[`neurodebian:groovy`](#neurodebiangroovy)
-	[`neurodebian:groovy-non-free`](#neurodebiangroovy-non-free)
-	[`neurodebian:latest`](#neurodebianlatest)
-	[`neurodebian:nd`](#neurodebiannd)
-	[`neurodebian:nd100`](#neurodebiannd100)
-	[`neurodebian:nd100-non-free`](#neurodebiannd100-non-free)
-	[`neurodebian:nd110`](#neurodebiannd110)
-	[`neurodebian:nd110-non-free`](#neurodebiannd110-non-free)
-	[`neurodebian:nd16.04`](#neurodebiannd1604)
-	[`neurodebian:nd16.04-non-free`](#neurodebiannd1604-non-free)
-	[`neurodebian:nd18.04`](#neurodebiannd1804)
-	[`neurodebian:nd18.04-non-free`](#neurodebiannd1804-non-free)
-	[`neurodebian:nd20.04`](#neurodebiannd2004)
-	[`neurodebian:nd20.04-non-free`](#neurodebiannd2004-non-free)
-	[`neurodebian:nd20.10`](#neurodebiannd2010)
-	[`neurodebian:nd20.10-non-free`](#neurodebiannd2010-non-free)
-	[`neurodebian:nd90`](#neurodebiannd90)
-	[`neurodebian:nd90-non-free`](#neurodebiannd90-non-free)
-	[`neurodebian:nd-non-free`](#neurodebiannd-non-free)
-	[`neurodebian:non-free`](#neurodebiannon-free)
-	[`neurodebian:sid`](#neurodebiansid)
-	[`neurodebian:sid-non-free`](#neurodebiansid-non-free)
-	[`neurodebian:stretch`](#neurodebianstretch)
-	[`neurodebian:stretch-non-free`](#neurodebianstretch-non-free)
-	[`neurodebian:xenial`](#neurodebianxenial)
-	[`neurodebian:xenial-non-free`](#neurodebianxenial-non-free)

## `neurodebian:bionic`

```console
$ docker pull neurodebian@sha256:65ac4060f499f820afebcf42f24dbdae9cfd3b186d4b4b0af9de00ec91bc1b6a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `neurodebian:bionic` - linux; amd64

```console
$ docker pull neurodebian@sha256:db24a8f8cc9639d8472b8b2924435a1bc84d694d120e286a48ba359b96b0eaf4
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.8 MB (31763464 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36e2dc1395b7c38f8f83562e178128c855380b90402a989caf0e094508c4b9eb`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 25 Nov 2020 22:25:13 GMT
ADD file:6ef542de9959c3061f2d0758adb031e226b221a1a2cd748ff59e6fc13216a1c0 in / 
# Wed, 25 Nov 2020 22:25:14 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 25 Nov 2020 22:25:15 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Wed, 25 Nov 2020 22:25:16 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 25 Nov 2020 22:25:17 GMT
CMD ["/bin/bash"]
# Thu, 26 Nov 2020 01:32:12 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Thu, 26 Nov 2020 01:32:13 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Thu, 26 Nov 2020 01:32:14 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bionic main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bionic main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Thu, 26 Nov 2020 01:32:20 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:f22ccc0b8772d8e1bcb40f137b373686bc27427a70c0e41dd22b38016e09e7e0`  
		Last Modified: Fri, 20 Nov 2020 13:21:30 GMT  
		Size: 26.7 MB (26708056 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cf8fb62ba5ffb221a2edb2208741346eb4d2d99a174138e4afbb69ce1fd9966`  
		Last Modified: Wed, 25 Nov 2020 22:26:30 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e80c964ece6a3edf0db1cfc72ae0e6f0699fb776bbfcc92b708fbb945b0b9547`  
		Last Modified: Wed, 25 Nov 2020 22:26:30 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ca0d91fa7b32b3c4f0af52d770b27a7263f153342f69e086d84de98ef12fa93`  
		Last Modified: Thu, 26 Nov 2020 01:34:00 GMT  
		Size: 4.8 MB (4811258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:087a6d7d9519c3900a4acee2fa77ae27d8c43c7da392af1cdc45f39cbd978860`  
		Last Modified: Thu, 26 Nov 2020 01:33:59 GMT  
		Size: 3.2 KB (3152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bee7f2ef708fa33cb50d2bf6eac1be4a866ae0efdc5533a02e88afd251c4498c`  
		Last Modified: Thu, 26 Nov 2020 01:33:59 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33e65a366feff49db614f5532727baa7982b8453ac4502bbdb7fca87d52c99db`  
		Last Modified: Thu, 26 Nov 2020 01:34:00 GMT  
		Size: 239.7 KB (239739 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:bionic-non-free`

```console
$ docker pull neurodebian@sha256:deec237dbb45a9e49721914b3767f6350007873b901500f007eaa79a4a14f7b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `neurodebian:bionic-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:a62d8c18bfb48dcd86cd58342c454705ba1977f77e0679c595dd06e17c1675ef
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.8 MB (31763722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c069995b43ee1f427ea87f9e932fce44344601adea76ac14b4aa4af4a8815a2f`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 25 Nov 2020 22:25:13 GMT
ADD file:6ef542de9959c3061f2d0758adb031e226b221a1a2cd748ff59e6fc13216a1c0 in / 
# Wed, 25 Nov 2020 22:25:14 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 25 Nov 2020 22:25:15 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Wed, 25 Nov 2020 22:25:16 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 25 Nov 2020 22:25:17 GMT
CMD ["/bin/bash"]
# Thu, 26 Nov 2020 01:32:12 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Thu, 26 Nov 2020 01:32:13 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Thu, 26 Nov 2020 01:32:14 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bionic main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bionic main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Thu, 26 Nov 2020 01:32:20 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Thu, 26 Nov 2020 01:32:25 GMT
RUN sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list; grep -q 'deb .* multiverse$' /etc/apt/sources.list || sed -i -e 's,universe *$,universe multiverse,g' /etc/apt/sources.list
```

-	Layers:
	-	`sha256:f22ccc0b8772d8e1bcb40f137b373686bc27427a70c0e41dd22b38016e09e7e0`  
		Last Modified: Fri, 20 Nov 2020 13:21:30 GMT  
		Size: 26.7 MB (26708056 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cf8fb62ba5ffb221a2edb2208741346eb4d2d99a174138e4afbb69ce1fd9966`  
		Last Modified: Wed, 25 Nov 2020 22:26:30 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e80c964ece6a3edf0db1cfc72ae0e6f0699fb776bbfcc92b708fbb945b0b9547`  
		Last Modified: Wed, 25 Nov 2020 22:26:30 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ca0d91fa7b32b3c4f0af52d770b27a7263f153342f69e086d84de98ef12fa93`  
		Last Modified: Thu, 26 Nov 2020 01:34:00 GMT  
		Size: 4.8 MB (4811258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:087a6d7d9519c3900a4acee2fa77ae27d8c43c7da392af1cdc45f39cbd978860`  
		Last Modified: Thu, 26 Nov 2020 01:33:59 GMT  
		Size: 3.2 KB (3152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bee7f2ef708fa33cb50d2bf6eac1be4a866ae0efdc5533a02e88afd251c4498c`  
		Last Modified: Thu, 26 Nov 2020 01:33:59 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33e65a366feff49db614f5532727baa7982b8453ac4502bbdb7fca87d52c99db`  
		Last Modified: Thu, 26 Nov 2020 01:34:00 GMT  
		Size: 239.7 KB (239739 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:069a129990abe1118de00542968007b5f1e9322d1e6163dca1296776742fc105`  
		Last Modified: Thu, 26 Nov 2020 01:34:05 GMT  
		Size: 258.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:bullseye`

```console
$ docker pull neurodebian@sha256:dca7df967bdd425d17c5ae33dfb5c4b06ef8462cabc0c2f2175395f40abc910e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `neurodebian:bullseye` - linux; amd64

```console
$ docker pull neurodebian@sha256:4822d6aed16d14b3669592a692e8c5b905611b7cce831ac8da2c0b5fe76702fb
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.5 MB (64482086 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a52c6da805609fb1ce4134b127b4ae23b51bfda1a0bf62959f54be7774254c3`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 11 Dec 2020 02:05:18 GMT
ADD file:ec1a9a704ae13b142c48069368561119760ccdf3d65d854c426d0dc9c39e60fb in / 
# Fri, 11 Dec 2020 02:05:18 GMT
CMD ["bash"]
# Fri, 11 Dec 2020 17:13:15 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Fri, 11 Dec 2020 17:13:17 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Fri, 11 Dec 2020 17:13:18 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bullseye main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Fri, 11 Dec 2020 17:13:22 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:e4991c356405721fc787980835bdbf5c529ae12379346a771feb34407c522bd6`  
		Last Modified: Fri, 11 Dec 2020 02:11:29 GMT  
		Size: 53.1 MB (53113553 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:353792b9e936b188911447b02e0aff739e6f0e161b04c62ba4c7f5abc5cb1e38`  
		Last Modified: Fri, 11 Dec 2020 17:15:24 GMT  
		Size: 11.1 MB (11067471 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6457673d7b064448a5710fe6f5cd263a5cea3dbfae10351d3c824e52772a8c84`  
		Last Modified: Fri, 11 Dec 2020 17:15:23 GMT  
		Size: 1.8 KB (1760 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d34e7c7dcff96673e9fbe9761465d1e98bcf967fdaa476049f13f5426388d8f4`  
		Last Modified: Fri, 11 Dec 2020 17:15:23 GMT  
		Size: 245.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf620bacf3a0e8bee1c96a446f79206ab8fbbff0a82b9c661afed05a9172e95a`  
		Last Modified: Fri, 11 Dec 2020 17:15:24 GMT  
		Size: 299.1 KB (299057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:bullseye-non-free`

```console
$ docker pull neurodebian@sha256:75ae55657348a156032e0a0ecea5f009b3dcf51d942e02171e420985ab3a882e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `neurodebian:bullseye-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:9bf19a92d933b6fb1f7ac038c684a7f6e317a44386d68aadd6d47a4f90f429d3
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.5 MB (64482451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ad9bb9e2d7f8d12558afc7e0b79f0d1a0e4128606d9b6d48847ea3611e9e278`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 11 Dec 2020 02:05:18 GMT
ADD file:ec1a9a704ae13b142c48069368561119760ccdf3d65d854c426d0dc9c39e60fb in / 
# Fri, 11 Dec 2020 02:05:18 GMT
CMD ["bash"]
# Fri, 11 Dec 2020 17:13:15 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Fri, 11 Dec 2020 17:13:17 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Fri, 11 Dec 2020 17:13:18 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bullseye main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Fri, 11 Dec 2020 17:13:22 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Fri, 11 Dec 2020 17:13:28 GMT
RUN sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list /etc/apt/sources.list
```

-	Layers:
	-	`sha256:e4991c356405721fc787980835bdbf5c529ae12379346a771feb34407c522bd6`  
		Last Modified: Fri, 11 Dec 2020 02:11:29 GMT  
		Size: 53.1 MB (53113553 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:353792b9e936b188911447b02e0aff739e6f0e161b04c62ba4c7f5abc5cb1e38`  
		Last Modified: Fri, 11 Dec 2020 17:15:24 GMT  
		Size: 11.1 MB (11067471 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6457673d7b064448a5710fe6f5cd263a5cea3dbfae10351d3c824e52772a8c84`  
		Last Modified: Fri, 11 Dec 2020 17:15:23 GMT  
		Size: 1.8 KB (1760 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d34e7c7dcff96673e9fbe9761465d1e98bcf967fdaa476049f13f5426388d8f4`  
		Last Modified: Fri, 11 Dec 2020 17:15:23 GMT  
		Size: 245.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf620bacf3a0e8bee1c96a446f79206ab8fbbff0a82b9c661afed05a9172e95a`  
		Last Modified: Fri, 11 Dec 2020 17:15:24 GMT  
		Size: 299.1 KB (299057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca63a627aa245fcab33f7b58024e3aeeb0ab247a5a7358c5773ed0399cfaa7fc`  
		Last Modified: Fri, 11 Dec 2020 17:15:29 GMT  
		Size: 365.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:buster`

```console
$ docker pull neurodebian@sha256:3d147e7c7637dd2ced05b49da1ba17953d83a9e8c281adcd37e01b990985a0fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `neurodebian:buster` - linux; amd64

```console
$ docker pull neurodebian@sha256:d360a60248aab9fc8c739a53efb721a0a35ee67a24edcc8792966a126722995a
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.2 MB (61200180 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65e14b08c68c94814159844d257bcd370d1a317e0cccd44d64440e6bd2ef1dd3`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 11 Dec 2020 02:05:52 GMT
ADD file:6014cd9d7466825f80d4a3345847efd6fd7ef600b8135811cab4f0e304f66cd7 in / 
# Fri, 11 Dec 2020 02:05:52 GMT
CMD ["bash"]
# Fri, 11 Dec 2020 17:12:52 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Fri, 11 Dec 2020 17:12:53 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Fri, 11 Dec 2020 17:12:54 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian buster main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel buster main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Fri, 11 Dec 2020 17:12:58 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:6c33745f49b41daad28b7b192c447938452ea4de9fe8c7cc3edf1433b1366946`  
		Last Modified: Fri, 11 Dec 2020 02:12:07 GMT  
		Size: 50.4 MB (50397728 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6c66699048e52432819f9112d0e4b7f96214e221978455d6b0b03b0da33342e`  
		Last Modified: Fri, 11 Dec 2020 17:15:11 GMT  
		Size: 10.5 MB (10497948 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0303af6cf2347aeb70ef9a23a7c4be666d35d14fddf1c2d81790bb35f8ac4a25`  
		Last Modified: Fri, 11 Dec 2020 17:15:10 GMT  
		Size: 1.8 KB (1757 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:726d52d9a1e530d78590b2b3bfe3bf0b22d178caa9a5b2618823d4840fbebe41`  
		Last Modified: Fri, 11 Dec 2020 17:15:10 GMT  
		Size: 243.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6b82482aaca0612234b7f4945ef4c4804eadc900afcbd5b30589006f175de3e`  
		Last Modified: Fri, 11 Dec 2020 17:15:10 GMT  
		Size: 302.5 KB (302504 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:buster-non-free`

```console
$ docker pull neurodebian@sha256:13a3ae717588d73d1d91a3f997209fc927701801068aa69c46d26eef457f3939
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `neurodebian:buster-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:917edfa4143b97d15a361baca32e01405cf22c3c2e1e6b2dc8d0c196fa9b775b
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.2 MB (61200549 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4005d67eed11091e26c769248175261693ae56fd9d3d6bbeb40ba2965eafb7c3`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 11 Dec 2020 02:05:52 GMT
ADD file:6014cd9d7466825f80d4a3345847efd6fd7ef600b8135811cab4f0e304f66cd7 in / 
# Fri, 11 Dec 2020 02:05:52 GMT
CMD ["bash"]
# Fri, 11 Dec 2020 17:12:52 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Fri, 11 Dec 2020 17:12:53 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Fri, 11 Dec 2020 17:12:54 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian buster main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel buster main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Fri, 11 Dec 2020 17:12:58 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Fri, 11 Dec 2020 17:13:04 GMT
RUN sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list /etc/apt/sources.list
```

-	Layers:
	-	`sha256:6c33745f49b41daad28b7b192c447938452ea4de9fe8c7cc3edf1433b1366946`  
		Last Modified: Fri, 11 Dec 2020 02:12:07 GMT  
		Size: 50.4 MB (50397728 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6c66699048e52432819f9112d0e4b7f96214e221978455d6b0b03b0da33342e`  
		Last Modified: Fri, 11 Dec 2020 17:15:11 GMT  
		Size: 10.5 MB (10497948 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0303af6cf2347aeb70ef9a23a7c4be666d35d14fddf1c2d81790bb35f8ac4a25`  
		Last Modified: Fri, 11 Dec 2020 17:15:10 GMT  
		Size: 1.8 KB (1757 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:726d52d9a1e530d78590b2b3bfe3bf0b22d178caa9a5b2618823d4840fbebe41`  
		Last Modified: Fri, 11 Dec 2020 17:15:10 GMT  
		Size: 243.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6b82482aaca0612234b7f4945ef4c4804eadc900afcbd5b30589006f175de3e`  
		Last Modified: Fri, 11 Dec 2020 17:15:10 GMT  
		Size: 302.5 KB (302504 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00739c9533012cde6c9d655074328bc2cc018efbc85e2a3bc98cda4048d7fe8a`  
		Last Modified: Fri, 11 Dec 2020 17:15:17 GMT  
		Size: 369.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:focal`

```console
$ docker pull neurodebian@sha256:21fe3961e4bd95b1c18f1d260a0431c8f24ccb2c8eb211e0844a3e92f8f7361e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `neurodebian:focal` - linux; amd64

```console
$ docker pull neurodebian@sha256:4306f51a71208c35f371bc94acc23f2868063bbf9693f8e56452559dd61bf703
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.3 MB (34292226 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69591e3d5d301ba10bd61e8c7fbc2f8ac1b45f692de7a15c268ae4a6f3ca31ac`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 25 Nov 2020 22:25:26 GMT
ADD file:4f15c4475fbafb3fe335e415e3ea1ac416c34af911fcdfe273c5759438aa8eb4 in / 
# Wed, 25 Nov 2020 22:25:27 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 25 Nov 2020 22:25:28 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Wed, 25 Nov 2020 22:25:29 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 25 Nov 2020 22:25:29 GMT
CMD ["/bin/bash"]
# Thu, 26 Nov 2020 01:32:38 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Thu, 26 Nov 2020 01:32:39 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Thu, 26 Nov 2020 01:32:40 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian focal main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel focal main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Thu, 26 Nov 2020 01:32:45 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:da7391352a9bb76b292a568c066aa4c3cbae8d494e6a3c68e3c596d34f7c75f8`  
		Last Modified: Fri, 06 Nov 2020 15:20:07 GMT  
		Size: 28.6 MB (28563271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14428a6d4bcdba49a64127900a0691fb00a3f329aced25eb77e3b65646638f8d`  
		Last Modified: Wed, 25 Nov 2020 22:26:39 GMT  
		Size: 847.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c2d948710f21ad82dce71743b1654b45acb5c059cf5c19da491582cef6f2601`  
		Last Modified: Wed, 25 Nov 2020 22:26:40 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f86c3b4c99036f64b464b8140bc6c472ba747187f7f57a7b205d539f020153f6`  
		Last Modified: Thu, 26 Nov 2020 01:34:10 GMT  
		Size: 5.5 MB (5488639 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e5193e0ea755747e6f1cd8ac2ca3794de0999da33d813967d550d0152ad15a3`  
		Last Modified: Thu, 26 Nov 2020 01:34:09 GMT  
		Size: 1.8 KB (1762 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b50ddfffb6545abe8a0b6b80c12489cf28758a08e7527ce5a2c718342498abea`  
		Last Modified: Thu, 26 Nov 2020 01:34:09 GMT  
		Size: 246.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40ced8c5fd0802ddf5f60d25c217cac2249a352965d966161986d93356fd8691`  
		Last Modified: Thu, 26 Nov 2020 01:34:10 GMT  
		Size: 237.3 KB (237299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:focal-non-free`

```console
$ docker pull neurodebian@sha256:3abc2595a31a5f486205a01bff7ca744134f12405930d1bcd14bc14158652efa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `neurodebian:focal-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:f0677bfdf4e0908aea3bc494c414c3eee01724c525934b474cc93b2c9a4f933a
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.3 MB (34292484 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aed7f5ec0212522d69fe51e63fa9dd5faab0e245e4c64d10075df7f5643b2403`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 25 Nov 2020 22:25:26 GMT
ADD file:4f15c4475fbafb3fe335e415e3ea1ac416c34af911fcdfe273c5759438aa8eb4 in / 
# Wed, 25 Nov 2020 22:25:27 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 25 Nov 2020 22:25:28 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Wed, 25 Nov 2020 22:25:29 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 25 Nov 2020 22:25:29 GMT
CMD ["/bin/bash"]
# Thu, 26 Nov 2020 01:32:38 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Thu, 26 Nov 2020 01:32:39 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Thu, 26 Nov 2020 01:32:40 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian focal main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel focal main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Thu, 26 Nov 2020 01:32:45 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Thu, 26 Nov 2020 01:32:52 GMT
RUN sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list; grep -q 'deb .* multiverse$' /etc/apt/sources.list || sed -i -e 's,universe *$,universe multiverse,g' /etc/apt/sources.list
```

-	Layers:
	-	`sha256:da7391352a9bb76b292a568c066aa4c3cbae8d494e6a3c68e3c596d34f7c75f8`  
		Last Modified: Fri, 06 Nov 2020 15:20:07 GMT  
		Size: 28.6 MB (28563271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14428a6d4bcdba49a64127900a0691fb00a3f329aced25eb77e3b65646638f8d`  
		Last Modified: Wed, 25 Nov 2020 22:26:39 GMT  
		Size: 847.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c2d948710f21ad82dce71743b1654b45acb5c059cf5c19da491582cef6f2601`  
		Last Modified: Wed, 25 Nov 2020 22:26:40 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f86c3b4c99036f64b464b8140bc6c472ba747187f7f57a7b205d539f020153f6`  
		Last Modified: Thu, 26 Nov 2020 01:34:10 GMT  
		Size: 5.5 MB (5488639 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e5193e0ea755747e6f1cd8ac2ca3794de0999da33d813967d550d0152ad15a3`  
		Last Modified: Thu, 26 Nov 2020 01:34:09 GMT  
		Size: 1.8 KB (1762 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b50ddfffb6545abe8a0b6b80c12489cf28758a08e7527ce5a2c718342498abea`  
		Last Modified: Thu, 26 Nov 2020 01:34:09 GMT  
		Size: 246.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40ced8c5fd0802ddf5f60d25c217cac2249a352965d966161986d93356fd8691`  
		Last Modified: Thu, 26 Nov 2020 01:34:10 GMT  
		Size: 237.3 KB (237299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:620898574f9a938524e0b445bceb7387bc3b43e92039121386dd3c353a512373`  
		Last Modified: Thu, 26 Nov 2020 01:34:14 GMT  
		Size: 258.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:groovy`

```console
$ docker pull neurodebian@sha256:54802a0e2cdd1f94cda0fae562aa7b6022eaf5cddde1b2905754dc467fb9d3a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `neurodebian:groovy` - linux; amd64

```console
$ docker pull neurodebian@sha256:1dafbb55b2dc2db73711fbc7a901132e4efdfe599d041f5389b1f31f5f67959b
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.2 MB (37174168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a4ee3d1adbeedcd622384f71c3aef2e8c78fbdc4ffa6a46db3c951e0143da29`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 25 Nov 2020 22:25:38 GMT
ADD file:6248e4aba6d7654cf97495ddc060cc9d68c5498500fe6ae03a10d955f0cc09b4 in / 
# Wed, 25 Nov 2020 22:25:39 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 25 Nov 2020 22:25:40 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Wed, 25 Nov 2020 22:25:41 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 25 Nov 2020 22:25:42 GMT
CMD ["/bin/bash"]
# Tue, 22 Dec 2020 22:25:30 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Tue, 22 Dec 2020 22:25:31 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Tue, 22 Dec 2020 22:25:32 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian groovy main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel groovy main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Tue, 22 Dec 2020 22:25:37 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:d8b994c442864dd519627740d3a4d134f385a2caa54b7f59bf9d372adcf7def0`  
		Last Modified: Wed, 25 Nov 2020 22:26:56 GMT  
		Size: 31.3 MB (31340118 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0773f3f14174f9bc8047861c64c2aa0cc581e73b16b48194a2884ad3918d01b`  
		Last Modified: Wed, 25 Nov 2020 22:26:50 GMT  
		Size: 847.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b20aefff2dc282ec6e2f496acce5b228bd1dfc30057a8ed41eae0513191b312`  
		Last Modified: Wed, 25 Nov 2020 22:26:50 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:639903bcac214566aebdaeb8513061996afad493070beb9504839f6908f5168a`  
		Last Modified: Tue, 22 Dec 2020 22:26:54 GMT  
		Size: 5.6 MB (5577397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17d4893825aa5203f3874bc7f215b9056618d765a6c5cb95a2322c8edd35cae8`  
		Last Modified: Tue, 22 Dec 2020 22:26:53 GMT  
		Size: 1.8 KB (1764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4965dd26526b8cac69077cb0bc04d51d5d7a08cc67bbd3394bcbd9914f13d87`  
		Last Modified: Tue, 22 Dec 2020 22:26:53 GMT  
		Size: 250.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1a6840143a335ce08e805745418d5a6c1fb2aaf56a7f3e31e3080635a6d0c94`  
		Last Modified: Tue, 22 Dec 2020 22:26:53 GMT  
		Size: 253.6 KB (253630 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:groovy-non-free`

```console
$ docker pull neurodebian@sha256:9c32a43d53cee336f3b3edc1ada94ea7178e8833a5c1aa7b17b26b3e5be164c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `neurodebian:groovy-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:3f38a8301d6959f6f118cb535498603146eb5236d7d652961cca17b130525d8c
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.2 MB (37174427 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bcd04ff14b631834196c9368b88009f79ade41d7598dab94156e500cc259646a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 25 Nov 2020 22:25:38 GMT
ADD file:6248e4aba6d7654cf97495ddc060cc9d68c5498500fe6ae03a10d955f0cc09b4 in / 
# Wed, 25 Nov 2020 22:25:39 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 25 Nov 2020 22:25:40 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Wed, 25 Nov 2020 22:25:41 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 25 Nov 2020 22:25:42 GMT
CMD ["/bin/bash"]
# Tue, 22 Dec 2020 22:25:30 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Tue, 22 Dec 2020 22:25:31 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Tue, 22 Dec 2020 22:25:32 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian groovy main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel groovy main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Tue, 22 Dec 2020 22:25:37 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Tue, 22 Dec 2020 22:25:42 GMT
RUN sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list; grep -q 'deb .* multiverse$' /etc/apt/sources.list || sed -i -e 's,universe *$,universe multiverse,g' /etc/apt/sources.list
```

-	Layers:
	-	`sha256:d8b994c442864dd519627740d3a4d134f385a2caa54b7f59bf9d372adcf7def0`  
		Last Modified: Wed, 25 Nov 2020 22:26:56 GMT  
		Size: 31.3 MB (31340118 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0773f3f14174f9bc8047861c64c2aa0cc581e73b16b48194a2884ad3918d01b`  
		Last Modified: Wed, 25 Nov 2020 22:26:50 GMT  
		Size: 847.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b20aefff2dc282ec6e2f496acce5b228bd1dfc30057a8ed41eae0513191b312`  
		Last Modified: Wed, 25 Nov 2020 22:26:50 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:639903bcac214566aebdaeb8513061996afad493070beb9504839f6908f5168a`  
		Last Modified: Tue, 22 Dec 2020 22:26:54 GMT  
		Size: 5.6 MB (5577397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17d4893825aa5203f3874bc7f215b9056618d765a6c5cb95a2322c8edd35cae8`  
		Last Modified: Tue, 22 Dec 2020 22:26:53 GMT  
		Size: 1.8 KB (1764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4965dd26526b8cac69077cb0bc04d51d5d7a08cc67bbd3394bcbd9914f13d87`  
		Last Modified: Tue, 22 Dec 2020 22:26:53 GMT  
		Size: 250.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1a6840143a335ce08e805745418d5a6c1fb2aaf56a7f3e31e3080635a6d0c94`  
		Last Modified: Tue, 22 Dec 2020 22:26:53 GMT  
		Size: 253.6 KB (253630 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a0b390e79b834f01b99f5a077eb8e8ae64b3983db28e1fa496ba42812e3d417`  
		Last Modified: Tue, 22 Dec 2020 22:26:58 GMT  
		Size: 259.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:latest`

```console
$ docker pull neurodebian@sha256:3d147e7c7637dd2ced05b49da1ba17953d83a9e8c281adcd37e01b990985a0fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `neurodebian:latest` - linux; amd64

```console
$ docker pull neurodebian@sha256:d360a60248aab9fc8c739a53efb721a0a35ee67a24edcc8792966a126722995a
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.2 MB (61200180 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65e14b08c68c94814159844d257bcd370d1a317e0cccd44d64440e6bd2ef1dd3`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 11 Dec 2020 02:05:52 GMT
ADD file:6014cd9d7466825f80d4a3345847efd6fd7ef600b8135811cab4f0e304f66cd7 in / 
# Fri, 11 Dec 2020 02:05:52 GMT
CMD ["bash"]
# Fri, 11 Dec 2020 17:12:52 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Fri, 11 Dec 2020 17:12:53 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Fri, 11 Dec 2020 17:12:54 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian buster main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel buster main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Fri, 11 Dec 2020 17:12:58 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:6c33745f49b41daad28b7b192c447938452ea4de9fe8c7cc3edf1433b1366946`  
		Last Modified: Fri, 11 Dec 2020 02:12:07 GMT  
		Size: 50.4 MB (50397728 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6c66699048e52432819f9112d0e4b7f96214e221978455d6b0b03b0da33342e`  
		Last Modified: Fri, 11 Dec 2020 17:15:11 GMT  
		Size: 10.5 MB (10497948 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0303af6cf2347aeb70ef9a23a7c4be666d35d14fddf1c2d81790bb35f8ac4a25`  
		Last Modified: Fri, 11 Dec 2020 17:15:10 GMT  
		Size: 1.8 KB (1757 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:726d52d9a1e530d78590b2b3bfe3bf0b22d178caa9a5b2618823d4840fbebe41`  
		Last Modified: Fri, 11 Dec 2020 17:15:10 GMT  
		Size: 243.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6b82482aaca0612234b7f4945ef4c4804eadc900afcbd5b30589006f175de3e`  
		Last Modified: Fri, 11 Dec 2020 17:15:10 GMT  
		Size: 302.5 KB (302504 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:nd`

```console
$ docker pull neurodebian@sha256:487e0fda83dfc290539e7c4fb2aced9b79a524a3eb9caef7590894428e9501be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `neurodebian:nd` - linux; amd64

```console
$ docker pull neurodebian@sha256:3736fc73e61c4ce1544861d40c347db86bd5629db51c42d6a96d1ac4b3ee957b
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.7 MB (64721045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aedcb6385286c612e36654ae662593eceeae4eac97b3328ba9b1b03426278252`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 11 Dec 2020 02:07:48 GMT
ADD file:51a85ad79ebd7e288cd0ea14cd2ae41990aab2d77352f801f09c3a4682cb83a9 in / 
# Fri, 11 Dec 2020 02:07:48 GMT
CMD ["bash"]
# Fri, 11 Dec 2020 17:13:39 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Fri, 11 Dec 2020 17:13:41 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Fri, 11 Dec 2020 17:13:42 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian sid main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Fri, 11 Dec 2020 17:13:46 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:ff8cddfd21234a3c42ee0af471b251a807aa29af4ca00392976a17d3257ed269`  
		Last Modified: Fri, 11 Dec 2020 02:14:23 GMT  
		Size: 53.4 MB (53352668 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce2727b136c25fc091264e7b123438827cbf21b009f9c493bff195b43fe11862`  
		Last Modified: Fri, 11 Dec 2020 17:15:35 GMT  
		Size: 11.1 MB (11067345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:617bbba7816c68b01e9737f10ce63810794331e00f9e16660ca78aff616e7e68`  
		Last Modified: Fri, 11 Dec 2020 17:15:34 GMT  
		Size: 1.8 KB (1760 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:464c117400d03f730f7dea39e3cde59a514a4eeafcc63ccb72b29be814d3a56d`  
		Last Modified: Fri, 11 Dec 2020 17:15:34 GMT  
		Size: 240.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d3c7e0b6f6db759c0c88baa1dcf7186643ebb6da7f6508424e17ec4886daad3`  
		Last Modified: Fri, 11 Dec 2020 17:15:34 GMT  
		Size: 299.0 KB (299032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:nd100`

```console
$ docker pull neurodebian@sha256:3d147e7c7637dd2ced05b49da1ba17953d83a9e8c281adcd37e01b990985a0fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `neurodebian:nd100` - linux; amd64

```console
$ docker pull neurodebian@sha256:d360a60248aab9fc8c739a53efb721a0a35ee67a24edcc8792966a126722995a
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.2 MB (61200180 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65e14b08c68c94814159844d257bcd370d1a317e0cccd44d64440e6bd2ef1dd3`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 11 Dec 2020 02:05:52 GMT
ADD file:6014cd9d7466825f80d4a3345847efd6fd7ef600b8135811cab4f0e304f66cd7 in / 
# Fri, 11 Dec 2020 02:05:52 GMT
CMD ["bash"]
# Fri, 11 Dec 2020 17:12:52 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Fri, 11 Dec 2020 17:12:53 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Fri, 11 Dec 2020 17:12:54 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian buster main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel buster main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Fri, 11 Dec 2020 17:12:58 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:6c33745f49b41daad28b7b192c447938452ea4de9fe8c7cc3edf1433b1366946`  
		Last Modified: Fri, 11 Dec 2020 02:12:07 GMT  
		Size: 50.4 MB (50397728 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6c66699048e52432819f9112d0e4b7f96214e221978455d6b0b03b0da33342e`  
		Last Modified: Fri, 11 Dec 2020 17:15:11 GMT  
		Size: 10.5 MB (10497948 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0303af6cf2347aeb70ef9a23a7c4be666d35d14fddf1c2d81790bb35f8ac4a25`  
		Last Modified: Fri, 11 Dec 2020 17:15:10 GMT  
		Size: 1.8 KB (1757 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:726d52d9a1e530d78590b2b3bfe3bf0b22d178caa9a5b2618823d4840fbebe41`  
		Last Modified: Fri, 11 Dec 2020 17:15:10 GMT  
		Size: 243.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6b82482aaca0612234b7f4945ef4c4804eadc900afcbd5b30589006f175de3e`  
		Last Modified: Fri, 11 Dec 2020 17:15:10 GMT  
		Size: 302.5 KB (302504 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:nd100-non-free`

```console
$ docker pull neurodebian@sha256:13a3ae717588d73d1d91a3f997209fc927701801068aa69c46d26eef457f3939
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `neurodebian:nd100-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:917edfa4143b97d15a361baca32e01405cf22c3c2e1e6b2dc8d0c196fa9b775b
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.2 MB (61200549 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4005d67eed11091e26c769248175261693ae56fd9d3d6bbeb40ba2965eafb7c3`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 11 Dec 2020 02:05:52 GMT
ADD file:6014cd9d7466825f80d4a3345847efd6fd7ef600b8135811cab4f0e304f66cd7 in / 
# Fri, 11 Dec 2020 02:05:52 GMT
CMD ["bash"]
# Fri, 11 Dec 2020 17:12:52 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Fri, 11 Dec 2020 17:12:53 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Fri, 11 Dec 2020 17:12:54 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian buster main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel buster main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Fri, 11 Dec 2020 17:12:58 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Fri, 11 Dec 2020 17:13:04 GMT
RUN sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list /etc/apt/sources.list
```

-	Layers:
	-	`sha256:6c33745f49b41daad28b7b192c447938452ea4de9fe8c7cc3edf1433b1366946`  
		Last Modified: Fri, 11 Dec 2020 02:12:07 GMT  
		Size: 50.4 MB (50397728 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6c66699048e52432819f9112d0e4b7f96214e221978455d6b0b03b0da33342e`  
		Last Modified: Fri, 11 Dec 2020 17:15:11 GMT  
		Size: 10.5 MB (10497948 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0303af6cf2347aeb70ef9a23a7c4be666d35d14fddf1c2d81790bb35f8ac4a25`  
		Last Modified: Fri, 11 Dec 2020 17:15:10 GMT  
		Size: 1.8 KB (1757 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:726d52d9a1e530d78590b2b3bfe3bf0b22d178caa9a5b2618823d4840fbebe41`  
		Last Modified: Fri, 11 Dec 2020 17:15:10 GMT  
		Size: 243.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6b82482aaca0612234b7f4945ef4c4804eadc900afcbd5b30589006f175de3e`  
		Last Modified: Fri, 11 Dec 2020 17:15:10 GMT  
		Size: 302.5 KB (302504 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00739c9533012cde6c9d655074328bc2cc018efbc85e2a3bc98cda4048d7fe8a`  
		Last Modified: Fri, 11 Dec 2020 17:15:17 GMT  
		Size: 369.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:nd110`

```console
$ docker pull neurodebian@sha256:dca7df967bdd425d17c5ae33dfb5c4b06ef8462cabc0c2f2175395f40abc910e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `neurodebian:nd110` - linux; amd64

```console
$ docker pull neurodebian@sha256:4822d6aed16d14b3669592a692e8c5b905611b7cce831ac8da2c0b5fe76702fb
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.5 MB (64482086 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a52c6da805609fb1ce4134b127b4ae23b51bfda1a0bf62959f54be7774254c3`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 11 Dec 2020 02:05:18 GMT
ADD file:ec1a9a704ae13b142c48069368561119760ccdf3d65d854c426d0dc9c39e60fb in / 
# Fri, 11 Dec 2020 02:05:18 GMT
CMD ["bash"]
# Fri, 11 Dec 2020 17:13:15 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Fri, 11 Dec 2020 17:13:17 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Fri, 11 Dec 2020 17:13:18 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bullseye main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Fri, 11 Dec 2020 17:13:22 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:e4991c356405721fc787980835bdbf5c529ae12379346a771feb34407c522bd6`  
		Last Modified: Fri, 11 Dec 2020 02:11:29 GMT  
		Size: 53.1 MB (53113553 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:353792b9e936b188911447b02e0aff739e6f0e161b04c62ba4c7f5abc5cb1e38`  
		Last Modified: Fri, 11 Dec 2020 17:15:24 GMT  
		Size: 11.1 MB (11067471 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6457673d7b064448a5710fe6f5cd263a5cea3dbfae10351d3c824e52772a8c84`  
		Last Modified: Fri, 11 Dec 2020 17:15:23 GMT  
		Size: 1.8 KB (1760 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d34e7c7dcff96673e9fbe9761465d1e98bcf967fdaa476049f13f5426388d8f4`  
		Last Modified: Fri, 11 Dec 2020 17:15:23 GMT  
		Size: 245.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf620bacf3a0e8bee1c96a446f79206ab8fbbff0a82b9c661afed05a9172e95a`  
		Last Modified: Fri, 11 Dec 2020 17:15:24 GMT  
		Size: 299.1 KB (299057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:nd110-non-free`

```console
$ docker pull neurodebian@sha256:75ae55657348a156032e0a0ecea5f009b3dcf51d942e02171e420985ab3a882e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `neurodebian:nd110-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:9bf19a92d933b6fb1f7ac038c684a7f6e317a44386d68aadd6d47a4f90f429d3
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.5 MB (64482451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ad9bb9e2d7f8d12558afc7e0b79f0d1a0e4128606d9b6d48847ea3611e9e278`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 11 Dec 2020 02:05:18 GMT
ADD file:ec1a9a704ae13b142c48069368561119760ccdf3d65d854c426d0dc9c39e60fb in / 
# Fri, 11 Dec 2020 02:05:18 GMT
CMD ["bash"]
# Fri, 11 Dec 2020 17:13:15 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Fri, 11 Dec 2020 17:13:17 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Fri, 11 Dec 2020 17:13:18 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bullseye main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Fri, 11 Dec 2020 17:13:22 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Fri, 11 Dec 2020 17:13:28 GMT
RUN sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list /etc/apt/sources.list
```

-	Layers:
	-	`sha256:e4991c356405721fc787980835bdbf5c529ae12379346a771feb34407c522bd6`  
		Last Modified: Fri, 11 Dec 2020 02:11:29 GMT  
		Size: 53.1 MB (53113553 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:353792b9e936b188911447b02e0aff739e6f0e161b04c62ba4c7f5abc5cb1e38`  
		Last Modified: Fri, 11 Dec 2020 17:15:24 GMT  
		Size: 11.1 MB (11067471 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6457673d7b064448a5710fe6f5cd263a5cea3dbfae10351d3c824e52772a8c84`  
		Last Modified: Fri, 11 Dec 2020 17:15:23 GMT  
		Size: 1.8 KB (1760 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d34e7c7dcff96673e9fbe9761465d1e98bcf967fdaa476049f13f5426388d8f4`  
		Last Modified: Fri, 11 Dec 2020 17:15:23 GMT  
		Size: 245.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf620bacf3a0e8bee1c96a446f79206ab8fbbff0a82b9c661afed05a9172e95a`  
		Last Modified: Fri, 11 Dec 2020 17:15:24 GMT  
		Size: 299.1 KB (299057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca63a627aa245fcab33f7b58024e3aeeb0ab247a5a7358c5773ed0399cfaa7fc`  
		Last Modified: Fri, 11 Dec 2020 17:15:29 GMT  
		Size: 365.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:nd16.04`

```console
$ docker pull neurodebian@sha256:99d3daba4215efae715ab91ca51cf69a398861445f0eb0f351dfadc1bf560027
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `neurodebian:nd16.04` - linux; amd64

```console
$ docker pull neurodebian@sha256:842d6d6b271deb6dc93694e18d7f5c5a49dc720ab92724ae1d58572d4ec7cb0c
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.1 MB (46070191 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad6069c8aac6e1f68e62bc20e9bac247f85a5baa22566458bb637ef3a3b3233e`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 25 Nov 2020 22:26:11 GMT
ADD file:8eef54430e581236e6d529a7d09df648f43c840e889d9ae132e5ed25d7bd2b88 in / 
# Wed, 25 Nov 2020 22:26:12 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 25 Nov 2020 22:26:13 GMT
RUN rm -rf /var/lib/apt/lists/*
# Wed, 25 Nov 2020 22:26:14 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 25 Nov 2020 22:26:14 GMT
CMD ["/bin/bash"]
# Thu, 26 Nov 2020 01:31:45 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Thu, 26 Nov 2020 01:31:46 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Thu, 26 Nov 2020 01:31:47 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian xenial main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel xenial main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Thu, 26 Nov 2020 01:31:53 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:be8ec4e48d7f24a9a1c01063e5dfabb092c2c1ec73e125113848553c9b07eb8c`  
		Last Modified: Sat, 31 Oct 2020 14:20:23 GMT  
		Size: 45.8 MB (45838270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33b8b485aff0509bb0fa67dff6a2aa82e9b7b17e5ef28c1673467ec83edb945d`  
		Last Modified: Wed, 25 Nov 2020 22:27:15 GMT  
		Size: 849.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d887158cc58cbfc3d03cefd5c0b15175fae66ffbf6f28a56180c51cbb5062b8a`  
		Last Modified: Wed, 25 Nov 2020 22:27:14 GMT  
		Size: 533.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05895bb28c18264f614acd13e401b3c5594e12d9fe90d7e52929d3e810e11e97`  
		Last Modified: Wed, 25 Nov 2020 22:27:15 GMT  
		Size: 167.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4a381e547592e23b46523b0dab60f6c4bd467b602f43a16343b5559da0d4686`  
		Last Modified: Thu, 26 Nov 2020 01:33:50 GMT  
		Size: 182.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a7acad501fc13e842de1e4bd4429cd32a570aa3345101ab9113c7965de95ac0`  
		Last Modified: Thu, 26 Nov 2020 01:33:50 GMT  
		Size: 3.2 KB (3152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c20da126479df0535aad7be815dd7f724e0df2ef817ec5aab5542bb981300db4`  
		Last Modified: Thu, 26 Nov 2020 01:33:50 GMT  
		Size: 249.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a01b6c31d56c9536a38779046a52ab23cae4de7b819cdb22047788474cd2d8db`  
		Last Modified: Thu, 26 Nov 2020 01:33:50 GMT  
		Size: 226.8 KB (226789 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:nd16.04-non-free`

```console
$ docker pull neurodebian@sha256:9c7a17e1ea546d92934acf1d917947ab407c8ca4a8fd8763e23c03bf002e5218
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `neurodebian:nd16.04-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:d66d5c1d7c22f6b240d56c964e2829a66dceedd2d4cedbbb30b487c8b8148b74
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.1 MB (46070450 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23236a17a48c8328eee81a77511734ab54cfb47397137177d1e6bbcbafbfaa20`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 25 Nov 2020 22:26:11 GMT
ADD file:8eef54430e581236e6d529a7d09df648f43c840e889d9ae132e5ed25d7bd2b88 in / 
# Wed, 25 Nov 2020 22:26:12 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 25 Nov 2020 22:26:13 GMT
RUN rm -rf /var/lib/apt/lists/*
# Wed, 25 Nov 2020 22:26:14 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 25 Nov 2020 22:26:14 GMT
CMD ["/bin/bash"]
# Thu, 26 Nov 2020 01:31:45 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Thu, 26 Nov 2020 01:31:46 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Thu, 26 Nov 2020 01:31:47 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian xenial main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel xenial main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Thu, 26 Nov 2020 01:31:53 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Thu, 26 Nov 2020 01:31:58 GMT
RUN sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list; grep -q 'deb .* multiverse$' /etc/apt/sources.list || sed -i -e 's,universe *$,universe multiverse,g' /etc/apt/sources.list
```

-	Layers:
	-	`sha256:be8ec4e48d7f24a9a1c01063e5dfabb092c2c1ec73e125113848553c9b07eb8c`  
		Last Modified: Sat, 31 Oct 2020 14:20:23 GMT  
		Size: 45.8 MB (45838270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33b8b485aff0509bb0fa67dff6a2aa82e9b7b17e5ef28c1673467ec83edb945d`  
		Last Modified: Wed, 25 Nov 2020 22:27:15 GMT  
		Size: 849.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d887158cc58cbfc3d03cefd5c0b15175fae66ffbf6f28a56180c51cbb5062b8a`  
		Last Modified: Wed, 25 Nov 2020 22:27:14 GMT  
		Size: 533.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05895bb28c18264f614acd13e401b3c5594e12d9fe90d7e52929d3e810e11e97`  
		Last Modified: Wed, 25 Nov 2020 22:27:15 GMT  
		Size: 167.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4a381e547592e23b46523b0dab60f6c4bd467b602f43a16343b5559da0d4686`  
		Last Modified: Thu, 26 Nov 2020 01:33:50 GMT  
		Size: 182.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a7acad501fc13e842de1e4bd4429cd32a570aa3345101ab9113c7965de95ac0`  
		Last Modified: Thu, 26 Nov 2020 01:33:50 GMT  
		Size: 3.2 KB (3152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c20da126479df0535aad7be815dd7f724e0df2ef817ec5aab5542bb981300db4`  
		Last Modified: Thu, 26 Nov 2020 01:33:50 GMT  
		Size: 249.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a01b6c31d56c9536a38779046a52ab23cae4de7b819cdb22047788474cd2d8db`  
		Last Modified: Thu, 26 Nov 2020 01:33:50 GMT  
		Size: 226.8 KB (226789 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08277deecb4c0895f5ee6388a873f54d7c60f1bdcfd4d6019e6ef70cca187718`  
		Last Modified: Thu, 26 Nov 2020 01:33:54 GMT  
		Size: 259.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:nd18.04`

```console
$ docker pull neurodebian@sha256:65ac4060f499f820afebcf42f24dbdae9cfd3b186d4b4b0af9de00ec91bc1b6a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `neurodebian:nd18.04` - linux; amd64

```console
$ docker pull neurodebian@sha256:db24a8f8cc9639d8472b8b2924435a1bc84d694d120e286a48ba359b96b0eaf4
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.8 MB (31763464 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36e2dc1395b7c38f8f83562e178128c855380b90402a989caf0e094508c4b9eb`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 25 Nov 2020 22:25:13 GMT
ADD file:6ef542de9959c3061f2d0758adb031e226b221a1a2cd748ff59e6fc13216a1c0 in / 
# Wed, 25 Nov 2020 22:25:14 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 25 Nov 2020 22:25:15 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Wed, 25 Nov 2020 22:25:16 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 25 Nov 2020 22:25:17 GMT
CMD ["/bin/bash"]
# Thu, 26 Nov 2020 01:32:12 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Thu, 26 Nov 2020 01:32:13 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Thu, 26 Nov 2020 01:32:14 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bionic main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bionic main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Thu, 26 Nov 2020 01:32:20 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:f22ccc0b8772d8e1bcb40f137b373686bc27427a70c0e41dd22b38016e09e7e0`  
		Last Modified: Fri, 20 Nov 2020 13:21:30 GMT  
		Size: 26.7 MB (26708056 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cf8fb62ba5ffb221a2edb2208741346eb4d2d99a174138e4afbb69ce1fd9966`  
		Last Modified: Wed, 25 Nov 2020 22:26:30 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e80c964ece6a3edf0db1cfc72ae0e6f0699fb776bbfcc92b708fbb945b0b9547`  
		Last Modified: Wed, 25 Nov 2020 22:26:30 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ca0d91fa7b32b3c4f0af52d770b27a7263f153342f69e086d84de98ef12fa93`  
		Last Modified: Thu, 26 Nov 2020 01:34:00 GMT  
		Size: 4.8 MB (4811258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:087a6d7d9519c3900a4acee2fa77ae27d8c43c7da392af1cdc45f39cbd978860`  
		Last Modified: Thu, 26 Nov 2020 01:33:59 GMT  
		Size: 3.2 KB (3152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bee7f2ef708fa33cb50d2bf6eac1be4a866ae0efdc5533a02e88afd251c4498c`  
		Last Modified: Thu, 26 Nov 2020 01:33:59 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33e65a366feff49db614f5532727baa7982b8453ac4502bbdb7fca87d52c99db`  
		Last Modified: Thu, 26 Nov 2020 01:34:00 GMT  
		Size: 239.7 KB (239739 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:nd18.04-non-free`

```console
$ docker pull neurodebian@sha256:deec237dbb45a9e49721914b3767f6350007873b901500f007eaa79a4a14f7b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `neurodebian:nd18.04-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:a62d8c18bfb48dcd86cd58342c454705ba1977f77e0679c595dd06e17c1675ef
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.8 MB (31763722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c069995b43ee1f427ea87f9e932fce44344601adea76ac14b4aa4af4a8815a2f`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 25 Nov 2020 22:25:13 GMT
ADD file:6ef542de9959c3061f2d0758adb031e226b221a1a2cd748ff59e6fc13216a1c0 in / 
# Wed, 25 Nov 2020 22:25:14 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 25 Nov 2020 22:25:15 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Wed, 25 Nov 2020 22:25:16 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 25 Nov 2020 22:25:17 GMT
CMD ["/bin/bash"]
# Thu, 26 Nov 2020 01:32:12 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Thu, 26 Nov 2020 01:32:13 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Thu, 26 Nov 2020 01:32:14 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bionic main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bionic main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Thu, 26 Nov 2020 01:32:20 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Thu, 26 Nov 2020 01:32:25 GMT
RUN sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list; grep -q 'deb .* multiverse$' /etc/apt/sources.list || sed -i -e 's,universe *$,universe multiverse,g' /etc/apt/sources.list
```

-	Layers:
	-	`sha256:f22ccc0b8772d8e1bcb40f137b373686bc27427a70c0e41dd22b38016e09e7e0`  
		Last Modified: Fri, 20 Nov 2020 13:21:30 GMT  
		Size: 26.7 MB (26708056 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cf8fb62ba5ffb221a2edb2208741346eb4d2d99a174138e4afbb69ce1fd9966`  
		Last Modified: Wed, 25 Nov 2020 22:26:30 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e80c964ece6a3edf0db1cfc72ae0e6f0699fb776bbfcc92b708fbb945b0b9547`  
		Last Modified: Wed, 25 Nov 2020 22:26:30 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ca0d91fa7b32b3c4f0af52d770b27a7263f153342f69e086d84de98ef12fa93`  
		Last Modified: Thu, 26 Nov 2020 01:34:00 GMT  
		Size: 4.8 MB (4811258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:087a6d7d9519c3900a4acee2fa77ae27d8c43c7da392af1cdc45f39cbd978860`  
		Last Modified: Thu, 26 Nov 2020 01:33:59 GMT  
		Size: 3.2 KB (3152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bee7f2ef708fa33cb50d2bf6eac1be4a866ae0efdc5533a02e88afd251c4498c`  
		Last Modified: Thu, 26 Nov 2020 01:33:59 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33e65a366feff49db614f5532727baa7982b8453ac4502bbdb7fca87d52c99db`  
		Last Modified: Thu, 26 Nov 2020 01:34:00 GMT  
		Size: 239.7 KB (239739 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:069a129990abe1118de00542968007b5f1e9322d1e6163dca1296776742fc105`  
		Last Modified: Thu, 26 Nov 2020 01:34:05 GMT  
		Size: 258.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:nd20.04`

```console
$ docker pull neurodebian@sha256:21fe3961e4bd95b1c18f1d260a0431c8f24ccb2c8eb211e0844a3e92f8f7361e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `neurodebian:nd20.04` - linux; amd64

```console
$ docker pull neurodebian@sha256:4306f51a71208c35f371bc94acc23f2868063bbf9693f8e56452559dd61bf703
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.3 MB (34292226 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69591e3d5d301ba10bd61e8c7fbc2f8ac1b45f692de7a15c268ae4a6f3ca31ac`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 25 Nov 2020 22:25:26 GMT
ADD file:4f15c4475fbafb3fe335e415e3ea1ac416c34af911fcdfe273c5759438aa8eb4 in / 
# Wed, 25 Nov 2020 22:25:27 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 25 Nov 2020 22:25:28 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Wed, 25 Nov 2020 22:25:29 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 25 Nov 2020 22:25:29 GMT
CMD ["/bin/bash"]
# Thu, 26 Nov 2020 01:32:38 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Thu, 26 Nov 2020 01:32:39 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Thu, 26 Nov 2020 01:32:40 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian focal main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel focal main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Thu, 26 Nov 2020 01:32:45 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:da7391352a9bb76b292a568c066aa4c3cbae8d494e6a3c68e3c596d34f7c75f8`  
		Last Modified: Fri, 06 Nov 2020 15:20:07 GMT  
		Size: 28.6 MB (28563271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14428a6d4bcdba49a64127900a0691fb00a3f329aced25eb77e3b65646638f8d`  
		Last Modified: Wed, 25 Nov 2020 22:26:39 GMT  
		Size: 847.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c2d948710f21ad82dce71743b1654b45acb5c059cf5c19da491582cef6f2601`  
		Last Modified: Wed, 25 Nov 2020 22:26:40 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f86c3b4c99036f64b464b8140bc6c472ba747187f7f57a7b205d539f020153f6`  
		Last Modified: Thu, 26 Nov 2020 01:34:10 GMT  
		Size: 5.5 MB (5488639 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e5193e0ea755747e6f1cd8ac2ca3794de0999da33d813967d550d0152ad15a3`  
		Last Modified: Thu, 26 Nov 2020 01:34:09 GMT  
		Size: 1.8 KB (1762 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b50ddfffb6545abe8a0b6b80c12489cf28758a08e7527ce5a2c718342498abea`  
		Last Modified: Thu, 26 Nov 2020 01:34:09 GMT  
		Size: 246.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40ced8c5fd0802ddf5f60d25c217cac2249a352965d966161986d93356fd8691`  
		Last Modified: Thu, 26 Nov 2020 01:34:10 GMT  
		Size: 237.3 KB (237299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:nd20.04-non-free`

```console
$ docker pull neurodebian@sha256:3abc2595a31a5f486205a01bff7ca744134f12405930d1bcd14bc14158652efa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `neurodebian:nd20.04-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:f0677bfdf4e0908aea3bc494c414c3eee01724c525934b474cc93b2c9a4f933a
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.3 MB (34292484 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aed7f5ec0212522d69fe51e63fa9dd5faab0e245e4c64d10075df7f5643b2403`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 25 Nov 2020 22:25:26 GMT
ADD file:4f15c4475fbafb3fe335e415e3ea1ac416c34af911fcdfe273c5759438aa8eb4 in / 
# Wed, 25 Nov 2020 22:25:27 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 25 Nov 2020 22:25:28 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Wed, 25 Nov 2020 22:25:29 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 25 Nov 2020 22:25:29 GMT
CMD ["/bin/bash"]
# Thu, 26 Nov 2020 01:32:38 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Thu, 26 Nov 2020 01:32:39 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Thu, 26 Nov 2020 01:32:40 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian focal main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel focal main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Thu, 26 Nov 2020 01:32:45 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Thu, 26 Nov 2020 01:32:52 GMT
RUN sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list; grep -q 'deb .* multiverse$' /etc/apt/sources.list || sed -i -e 's,universe *$,universe multiverse,g' /etc/apt/sources.list
```

-	Layers:
	-	`sha256:da7391352a9bb76b292a568c066aa4c3cbae8d494e6a3c68e3c596d34f7c75f8`  
		Last Modified: Fri, 06 Nov 2020 15:20:07 GMT  
		Size: 28.6 MB (28563271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14428a6d4bcdba49a64127900a0691fb00a3f329aced25eb77e3b65646638f8d`  
		Last Modified: Wed, 25 Nov 2020 22:26:39 GMT  
		Size: 847.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c2d948710f21ad82dce71743b1654b45acb5c059cf5c19da491582cef6f2601`  
		Last Modified: Wed, 25 Nov 2020 22:26:40 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f86c3b4c99036f64b464b8140bc6c472ba747187f7f57a7b205d539f020153f6`  
		Last Modified: Thu, 26 Nov 2020 01:34:10 GMT  
		Size: 5.5 MB (5488639 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e5193e0ea755747e6f1cd8ac2ca3794de0999da33d813967d550d0152ad15a3`  
		Last Modified: Thu, 26 Nov 2020 01:34:09 GMT  
		Size: 1.8 KB (1762 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b50ddfffb6545abe8a0b6b80c12489cf28758a08e7527ce5a2c718342498abea`  
		Last Modified: Thu, 26 Nov 2020 01:34:09 GMT  
		Size: 246.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40ced8c5fd0802ddf5f60d25c217cac2249a352965d966161986d93356fd8691`  
		Last Modified: Thu, 26 Nov 2020 01:34:10 GMT  
		Size: 237.3 KB (237299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:620898574f9a938524e0b445bceb7387bc3b43e92039121386dd3c353a512373`  
		Last Modified: Thu, 26 Nov 2020 01:34:14 GMT  
		Size: 258.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:nd20.10`

```console
$ docker pull neurodebian@sha256:54802a0e2cdd1f94cda0fae562aa7b6022eaf5cddde1b2905754dc467fb9d3a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `neurodebian:nd20.10` - linux; amd64

```console
$ docker pull neurodebian@sha256:1dafbb55b2dc2db73711fbc7a901132e4efdfe599d041f5389b1f31f5f67959b
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.2 MB (37174168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a4ee3d1adbeedcd622384f71c3aef2e8c78fbdc4ffa6a46db3c951e0143da29`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 25 Nov 2020 22:25:38 GMT
ADD file:6248e4aba6d7654cf97495ddc060cc9d68c5498500fe6ae03a10d955f0cc09b4 in / 
# Wed, 25 Nov 2020 22:25:39 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 25 Nov 2020 22:25:40 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Wed, 25 Nov 2020 22:25:41 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 25 Nov 2020 22:25:42 GMT
CMD ["/bin/bash"]
# Tue, 22 Dec 2020 22:25:30 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Tue, 22 Dec 2020 22:25:31 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Tue, 22 Dec 2020 22:25:32 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian groovy main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel groovy main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Tue, 22 Dec 2020 22:25:37 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:d8b994c442864dd519627740d3a4d134f385a2caa54b7f59bf9d372adcf7def0`  
		Last Modified: Wed, 25 Nov 2020 22:26:56 GMT  
		Size: 31.3 MB (31340118 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0773f3f14174f9bc8047861c64c2aa0cc581e73b16b48194a2884ad3918d01b`  
		Last Modified: Wed, 25 Nov 2020 22:26:50 GMT  
		Size: 847.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b20aefff2dc282ec6e2f496acce5b228bd1dfc30057a8ed41eae0513191b312`  
		Last Modified: Wed, 25 Nov 2020 22:26:50 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:639903bcac214566aebdaeb8513061996afad493070beb9504839f6908f5168a`  
		Last Modified: Tue, 22 Dec 2020 22:26:54 GMT  
		Size: 5.6 MB (5577397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17d4893825aa5203f3874bc7f215b9056618d765a6c5cb95a2322c8edd35cae8`  
		Last Modified: Tue, 22 Dec 2020 22:26:53 GMT  
		Size: 1.8 KB (1764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4965dd26526b8cac69077cb0bc04d51d5d7a08cc67bbd3394bcbd9914f13d87`  
		Last Modified: Tue, 22 Dec 2020 22:26:53 GMT  
		Size: 250.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1a6840143a335ce08e805745418d5a6c1fb2aaf56a7f3e31e3080635a6d0c94`  
		Last Modified: Tue, 22 Dec 2020 22:26:53 GMT  
		Size: 253.6 KB (253630 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:nd20.10-non-free`

```console
$ docker pull neurodebian@sha256:9c32a43d53cee336f3b3edc1ada94ea7178e8833a5c1aa7b17b26b3e5be164c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `neurodebian:nd20.10-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:3f38a8301d6959f6f118cb535498603146eb5236d7d652961cca17b130525d8c
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.2 MB (37174427 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bcd04ff14b631834196c9368b88009f79ade41d7598dab94156e500cc259646a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 25 Nov 2020 22:25:38 GMT
ADD file:6248e4aba6d7654cf97495ddc060cc9d68c5498500fe6ae03a10d955f0cc09b4 in / 
# Wed, 25 Nov 2020 22:25:39 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 25 Nov 2020 22:25:40 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Wed, 25 Nov 2020 22:25:41 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 25 Nov 2020 22:25:42 GMT
CMD ["/bin/bash"]
# Tue, 22 Dec 2020 22:25:30 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Tue, 22 Dec 2020 22:25:31 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Tue, 22 Dec 2020 22:25:32 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian groovy main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel groovy main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Tue, 22 Dec 2020 22:25:37 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Tue, 22 Dec 2020 22:25:42 GMT
RUN sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list; grep -q 'deb .* multiverse$' /etc/apt/sources.list || sed -i -e 's,universe *$,universe multiverse,g' /etc/apt/sources.list
```

-	Layers:
	-	`sha256:d8b994c442864dd519627740d3a4d134f385a2caa54b7f59bf9d372adcf7def0`  
		Last Modified: Wed, 25 Nov 2020 22:26:56 GMT  
		Size: 31.3 MB (31340118 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0773f3f14174f9bc8047861c64c2aa0cc581e73b16b48194a2884ad3918d01b`  
		Last Modified: Wed, 25 Nov 2020 22:26:50 GMT  
		Size: 847.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b20aefff2dc282ec6e2f496acce5b228bd1dfc30057a8ed41eae0513191b312`  
		Last Modified: Wed, 25 Nov 2020 22:26:50 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:639903bcac214566aebdaeb8513061996afad493070beb9504839f6908f5168a`  
		Last Modified: Tue, 22 Dec 2020 22:26:54 GMT  
		Size: 5.6 MB (5577397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17d4893825aa5203f3874bc7f215b9056618d765a6c5cb95a2322c8edd35cae8`  
		Last Modified: Tue, 22 Dec 2020 22:26:53 GMT  
		Size: 1.8 KB (1764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4965dd26526b8cac69077cb0bc04d51d5d7a08cc67bbd3394bcbd9914f13d87`  
		Last Modified: Tue, 22 Dec 2020 22:26:53 GMT  
		Size: 250.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1a6840143a335ce08e805745418d5a6c1fb2aaf56a7f3e31e3080635a6d0c94`  
		Last Modified: Tue, 22 Dec 2020 22:26:53 GMT  
		Size: 253.6 KB (253630 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a0b390e79b834f01b99f5a077eb8e8ae64b3983db28e1fa496ba42812e3d417`  
		Last Modified: Tue, 22 Dec 2020 22:26:58 GMT  
		Size: 259.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:nd90`

```console
$ docker pull neurodebian@sha256:b4a7991299d24b2cde0bf1d75dba13f912b4fef9512274eaa80ac45adac33fd5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `neurodebian:nd90` - linux; amd64

```console
$ docker pull neurodebian@sha256:51fc1f73dc9855c9678e90cc782e49a592e10666cc50511ecbd33a1faea92738
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.2 MB (52242003 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:889a5c29d5d1661806072af3b3d268f4202e23133c705a20951dd3ae1a11e848`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 11 Dec 2020 02:08:43 GMT
ADD file:c3a852d22b3aac160ba028af69d56b491a2a9419f32a459c4b9b2cbd9129c004 in / 
# Fri, 11 Dec 2020 02:08:43 GMT
CMD ["bash"]
# Fri, 11 Dec 2020 17:12:27 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Fri, 11 Dec 2020 17:12:30 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Fri, 11 Dec 2020 17:12:31 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian stretch main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel stretch main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Fri, 11 Dec 2020 17:12:35 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:22f9b9782fc328ea8192a309b7517c33b1c786697804153ed52a03005919f659`  
		Last Modified: Fri, 11 Dec 2020 02:15:19 GMT  
		Size: 45.4 MB (45377606 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac6153b9908ddb81584cd82100f9820fd5776de9a2f6eecf3db92c8d87ba6275`  
		Last Modified: Fri, 11 Dec 2020 17:14:58 GMT  
		Size: 6.6 MB (6568887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ede09df97d3fdd31fa406d0f493fd97a0133549433df75de6019255fe65f268b`  
		Last Modified: Fri, 11 Dec 2020 17:14:57 GMT  
		Size: 3.1 KB (3149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2dfc2078fc7931a0a6e61bb82ed841e6bbcdc5b77c709958a2379546d5d8ee9a`  
		Last Modified: Fri, 11 Dec 2020 17:14:58 GMT  
		Size: 242.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b937354e0832143c74a23955ff6ac45f53e69a323c7c5bf5eb37a2a02520b21`  
		Last Modified: Fri, 11 Dec 2020 17:14:58 GMT  
		Size: 292.1 KB (292119 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:nd90-non-free`

```console
$ docker pull neurodebian@sha256:2cf0deca9ea504c2206e63ffeb2312d7edc509e8bb2a7cd582d28e94c64c9d3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `neurodebian:nd90-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:fdd83a6f5ef34f31485f0e396dd1942c3a5d82f5721c448231dcc767807176e7
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.2 MB (52242371 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7fe35165902a9928d2c3766b24ead0d17e650486d0a5e7c891c7d2c4869a423a`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 11 Dec 2020 02:08:43 GMT
ADD file:c3a852d22b3aac160ba028af69d56b491a2a9419f32a459c4b9b2cbd9129c004 in / 
# Fri, 11 Dec 2020 02:08:43 GMT
CMD ["bash"]
# Fri, 11 Dec 2020 17:12:27 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Fri, 11 Dec 2020 17:12:30 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Fri, 11 Dec 2020 17:12:31 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian stretch main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel stretch main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Fri, 11 Dec 2020 17:12:35 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Fri, 11 Dec 2020 17:12:40 GMT
RUN sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list /etc/apt/sources.list
```

-	Layers:
	-	`sha256:22f9b9782fc328ea8192a309b7517c33b1c786697804153ed52a03005919f659`  
		Last Modified: Fri, 11 Dec 2020 02:15:19 GMT  
		Size: 45.4 MB (45377606 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac6153b9908ddb81584cd82100f9820fd5776de9a2f6eecf3db92c8d87ba6275`  
		Last Modified: Fri, 11 Dec 2020 17:14:58 GMT  
		Size: 6.6 MB (6568887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ede09df97d3fdd31fa406d0f493fd97a0133549433df75de6019255fe65f268b`  
		Last Modified: Fri, 11 Dec 2020 17:14:57 GMT  
		Size: 3.1 KB (3149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2dfc2078fc7931a0a6e61bb82ed841e6bbcdc5b77c709958a2379546d5d8ee9a`  
		Last Modified: Fri, 11 Dec 2020 17:14:58 GMT  
		Size: 242.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b937354e0832143c74a23955ff6ac45f53e69a323c7c5bf5eb37a2a02520b21`  
		Last Modified: Fri, 11 Dec 2020 17:14:58 GMT  
		Size: 292.1 KB (292119 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fabc3457747b85e85449126789d8fba257dd134e2e3d36aedc0dac257e9d1d52`  
		Last Modified: Fri, 11 Dec 2020 17:15:04 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:nd-non-free`

```console
$ docker pull neurodebian@sha256:8d214312634469d3a1602f55927569503911cd14a4af62cc958ad292c173f061
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `neurodebian:nd-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:b7aa4b170ef3e073a51f9cd2a8d17924dd565b1c81159bc2cf96727755e89833
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.7 MB (64721364 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84c86ab88ea51ed31d376d90f7950a62b4c5766a025214de6988787cde4991f7`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 11 Dec 2020 02:07:48 GMT
ADD file:51a85ad79ebd7e288cd0ea14cd2ae41990aab2d77352f801f09c3a4682cb83a9 in / 
# Fri, 11 Dec 2020 02:07:48 GMT
CMD ["bash"]
# Fri, 11 Dec 2020 17:13:39 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Fri, 11 Dec 2020 17:13:41 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Fri, 11 Dec 2020 17:13:42 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian sid main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Fri, 11 Dec 2020 17:13:46 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Fri, 11 Dec 2020 17:13:51 GMT
RUN sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list /etc/apt/sources.list
```

-	Layers:
	-	`sha256:ff8cddfd21234a3c42ee0af471b251a807aa29af4ca00392976a17d3257ed269`  
		Last Modified: Fri, 11 Dec 2020 02:14:23 GMT  
		Size: 53.4 MB (53352668 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce2727b136c25fc091264e7b123438827cbf21b009f9c493bff195b43fe11862`  
		Last Modified: Fri, 11 Dec 2020 17:15:35 GMT  
		Size: 11.1 MB (11067345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:617bbba7816c68b01e9737f10ce63810794331e00f9e16660ca78aff616e7e68`  
		Last Modified: Fri, 11 Dec 2020 17:15:34 GMT  
		Size: 1.8 KB (1760 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:464c117400d03f730f7dea39e3cde59a514a4eeafcc63ccb72b29be814d3a56d`  
		Last Modified: Fri, 11 Dec 2020 17:15:34 GMT  
		Size: 240.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d3c7e0b6f6db759c0c88baa1dcf7186643ebb6da7f6508424e17ec4886daad3`  
		Last Modified: Fri, 11 Dec 2020 17:15:34 GMT  
		Size: 299.0 KB (299032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7cd34a181394b52b86cdf41bae92e6d92fb4ff7dae7df8f3813cad02804ad8c`  
		Last Modified: Fri, 11 Dec 2020 17:15:41 GMT  
		Size: 319.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:non-free`

```console
$ docker pull neurodebian@sha256:13a3ae717588d73d1d91a3f997209fc927701801068aa69c46d26eef457f3939
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `neurodebian:non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:917edfa4143b97d15a361baca32e01405cf22c3c2e1e6b2dc8d0c196fa9b775b
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.2 MB (61200549 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4005d67eed11091e26c769248175261693ae56fd9d3d6bbeb40ba2965eafb7c3`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 11 Dec 2020 02:05:52 GMT
ADD file:6014cd9d7466825f80d4a3345847efd6fd7ef600b8135811cab4f0e304f66cd7 in / 
# Fri, 11 Dec 2020 02:05:52 GMT
CMD ["bash"]
# Fri, 11 Dec 2020 17:12:52 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Fri, 11 Dec 2020 17:12:53 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Fri, 11 Dec 2020 17:12:54 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian buster main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel buster main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Fri, 11 Dec 2020 17:12:58 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Fri, 11 Dec 2020 17:13:04 GMT
RUN sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list /etc/apt/sources.list
```

-	Layers:
	-	`sha256:6c33745f49b41daad28b7b192c447938452ea4de9fe8c7cc3edf1433b1366946`  
		Last Modified: Fri, 11 Dec 2020 02:12:07 GMT  
		Size: 50.4 MB (50397728 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6c66699048e52432819f9112d0e4b7f96214e221978455d6b0b03b0da33342e`  
		Last Modified: Fri, 11 Dec 2020 17:15:11 GMT  
		Size: 10.5 MB (10497948 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0303af6cf2347aeb70ef9a23a7c4be666d35d14fddf1c2d81790bb35f8ac4a25`  
		Last Modified: Fri, 11 Dec 2020 17:15:10 GMT  
		Size: 1.8 KB (1757 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:726d52d9a1e530d78590b2b3bfe3bf0b22d178caa9a5b2618823d4840fbebe41`  
		Last Modified: Fri, 11 Dec 2020 17:15:10 GMT  
		Size: 243.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6b82482aaca0612234b7f4945ef4c4804eadc900afcbd5b30589006f175de3e`  
		Last Modified: Fri, 11 Dec 2020 17:15:10 GMT  
		Size: 302.5 KB (302504 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00739c9533012cde6c9d655074328bc2cc018efbc85e2a3bc98cda4048d7fe8a`  
		Last Modified: Fri, 11 Dec 2020 17:15:17 GMT  
		Size: 369.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:sid`

```console
$ docker pull neurodebian@sha256:487e0fda83dfc290539e7c4fb2aced9b79a524a3eb9caef7590894428e9501be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `neurodebian:sid` - linux; amd64

```console
$ docker pull neurodebian@sha256:3736fc73e61c4ce1544861d40c347db86bd5629db51c42d6a96d1ac4b3ee957b
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.7 MB (64721045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aedcb6385286c612e36654ae662593eceeae4eac97b3328ba9b1b03426278252`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 11 Dec 2020 02:07:48 GMT
ADD file:51a85ad79ebd7e288cd0ea14cd2ae41990aab2d77352f801f09c3a4682cb83a9 in / 
# Fri, 11 Dec 2020 02:07:48 GMT
CMD ["bash"]
# Fri, 11 Dec 2020 17:13:39 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Fri, 11 Dec 2020 17:13:41 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Fri, 11 Dec 2020 17:13:42 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian sid main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Fri, 11 Dec 2020 17:13:46 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:ff8cddfd21234a3c42ee0af471b251a807aa29af4ca00392976a17d3257ed269`  
		Last Modified: Fri, 11 Dec 2020 02:14:23 GMT  
		Size: 53.4 MB (53352668 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce2727b136c25fc091264e7b123438827cbf21b009f9c493bff195b43fe11862`  
		Last Modified: Fri, 11 Dec 2020 17:15:35 GMT  
		Size: 11.1 MB (11067345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:617bbba7816c68b01e9737f10ce63810794331e00f9e16660ca78aff616e7e68`  
		Last Modified: Fri, 11 Dec 2020 17:15:34 GMT  
		Size: 1.8 KB (1760 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:464c117400d03f730f7dea39e3cde59a514a4eeafcc63ccb72b29be814d3a56d`  
		Last Modified: Fri, 11 Dec 2020 17:15:34 GMT  
		Size: 240.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d3c7e0b6f6db759c0c88baa1dcf7186643ebb6da7f6508424e17ec4886daad3`  
		Last Modified: Fri, 11 Dec 2020 17:15:34 GMT  
		Size: 299.0 KB (299032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:sid-non-free`

```console
$ docker pull neurodebian@sha256:8d214312634469d3a1602f55927569503911cd14a4af62cc958ad292c173f061
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `neurodebian:sid-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:b7aa4b170ef3e073a51f9cd2a8d17924dd565b1c81159bc2cf96727755e89833
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.7 MB (64721364 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84c86ab88ea51ed31d376d90f7950a62b4c5766a025214de6988787cde4991f7`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 11 Dec 2020 02:07:48 GMT
ADD file:51a85ad79ebd7e288cd0ea14cd2ae41990aab2d77352f801f09c3a4682cb83a9 in / 
# Fri, 11 Dec 2020 02:07:48 GMT
CMD ["bash"]
# Fri, 11 Dec 2020 17:13:39 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Fri, 11 Dec 2020 17:13:41 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Fri, 11 Dec 2020 17:13:42 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian sid main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Fri, 11 Dec 2020 17:13:46 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Fri, 11 Dec 2020 17:13:51 GMT
RUN sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list /etc/apt/sources.list
```

-	Layers:
	-	`sha256:ff8cddfd21234a3c42ee0af471b251a807aa29af4ca00392976a17d3257ed269`  
		Last Modified: Fri, 11 Dec 2020 02:14:23 GMT  
		Size: 53.4 MB (53352668 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce2727b136c25fc091264e7b123438827cbf21b009f9c493bff195b43fe11862`  
		Last Modified: Fri, 11 Dec 2020 17:15:35 GMT  
		Size: 11.1 MB (11067345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:617bbba7816c68b01e9737f10ce63810794331e00f9e16660ca78aff616e7e68`  
		Last Modified: Fri, 11 Dec 2020 17:15:34 GMT  
		Size: 1.8 KB (1760 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:464c117400d03f730f7dea39e3cde59a514a4eeafcc63ccb72b29be814d3a56d`  
		Last Modified: Fri, 11 Dec 2020 17:15:34 GMT  
		Size: 240.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d3c7e0b6f6db759c0c88baa1dcf7186643ebb6da7f6508424e17ec4886daad3`  
		Last Modified: Fri, 11 Dec 2020 17:15:34 GMT  
		Size: 299.0 KB (299032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7cd34a181394b52b86cdf41bae92e6d92fb4ff7dae7df8f3813cad02804ad8c`  
		Last Modified: Fri, 11 Dec 2020 17:15:41 GMT  
		Size: 319.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:stretch`

```console
$ docker pull neurodebian@sha256:b4a7991299d24b2cde0bf1d75dba13f912b4fef9512274eaa80ac45adac33fd5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `neurodebian:stretch` - linux; amd64

```console
$ docker pull neurodebian@sha256:51fc1f73dc9855c9678e90cc782e49a592e10666cc50511ecbd33a1faea92738
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.2 MB (52242003 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:889a5c29d5d1661806072af3b3d268f4202e23133c705a20951dd3ae1a11e848`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 11 Dec 2020 02:08:43 GMT
ADD file:c3a852d22b3aac160ba028af69d56b491a2a9419f32a459c4b9b2cbd9129c004 in / 
# Fri, 11 Dec 2020 02:08:43 GMT
CMD ["bash"]
# Fri, 11 Dec 2020 17:12:27 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Fri, 11 Dec 2020 17:12:30 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Fri, 11 Dec 2020 17:12:31 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian stretch main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel stretch main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Fri, 11 Dec 2020 17:12:35 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:22f9b9782fc328ea8192a309b7517c33b1c786697804153ed52a03005919f659`  
		Last Modified: Fri, 11 Dec 2020 02:15:19 GMT  
		Size: 45.4 MB (45377606 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac6153b9908ddb81584cd82100f9820fd5776de9a2f6eecf3db92c8d87ba6275`  
		Last Modified: Fri, 11 Dec 2020 17:14:58 GMT  
		Size: 6.6 MB (6568887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ede09df97d3fdd31fa406d0f493fd97a0133549433df75de6019255fe65f268b`  
		Last Modified: Fri, 11 Dec 2020 17:14:57 GMT  
		Size: 3.1 KB (3149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2dfc2078fc7931a0a6e61bb82ed841e6bbcdc5b77c709958a2379546d5d8ee9a`  
		Last Modified: Fri, 11 Dec 2020 17:14:58 GMT  
		Size: 242.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b937354e0832143c74a23955ff6ac45f53e69a323c7c5bf5eb37a2a02520b21`  
		Last Modified: Fri, 11 Dec 2020 17:14:58 GMT  
		Size: 292.1 KB (292119 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:stretch-non-free`

```console
$ docker pull neurodebian@sha256:2cf0deca9ea504c2206e63ffeb2312d7edc509e8bb2a7cd582d28e94c64c9d3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `neurodebian:stretch-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:fdd83a6f5ef34f31485f0e396dd1942c3a5d82f5721c448231dcc767807176e7
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.2 MB (52242371 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7fe35165902a9928d2c3766b24ead0d17e650486d0a5e7c891c7d2c4869a423a`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 11 Dec 2020 02:08:43 GMT
ADD file:c3a852d22b3aac160ba028af69d56b491a2a9419f32a459c4b9b2cbd9129c004 in / 
# Fri, 11 Dec 2020 02:08:43 GMT
CMD ["bash"]
# Fri, 11 Dec 2020 17:12:27 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Fri, 11 Dec 2020 17:12:30 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Fri, 11 Dec 2020 17:12:31 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian stretch main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel stretch main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Fri, 11 Dec 2020 17:12:35 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Fri, 11 Dec 2020 17:12:40 GMT
RUN sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list /etc/apt/sources.list
```

-	Layers:
	-	`sha256:22f9b9782fc328ea8192a309b7517c33b1c786697804153ed52a03005919f659`  
		Last Modified: Fri, 11 Dec 2020 02:15:19 GMT  
		Size: 45.4 MB (45377606 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac6153b9908ddb81584cd82100f9820fd5776de9a2f6eecf3db92c8d87ba6275`  
		Last Modified: Fri, 11 Dec 2020 17:14:58 GMT  
		Size: 6.6 MB (6568887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ede09df97d3fdd31fa406d0f493fd97a0133549433df75de6019255fe65f268b`  
		Last Modified: Fri, 11 Dec 2020 17:14:57 GMT  
		Size: 3.1 KB (3149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2dfc2078fc7931a0a6e61bb82ed841e6bbcdc5b77c709958a2379546d5d8ee9a`  
		Last Modified: Fri, 11 Dec 2020 17:14:58 GMT  
		Size: 242.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b937354e0832143c74a23955ff6ac45f53e69a323c7c5bf5eb37a2a02520b21`  
		Last Modified: Fri, 11 Dec 2020 17:14:58 GMT  
		Size: 292.1 KB (292119 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fabc3457747b85e85449126789d8fba257dd134e2e3d36aedc0dac257e9d1d52`  
		Last Modified: Fri, 11 Dec 2020 17:15:04 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:xenial`

```console
$ docker pull neurodebian@sha256:99d3daba4215efae715ab91ca51cf69a398861445f0eb0f351dfadc1bf560027
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `neurodebian:xenial` - linux; amd64

```console
$ docker pull neurodebian@sha256:842d6d6b271deb6dc93694e18d7f5c5a49dc720ab92724ae1d58572d4ec7cb0c
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.1 MB (46070191 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad6069c8aac6e1f68e62bc20e9bac247f85a5baa22566458bb637ef3a3b3233e`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 25 Nov 2020 22:26:11 GMT
ADD file:8eef54430e581236e6d529a7d09df648f43c840e889d9ae132e5ed25d7bd2b88 in / 
# Wed, 25 Nov 2020 22:26:12 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 25 Nov 2020 22:26:13 GMT
RUN rm -rf /var/lib/apt/lists/*
# Wed, 25 Nov 2020 22:26:14 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 25 Nov 2020 22:26:14 GMT
CMD ["/bin/bash"]
# Thu, 26 Nov 2020 01:31:45 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Thu, 26 Nov 2020 01:31:46 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Thu, 26 Nov 2020 01:31:47 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian xenial main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel xenial main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Thu, 26 Nov 2020 01:31:53 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:be8ec4e48d7f24a9a1c01063e5dfabb092c2c1ec73e125113848553c9b07eb8c`  
		Last Modified: Sat, 31 Oct 2020 14:20:23 GMT  
		Size: 45.8 MB (45838270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33b8b485aff0509bb0fa67dff6a2aa82e9b7b17e5ef28c1673467ec83edb945d`  
		Last Modified: Wed, 25 Nov 2020 22:27:15 GMT  
		Size: 849.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d887158cc58cbfc3d03cefd5c0b15175fae66ffbf6f28a56180c51cbb5062b8a`  
		Last Modified: Wed, 25 Nov 2020 22:27:14 GMT  
		Size: 533.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05895bb28c18264f614acd13e401b3c5594e12d9fe90d7e52929d3e810e11e97`  
		Last Modified: Wed, 25 Nov 2020 22:27:15 GMT  
		Size: 167.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4a381e547592e23b46523b0dab60f6c4bd467b602f43a16343b5559da0d4686`  
		Last Modified: Thu, 26 Nov 2020 01:33:50 GMT  
		Size: 182.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a7acad501fc13e842de1e4bd4429cd32a570aa3345101ab9113c7965de95ac0`  
		Last Modified: Thu, 26 Nov 2020 01:33:50 GMT  
		Size: 3.2 KB (3152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c20da126479df0535aad7be815dd7f724e0df2ef817ec5aab5542bb981300db4`  
		Last Modified: Thu, 26 Nov 2020 01:33:50 GMT  
		Size: 249.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a01b6c31d56c9536a38779046a52ab23cae4de7b819cdb22047788474cd2d8db`  
		Last Modified: Thu, 26 Nov 2020 01:33:50 GMT  
		Size: 226.8 KB (226789 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:xenial-non-free`

```console
$ docker pull neurodebian@sha256:9c7a17e1ea546d92934acf1d917947ab407c8ca4a8fd8763e23c03bf002e5218
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `neurodebian:xenial-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:d66d5c1d7c22f6b240d56c964e2829a66dceedd2d4cedbbb30b487c8b8148b74
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.1 MB (46070450 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23236a17a48c8328eee81a77511734ab54cfb47397137177d1e6bbcbafbfaa20`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 25 Nov 2020 22:26:11 GMT
ADD file:8eef54430e581236e6d529a7d09df648f43c840e889d9ae132e5ed25d7bd2b88 in / 
# Wed, 25 Nov 2020 22:26:12 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 25 Nov 2020 22:26:13 GMT
RUN rm -rf /var/lib/apt/lists/*
# Wed, 25 Nov 2020 22:26:14 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 25 Nov 2020 22:26:14 GMT
CMD ["/bin/bash"]
# Thu, 26 Nov 2020 01:31:45 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Thu, 26 Nov 2020 01:31:46 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Thu, 26 Nov 2020 01:31:47 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian xenial main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel xenial main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Thu, 26 Nov 2020 01:31:53 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Thu, 26 Nov 2020 01:31:58 GMT
RUN sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list; grep -q 'deb .* multiverse$' /etc/apt/sources.list || sed -i -e 's,universe *$,universe multiverse,g' /etc/apt/sources.list
```

-	Layers:
	-	`sha256:be8ec4e48d7f24a9a1c01063e5dfabb092c2c1ec73e125113848553c9b07eb8c`  
		Last Modified: Sat, 31 Oct 2020 14:20:23 GMT  
		Size: 45.8 MB (45838270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33b8b485aff0509bb0fa67dff6a2aa82e9b7b17e5ef28c1673467ec83edb945d`  
		Last Modified: Wed, 25 Nov 2020 22:27:15 GMT  
		Size: 849.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d887158cc58cbfc3d03cefd5c0b15175fae66ffbf6f28a56180c51cbb5062b8a`  
		Last Modified: Wed, 25 Nov 2020 22:27:14 GMT  
		Size: 533.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05895bb28c18264f614acd13e401b3c5594e12d9fe90d7e52929d3e810e11e97`  
		Last Modified: Wed, 25 Nov 2020 22:27:15 GMT  
		Size: 167.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4a381e547592e23b46523b0dab60f6c4bd467b602f43a16343b5559da0d4686`  
		Last Modified: Thu, 26 Nov 2020 01:33:50 GMT  
		Size: 182.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a7acad501fc13e842de1e4bd4429cd32a570aa3345101ab9113c7965de95ac0`  
		Last Modified: Thu, 26 Nov 2020 01:33:50 GMT  
		Size: 3.2 KB (3152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c20da126479df0535aad7be815dd7f724e0df2ef817ec5aab5542bb981300db4`  
		Last Modified: Thu, 26 Nov 2020 01:33:50 GMT  
		Size: 249.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a01b6c31d56c9536a38779046a52ab23cae4de7b819cdb22047788474cd2d8db`  
		Last Modified: Thu, 26 Nov 2020 01:33:50 GMT  
		Size: 226.8 KB (226789 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08277deecb4c0895f5ee6388a873f54d7c60f1bdcfd4d6019e6ef70cca187718`  
		Last Modified: Thu, 26 Nov 2020 01:33:54 GMT  
		Size: 259.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
