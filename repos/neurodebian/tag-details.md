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
-	[`neurodebian:nd-non-free`](#neurodebiannd-non-free)
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
-	[`neurodebian:non-free`](#neurodebiannon-free)
-	[`neurodebian:sid`](#neurodebiansid)
-	[`neurodebian:sid-non-free`](#neurodebiansid-non-free)
-	[`neurodebian:stretch`](#neurodebianstretch)
-	[`neurodebian:stretch-non-free`](#neurodebianstretch-non-free)
-	[`neurodebian:xenial`](#neurodebianxenial)
-	[`neurodebian:xenial-non-free`](#neurodebianxenial-non-free)

## `neurodebian:bionic`

```console
$ docker pull neurodebian@sha256:0a35b8245472edd88081562c7b7bce8a5cd9b7aa37641d03c5ae647534faa11c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `neurodebian:bionic` - linux; amd64

```console
$ docker pull neurodebian@sha256:f8ae720c75ebf6b8f0cdb65c65413be1f871956f6563081b9950a70c2ed8a37e
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.8 MB (31767497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67e271e2abb7e50bd2c7fff8736b5fb88cc0491f00e030a5264ad87fa230f867`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 25 Mar 2021 22:32:58 GMT
ADD file:e80ae8d359b484dac5346f98c549abc694e1d0c87e1d9753d495aed4d9c8b2b3 in / 
# Thu, 25 Mar 2021 22:32:59 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 25 Mar 2021 22:33:00 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 25 Mar 2021 22:33:01 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 25 Mar 2021 22:33:02 GMT
CMD ["/bin/bash"]
# Fri, 26 Mar 2021 12:09:42 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Fri, 26 Mar 2021 12:09:45 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Fri, 26 Mar 2021 12:09:47 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bionic main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bionic main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Fri, 26 Mar 2021 12:09:57 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:6e0aa5e7af40303f56126b1469d1f37525b3a55a788836a6c9b773f6ce8bc446`  
		Last Modified: Thu, 25 Mar 2021 22:34:24 GMT  
		Size: 26.7 MB (26710781 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d47239a868b3375462d644f2ffb1b20114623fac03109d2950bdf0d57ab487d2`  
		Last Modified: Thu, 25 Mar 2021 22:34:20 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49cbb10cca8504e3dbd65eb5db3c1dd0cd27070154386f819c5936de321c14b1`  
		Last Modified: Thu, 25 Mar 2021 22:34:20 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4970d4a7396b83846b2c10fff27c5d6bd71ffcee89de50834a2515daa86262f`  
		Last Modified: Fri, 26 Mar 2021 12:13:23 GMT  
		Size: 4.8 MB (4812764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4912983ad449bb8b1aaca073802b350bd31faee51a27d116347fd17a7c00d982`  
		Last Modified: Fri, 26 Mar 2021 12:13:22 GMT  
		Size: 3.2 KB (3152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b3201fc2bdd374fed29a81ca8239554e344b58a048daef7041cab1f9d5ccd05`  
		Last Modified: Fri, 26 Mar 2021 12:13:22 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffd04cb91b2f6e79464f13618a76e54a87df86f33b7e27965f81af0cb6bb49de`  
		Last Modified: Fri, 26 Mar 2021 12:13:22 GMT  
		Size: 239.5 KB (239514 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:bionic-non-free`

```console
$ docker pull neurodebian@sha256:d8c6e15da128d439b4825bf36f2b48811038e18a8899b185a8368400347621d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `neurodebian:bionic-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:329d04f39b0a5d37637d1a0a24ce1d83f9787a1dac6d01d5c6d9741353ced245
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.8 MB (31767753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:507cef35077053e0c9e9a73a3190034818ac4744f9393df7b2aa2542cc398d66`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 25 Mar 2021 22:32:58 GMT
ADD file:e80ae8d359b484dac5346f98c549abc694e1d0c87e1d9753d495aed4d9c8b2b3 in / 
# Thu, 25 Mar 2021 22:32:59 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 25 Mar 2021 22:33:00 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 25 Mar 2021 22:33:01 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 25 Mar 2021 22:33:02 GMT
CMD ["/bin/bash"]
# Fri, 26 Mar 2021 12:09:42 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Fri, 26 Mar 2021 12:09:45 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Fri, 26 Mar 2021 12:09:47 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bionic main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bionic main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Fri, 26 Mar 2021 12:09:57 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Fri, 26 Mar 2021 12:10:03 GMT
RUN sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list; grep -q 'deb .* multiverse$' /etc/apt/sources.list || sed -i -e 's,universe *$,universe multiverse,g' /etc/apt/sources.list
```

-	Layers:
	-	`sha256:6e0aa5e7af40303f56126b1469d1f37525b3a55a788836a6c9b773f6ce8bc446`  
		Last Modified: Thu, 25 Mar 2021 22:34:24 GMT  
		Size: 26.7 MB (26710781 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d47239a868b3375462d644f2ffb1b20114623fac03109d2950bdf0d57ab487d2`  
		Last Modified: Thu, 25 Mar 2021 22:34:20 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49cbb10cca8504e3dbd65eb5db3c1dd0cd27070154386f819c5936de321c14b1`  
		Last Modified: Thu, 25 Mar 2021 22:34:20 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4970d4a7396b83846b2c10fff27c5d6bd71ffcee89de50834a2515daa86262f`  
		Last Modified: Fri, 26 Mar 2021 12:13:23 GMT  
		Size: 4.8 MB (4812764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4912983ad449bb8b1aaca073802b350bd31faee51a27d116347fd17a7c00d982`  
		Last Modified: Fri, 26 Mar 2021 12:13:22 GMT  
		Size: 3.2 KB (3152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b3201fc2bdd374fed29a81ca8239554e344b58a048daef7041cab1f9d5ccd05`  
		Last Modified: Fri, 26 Mar 2021 12:13:22 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffd04cb91b2f6e79464f13618a76e54a87df86f33b7e27965f81af0cb6bb49de`  
		Last Modified: Fri, 26 Mar 2021 12:13:22 GMT  
		Size: 239.5 KB (239514 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07707c525f79ec8ebe0387fd457d3c5d2f76c8e44adcdb9de1b82c631529c608`  
		Last Modified: Fri, 26 Mar 2021 12:13:34 GMT  
		Size: 256.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:bullseye`

```console
$ docker pull neurodebian@sha256:c82eb4a0295a6c462d1a6fbfcad669ba6a1781427a03bcda35d1d23f7a113a80
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `neurodebian:bullseye` - linux; amd64

```console
$ docker pull neurodebian@sha256:60436cae9526ecd47b03c3e10bd77ec75e14f59ae0fe2c551bd61b6124fd1095
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.5 MB (66485588 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e9ef797259b3acbdcbb2f69a112f9b186b5839854a8b680548b1d6d58555e67`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 26 Mar 2021 15:20:11 GMT
ADD file:54b23fc0b4b728c85082d50693e314d74e46329004bb55a97f43fea46c497dd2 in / 
# Fri, 26 Mar 2021 15:20:12 GMT
CMD ["bash"]
# Sat, 27 Mar 2021 06:46:38 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Sat, 27 Mar 2021 06:46:39 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Sat, 27 Mar 2021 06:46:41 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bullseye main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Sat, 27 Mar 2021 06:46:45 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:efee637ec1bae521f17fb8d92548c288e3396988c475551b8774c0d08c01c70f`  
		Last Modified: Fri, 26 Mar 2021 15:26:18 GMT  
		Size: 54.9 MB (54867948 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:350cfcb24a0700ecab33841e238931ed0b5ecc0921f08b4bfa88c8cfbfec42ea`  
		Last Modified: Sat, 27 Mar 2021 06:49:14 GMT  
		Size: 11.3 MB (11304981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4fd1b4cb2211ac50cae4086cac774572af0ccb31ab78c3f0d89d27a9ab31c04`  
		Last Modified: Sat, 27 Mar 2021 06:49:12 GMT  
		Size: 1.8 KB (1763 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f60fef2a8c3817d52f22d03e0a7fdb439d4a7259198622db80408b9d698f34b7`  
		Last Modified: Sat, 27 Mar 2021 06:49:13 GMT  
		Size: 248.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4462f910e6970d025db2d16bde1b4f993163e93d24a1499b1e256eb9287afdec`  
		Last Modified: Sat, 27 Mar 2021 06:49:13 GMT  
		Size: 310.6 KB (310648 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:bullseye-non-free`

```console
$ docker pull neurodebian@sha256:becd0ff3c24024c497d97e711d06fd9de9c00f8b66241f3d58056aa93324cb4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `neurodebian:bullseye-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:37011dd5b5412d0d20ef04e41dbab4471a61fa4e8aa2ac0d8f690022949e03e1
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.5 MB (66485955 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24559cbd405e2ffc0e68df9dfcee16c7db5aa17db9a25d697ffb2259148d05ee`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 26 Mar 2021 15:20:11 GMT
ADD file:54b23fc0b4b728c85082d50693e314d74e46329004bb55a97f43fea46c497dd2 in / 
# Fri, 26 Mar 2021 15:20:12 GMT
CMD ["bash"]
# Sat, 27 Mar 2021 06:46:38 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Sat, 27 Mar 2021 06:46:39 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Sat, 27 Mar 2021 06:46:41 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bullseye main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Sat, 27 Mar 2021 06:46:45 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Sat, 27 Mar 2021 06:46:50 GMT
RUN sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list /etc/apt/sources.list
```

-	Layers:
	-	`sha256:efee637ec1bae521f17fb8d92548c288e3396988c475551b8774c0d08c01c70f`  
		Last Modified: Fri, 26 Mar 2021 15:26:18 GMT  
		Size: 54.9 MB (54867948 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:350cfcb24a0700ecab33841e238931ed0b5ecc0921f08b4bfa88c8cfbfec42ea`  
		Last Modified: Sat, 27 Mar 2021 06:49:14 GMT  
		Size: 11.3 MB (11304981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4fd1b4cb2211ac50cae4086cac774572af0ccb31ab78c3f0d89d27a9ab31c04`  
		Last Modified: Sat, 27 Mar 2021 06:49:12 GMT  
		Size: 1.8 KB (1763 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f60fef2a8c3817d52f22d03e0a7fdb439d4a7259198622db80408b9d698f34b7`  
		Last Modified: Sat, 27 Mar 2021 06:49:13 GMT  
		Size: 248.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4462f910e6970d025db2d16bde1b4f993163e93d24a1499b1e256eb9287afdec`  
		Last Modified: Sat, 27 Mar 2021 06:49:13 GMT  
		Size: 310.6 KB (310648 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c8ab3bfecbd23089079ac440e8baa55b82f81a91bfa4c7d4bdd3bd5d6c5a700`  
		Last Modified: Sat, 27 Mar 2021 06:49:25 GMT  
		Size: 367.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:buster`

```console
$ docker pull neurodebian@sha256:a5ff89b97fb67a1d1bf4c3e4a6cf9ae3670db62ca1880a97a88fe2d71d5158bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `neurodebian:buster` - linux; amd64

```console
$ docker pull neurodebian@sha256:e697fe7c19062bcd4bde4c34bbf970f7b43e7e5d1d32a9ea087d659a8caf7477
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.2 MB (61204967 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0dbea0f38d2a9f621a190f3cf9701142fe00d7400d8c11c1490d3439f95a98b8`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 26 Mar 2021 15:20:41 GMT
ADD file:89234bb2f86c7eb890235a48904d1c9898a8d287a525c4fe5698d4a04cdd8f12 in / 
# Fri, 26 Mar 2021 15:20:42 GMT
CMD ["bash"]
# Sat, 27 Mar 2021 06:46:13 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Sat, 27 Mar 2021 06:46:15 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Sat, 27 Mar 2021 06:46:16 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian buster main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel buster main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Sat, 27 Mar 2021 06:46:21 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:8bf9c589d5f9475f1fcc050e02308d6b4eeb86eab7752ef948a13693e81a6aaa`  
		Last Modified: Fri, 26 Mar 2021 15:27:11 GMT  
		Size: 50.4 MB (50400278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:364a64e1f4b60995fac7bd8a65ddcc94f637ced0ed4662fa7d8ffa3ca8947238`  
		Last Modified: Sat, 27 Mar 2021 06:48:44 GMT  
		Size: 10.5 MB (10499932 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0500ee5393cea56c36ff618c71cb990c7f140aec2ca0061e96ac96250bef0e0c`  
		Last Modified: Sat, 27 Mar 2021 06:48:42 GMT  
		Size: 1.8 KB (1763 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64f5bb07b57b9524913e9c7d15292dfd3f125836f353facc7e7934a8dd647db6`  
		Last Modified: Sat, 27 Mar 2021 06:48:42 GMT  
		Size: 243.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a585715510bbe7dc1a5499fbed076b9886c6e83b5b8dca19614ae03984ceec6`  
		Last Modified: Sat, 27 Mar 2021 06:48:42 GMT  
		Size: 302.8 KB (302751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:buster-non-free`

```console
$ docker pull neurodebian@sha256:ca376ab717fc9ca7a9bdb361a6edb6ebcc20426db5f042fd3062df9df5c01a10
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `neurodebian:buster-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:167a22f317623d6cbfb5c56ffae7ad083512ce4a16a338f7752e5c93f2dbe399
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.2 MB (61205332 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd1962dde500ab6b345fd947e1aab221ec5319859b49ae1e0b99ebcd9833b646`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 26 Mar 2021 15:20:41 GMT
ADD file:89234bb2f86c7eb890235a48904d1c9898a8d287a525c4fe5698d4a04cdd8f12 in / 
# Fri, 26 Mar 2021 15:20:42 GMT
CMD ["bash"]
# Sat, 27 Mar 2021 06:46:13 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Sat, 27 Mar 2021 06:46:15 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Sat, 27 Mar 2021 06:46:16 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian buster main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel buster main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Sat, 27 Mar 2021 06:46:21 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Sat, 27 Mar 2021 06:46:27 GMT
RUN sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list /etc/apt/sources.list
```

-	Layers:
	-	`sha256:8bf9c589d5f9475f1fcc050e02308d6b4eeb86eab7752ef948a13693e81a6aaa`  
		Last Modified: Fri, 26 Mar 2021 15:27:11 GMT  
		Size: 50.4 MB (50400278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:364a64e1f4b60995fac7bd8a65ddcc94f637ced0ed4662fa7d8ffa3ca8947238`  
		Last Modified: Sat, 27 Mar 2021 06:48:44 GMT  
		Size: 10.5 MB (10499932 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0500ee5393cea56c36ff618c71cb990c7f140aec2ca0061e96ac96250bef0e0c`  
		Last Modified: Sat, 27 Mar 2021 06:48:42 GMT  
		Size: 1.8 KB (1763 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64f5bb07b57b9524913e9c7d15292dfd3f125836f353facc7e7934a8dd647db6`  
		Last Modified: Sat, 27 Mar 2021 06:48:42 GMT  
		Size: 243.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a585715510bbe7dc1a5499fbed076b9886c6e83b5b8dca19614ae03984ceec6`  
		Last Modified: Sat, 27 Mar 2021 06:48:42 GMT  
		Size: 302.8 KB (302751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:474336b7160442315e21450ba11dc70cd1a99451f34b64e60122100ec3e80ddf`  
		Last Modified: Sat, 27 Mar 2021 06:48:56 GMT  
		Size: 365.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:focal`

```console
$ docker pull neurodebian@sha256:f89a1d739548d9fb9d8436c222089a2d198c02517fe1094e2b644a9683ac03f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `neurodebian:focal` - linux; amd64

```console
$ docker pull neurodebian@sha256:2902dcc33f6d0f3c097fd965f9d8a8006ef4ca178d2ae0687cb32159f9b81c4d
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.3 MB (34299802 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7de42b355c50738b1dbd006dbeba4b909c5c7703ab680e49f5c877874d96738`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 25 Mar 2021 22:33:08 GMT
ADD file:a8d2f02fbaddf8cec8e4da320cd03c06435f395e9d454f69954efe422eb6e1ba in / 
# Thu, 25 Mar 2021 22:33:09 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 25 Mar 2021 22:33:10 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 25 Mar 2021 22:33:11 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 25 Mar 2021 22:33:11 GMT
CMD ["/bin/bash"]
# Fri, 26 Mar 2021 12:10:19 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Fri, 26 Mar 2021 12:10:20 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Fri, 26 Mar 2021 12:10:22 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian focal main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel focal main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Fri, 26 Mar 2021 12:10:26 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:04a5f4cda3eea2313a61a2f72208342a57ea36a9326dff54f4f26ed47d145c7c`  
		Last Modified: Thu, 25 Mar 2021 22:34:46 GMT  
		Size: 28.6 MB (28569428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff496a88c8ed9b745dab2f00bfbd9013c6d1db198442a6a8683998a29a85458a`  
		Last Modified: Thu, 25 Mar 2021 22:34:37 GMT  
		Size: 846.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ce83f459fe7e0bf459d0c222ef3b2ca4d9911f6b0f9aae02c2120561b54ca18`  
		Last Modified: Thu, 25 Mar 2021 22:34:37 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bee7f820a96305ada827738a0d9bb1e8d431c59290f51cc1cb0b7bc03899c66`  
		Last Modified: Fri, 26 Mar 2021 12:13:46 GMT  
		Size: 5.5 MB (5489298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2a7803a8970682225aa3a42e3edb1de754b632f691268919af92243340cdd44`  
		Last Modified: Fri, 26 Mar 2021 12:13:45 GMT  
		Size: 1.8 KB (1763 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04df21c9180a8b40e1d992e773ebaff2360e317a2edfa9071e96374a9129a62a`  
		Last Modified: Fri, 26 Mar 2021 12:13:45 GMT  
		Size: 243.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43d2de458590b00504788c09aed1e67ac4139d8b58cf562a5f8790578ca27273`  
		Last Modified: Fri, 26 Mar 2021 12:13:45 GMT  
		Size: 238.0 KB (238035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:focal-non-free`

```console
$ docker pull neurodebian@sha256:6c518e31030357194ba834b4688c1c6794f5a27388049871f40bdb3860e4410e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `neurodebian:focal-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:aa4136f3a9a91a35b9b0577df29c9585856ff976a4294e90ddc1fd2dba90a41c
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.3 MB (34300057 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b16a883db8ac895cb451edf9a4dc35320debbd2b3106d266b28098e5195e8a5e`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 25 Mar 2021 22:33:08 GMT
ADD file:a8d2f02fbaddf8cec8e4da320cd03c06435f395e9d454f69954efe422eb6e1ba in / 
# Thu, 25 Mar 2021 22:33:09 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 25 Mar 2021 22:33:10 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 25 Mar 2021 22:33:11 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 25 Mar 2021 22:33:11 GMT
CMD ["/bin/bash"]
# Fri, 26 Mar 2021 12:10:19 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Fri, 26 Mar 2021 12:10:20 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Fri, 26 Mar 2021 12:10:22 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian focal main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel focal main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Fri, 26 Mar 2021 12:10:26 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Fri, 26 Mar 2021 12:10:34 GMT
RUN sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list; grep -q 'deb .* multiverse$' /etc/apt/sources.list || sed -i -e 's,universe *$,universe multiverse,g' /etc/apt/sources.list
```

-	Layers:
	-	`sha256:04a5f4cda3eea2313a61a2f72208342a57ea36a9326dff54f4f26ed47d145c7c`  
		Last Modified: Thu, 25 Mar 2021 22:34:46 GMT  
		Size: 28.6 MB (28569428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff496a88c8ed9b745dab2f00bfbd9013c6d1db198442a6a8683998a29a85458a`  
		Last Modified: Thu, 25 Mar 2021 22:34:37 GMT  
		Size: 846.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ce83f459fe7e0bf459d0c222ef3b2ca4d9911f6b0f9aae02c2120561b54ca18`  
		Last Modified: Thu, 25 Mar 2021 22:34:37 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bee7f820a96305ada827738a0d9bb1e8d431c59290f51cc1cb0b7bc03899c66`  
		Last Modified: Fri, 26 Mar 2021 12:13:46 GMT  
		Size: 5.5 MB (5489298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2a7803a8970682225aa3a42e3edb1de754b632f691268919af92243340cdd44`  
		Last Modified: Fri, 26 Mar 2021 12:13:45 GMT  
		Size: 1.8 KB (1763 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04df21c9180a8b40e1d992e773ebaff2360e317a2edfa9071e96374a9129a62a`  
		Last Modified: Fri, 26 Mar 2021 12:13:45 GMT  
		Size: 243.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43d2de458590b00504788c09aed1e67ac4139d8b58cf562a5f8790578ca27273`  
		Last Modified: Fri, 26 Mar 2021 12:13:45 GMT  
		Size: 238.0 KB (238035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c050c67f2ae77329e34ce9637e5cda451deac0cdf810c9103c2035a7b90d4e80`  
		Last Modified: Fri, 26 Mar 2021 12:13:57 GMT  
		Size: 255.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:groovy`

```console
$ docker pull neurodebian@sha256:3df2b6e6c07f68f5134d96f44936168e6be505fb1c9356de475afae3c054a04d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `neurodebian:groovy` - linux; amd64

```console
$ docker pull neurodebian@sha256:1a807c8f49726ef91d5bb172e78f45929c34de68265eb90be3f2a490a1de42c2
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.2 MB (37201415 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65aca515f341f3ac73709711f4289a4b6ce4cc4f0618533f31fc7bc8469a49a9`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 25 Mar 2021 22:33:18 GMT
ADD file:4aba1ec4c6317039d27ed2f8cdda90160c834d979269ba6253f4b8839e6a8c06 in / 
# Thu, 25 Mar 2021 22:33:19 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 25 Mar 2021 22:33:20 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 25 Mar 2021 22:33:21 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 25 Mar 2021 22:33:21 GMT
CMD ["/bin/bash"]
# Fri, 26 Mar 2021 12:11:13 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Fri, 26 Mar 2021 12:11:18 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Fri, 26 Mar 2021 12:11:19 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian groovy main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel groovy main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Fri, 26 Mar 2021 12:11:25 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:67b8b51191f1c23048b4af7390755377b07b7033f43a5bc7a5bcf37f863f7adb`  
		Last Modified: Thu, 25 Mar 2021 22:35:06 GMT  
		Size: 31.3 MB (31348493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bee746ea8f946b8bb5dee1458e4bf97293706926511644fdfd4411b9bac5710`  
		Last Modified: Thu, 25 Mar 2021 22:35:01 GMT  
		Size: 849.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:014d36ded12e82e314bb890faf3e15c110c39688e938f9c8c8ba8ebda5cbcbb7`  
		Last Modified: Thu, 25 Mar 2021 22:35:01 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0164949a4da1051c6005cd738a630f9252eb9fbc824f3bd5f3e2cbbc414b973e`  
		Last Modified: Fri, 26 Mar 2021 12:14:09 GMT  
		Size: 5.6 MB (5595460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f1c7a4f84e8d1a5821e81adf0643c5c424473be6fcde0673b696af0c3e39e4c`  
		Last Modified: Fri, 26 Mar 2021 12:14:08 GMT  
		Size: 1.8 KB (1763 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b979e50699487552db50c9530225510a01e15f7b33780491654cefa9c6a8275`  
		Last Modified: Fri, 26 Mar 2021 12:14:08 GMT  
		Size: 249.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:002e4319932a9d2ff199106cfee0009b10e2eacdff9f054b6c3df24d366115ef`  
		Last Modified: Fri, 26 Mar 2021 12:14:08 GMT  
		Size: 254.4 KB (254412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:groovy-non-free`

```console
$ docker pull neurodebian@sha256:546f3dddf78bd5ac7799f5ece18bd8d1d621d8681450f5daa15034f65cb7391c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `neurodebian:groovy-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:31300d76ebc71bad011d0f3a3c88ae6cb70247ce8091a4785210fbdf82eb5045
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.2 MB (37201673 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:143f76821bb6890cdf0ff70cb8435a172b108c007f6bb8c1b3deb6fa2a567608`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 25 Mar 2021 22:33:18 GMT
ADD file:4aba1ec4c6317039d27ed2f8cdda90160c834d979269ba6253f4b8839e6a8c06 in / 
# Thu, 25 Mar 2021 22:33:19 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 25 Mar 2021 22:33:20 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 25 Mar 2021 22:33:21 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 25 Mar 2021 22:33:21 GMT
CMD ["/bin/bash"]
# Fri, 26 Mar 2021 12:11:13 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Fri, 26 Mar 2021 12:11:18 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Fri, 26 Mar 2021 12:11:19 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian groovy main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel groovy main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Fri, 26 Mar 2021 12:11:25 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Fri, 26 Mar 2021 12:11:31 GMT
RUN sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list; grep -q 'deb .* multiverse$' /etc/apt/sources.list || sed -i -e 's,universe *$,universe multiverse,g' /etc/apt/sources.list
```

-	Layers:
	-	`sha256:67b8b51191f1c23048b4af7390755377b07b7033f43a5bc7a5bcf37f863f7adb`  
		Last Modified: Thu, 25 Mar 2021 22:35:06 GMT  
		Size: 31.3 MB (31348493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bee746ea8f946b8bb5dee1458e4bf97293706926511644fdfd4411b9bac5710`  
		Last Modified: Thu, 25 Mar 2021 22:35:01 GMT  
		Size: 849.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:014d36ded12e82e314bb890faf3e15c110c39688e938f9c8c8ba8ebda5cbcbb7`  
		Last Modified: Thu, 25 Mar 2021 22:35:01 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0164949a4da1051c6005cd738a630f9252eb9fbc824f3bd5f3e2cbbc414b973e`  
		Last Modified: Fri, 26 Mar 2021 12:14:09 GMT  
		Size: 5.6 MB (5595460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f1c7a4f84e8d1a5821e81adf0643c5c424473be6fcde0673b696af0c3e39e4c`  
		Last Modified: Fri, 26 Mar 2021 12:14:08 GMT  
		Size: 1.8 KB (1763 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b979e50699487552db50c9530225510a01e15f7b33780491654cefa9c6a8275`  
		Last Modified: Fri, 26 Mar 2021 12:14:08 GMT  
		Size: 249.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:002e4319932a9d2ff199106cfee0009b10e2eacdff9f054b6c3df24d366115ef`  
		Last Modified: Fri, 26 Mar 2021 12:14:08 GMT  
		Size: 254.4 KB (254412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2394fbebf42105a54df60bbc290a6901749e6760141abe2996234b8680f94d8e`  
		Last Modified: Fri, 26 Mar 2021 12:14:21 GMT  
		Size: 258.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:latest`

```console
$ docker pull neurodebian@sha256:a5ff89b97fb67a1d1bf4c3e4a6cf9ae3670db62ca1880a97a88fe2d71d5158bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `neurodebian:latest` - linux; amd64

```console
$ docker pull neurodebian@sha256:e697fe7c19062bcd4bde4c34bbf970f7b43e7e5d1d32a9ea087d659a8caf7477
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.2 MB (61204967 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0dbea0f38d2a9f621a190f3cf9701142fe00d7400d8c11c1490d3439f95a98b8`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 26 Mar 2021 15:20:41 GMT
ADD file:89234bb2f86c7eb890235a48904d1c9898a8d287a525c4fe5698d4a04cdd8f12 in / 
# Fri, 26 Mar 2021 15:20:42 GMT
CMD ["bash"]
# Sat, 27 Mar 2021 06:46:13 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Sat, 27 Mar 2021 06:46:15 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Sat, 27 Mar 2021 06:46:16 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian buster main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel buster main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Sat, 27 Mar 2021 06:46:21 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:8bf9c589d5f9475f1fcc050e02308d6b4eeb86eab7752ef948a13693e81a6aaa`  
		Last Modified: Fri, 26 Mar 2021 15:27:11 GMT  
		Size: 50.4 MB (50400278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:364a64e1f4b60995fac7bd8a65ddcc94f637ced0ed4662fa7d8ffa3ca8947238`  
		Last Modified: Sat, 27 Mar 2021 06:48:44 GMT  
		Size: 10.5 MB (10499932 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0500ee5393cea56c36ff618c71cb990c7f140aec2ca0061e96ac96250bef0e0c`  
		Last Modified: Sat, 27 Mar 2021 06:48:42 GMT  
		Size: 1.8 KB (1763 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64f5bb07b57b9524913e9c7d15292dfd3f125836f353facc7e7934a8dd647db6`  
		Last Modified: Sat, 27 Mar 2021 06:48:42 GMT  
		Size: 243.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a585715510bbe7dc1a5499fbed076b9886c6e83b5b8dca19614ae03984ceec6`  
		Last Modified: Sat, 27 Mar 2021 06:48:42 GMT  
		Size: 302.8 KB (302751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:nd`

```console
$ docker pull neurodebian@sha256:5ec46d7f26ae63961dd31c66c24980c8d67a2790b2554c2976c3946c501ff408
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `neurodebian:nd` - linux; amd64

```console
$ docker pull neurodebian@sha256:8f1c27c5f380c56971be630eaa17fac9504108e027226c42cfd5720c5068ad6a
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.5 MB (66486538 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:159a3505079e6ec7ccae5c6295ef4ade9339f7e92ef43031933472e7e01797df`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 26 Mar 2021 15:22:32 GMT
ADD file:2077716d4a510c614acac732f9b9130b649ac696764e3becc6e21e732f39e9c6 in / 
# Fri, 26 Mar 2021 15:22:33 GMT
CMD ["bash"]
# Sat, 27 Mar 2021 06:47:00 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Sat, 27 Mar 2021 06:47:02 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Sat, 27 Mar 2021 06:47:03 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian sid main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Sat, 27 Mar 2021 06:47:07 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:e6db1addbc87ce8e502d75dae59834703a516712298c58eaee03f40a399e8292`  
		Last Modified: Fri, 26 Mar 2021 15:30:40 GMT  
		Size: 54.9 MB (54868141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae9eeffb47c540d6fa5caef3fcaa66750050bfd0c116253947d087ecf0ef7a84`  
		Last Modified: Sat, 27 Mar 2021 06:49:37 GMT  
		Size: 11.3 MB (11305751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a02159ef5c0b757456dd3da2955f66136688806aee6cddc4e04a5840918df1e`  
		Last Modified: Sat, 27 Mar 2021 06:49:35 GMT  
		Size: 1.8 KB (1757 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6baa1a0325071f162dcf13db50337fd626e0bbc7daeaba6ca66b3defd7af512`  
		Last Modified: Sat, 27 Mar 2021 06:49:36 GMT  
		Size: 240.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed6b1df463008071e0f80383eef835d97ef56cb9dfb77baf28a22387a68c018c`  
		Last Modified: Sat, 27 Mar 2021 06:49:36 GMT  
		Size: 310.6 KB (310649 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:nd-non-free`

```console
$ docker pull neurodebian@sha256:3631eba6e722b93c9ea8453bfc14205e87a151e4c79c734677ce9c0ca7c6d74a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `neurodebian:nd-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:be3126a5bfa93199db8328bc4e8595b3a501fb5e5f0cd960c9ec08d66fd3818b
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.5 MB (66486857 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ee20d7a1607afa108b40f745dcf9487f1d9fd75208d8db7657d06b166fda500`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 26 Mar 2021 15:22:32 GMT
ADD file:2077716d4a510c614acac732f9b9130b649ac696764e3becc6e21e732f39e9c6 in / 
# Fri, 26 Mar 2021 15:22:33 GMT
CMD ["bash"]
# Sat, 27 Mar 2021 06:47:00 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Sat, 27 Mar 2021 06:47:02 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Sat, 27 Mar 2021 06:47:03 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian sid main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Sat, 27 Mar 2021 06:47:07 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Sat, 27 Mar 2021 06:47:15 GMT
RUN sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list /etc/apt/sources.list
```

-	Layers:
	-	`sha256:e6db1addbc87ce8e502d75dae59834703a516712298c58eaee03f40a399e8292`  
		Last Modified: Fri, 26 Mar 2021 15:30:40 GMT  
		Size: 54.9 MB (54868141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae9eeffb47c540d6fa5caef3fcaa66750050bfd0c116253947d087ecf0ef7a84`  
		Last Modified: Sat, 27 Mar 2021 06:49:37 GMT  
		Size: 11.3 MB (11305751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a02159ef5c0b757456dd3da2955f66136688806aee6cddc4e04a5840918df1e`  
		Last Modified: Sat, 27 Mar 2021 06:49:35 GMT  
		Size: 1.8 KB (1757 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6baa1a0325071f162dcf13db50337fd626e0bbc7daeaba6ca66b3defd7af512`  
		Last Modified: Sat, 27 Mar 2021 06:49:36 GMT  
		Size: 240.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed6b1df463008071e0f80383eef835d97ef56cb9dfb77baf28a22387a68c018c`  
		Last Modified: Sat, 27 Mar 2021 06:49:36 GMT  
		Size: 310.6 KB (310649 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ad000ff0f4e95c054964ef57e7b5b7d13a876f78fe8312cac4b71d21793b8d0`  
		Last Modified: Sat, 27 Mar 2021 06:49:47 GMT  
		Size: 319.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:nd100`

```console
$ docker pull neurodebian@sha256:a5ff89b97fb67a1d1bf4c3e4a6cf9ae3670db62ca1880a97a88fe2d71d5158bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `neurodebian:nd100` - linux; amd64

```console
$ docker pull neurodebian@sha256:e697fe7c19062bcd4bde4c34bbf970f7b43e7e5d1d32a9ea087d659a8caf7477
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.2 MB (61204967 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0dbea0f38d2a9f621a190f3cf9701142fe00d7400d8c11c1490d3439f95a98b8`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 26 Mar 2021 15:20:41 GMT
ADD file:89234bb2f86c7eb890235a48904d1c9898a8d287a525c4fe5698d4a04cdd8f12 in / 
# Fri, 26 Mar 2021 15:20:42 GMT
CMD ["bash"]
# Sat, 27 Mar 2021 06:46:13 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Sat, 27 Mar 2021 06:46:15 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Sat, 27 Mar 2021 06:46:16 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian buster main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel buster main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Sat, 27 Mar 2021 06:46:21 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:8bf9c589d5f9475f1fcc050e02308d6b4eeb86eab7752ef948a13693e81a6aaa`  
		Last Modified: Fri, 26 Mar 2021 15:27:11 GMT  
		Size: 50.4 MB (50400278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:364a64e1f4b60995fac7bd8a65ddcc94f637ced0ed4662fa7d8ffa3ca8947238`  
		Last Modified: Sat, 27 Mar 2021 06:48:44 GMT  
		Size: 10.5 MB (10499932 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0500ee5393cea56c36ff618c71cb990c7f140aec2ca0061e96ac96250bef0e0c`  
		Last Modified: Sat, 27 Mar 2021 06:48:42 GMT  
		Size: 1.8 KB (1763 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64f5bb07b57b9524913e9c7d15292dfd3f125836f353facc7e7934a8dd647db6`  
		Last Modified: Sat, 27 Mar 2021 06:48:42 GMT  
		Size: 243.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a585715510bbe7dc1a5499fbed076b9886c6e83b5b8dca19614ae03984ceec6`  
		Last Modified: Sat, 27 Mar 2021 06:48:42 GMT  
		Size: 302.8 KB (302751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:nd100-non-free`

```console
$ docker pull neurodebian@sha256:ca376ab717fc9ca7a9bdb361a6edb6ebcc20426db5f042fd3062df9df5c01a10
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `neurodebian:nd100-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:167a22f317623d6cbfb5c56ffae7ad083512ce4a16a338f7752e5c93f2dbe399
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.2 MB (61205332 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd1962dde500ab6b345fd947e1aab221ec5319859b49ae1e0b99ebcd9833b646`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 26 Mar 2021 15:20:41 GMT
ADD file:89234bb2f86c7eb890235a48904d1c9898a8d287a525c4fe5698d4a04cdd8f12 in / 
# Fri, 26 Mar 2021 15:20:42 GMT
CMD ["bash"]
# Sat, 27 Mar 2021 06:46:13 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Sat, 27 Mar 2021 06:46:15 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Sat, 27 Mar 2021 06:46:16 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian buster main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel buster main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Sat, 27 Mar 2021 06:46:21 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Sat, 27 Mar 2021 06:46:27 GMT
RUN sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list /etc/apt/sources.list
```

-	Layers:
	-	`sha256:8bf9c589d5f9475f1fcc050e02308d6b4eeb86eab7752ef948a13693e81a6aaa`  
		Last Modified: Fri, 26 Mar 2021 15:27:11 GMT  
		Size: 50.4 MB (50400278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:364a64e1f4b60995fac7bd8a65ddcc94f637ced0ed4662fa7d8ffa3ca8947238`  
		Last Modified: Sat, 27 Mar 2021 06:48:44 GMT  
		Size: 10.5 MB (10499932 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0500ee5393cea56c36ff618c71cb990c7f140aec2ca0061e96ac96250bef0e0c`  
		Last Modified: Sat, 27 Mar 2021 06:48:42 GMT  
		Size: 1.8 KB (1763 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64f5bb07b57b9524913e9c7d15292dfd3f125836f353facc7e7934a8dd647db6`  
		Last Modified: Sat, 27 Mar 2021 06:48:42 GMT  
		Size: 243.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a585715510bbe7dc1a5499fbed076b9886c6e83b5b8dca19614ae03984ceec6`  
		Last Modified: Sat, 27 Mar 2021 06:48:42 GMT  
		Size: 302.8 KB (302751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:474336b7160442315e21450ba11dc70cd1a99451f34b64e60122100ec3e80ddf`  
		Last Modified: Sat, 27 Mar 2021 06:48:56 GMT  
		Size: 365.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:nd110`

```console
$ docker pull neurodebian@sha256:c82eb4a0295a6c462d1a6fbfcad669ba6a1781427a03bcda35d1d23f7a113a80
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `neurodebian:nd110` - linux; amd64

```console
$ docker pull neurodebian@sha256:60436cae9526ecd47b03c3e10bd77ec75e14f59ae0fe2c551bd61b6124fd1095
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.5 MB (66485588 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e9ef797259b3acbdcbb2f69a112f9b186b5839854a8b680548b1d6d58555e67`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 26 Mar 2021 15:20:11 GMT
ADD file:54b23fc0b4b728c85082d50693e314d74e46329004bb55a97f43fea46c497dd2 in / 
# Fri, 26 Mar 2021 15:20:12 GMT
CMD ["bash"]
# Sat, 27 Mar 2021 06:46:38 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Sat, 27 Mar 2021 06:46:39 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Sat, 27 Mar 2021 06:46:41 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bullseye main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Sat, 27 Mar 2021 06:46:45 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:efee637ec1bae521f17fb8d92548c288e3396988c475551b8774c0d08c01c70f`  
		Last Modified: Fri, 26 Mar 2021 15:26:18 GMT  
		Size: 54.9 MB (54867948 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:350cfcb24a0700ecab33841e238931ed0b5ecc0921f08b4bfa88c8cfbfec42ea`  
		Last Modified: Sat, 27 Mar 2021 06:49:14 GMT  
		Size: 11.3 MB (11304981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4fd1b4cb2211ac50cae4086cac774572af0ccb31ab78c3f0d89d27a9ab31c04`  
		Last Modified: Sat, 27 Mar 2021 06:49:12 GMT  
		Size: 1.8 KB (1763 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f60fef2a8c3817d52f22d03e0a7fdb439d4a7259198622db80408b9d698f34b7`  
		Last Modified: Sat, 27 Mar 2021 06:49:13 GMT  
		Size: 248.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4462f910e6970d025db2d16bde1b4f993163e93d24a1499b1e256eb9287afdec`  
		Last Modified: Sat, 27 Mar 2021 06:49:13 GMT  
		Size: 310.6 KB (310648 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:nd110-non-free`

```console
$ docker pull neurodebian@sha256:becd0ff3c24024c497d97e711d06fd9de9c00f8b66241f3d58056aa93324cb4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `neurodebian:nd110-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:37011dd5b5412d0d20ef04e41dbab4471a61fa4e8aa2ac0d8f690022949e03e1
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.5 MB (66485955 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24559cbd405e2ffc0e68df9dfcee16c7db5aa17db9a25d697ffb2259148d05ee`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 26 Mar 2021 15:20:11 GMT
ADD file:54b23fc0b4b728c85082d50693e314d74e46329004bb55a97f43fea46c497dd2 in / 
# Fri, 26 Mar 2021 15:20:12 GMT
CMD ["bash"]
# Sat, 27 Mar 2021 06:46:38 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Sat, 27 Mar 2021 06:46:39 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Sat, 27 Mar 2021 06:46:41 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bullseye main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Sat, 27 Mar 2021 06:46:45 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Sat, 27 Mar 2021 06:46:50 GMT
RUN sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list /etc/apt/sources.list
```

-	Layers:
	-	`sha256:efee637ec1bae521f17fb8d92548c288e3396988c475551b8774c0d08c01c70f`  
		Last Modified: Fri, 26 Mar 2021 15:26:18 GMT  
		Size: 54.9 MB (54867948 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:350cfcb24a0700ecab33841e238931ed0b5ecc0921f08b4bfa88c8cfbfec42ea`  
		Last Modified: Sat, 27 Mar 2021 06:49:14 GMT  
		Size: 11.3 MB (11304981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4fd1b4cb2211ac50cae4086cac774572af0ccb31ab78c3f0d89d27a9ab31c04`  
		Last Modified: Sat, 27 Mar 2021 06:49:12 GMT  
		Size: 1.8 KB (1763 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f60fef2a8c3817d52f22d03e0a7fdb439d4a7259198622db80408b9d698f34b7`  
		Last Modified: Sat, 27 Mar 2021 06:49:13 GMT  
		Size: 248.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4462f910e6970d025db2d16bde1b4f993163e93d24a1499b1e256eb9287afdec`  
		Last Modified: Sat, 27 Mar 2021 06:49:13 GMT  
		Size: 310.6 KB (310648 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c8ab3bfecbd23089079ac440e8baa55b82f81a91bfa4c7d4bdd3bd5d6c5a700`  
		Last Modified: Sat, 27 Mar 2021 06:49:25 GMT  
		Size: 367.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:nd16.04`

```console
$ docker pull neurodebian@sha256:8cbbcb2e27d56711ac78a442bd4ef3011dad185c3705859f4a7fb9445911598a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `neurodebian:nd16.04` - linux; amd64

```console
$ docker pull neurodebian@sha256:ee42f8053bf30a97dabd06fe7a679675506f87376b833c4d064658c776a4812e
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.2 MB (46194559 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f70324aa866fcefbb63c8fa890a1aeeea467a106b52d15894a4cf712468c37d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 25 Mar 2021 22:33:52 GMT
ADD file:925571658dd8453e5c80d862f5791d6b26b3c2a8688937b11741f2f2c5cdbfd7 in / 
# Thu, 25 Mar 2021 22:33:53 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 25 Mar 2021 22:33:54 GMT
RUN rm -rf /var/lib/apt/lists/*
# Thu, 25 Mar 2021 22:33:55 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 25 Mar 2021 22:33:55 GMT
CMD ["/bin/bash"]
# Fri, 26 Mar 2021 12:09:05 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Fri, 26 Mar 2021 12:09:08 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Fri, 26 Mar 2021 12:09:10 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian xenial main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel xenial main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Fri, 26 Mar 2021 12:09:19 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:4007a89234b4f56c03e6831dc220550d2e5fba935d9f5f5bcea64857ac4f4888`  
		Last Modified: Mon, 18 Jan 2021 19:38:08 GMT  
		Size: 46.0 MB (45962352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1de0f9cdfc1f9f595acd2ea8724ea92a509d64a6936f0e645c65b504e7e4bc6`  
		Last Modified: Thu, 25 Mar 2021 22:36:02 GMT  
		Size: 846.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8ee6ca703b866ac2b74b6129d2db331936292f899e8e3a794474fdf81343605`  
		Last Modified: Thu, 25 Mar 2021 22:36:02 GMT  
		Size: 526.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b39e2761d3d4971e78914857af4c6bd9989873b53426cf2fef3e76983b166fa2`  
		Last Modified: Thu, 25 Mar 2021 22:36:02 GMT  
		Size: 168.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:246e2fbfdb5416c63dcf63f4b1ff87529e9c95869c626b834447830f42a27e76`  
		Last Modified: Fri, 26 Mar 2021 12:12:57 GMT  
		Size: 177.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbfba0ba677947687db6fc0d522806505ac13da985638232b97294a05298a07f`  
		Last Modified: Fri, 26 Mar 2021 12:12:57 GMT  
		Size: 3.2 KB (3151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52429283d5b479729c1eb2900697631aa16136b78c0b9632fa39a9039136312b`  
		Last Modified: Fri, 26 Mar 2021 12:12:57 GMT  
		Size: 250.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bb0f6fc0209667118bfb6a71d36023a43b33bb6596e2f34c29691e66669b0db`  
		Last Modified: Fri, 26 Mar 2021 12:12:57 GMT  
		Size: 227.1 KB (227089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:nd16.04-non-free`

```console
$ docker pull neurodebian@sha256:a3275da187b67cc7bdac5c4dc16935e6f6e4d9ec3b7a5a12f3f49fe7c8b33078
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `neurodebian:nd16.04-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:ac30151d25adebbb903b0db493cc193ac41d7c03f19fccb1fb0a1f292dcba470
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.2 MB (46194817 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:905eaec96ee02d5a98dcd61a928b33e6a93935ff8d2d96341e12467fa560c644`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 25 Mar 2021 22:33:52 GMT
ADD file:925571658dd8453e5c80d862f5791d6b26b3c2a8688937b11741f2f2c5cdbfd7 in / 
# Thu, 25 Mar 2021 22:33:53 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 25 Mar 2021 22:33:54 GMT
RUN rm -rf /var/lib/apt/lists/*
# Thu, 25 Mar 2021 22:33:55 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 25 Mar 2021 22:33:55 GMT
CMD ["/bin/bash"]
# Fri, 26 Mar 2021 12:09:05 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Fri, 26 Mar 2021 12:09:08 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Fri, 26 Mar 2021 12:09:10 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian xenial main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel xenial main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Fri, 26 Mar 2021 12:09:19 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Fri, 26 Mar 2021 12:09:26 GMT
RUN sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list; grep -q 'deb .* multiverse$' /etc/apt/sources.list || sed -i -e 's,universe *$,universe multiverse,g' /etc/apt/sources.list
```

-	Layers:
	-	`sha256:4007a89234b4f56c03e6831dc220550d2e5fba935d9f5f5bcea64857ac4f4888`  
		Last Modified: Mon, 18 Jan 2021 19:38:08 GMT  
		Size: 46.0 MB (45962352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1de0f9cdfc1f9f595acd2ea8724ea92a509d64a6936f0e645c65b504e7e4bc6`  
		Last Modified: Thu, 25 Mar 2021 22:36:02 GMT  
		Size: 846.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8ee6ca703b866ac2b74b6129d2db331936292f899e8e3a794474fdf81343605`  
		Last Modified: Thu, 25 Mar 2021 22:36:02 GMT  
		Size: 526.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b39e2761d3d4971e78914857af4c6bd9989873b53426cf2fef3e76983b166fa2`  
		Last Modified: Thu, 25 Mar 2021 22:36:02 GMT  
		Size: 168.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:246e2fbfdb5416c63dcf63f4b1ff87529e9c95869c626b834447830f42a27e76`  
		Last Modified: Fri, 26 Mar 2021 12:12:57 GMT  
		Size: 177.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbfba0ba677947687db6fc0d522806505ac13da985638232b97294a05298a07f`  
		Last Modified: Fri, 26 Mar 2021 12:12:57 GMT  
		Size: 3.2 KB (3151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52429283d5b479729c1eb2900697631aa16136b78c0b9632fa39a9039136312b`  
		Last Modified: Fri, 26 Mar 2021 12:12:57 GMT  
		Size: 250.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bb0f6fc0209667118bfb6a71d36023a43b33bb6596e2f34c29691e66669b0db`  
		Last Modified: Fri, 26 Mar 2021 12:12:57 GMT  
		Size: 227.1 KB (227089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3763a04ce6f958325f23ee4cf4cadbaea201e6a0dfde5762a750f3e1355b735`  
		Last Modified: Fri, 26 Mar 2021 12:13:08 GMT  
		Size: 258.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:nd18.04`

```console
$ docker pull neurodebian@sha256:0a35b8245472edd88081562c7b7bce8a5cd9b7aa37641d03c5ae647534faa11c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `neurodebian:nd18.04` - linux; amd64

```console
$ docker pull neurodebian@sha256:f8ae720c75ebf6b8f0cdb65c65413be1f871956f6563081b9950a70c2ed8a37e
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.8 MB (31767497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67e271e2abb7e50bd2c7fff8736b5fb88cc0491f00e030a5264ad87fa230f867`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 25 Mar 2021 22:32:58 GMT
ADD file:e80ae8d359b484dac5346f98c549abc694e1d0c87e1d9753d495aed4d9c8b2b3 in / 
# Thu, 25 Mar 2021 22:32:59 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 25 Mar 2021 22:33:00 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 25 Mar 2021 22:33:01 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 25 Mar 2021 22:33:02 GMT
CMD ["/bin/bash"]
# Fri, 26 Mar 2021 12:09:42 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Fri, 26 Mar 2021 12:09:45 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Fri, 26 Mar 2021 12:09:47 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bionic main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bionic main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Fri, 26 Mar 2021 12:09:57 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:6e0aa5e7af40303f56126b1469d1f37525b3a55a788836a6c9b773f6ce8bc446`  
		Last Modified: Thu, 25 Mar 2021 22:34:24 GMT  
		Size: 26.7 MB (26710781 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d47239a868b3375462d644f2ffb1b20114623fac03109d2950bdf0d57ab487d2`  
		Last Modified: Thu, 25 Mar 2021 22:34:20 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49cbb10cca8504e3dbd65eb5db3c1dd0cd27070154386f819c5936de321c14b1`  
		Last Modified: Thu, 25 Mar 2021 22:34:20 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4970d4a7396b83846b2c10fff27c5d6bd71ffcee89de50834a2515daa86262f`  
		Last Modified: Fri, 26 Mar 2021 12:13:23 GMT  
		Size: 4.8 MB (4812764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4912983ad449bb8b1aaca073802b350bd31faee51a27d116347fd17a7c00d982`  
		Last Modified: Fri, 26 Mar 2021 12:13:22 GMT  
		Size: 3.2 KB (3152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b3201fc2bdd374fed29a81ca8239554e344b58a048daef7041cab1f9d5ccd05`  
		Last Modified: Fri, 26 Mar 2021 12:13:22 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffd04cb91b2f6e79464f13618a76e54a87df86f33b7e27965f81af0cb6bb49de`  
		Last Modified: Fri, 26 Mar 2021 12:13:22 GMT  
		Size: 239.5 KB (239514 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:nd18.04-non-free`

```console
$ docker pull neurodebian@sha256:d8c6e15da128d439b4825bf36f2b48811038e18a8899b185a8368400347621d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `neurodebian:nd18.04-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:329d04f39b0a5d37637d1a0a24ce1d83f9787a1dac6d01d5c6d9741353ced245
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.8 MB (31767753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:507cef35077053e0c9e9a73a3190034818ac4744f9393df7b2aa2542cc398d66`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 25 Mar 2021 22:32:58 GMT
ADD file:e80ae8d359b484dac5346f98c549abc694e1d0c87e1d9753d495aed4d9c8b2b3 in / 
# Thu, 25 Mar 2021 22:32:59 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 25 Mar 2021 22:33:00 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 25 Mar 2021 22:33:01 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 25 Mar 2021 22:33:02 GMT
CMD ["/bin/bash"]
# Fri, 26 Mar 2021 12:09:42 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Fri, 26 Mar 2021 12:09:45 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Fri, 26 Mar 2021 12:09:47 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bionic main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bionic main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Fri, 26 Mar 2021 12:09:57 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Fri, 26 Mar 2021 12:10:03 GMT
RUN sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list; grep -q 'deb .* multiverse$' /etc/apt/sources.list || sed -i -e 's,universe *$,universe multiverse,g' /etc/apt/sources.list
```

-	Layers:
	-	`sha256:6e0aa5e7af40303f56126b1469d1f37525b3a55a788836a6c9b773f6ce8bc446`  
		Last Modified: Thu, 25 Mar 2021 22:34:24 GMT  
		Size: 26.7 MB (26710781 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d47239a868b3375462d644f2ffb1b20114623fac03109d2950bdf0d57ab487d2`  
		Last Modified: Thu, 25 Mar 2021 22:34:20 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49cbb10cca8504e3dbd65eb5db3c1dd0cd27070154386f819c5936de321c14b1`  
		Last Modified: Thu, 25 Mar 2021 22:34:20 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4970d4a7396b83846b2c10fff27c5d6bd71ffcee89de50834a2515daa86262f`  
		Last Modified: Fri, 26 Mar 2021 12:13:23 GMT  
		Size: 4.8 MB (4812764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4912983ad449bb8b1aaca073802b350bd31faee51a27d116347fd17a7c00d982`  
		Last Modified: Fri, 26 Mar 2021 12:13:22 GMT  
		Size: 3.2 KB (3152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b3201fc2bdd374fed29a81ca8239554e344b58a048daef7041cab1f9d5ccd05`  
		Last Modified: Fri, 26 Mar 2021 12:13:22 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffd04cb91b2f6e79464f13618a76e54a87df86f33b7e27965f81af0cb6bb49de`  
		Last Modified: Fri, 26 Mar 2021 12:13:22 GMT  
		Size: 239.5 KB (239514 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07707c525f79ec8ebe0387fd457d3c5d2f76c8e44adcdb9de1b82c631529c608`  
		Last Modified: Fri, 26 Mar 2021 12:13:34 GMT  
		Size: 256.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:nd20.04`

```console
$ docker pull neurodebian@sha256:f89a1d739548d9fb9d8436c222089a2d198c02517fe1094e2b644a9683ac03f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `neurodebian:nd20.04` - linux; amd64

```console
$ docker pull neurodebian@sha256:2902dcc33f6d0f3c097fd965f9d8a8006ef4ca178d2ae0687cb32159f9b81c4d
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.3 MB (34299802 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7de42b355c50738b1dbd006dbeba4b909c5c7703ab680e49f5c877874d96738`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 25 Mar 2021 22:33:08 GMT
ADD file:a8d2f02fbaddf8cec8e4da320cd03c06435f395e9d454f69954efe422eb6e1ba in / 
# Thu, 25 Mar 2021 22:33:09 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 25 Mar 2021 22:33:10 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 25 Mar 2021 22:33:11 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 25 Mar 2021 22:33:11 GMT
CMD ["/bin/bash"]
# Fri, 26 Mar 2021 12:10:19 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Fri, 26 Mar 2021 12:10:20 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Fri, 26 Mar 2021 12:10:22 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian focal main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel focal main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Fri, 26 Mar 2021 12:10:26 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:04a5f4cda3eea2313a61a2f72208342a57ea36a9326dff54f4f26ed47d145c7c`  
		Last Modified: Thu, 25 Mar 2021 22:34:46 GMT  
		Size: 28.6 MB (28569428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff496a88c8ed9b745dab2f00bfbd9013c6d1db198442a6a8683998a29a85458a`  
		Last Modified: Thu, 25 Mar 2021 22:34:37 GMT  
		Size: 846.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ce83f459fe7e0bf459d0c222ef3b2ca4d9911f6b0f9aae02c2120561b54ca18`  
		Last Modified: Thu, 25 Mar 2021 22:34:37 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bee7f820a96305ada827738a0d9bb1e8d431c59290f51cc1cb0b7bc03899c66`  
		Last Modified: Fri, 26 Mar 2021 12:13:46 GMT  
		Size: 5.5 MB (5489298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2a7803a8970682225aa3a42e3edb1de754b632f691268919af92243340cdd44`  
		Last Modified: Fri, 26 Mar 2021 12:13:45 GMT  
		Size: 1.8 KB (1763 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04df21c9180a8b40e1d992e773ebaff2360e317a2edfa9071e96374a9129a62a`  
		Last Modified: Fri, 26 Mar 2021 12:13:45 GMT  
		Size: 243.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43d2de458590b00504788c09aed1e67ac4139d8b58cf562a5f8790578ca27273`  
		Last Modified: Fri, 26 Mar 2021 12:13:45 GMT  
		Size: 238.0 KB (238035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:nd20.04-non-free`

```console
$ docker pull neurodebian@sha256:6c518e31030357194ba834b4688c1c6794f5a27388049871f40bdb3860e4410e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `neurodebian:nd20.04-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:aa4136f3a9a91a35b9b0577df29c9585856ff976a4294e90ddc1fd2dba90a41c
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.3 MB (34300057 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b16a883db8ac895cb451edf9a4dc35320debbd2b3106d266b28098e5195e8a5e`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 25 Mar 2021 22:33:08 GMT
ADD file:a8d2f02fbaddf8cec8e4da320cd03c06435f395e9d454f69954efe422eb6e1ba in / 
# Thu, 25 Mar 2021 22:33:09 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 25 Mar 2021 22:33:10 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 25 Mar 2021 22:33:11 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 25 Mar 2021 22:33:11 GMT
CMD ["/bin/bash"]
# Fri, 26 Mar 2021 12:10:19 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Fri, 26 Mar 2021 12:10:20 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Fri, 26 Mar 2021 12:10:22 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian focal main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel focal main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Fri, 26 Mar 2021 12:10:26 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Fri, 26 Mar 2021 12:10:34 GMT
RUN sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list; grep -q 'deb .* multiverse$' /etc/apt/sources.list || sed -i -e 's,universe *$,universe multiverse,g' /etc/apt/sources.list
```

-	Layers:
	-	`sha256:04a5f4cda3eea2313a61a2f72208342a57ea36a9326dff54f4f26ed47d145c7c`  
		Last Modified: Thu, 25 Mar 2021 22:34:46 GMT  
		Size: 28.6 MB (28569428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff496a88c8ed9b745dab2f00bfbd9013c6d1db198442a6a8683998a29a85458a`  
		Last Modified: Thu, 25 Mar 2021 22:34:37 GMT  
		Size: 846.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ce83f459fe7e0bf459d0c222ef3b2ca4d9911f6b0f9aae02c2120561b54ca18`  
		Last Modified: Thu, 25 Mar 2021 22:34:37 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bee7f820a96305ada827738a0d9bb1e8d431c59290f51cc1cb0b7bc03899c66`  
		Last Modified: Fri, 26 Mar 2021 12:13:46 GMT  
		Size: 5.5 MB (5489298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2a7803a8970682225aa3a42e3edb1de754b632f691268919af92243340cdd44`  
		Last Modified: Fri, 26 Mar 2021 12:13:45 GMT  
		Size: 1.8 KB (1763 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04df21c9180a8b40e1d992e773ebaff2360e317a2edfa9071e96374a9129a62a`  
		Last Modified: Fri, 26 Mar 2021 12:13:45 GMT  
		Size: 243.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43d2de458590b00504788c09aed1e67ac4139d8b58cf562a5f8790578ca27273`  
		Last Modified: Fri, 26 Mar 2021 12:13:45 GMT  
		Size: 238.0 KB (238035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c050c67f2ae77329e34ce9637e5cda451deac0cdf810c9103c2035a7b90d4e80`  
		Last Modified: Fri, 26 Mar 2021 12:13:57 GMT  
		Size: 255.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:nd20.10`

```console
$ docker pull neurodebian@sha256:3df2b6e6c07f68f5134d96f44936168e6be505fb1c9356de475afae3c054a04d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `neurodebian:nd20.10` - linux; amd64

```console
$ docker pull neurodebian@sha256:1a807c8f49726ef91d5bb172e78f45929c34de68265eb90be3f2a490a1de42c2
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.2 MB (37201415 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65aca515f341f3ac73709711f4289a4b6ce4cc4f0618533f31fc7bc8469a49a9`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 25 Mar 2021 22:33:18 GMT
ADD file:4aba1ec4c6317039d27ed2f8cdda90160c834d979269ba6253f4b8839e6a8c06 in / 
# Thu, 25 Mar 2021 22:33:19 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 25 Mar 2021 22:33:20 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 25 Mar 2021 22:33:21 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 25 Mar 2021 22:33:21 GMT
CMD ["/bin/bash"]
# Fri, 26 Mar 2021 12:11:13 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Fri, 26 Mar 2021 12:11:18 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Fri, 26 Mar 2021 12:11:19 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian groovy main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel groovy main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Fri, 26 Mar 2021 12:11:25 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:67b8b51191f1c23048b4af7390755377b07b7033f43a5bc7a5bcf37f863f7adb`  
		Last Modified: Thu, 25 Mar 2021 22:35:06 GMT  
		Size: 31.3 MB (31348493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bee746ea8f946b8bb5dee1458e4bf97293706926511644fdfd4411b9bac5710`  
		Last Modified: Thu, 25 Mar 2021 22:35:01 GMT  
		Size: 849.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:014d36ded12e82e314bb890faf3e15c110c39688e938f9c8c8ba8ebda5cbcbb7`  
		Last Modified: Thu, 25 Mar 2021 22:35:01 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0164949a4da1051c6005cd738a630f9252eb9fbc824f3bd5f3e2cbbc414b973e`  
		Last Modified: Fri, 26 Mar 2021 12:14:09 GMT  
		Size: 5.6 MB (5595460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f1c7a4f84e8d1a5821e81adf0643c5c424473be6fcde0673b696af0c3e39e4c`  
		Last Modified: Fri, 26 Mar 2021 12:14:08 GMT  
		Size: 1.8 KB (1763 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b979e50699487552db50c9530225510a01e15f7b33780491654cefa9c6a8275`  
		Last Modified: Fri, 26 Mar 2021 12:14:08 GMT  
		Size: 249.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:002e4319932a9d2ff199106cfee0009b10e2eacdff9f054b6c3df24d366115ef`  
		Last Modified: Fri, 26 Mar 2021 12:14:08 GMT  
		Size: 254.4 KB (254412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:nd20.10-non-free`

```console
$ docker pull neurodebian@sha256:546f3dddf78bd5ac7799f5ece18bd8d1d621d8681450f5daa15034f65cb7391c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `neurodebian:nd20.10-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:31300d76ebc71bad011d0f3a3c88ae6cb70247ce8091a4785210fbdf82eb5045
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.2 MB (37201673 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:143f76821bb6890cdf0ff70cb8435a172b108c007f6bb8c1b3deb6fa2a567608`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 25 Mar 2021 22:33:18 GMT
ADD file:4aba1ec4c6317039d27ed2f8cdda90160c834d979269ba6253f4b8839e6a8c06 in / 
# Thu, 25 Mar 2021 22:33:19 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 25 Mar 2021 22:33:20 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 25 Mar 2021 22:33:21 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 25 Mar 2021 22:33:21 GMT
CMD ["/bin/bash"]
# Fri, 26 Mar 2021 12:11:13 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Fri, 26 Mar 2021 12:11:18 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Fri, 26 Mar 2021 12:11:19 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian groovy main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel groovy main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Fri, 26 Mar 2021 12:11:25 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Fri, 26 Mar 2021 12:11:31 GMT
RUN sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list; grep -q 'deb .* multiverse$' /etc/apt/sources.list || sed -i -e 's,universe *$,universe multiverse,g' /etc/apt/sources.list
```

-	Layers:
	-	`sha256:67b8b51191f1c23048b4af7390755377b07b7033f43a5bc7a5bcf37f863f7adb`  
		Last Modified: Thu, 25 Mar 2021 22:35:06 GMT  
		Size: 31.3 MB (31348493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bee746ea8f946b8bb5dee1458e4bf97293706926511644fdfd4411b9bac5710`  
		Last Modified: Thu, 25 Mar 2021 22:35:01 GMT  
		Size: 849.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:014d36ded12e82e314bb890faf3e15c110c39688e938f9c8c8ba8ebda5cbcbb7`  
		Last Modified: Thu, 25 Mar 2021 22:35:01 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0164949a4da1051c6005cd738a630f9252eb9fbc824f3bd5f3e2cbbc414b973e`  
		Last Modified: Fri, 26 Mar 2021 12:14:09 GMT  
		Size: 5.6 MB (5595460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f1c7a4f84e8d1a5821e81adf0643c5c424473be6fcde0673b696af0c3e39e4c`  
		Last Modified: Fri, 26 Mar 2021 12:14:08 GMT  
		Size: 1.8 KB (1763 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b979e50699487552db50c9530225510a01e15f7b33780491654cefa9c6a8275`  
		Last Modified: Fri, 26 Mar 2021 12:14:08 GMT  
		Size: 249.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:002e4319932a9d2ff199106cfee0009b10e2eacdff9f054b6c3df24d366115ef`  
		Last Modified: Fri, 26 Mar 2021 12:14:08 GMT  
		Size: 254.4 KB (254412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2394fbebf42105a54df60bbc290a6901749e6760141abe2996234b8680f94d8e`  
		Last Modified: Fri, 26 Mar 2021 12:14:21 GMT  
		Size: 258.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:nd90`

```console
$ docker pull neurodebian@sha256:24043c0f78ee4d3897329f903e21c2d94eef310e02926d949a45cc72ee3047ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `neurodebian:nd90` - linux; amd64

```console
$ docker pull neurodebian@sha256:82ded91f3e02c4db9a1ba14630befd80427882deb57130df10f09704ae545868
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.2 MB (52246828 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2cfed040b67f808b28f2abf43f1d527193af3a483756651109c7bb3b09b52e1`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 26 Mar 2021 15:23:17 GMT
ADD file:f7a6b2066de76eb559d8ab8bf8972d519c3b4dcafc62e46253227559091f7c8f in / 
# Fri, 26 Mar 2021 15:23:18 GMT
CMD ["bash"]
# Sat, 27 Mar 2021 06:45:51 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Sat, 27 Mar 2021 06:45:54 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Sat, 27 Mar 2021 06:45:55 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian stretch main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel stretch main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Sat, 27 Mar 2021 06:46:00 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:1dfe7e1e1bffb84b5330514880896199259b01ebe2b9d531dd88f7ce7db8cd18`  
		Last Modified: Fri, 26 Mar 2021 15:32:18 GMT  
		Size: 45.4 MB (45379513 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:219624edc57f8ae307096765b713cbc6cefdc69fec74c06c78613579cefb7005`  
		Last Modified: Sat, 27 Mar 2021 06:48:21 GMT  
		Size: 6.6 MB (6571660 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11c6115d3a6671264c4594e46054ab582065636218e4e63a8aff8d122275f3d8`  
		Last Modified: Sat, 27 Mar 2021 06:48:19 GMT  
		Size: 3.2 KB (3152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ef4b6c402970f4c8ce03bf72d618dca5c1e883e855255f80d2d99d50c79a666`  
		Last Modified: Sat, 27 Mar 2021 06:48:19 GMT  
		Size: 246.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:141c8f4ef1f6832be5df5cc7b9bc491a5c5ab0304cdb4281c6f3283d96012072`  
		Last Modified: Sat, 27 Mar 2021 06:48:20 GMT  
		Size: 292.3 KB (292257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:nd90-non-free`

```console
$ docker pull neurodebian@sha256:b02a908cd6816c4ee8f62603a56772dfc00bb4b61cd5deec3e8f6dc26dec6507
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `neurodebian:nd90-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:bb875460f4b314032955092071b6a6fa77cbb87596ce350a66d3c26cea7205ac
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.2 MB (52247192 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d24e72e9258d6a875fa0086ee783aadfa097793735e3a470df60f377d310d3b0`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 26 Mar 2021 15:23:17 GMT
ADD file:f7a6b2066de76eb559d8ab8bf8972d519c3b4dcafc62e46253227559091f7c8f in / 
# Fri, 26 Mar 2021 15:23:18 GMT
CMD ["bash"]
# Sat, 27 Mar 2021 06:45:51 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Sat, 27 Mar 2021 06:45:54 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Sat, 27 Mar 2021 06:45:55 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian stretch main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel stretch main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Sat, 27 Mar 2021 06:46:00 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Sat, 27 Mar 2021 06:46:04 GMT
RUN sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list /etc/apt/sources.list
```

-	Layers:
	-	`sha256:1dfe7e1e1bffb84b5330514880896199259b01ebe2b9d531dd88f7ce7db8cd18`  
		Last Modified: Fri, 26 Mar 2021 15:32:18 GMT  
		Size: 45.4 MB (45379513 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:219624edc57f8ae307096765b713cbc6cefdc69fec74c06c78613579cefb7005`  
		Last Modified: Sat, 27 Mar 2021 06:48:21 GMT  
		Size: 6.6 MB (6571660 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11c6115d3a6671264c4594e46054ab582065636218e4e63a8aff8d122275f3d8`  
		Last Modified: Sat, 27 Mar 2021 06:48:19 GMT  
		Size: 3.2 KB (3152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ef4b6c402970f4c8ce03bf72d618dca5c1e883e855255f80d2d99d50c79a666`  
		Last Modified: Sat, 27 Mar 2021 06:48:19 GMT  
		Size: 246.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:141c8f4ef1f6832be5df5cc7b9bc491a5c5ab0304cdb4281c6f3283d96012072`  
		Last Modified: Sat, 27 Mar 2021 06:48:20 GMT  
		Size: 292.3 KB (292257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1bf9d19337ea3a2a51e67b71b32f41777ead165cae044e28b505930bbeaad73`  
		Last Modified: Sat, 27 Mar 2021 06:48:32 GMT  
		Size: 364.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:non-free`

```console
$ docker pull neurodebian@sha256:ca376ab717fc9ca7a9bdb361a6edb6ebcc20426db5f042fd3062df9df5c01a10
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `neurodebian:non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:167a22f317623d6cbfb5c56ffae7ad083512ce4a16a338f7752e5c93f2dbe399
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.2 MB (61205332 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd1962dde500ab6b345fd947e1aab221ec5319859b49ae1e0b99ebcd9833b646`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 26 Mar 2021 15:20:41 GMT
ADD file:89234bb2f86c7eb890235a48904d1c9898a8d287a525c4fe5698d4a04cdd8f12 in / 
# Fri, 26 Mar 2021 15:20:42 GMT
CMD ["bash"]
# Sat, 27 Mar 2021 06:46:13 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Sat, 27 Mar 2021 06:46:15 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Sat, 27 Mar 2021 06:46:16 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian buster main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel buster main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Sat, 27 Mar 2021 06:46:21 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Sat, 27 Mar 2021 06:46:27 GMT
RUN sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list /etc/apt/sources.list
```

-	Layers:
	-	`sha256:8bf9c589d5f9475f1fcc050e02308d6b4eeb86eab7752ef948a13693e81a6aaa`  
		Last Modified: Fri, 26 Mar 2021 15:27:11 GMT  
		Size: 50.4 MB (50400278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:364a64e1f4b60995fac7bd8a65ddcc94f637ced0ed4662fa7d8ffa3ca8947238`  
		Last Modified: Sat, 27 Mar 2021 06:48:44 GMT  
		Size: 10.5 MB (10499932 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0500ee5393cea56c36ff618c71cb990c7f140aec2ca0061e96ac96250bef0e0c`  
		Last Modified: Sat, 27 Mar 2021 06:48:42 GMT  
		Size: 1.8 KB (1763 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64f5bb07b57b9524913e9c7d15292dfd3f125836f353facc7e7934a8dd647db6`  
		Last Modified: Sat, 27 Mar 2021 06:48:42 GMT  
		Size: 243.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a585715510bbe7dc1a5499fbed076b9886c6e83b5b8dca19614ae03984ceec6`  
		Last Modified: Sat, 27 Mar 2021 06:48:42 GMT  
		Size: 302.8 KB (302751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:474336b7160442315e21450ba11dc70cd1a99451f34b64e60122100ec3e80ddf`  
		Last Modified: Sat, 27 Mar 2021 06:48:56 GMT  
		Size: 365.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:sid`

```console
$ docker pull neurodebian@sha256:5ec46d7f26ae63961dd31c66c24980c8d67a2790b2554c2976c3946c501ff408
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `neurodebian:sid` - linux; amd64

```console
$ docker pull neurodebian@sha256:8f1c27c5f380c56971be630eaa17fac9504108e027226c42cfd5720c5068ad6a
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.5 MB (66486538 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:159a3505079e6ec7ccae5c6295ef4ade9339f7e92ef43031933472e7e01797df`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 26 Mar 2021 15:22:32 GMT
ADD file:2077716d4a510c614acac732f9b9130b649ac696764e3becc6e21e732f39e9c6 in / 
# Fri, 26 Mar 2021 15:22:33 GMT
CMD ["bash"]
# Sat, 27 Mar 2021 06:47:00 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Sat, 27 Mar 2021 06:47:02 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Sat, 27 Mar 2021 06:47:03 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian sid main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Sat, 27 Mar 2021 06:47:07 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:e6db1addbc87ce8e502d75dae59834703a516712298c58eaee03f40a399e8292`  
		Last Modified: Fri, 26 Mar 2021 15:30:40 GMT  
		Size: 54.9 MB (54868141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae9eeffb47c540d6fa5caef3fcaa66750050bfd0c116253947d087ecf0ef7a84`  
		Last Modified: Sat, 27 Mar 2021 06:49:37 GMT  
		Size: 11.3 MB (11305751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a02159ef5c0b757456dd3da2955f66136688806aee6cddc4e04a5840918df1e`  
		Last Modified: Sat, 27 Mar 2021 06:49:35 GMT  
		Size: 1.8 KB (1757 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6baa1a0325071f162dcf13db50337fd626e0bbc7daeaba6ca66b3defd7af512`  
		Last Modified: Sat, 27 Mar 2021 06:49:36 GMT  
		Size: 240.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed6b1df463008071e0f80383eef835d97ef56cb9dfb77baf28a22387a68c018c`  
		Last Modified: Sat, 27 Mar 2021 06:49:36 GMT  
		Size: 310.6 KB (310649 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:sid-non-free`

```console
$ docker pull neurodebian@sha256:3631eba6e722b93c9ea8453bfc14205e87a151e4c79c734677ce9c0ca7c6d74a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `neurodebian:sid-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:be3126a5bfa93199db8328bc4e8595b3a501fb5e5f0cd960c9ec08d66fd3818b
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.5 MB (66486857 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ee20d7a1607afa108b40f745dcf9487f1d9fd75208d8db7657d06b166fda500`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 26 Mar 2021 15:22:32 GMT
ADD file:2077716d4a510c614acac732f9b9130b649ac696764e3becc6e21e732f39e9c6 in / 
# Fri, 26 Mar 2021 15:22:33 GMT
CMD ["bash"]
# Sat, 27 Mar 2021 06:47:00 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Sat, 27 Mar 2021 06:47:02 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Sat, 27 Mar 2021 06:47:03 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian sid main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Sat, 27 Mar 2021 06:47:07 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Sat, 27 Mar 2021 06:47:15 GMT
RUN sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list /etc/apt/sources.list
```

-	Layers:
	-	`sha256:e6db1addbc87ce8e502d75dae59834703a516712298c58eaee03f40a399e8292`  
		Last Modified: Fri, 26 Mar 2021 15:30:40 GMT  
		Size: 54.9 MB (54868141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae9eeffb47c540d6fa5caef3fcaa66750050bfd0c116253947d087ecf0ef7a84`  
		Last Modified: Sat, 27 Mar 2021 06:49:37 GMT  
		Size: 11.3 MB (11305751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a02159ef5c0b757456dd3da2955f66136688806aee6cddc4e04a5840918df1e`  
		Last Modified: Sat, 27 Mar 2021 06:49:35 GMT  
		Size: 1.8 KB (1757 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6baa1a0325071f162dcf13db50337fd626e0bbc7daeaba6ca66b3defd7af512`  
		Last Modified: Sat, 27 Mar 2021 06:49:36 GMT  
		Size: 240.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed6b1df463008071e0f80383eef835d97ef56cb9dfb77baf28a22387a68c018c`  
		Last Modified: Sat, 27 Mar 2021 06:49:36 GMT  
		Size: 310.6 KB (310649 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ad000ff0f4e95c054964ef57e7b5b7d13a876f78fe8312cac4b71d21793b8d0`  
		Last Modified: Sat, 27 Mar 2021 06:49:47 GMT  
		Size: 319.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:stretch`

```console
$ docker pull neurodebian@sha256:24043c0f78ee4d3897329f903e21c2d94eef310e02926d949a45cc72ee3047ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `neurodebian:stretch` - linux; amd64

```console
$ docker pull neurodebian@sha256:82ded91f3e02c4db9a1ba14630befd80427882deb57130df10f09704ae545868
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.2 MB (52246828 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2cfed040b67f808b28f2abf43f1d527193af3a483756651109c7bb3b09b52e1`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 26 Mar 2021 15:23:17 GMT
ADD file:f7a6b2066de76eb559d8ab8bf8972d519c3b4dcafc62e46253227559091f7c8f in / 
# Fri, 26 Mar 2021 15:23:18 GMT
CMD ["bash"]
# Sat, 27 Mar 2021 06:45:51 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Sat, 27 Mar 2021 06:45:54 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Sat, 27 Mar 2021 06:45:55 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian stretch main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel stretch main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Sat, 27 Mar 2021 06:46:00 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:1dfe7e1e1bffb84b5330514880896199259b01ebe2b9d531dd88f7ce7db8cd18`  
		Last Modified: Fri, 26 Mar 2021 15:32:18 GMT  
		Size: 45.4 MB (45379513 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:219624edc57f8ae307096765b713cbc6cefdc69fec74c06c78613579cefb7005`  
		Last Modified: Sat, 27 Mar 2021 06:48:21 GMT  
		Size: 6.6 MB (6571660 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11c6115d3a6671264c4594e46054ab582065636218e4e63a8aff8d122275f3d8`  
		Last Modified: Sat, 27 Mar 2021 06:48:19 GMT  
		Size: 3.2 KB (3152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ef4b6c402970f4c8ce03bf72d618dca5c1e883e855255f80d2d99d50c79a666`  
		Last Modified: Sat, 27 Mar 2021 06:48:19 GMT  
		Size: 246.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:141c8f4ef1f6832be5df5cc7b9bc491a5c5ab0304cdb4281c6f3283d96012072`  
		Last Modified: Sat, 27 Mar 2021 06:48:20 GMT  
		Size: 292.3 KB (292257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:stretch-non-free`

```console
$ docker pull neurodebian@sha256:b02a908cd6816c4ee8f62603a56772dfc00bb4b61cd5deec3e8f6dc26dec6507
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `neurodebian:stretch-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:bb875460f4b314032955092071b6a6fa77cbb87596ce350a66d3c26cea7205ac
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.2 MB (52247192 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d24e72e9258d6a875fa0086ee783aadfa097793735e3a470df60f377d310d3b0`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 26 Mar 2021 15:23:17 GMT
ADD file:f7a6b2066de76eb559d8ab8bf8972d519c3b4dcafc62e46253227559091f7c8f in / 
# Fri, 26 Mar 2021 15:23:18 GMT
CMD ["bash"]
# Sat, 27 Mar 2021 06:45:51 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Sat, 27 Mar 2021 06:45:54 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Sat, 27 Mar 2021 06:45:55 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian stretch main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel stretch main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Sat, 27 Mar 2021 06:46:00 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Sat, 27 Mar 2021 06:46:04 GMT
RUN sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list /etc/apt/sources.list
```

-	Layers:
	-	`sha256:1dfe7e1e1bffb84b5330514880896199259b01ebe2b9d531dd88f7ce7db8cd18`  
		Last Modified: Fri, 26 Mar 2021 15:32:18 GMT  
		Size: 45.4 MB (45379513 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:219624edc57f8ae307096765b713cbc6cefdc69fec74c06c78613579cefb7005`  
		Last Modified: Sat, 27 Mar 2021 06:48:21 GMT  
		Size: 6.6 MB (6571660 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11c6115d3a6671264c4594e46054ab582065636218e4e63a8aff8d122275f3d8`  
		Last Modified: Sat, 27 Mar 2021 06:48:19 GMT  
		Size: 3.2 KB (3152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ef4b6c402970f4c8ce03bf72d618dca5c1e883e855255f80d2d99d50c79a666`  
		Last Modified: Sat, 27 Mar 2021 06:48:19 GMT  
		Size: 246.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:141c8f4ef1f6832be5df5cc7b9bc491a5c5ab0304cdb4281c6f3283d96012072`  
		Last Modified: Sat, 27 Mar 2021 06:48:20 GMT  
		Size: 292.3 KB (292257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1bf9d19337ea3a2a51e67b71b32f41777ead165cae044e28b505930bbeaad73`  
		Last Modified: Sat, 27 Mar 2021 06:48:32 GMT  
		Size: 364.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:xenial`

```console
$ docker pull neurodebian@sha256:8cbbcb2e27d56711ac78a442bd4ef3011dad185c3705859f4a7fb9445911598a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `neurodebian:xenial` - linux; amd64

```console
$ docker pull neurodebian@sha256:ee42f8053bf30a97dabd06fe7a679675506f87376b833c4d064658c776a4812e
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.2 MB (46194559 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f70324aa866fcefbb63c8fa890a1aeeea467a106b52d15894a4cf712468c37d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 25 Mar 2021 22:33:52 GMT
ADD file:925571658dd8453e5c80d862f5791d6b26b3c2a8688937b11741f2f2c5cdbfd7 in / 
# Thu, 25 Mar 2021 22:33:53 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 25 Mar 2021 22:33:54 GMT
RUN rm -rf /var/lib/apt/lists/*
# Thu, 25 Mar 2021 22:33:55 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 25 Mar 2021 22:33:55 GMT
CMD ["/bin/bash"]
# Fri, 26 Mar 2021 12:09:05 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Fri, 26 Mar 2021 12:09:08 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Fri, 26 Mar 2021 12:09:10 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian xenial main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel xenial main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Fri, 26 Mar 2021 12:09:19 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:4007a89234b4f56c03e6831dc220550d2e5fba935d9f5f5bcea64857ac4f4888`  
		Last Modified: Mon, 18 Jan 2021 19:38:08 GMT  
		Size: 46.0 MB (45962352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1de0f9cdfc1f9f595acd2ea8724ea92a509d64a6936f0e645c65b504e7e4bc6`  
		Last Modified: Thu, 25 Mar 2021 22:36:02 GMT  
		Size: 846.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8ee6ca703b866ac2b74b6129d2db331936292f899e8e3a794474fdf81343605`  
		Last Modified: Thu, 25 Mar 2021 22:36:02 GMT  
		Size: 526.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b39e2761d3d4971e78914857af4c6bd9989873b53426cf2fef3e76983b166fa2`  
		Last Modified: Thu, 25 Mar 2021 22:36:02 GMT  
		Size: 168.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:246e2fbfdb5416c63dcf63f4b1ff87529e9c95869c626b834447830f42a27e76`  
		Last Modified: Fri, 26 Mar 2021 12:12:57 GMT  
		Size: 177.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbfba0ba677947687db6fc0d522806505ac13da985638232b97294a05298a07f`  
		Last Modified: Fri, 26 Mar 2021 12:12:57 GMT  
		Size: 3.2 KB (3151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52429283d5b479729c1eb2900697631aa16136b78c0b9632fa39a9039136312b`  
		Last Modified: Fri, 26 Mar 2021 12:12:57 GMT  
		Size: 250.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bb0f6fc0209667118bfb6a71d36023a43b33bb6596e2f34c29691e66669b0db`  
		Last Modified: Fri, 26 Mar 2021 12:12:57 GMT  
		Size: 227.1 KB (227089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:xenial-non-free`

```console
$ docker pull neurodebian@sha256:a3275da187b67cc7bdac5c4dc16935e6f6e4d9ec3b7a5a12f3f49fe7c8b33078
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `neurodebian:xenial-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:ac30151d25adebbb903b0db493cc193ac41d7c03f19fccb1fb0a1f292dcba470
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.2 MB (46194817 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:905eaec96ee02d5a98dcd61a928b33e6a93935ff8d2d96341e12467fa560c644`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 25 Mar 2021 22:33:52 GMT
ADD file:925571658dd8453e5c80d862f5791d6b26b3c2a8688937b11741f2f2c5cdbfd7 in / 
# Thu, 25 Mar 2021 22:33:53 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 25 Mar 2021 22:33:54 GMT
RUN rm -rf /var/lib/apt/lists/*
# Thu, 25 Mar 2021 22:33:55 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 25 Mar 2021 22:33:55 GMT
CMD ["/bin/bash"]
# Fri, 26 Mar 2021 12:09:05 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Fri, 26 Mar 2021 12:09:08 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Fri, 26 Mar 2021 12:09:10 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian xenial main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel xenial main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Fri, 26 Mar 2021 12:09:19 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Fri, 26 Mar 2021 12:09:26 GMT
RUN sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list; grep -q 'deb .* multiverse$' /etc/apt/sources.list || sed -i -e 's,universe *$,universe multiverse,g' /etc/apt/sources.list
```

-	Layers:
	-	`sha256:4007a89234b4f56c03e6831dc220550d2e5fba935d9f5f5bcea64857ac4f4888`  
		Last Modified: Mon, 18 Jan 2021 19:38:08 GMT  
		Size: 46.0 MB (45962352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1de0f9cdfc1f9f595acd2ea8724ea92a509d64a6936f0e645c65b504e7e4bc6`  
		Last Modified: Thu, 25 Mar 2021 22:36:02 GMT  
		Size: 846.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8ee6ca703b866ac2b74b6129d2db331936292f899e8e3a794474fdf81343605`  
		Last Modified: Thu, 25 Mar 2021 22:36:02 GMT  
		Size: 526.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b39e2761d3d4971e78914857af4c6bd9989873b53426cf2fef3e76983b166fa2`  
		Last Modified: Thu, 25 Mar 2021 22:36:02 GMT  
		Size: 168.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:246e2fbfdb5416c63dcf63f4b1ff87529e9c95869c626b834447830f42a27e76`  
		Last Modified: Fri, 26 Mar 2021 12:12:57 GMT  
		Size: 177.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbfba0ba677947687db6fc0d522806505ac13da985638232b97294a05298a07f`  
		Last Modified: Fri, 26 Mar 2021 12:12:57 GMT  
		Size: 3.2 KB (3151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52429283d5b479729c1eb2900697631aa16136b78c0b9632fa39a9039136312b`  
		Last Modified: Fri, 26 Mar 2021 12:12:57 GMT  
		Size: 250.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bb0f6fc0209667118bfb6a71d36023a43b33bb6596e2f34c29691e66669b0db`  
		Last Modified: Fri, 26 Mar 2021 12:12:57 GMT  
		Size: 227.1 KB (227089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3763a04ce6f958325f23ee4cf4cadbaea201e6a0dfde5762a750f3e1355b735`  
		Last Modified: Fri, 26 Mar 2021 12:13:08 GMT  
		Size: 258.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
