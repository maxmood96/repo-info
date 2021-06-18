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
$ docker pull neurodebian@sha256:db216a15ee6f153fa278e74ec41018677ccd2e7b6601cae05b70ee12df8e5262
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `neurodebian:bionic` - linux; amd64

```console
$ docker pull neurodebian@sha256:4571610dba14a3148eab203c2968f8aa1b51a4cc11fdf4c0d6b705d46f2848bf
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.8 MB (31758477 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83cafc4228b65934b0fa1c7219c2807081de2aafb130446bf27e111327c35e30`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Jun 2021 23:31:22 GMT
ADD file:900f735ff138e5137cf25ddd85a32a01921ebec26d86704d24b5f12e73a832c2 in / 
# Thu, 17 Jun 2021 23:31:22 GMT
CMD ["bash"]
# Fri, 18 Jun 2021 04:52:11 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Fri, 18 Jun 2021 04:52:13 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Fri, 18 Jun 2021 04:52:14 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bionic main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bionic main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Fri, 18 Jun 2021 04:52:19 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:25fa05cd42bd8fabb25d2a6f3f8c9f7ab34637903d00fd2ed1c1d0fa980427dd`  
		Last Modified: Thu, 17 Jun 2021 23:32:41 GMT  
		Size: 26.7 MB (26700706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a372806eca722b9500ca1c252a350a3e0441d81be91618655d70abc45dad7d12`  
		Last Modified: Fri, 18 Jun 2021 04:55:02 GMT  
		Size: 4.8 MB (4813844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:182b5f8f7126262ff9cee76fb70a5d94c2164b9d04d38f3f4921426d6a808244`  
		Last Modified: Fri, 18 Jun 2021 04:55:01 GMT  
		Size: 3.2 KB (3152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3986bc512fe32c67789ba6b338b2c23b00719f03a9619bd4e5427b03ef79346`  
		Last Modified: Fri, 18 Jun 2021 04:55:01 GMT  
		Size: 244.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3285e935d5c30552d33396c6914b9f8181419e461b918cc75419eb56584526d3`  
		Last Modified: Fri, 18 Jun 2021 04:55:01 GMT  
		Size: 240.5 KB (240531 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:bionic-non-free`

```console
$ docker pull neurodebian@sha256:137643bf32def556edce8ffbba26060623f95319e4a2d74d96fc6c0bb30d1e30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `neurodebian:bionic-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:0cd189273525767046fb18bb92c66839ba0c8994c93f48d36fc8660e77503f59
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.8 MB (31758733 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d96912b660ca96bd8bbbe6a08237f9bd013262c9fc3db7a2a7900e424acc56d`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Jun 2021 23:31:22 GMT
ADD file:900f735ff138e5137cf25ddd85a32a01921ebec26d86704d24b5f12e73a832c2 in / 
# Thu, 17 Jun 2021 23:31:22 GMT
CMD ["bash"]
# Fri, 18 Jun 2021 04:52:11 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Fri, 18 Jun 2021 04:52:13 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Fri, 18 Jun 2021 04:52:14 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bionic main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bionic main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Fri, 18 Jun 2021 04:52:19 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Fri, 18 Jun 2021 04:52:27 GMT
RUN sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list; grep -q 'deb .* multiverse$' /etc/apt/sources.list || sed -i -e 's,universe *$,universe multiverse,g' /etc/apt/sources.list
```

-	Layers:
	-	`sha256:25fa05cd42bd8fabb25d2a6f3f8c9f7ab34637903d00fd2ed1c1d0fa980427dd`  
		Last Modified: Thu, 17 Jun 2021 23:32:41 GMT  
		Size: 26.7 MB (26700706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a372806eca722b9500ca1c252a350a3e0441d81be91618655d70abc45dad7d12`  
		Last Modified: Fri, 18 Jun 2021 04:55:02 GMT  
		Size: 4.8 MB (4813844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:182b5f8f7126262ff9cee76fb70a5d94c2164b9d04d38f3f4921426d6a808244`  
		Last Modified: Fri, 18 Jun 2021 04:55:01 GMT  
		Size: 3.2 KB (3152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3986bc512fe32c67789ba6b338b2c23b00719f03a9619bd4e5427b03ef79346`  
		Last Modified: Fri, 18 Jun 2021 04:55:01 GMT  
		Size: 244.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3285e935d5c30552d33396c6914b9f8181419e461b918cc75419eb56584526d3`  
		Last Modified: Fri, 18 Jun 2021 04:55:01 GMT  
		Size: 240.5 KB (240531 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1ca3f59ea90b8f2dae868601d0485c3d456b3f511ba70fe32d1c8ea82d12b0f`  
		Last Modified: Fri, 18 Jun 2021 04:55:12 GMT  
		Size: 256.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:bullseye`

```console
$ docker pull neurodebian@sha256:37a70a1d18f74cc00a14aefd2e6f2fff9afd2b8d7e26ea63252422b95e77286f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `neurodebian:bullseye` - linux; amd64

```console
$ docker pull neurodebian@sha256:d3f45dffd49a2b162a4e01edaa391cac11585ef1570f877d83cbc7c39c9d5c58
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.5 MB (66519150 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9956cb29636d21fc4de6593382fe3a75f61eb7e8811d2145baab1c230630a2a6`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 May 2021 01:20:32 GMT
ADD file:22ed184e421fcac775f322850c24589ef2e78ddd12900395d44b2ea74220a62e in / 
# Wed, 12 May 2021 01:20:33 GMT
CMD ["bash"]
# Wed, 12 May 2021 08:15:49 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Wed, 12 May 2021 08:15:50 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Wed, 12 May 2021 08:15:51 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bullseye main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Wed, 12 May 2021 08:15:55 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:ad4592a9cb6deb788f794c7bc60f66d77280e79869f13e9eccbf34e1d381b95d`  
		Last Modified: Wed, 12 May 2021 01:26:05 GMT  
		Size: 54.9 MB (54897696 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8542129608a42399bc292c1994a3f2340d165d1040e98a2bf563841e5a3eebb2`  
		Last Modified: Wed, 12 May 2021 08:18:00 GMT  
		Size: 11.3 MB (11308850 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f358d6314ea033af895f5aebc4724359a9aa401aa672cc401d584a2465387aac`  
		Last Modified: Wed, 12 May 2021 08:17:58 GMT  
		Size: 1.8 KB (1762 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e876a28d30789565f8fb5724aa6186e85e0ec5d722e4e45ad3d6ea02b2cb4fc8`  
		Last Modified: Wed, 12 May 2021 08:17:58 GMT  
		Size: 248.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bab1c0263bda33d4f321fe0ed47941aa2373f4d0a6068478b03cf7f78d9820c`  
		Last Modified: Wed, 12 May 2021 08:17:59 GMT  
		Size: 310.6 KB (310594 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:bullseye-non-free`

```console
$ docker pull neurodebian@sha256:3c00f7abc74c5bbd7c80c41a5056a3b86f737b0bef1090404d3e6fc0602a9291
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `neurodebian:bullseye-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:5ac0bd054e017dd1fdb6ad359e849c6b895a05010522d81c0cfe950f6e94ee43
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.5 MB (66519517 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ed86d8135cd289d5987ae2871c1cf8750f28e606e25a625a9627d58eb602a48`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 May 2021 01:20:32 GMT
ADD file:22ed184e421fcac775f322850c24589ef2e78ddd12900395d44b2ea74220a62e in / 
# Wed, 12 May 2021 01:20:33 GMT
CMD ["bash"]
# Wed, 12 May 2021 08:15:49 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Wed, 12 May 2021 08:15:50 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Wed, 12 May 2021 08:15:51 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bullseye main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Wed, 12 May 2021 08:15:55 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Wed, 12 May 2021 08:16:00 GMT
RUN sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list /etc/apt/sources.list
```

-	Layers:
	-	`sha256:ad4592a9cb6deb788f794c7bc60f66d77280e79869f13e9eccbf34e1d381b95d`  
		Last Modified: Wed, 12 May 2021 01:26:05 GMT  
		Size: 54.9 MB (54897696 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8542129608a42399bc292c1994a3f2340d165d1040e98a2bf563841e5a3eebb2`  
		Last Modified: Wed, 12 May 2021 08:18:00 GMT  
		Size: 11.3 MB (11308850 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f358d6314ea033af895f5aebc4724359a9aa401aa672cc401d584a2465387aac`  
		Last Modified: Wed, 12 May 2021 08:17:58 GMT  
		Size: 1.8 KB (1762 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e876a28d30789565f8fb5724aa6186e85e0ec5d722e4e45ad3d6ea02b2cb4fc8`  
		Last Modified: Wed, 12 May 2021 08:17:58 GMT  
		Size: 248.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bab1c0263bda33d4f321fe0ed47941aa2373f4d0a6068478b03cf7f78d9820c`  
		Last Modified: Wed, 12 May 2021 08:17:59 GMT  
		Size: 310.6 KB (310594 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d8e264ceb5b955edcc0b63ff38202b1f0ac04026f3f14b151f524409a442e09`  
		Last Modified: Wed, 12 May 2021 08:18:10 GMT  
		Size: 367.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:buster`

```console
$ docker pull neurodebian@sha256:be75a622593d46b0c85c0dc55774436eb29a9b7b205c4228aaadfc7fdbe5fe89
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `neurodebian:buster` - linux; amd64

```console
$ docker pull neurodebian@sha256:b0fb9b986cdbacd0afaab5e742974bd3ef153dd73840d547ed841c41b5c4a768
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.2 MB (61237937 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a14430ab3dcd893dccbf9811e9c3825c96cc4fe29ed53702417e21f7324e4f77`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 May 2021 01:21:03 GMT
ADD file:1a1eae7a82c66d673971436ce2605e97d107e2934b7cdec876c64923ae6f4f85 in / 
# Wed, 12 May 2021 01:21:03 GMT
CMD ["bash"]
# Wed, 12 May 2021 08:15:25 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Wed, 12 May 2021 08:15:26 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Wed, 12 May 2021 08:15:27 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian buster main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel buster main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Wed, 12 May 2021 08:15:32 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:d960726af2bec62a87ceb07182f7b94c47be03909077e23d8226658f80b47f87`  
		Last Modified: Wed, 12 May 2021 01:26:49 GMT  
		Size: 50.4 MB (50433242 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a89553ed3a7797659596b70fac74c996633d5f2cecd4360db1b6bc5aa81131d`  
		Last Modified: Wed, 12 May 2021 08:17:32 GMT  
		Size: 10.5 MB (10499972 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32e2547b1380c9d77ce3ac458d0a28697a7064cda03c6239d421c365ab088738`  
		Last Modified: Wed, 12 May 2021 08:17:31 GMT  
		Size: 1.8 KB (1762 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40ba78ab5ae2bf7a1da1a747d895310235c2d28fa0a66c0eef0228e57d35e547`  
		Last Modified: Wed, 12 May 2021 08:17:31 GMT  
		Size: 246.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81703386770e4978fe71acaf5810bd4542e8e9fb5a7ed87bd780399f6885fddf`  
		Last Modified: Wed, 12 May 2021 08:17:32 GMT  
		Size: 302.7 KB (302715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:buster-non-free`

```console
$ docker pull neurodebian@sha256:c50965f97971d78ba53f4987c2df17ced4c4d421fffaa849e9c5dce778aad9a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `neurodebian:buster-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:595f1244408ebd2102c8e0c63f7adcb8c0d6a2a5cd77b68ea79925ee278a8b6a
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.2 MB (61238302 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de43c9d8833440ec409d45392795fe6df36f09be60f866657adc5672006e46e4`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 May 2021 01:21:03 GMT
ADD file:1a1eae7a82c66d673971436ce2605e97d107e2934b7cdec876c64923ae6f4f85 in / 
# Wed, 12 May 2021 01:21:03 GMT
CMD ["bash"]
# Wed, 12 May 2021 08:15:25 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Wed, 12 May 2021 08:15:26 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Wed, 12 May 2021 08:15:27 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian buster main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel buster main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Wed, 12 May 2021 08:15:32 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Wed, 12 May 2021 08:15:38 GMT
RUN sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list /etc/apt/sources.list
```

-	Layers:
	-	`sha256:d960726af2bec62a87ceb07182f7b94c47be03909077e23d8226658f80b47f87`  
		Last Modified: Wed, 12 May 2021 01:26:49 GMT  
		Size: 50.4 MB (50433242 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a89553ed3a7797659596b70fac74c996633d5f2cecd4360db1b6bc5aa81131d`  
		Last Modified: Wed, 12 May 2021 08:17:32 GMT  
		Size: 10.5 MB (10499972 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32e2547b1380c9d77ce3ac458d0a28697a7064cda03c6239d421c365ab088738`  
		Last Modified: Wed, 12 May 2021 08:17:31 GMT  
		Size: 1.8 KB (1762 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40ba78ab5ae2bf7a1da1a747d895310235c2d28fa0a66c0eef0228e57d35e547`  
		Last Modified: Wed, 12 May 2021 08:17:31 GMT  
		Size: 246.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81703386770e4978fe71acaf5810bd4542e8e9fb5a7ed87bd780399f6885fddf`  
		Last Modified: Wed, 12 May 2021 08:17:32 GMT  
		Size: 302.7 KB (302715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3269028ef6dfd1b263a7462e2cb26492f38f42e54fab284dba145e8dcd5806c`  
		Last Modified: Wed, 12 May 2021 08:17:45 GMT  
		Size: 365.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:focal`

```console
$ docker pull neurodebian@sha256:4c455036d37f289095299df3a4bd0e8f300d4d0ee2c886062534ebb3442a9f7e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `neurodebian:focal` - linux; amd64

```console
$ docker pull neurodebian@sha256:629c1e71294f3d83f64e640a5df834ca5c75274d36114803f07f7c273a721d4f
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.3 MB (34282594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a5707c344a0d6620e7086d356540cca35678d627c9ea94dae40997250bfc52b`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Jun 2021 23:31:29 GMT
ADD file:920cf788d1ba88f76c97e41e03e4dc2f3005b08d65b5e9da9dd1cbe20a74459b in / 
# Thu, 17 Jun 2021 23:31:29 GMT
CMD ["bash"]
# Fri, 18 Jun 2021 04:52:37 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Fri, 18 Jun 2021 04:52:38 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Fri, 18 Jun 2021 04:52:39 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian focal main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel focal main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Fri, 18 Jun 2021 04:52:44 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:c549ccf8d472c3bce9ce02e49c62b8f6cbc736ea2b8ba812a1ae9390c69d0b71`  
		Last Modified: Thu, 17 Jun 2021 23:32:58 GMT  
		Size: 28.6 MB (28553692 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc4a77e48a4e30ad5b9a0e8f57a8941b5e4afd803b768a118af1f4395e9af730`  
		Last Modified: Fri, 18 Jun 2021 04:55:23 GMT  
		Size: 5.5 MB (5488782 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2bc8c0b52966c29981f450a633c9e42cd66d2bc21ed88bdbb4bc8725848587c`  
		Last Modified: Fri, 18 Jun 2021 04:55:22 GMT  
		Size: 1.8 KB (1763 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c875b70270f67ed702580b6ff4c2fbcb6e07be3081b0884904af67c78aa811f`  
		Last Modified: Fri, 18 Jun 2021 04:55:22 GMT  
		Size: 245.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0629f8de5ae05b122171d9e1b056f0723c06414eef890d5630081aa0b06dcbe5`  
		Last Modified: Fri, 18 Jun 2021 04:55:22 GMT  
		Size: 238.1 KB (238112 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:focal-non-free`

```console
$ docker pull neurodebian@sha256:839119d3149fdabb9757dba9e8c8d2e4da0f3d6ff2cf67b5235a059bc629bbec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `neurodebian:focal-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:01e7915db023a737a56340dfe2fd95399210a85cc559374bc806d7bf55019d1b
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.3 MB (34282848 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f34fd1463d4c93e9554eb0926150b053f9b203c8d6b7451fb624faf1139dd84a`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Jun 2021 23:31:29 GMT
ADD file:920cf788d1ba88f76c97e41e03e4dc2f3005b08d65b5e9da9dd1cbe20a74459b in / 
# Thu, 17 Jun 2021 23:31:29 GMT
CMD ["bash"]
# Fri, 18 Jun 2021 04:52:37 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Fri, 18 Jun 2021 04:52:38 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Fri, 18 Jun 2021 04:52:39 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian focal main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel focal main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Fri, 18 Jun 2021 04:52:44 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Fri, 18 Jun 2021 04:52:49 GMT
RUN sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list; grep -q 'deb .* multiverse$' /etc/apt/sources.list || sed -i -e 's,universe *$,universe multiverse,g' /etc/apt/sources.list
```

-	Layers:
	-	`sha256:c549ccf8d472c3bce9ce02e49c62b8f6cbc736ea2b8ba812a1ae9390c69d0b71`  
		Last Modified: Thu, 17 Jun 2021 23:32:58 GMT  
		Size: 28.6 MB (28553692 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc4a77e48a4e30ad5b9a0e8f57a8941b5e4afd803b768a118af1f4395e9af730`  
		Last Modified: Fri, 18 Jun 2021 04:55:23 GMT  
		Size: 5.5 MB (5488782 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2bc8c0b52966c29981f450a633c9e42cd66d2bc21ed88bdbb4bc8725848587c`  
		Last Modified: Fri, 18 Jun 2021 04:55:22 GMT  
		Size: 1.8 KB (1763 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c875b70270f67ed702580b6ff4c2fbcb6e07be3081b0884904af67c78aa811f`  
		Last Modified: Fri, 18 Jun 2021 04:55:22 GMT  
		Size: 245.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0629f8de5ae05b122171d9e1b056f0723c06414eef890d5630081aa0b06dcbe5`  
		Last Modified: Fri, 18 Jun 2021 04:55:22 GMT  
		Size: 238.1 KB (238112 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c11f19f52782c866f0af53b6f977420b5fce2df64080ac5c2a1c45a7b530a39d`  
		Last Modified: Fri, 18 Jun 2021 04:55:32 GMT  
		Size: 254.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:groovy`

```console
$ docker pull neurodebian@sha256:52eef91cf9255c211253782c7e20ffa03412e4574a6e6f1c1d1363a613d9b10e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `neurodebian:groovy` - linux; amd64

```console
$ docker pull neurodebian@sha256:3d68604aebecfc0a701d12a8e822856e7488a783c5ff297d2632beed20ce03bd
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.2 MB (37195950 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49280897b29663747cd44465424ff0fe54a56cf77de43aa4930923cdad07e75b`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Jun 2021 23:31:36 GMT
ADD file:8fe6bbb03392c41fe275714978bd93f4c94d64366217e95415b50aa7edc3b7c8 in / 
# Thu, 17 Jun 2021 23:31:37 GMT
CMD ["bash"]
# Fri, 18 Jun 2021 04:53:26 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Fri, 18 Jun 2021 04:53:28 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Fri, 18 Jun 2021 04:53:28 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian groovy main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel groovy main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Fri, 18 Jun 2021 04:53:33 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:0166ff847fb08131d71f07d323c9814e7b7a658fabac8a5c3f07c7aa6e645460`  
		Last Modified: Thu, 17 Jun 2021 23:33:17 GMT  
		Size: 31.3 MB (31341655 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef5dc98630f1369b2b872c0f1433ee2264d024f77446e28c7ef0774320e53c72`  
		Last Modified: Fri, 18 Jun 2021 04:55:43 GMT  
		Size: 5.6 MB (5596604 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae632bbd84a049abf2e2b4c8de52b512d6a67261847ca558f1210f0cf549d49e`  
		Last Modified: Fri, 18 Jun 2021 04:55:42 GMT  
		Size: 1.8 KB (1764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:244285fe3e10b91f637478103b43cb3d726a844ea1fef7996911f74b75253171`  
		Last Modified: Fri, 18 Jun 2021 04:55:42 GMT  
		Size: 246.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b3df898e191dd5efbb4f30a12b4e1f94a74f1f6d0fdfd02b04d2322dee467e1`  
		Last Modified: Fri, 18 Jun 2021 04:55:42 GMT  
		Size: 255.7 KB (255681 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:groovy-non-free`

```console
$ docker pull neurodebian@sha256:d3ced1cd9e0a5f0e7621ca2ee50dce3f167c1609e44ed8f786f13a3e397726c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `neurodebian:groovy-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:89ba9aed80e6a2bd02ed99ae3b0fc1df099d4a148448dd17f4945cca583a9358
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.2 MB (37196210 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c162c7323f4dacbf0b562461152c03c25ea1abbf7bc42c8a92f19eb1a1278a9`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Jun 2021 23:31:36 GMT
ADD file:8fe6bbb03392c41fe275714978bd93f4c94d64366217e95415b50aa7edc3b7c8 in / 
# Thu, 17 Jun 2021 23:31:37 GMT
CMD ["bash"]
# Fri, 18 Jun 2021 04:53:26 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Fri, 18 Jun 2021 04:53:28 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Fri, 18 Jun 2021 04:53:28 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian groovy main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel groovy main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Fri, 18 Jun 2021 04:53:33 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Fri, 18 Jun 2021 04:53:43 GMT
RUN sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list; grep -q 'deb .* multiverse$' /etc/apt/sources.list || sed -i -e 's,universe *$,universe multiverse,g' /etc/apt/sources.list
```

-	Layers:
	-	`sha256:0166ff847fb08131d71f07d323c9814e7b7a658fabac8a5c3f07c7aa6e645460`  
		Last Modified: Thu, 17 Jun 2021 23:33:17 GMT  
		Size: 31.3 MB (31341655 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef5dc98630f1369b2b872c0f1433ee2264d024f77446e28c7ef0774320e53c72`  
		Last Modified: Fri, 18 Jun 2021 04:55:43 GMT  
		Size: 5.6 MB (5596604 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae632bbd84a049abf2e2b4c8de52b512d6a67261847ca558f1210f0cf549d49e`  
		Last Modified: Fri, 18 Jun 2021 04:55:42 GMT  
		Size: 1.8 KB (1764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:244285fe3e10b91f637478103b43cb3d726a844ea1fef7996911f74b75253171`  
		Last Modified: Fri, 18 Jun 2021 04:55:42 GMT  
		Size: 246.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b3df898e191dd5efbb4f30a12b4e1f94a74f1f6d0fdfd02b04d2322dee467e1`  
		Last Modified: Fri, 18 Jun 2021 04:55:42 GMT  
		Size: 255.7 KB (255681 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b6fb413d592ee23f758ed31d23e18e4415927a320ca525a6384358364051a76`  
		Last Modified: Fri, 18 Jun 2021 04:55:53 GMT  
		Size: 260.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:latest`

```console
$ docker pull neurodebian@sha256:be75a622593d46b0c85c0dc55774436eb29a9b7b205c4228aaadfc7fdbe5fe89
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `neurodebian:latest` - linux; amd64

```console
$ docker pull neurodebian@sha256:b0fb9b986cdbacd0afaab5e742974bd3ef153dd73840d547ed841c41b5c4a768
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.2 MB (61237937 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a14430ab3dcd893dccbf9811e9c3825c96cc4fe29ed53702417e21f7324e4f77`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 May 2021 01:21:03 GMT
ADD file:1a1eae7a82c66d673971436ce2605e97d107e2934b7cdec876c64923ae6f4f85 in / 
# Wed, 12 May 2021 01:21:03 GMT
CMD ["bash"]
# Wed, 12 May 2021 08:15:25 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Wed, 12 May 2021 08:15:26 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Wed, 12 May 2021 08:15:27 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian buster main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel buster main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Wed, 12 May 2021 08:15:32 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:d960726af2bec62a87ceb07182f7b94c47be03909077e23d8226658f80b47f87`  
		Last Modified: Wed, 12 May 2021 01:26:49 GMT  
		Size: 50.4 MB (50433242 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a89553ed3a7797659596b70fac74c996633d5f2cecd4360db1b6bc5aa81131d`  
		Last Modified: Wed, 12 May 2021 08:17:32 GMT  
		Size: 10.5 MB (10499972 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32e2547b1380c9d77ce3ac458d0a28697a7064cda03c6239d421c365ab088738`  
		Last Modified: Wed, 12 May 2021 08:17:31 GMT  
		Size: 1.8 KB (1762 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40ba78ab5ae2bf7a1da1a747d895310235c2d28fa0a66c0eef0228e57d35e547`  
		Last Modified: Wed, 12 May 2021 08:17:31 GMT  
		Size: 246.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81703386770e4978fe71acaf5810bd4542e8e9fb5a7ed87bd780399f6885fddf`  
		Last Modified: Wed, 12 May 2021 08:17:32 GMT  
		Size: 302.7 KB (302715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:nd`

```console
$ docker pull neurodebian@sha256:a7837f3e1fa8ddb0e990ff95f60ef492335b704dc329d7e12bd68854399eb1e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `neurodebian:nd` - linux; amd64

```console
$ docker pull neurodebian@sha256:ddb092b2331787edfd0af3d4b4e528328da48691ae71b8b1baccbe8bbaebb0c9
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.5 MB (66518353 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:606f43da98b618c3f2d43c8187dccf688e86da2f44abe582bd1684592b4f9523`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 May 2021 01:22:07 GMT
ADD file:b00402c4b2c5828b18b251f8a057510f9f7da733f833cd147ed1a8fcb8d574db in / 
# Wed, 12 May 2021 01:22:08 GMT
CMD ["bash"]
# Wed, 12 May 2021 08:16:11 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Wed, 12 May 2021 08:16:12 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Wed, 12 May 2021 08:16:13 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian sid main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Wed, 12 May 2021 08:16:17 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:d2746b657344bbd3149c23794266413a61b32b44f53688f3619e485894c87b09`  
		Last Modified: Wed, 12 May 2021 01:28:33 GMT  
		Size: 54.9 MB (54896691 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db24a845c6c5719feb645b6c40fc3b9ad68b478ee8f445438bb62ff239ce8c70`  
		Last Modified: Wed, 12 May 2021 08:18:23 GMT  
		Size: 11.3 MB (11309128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c809501e4bc2c38d8a90b9796e38b490408f53254f3d5fe0193dc1ec1e21711b`  
		Last Modified: Wed, 12 May 2021 08:18:20 GMT  
		Size: 1.8 KB (1760 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bee38428ade9f57f57507e89a9f0528339d2c6272bf80b7731266137c46b5f0`  
		Last Modified: Wed, 12 May 2021 08:18:20 GMT  
		Size: 243.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6df1b9768570a2168e04e6ace7e4a069e395c92065be4a06b0f2151f1d5332e`  
		Last Modified: Wed, 12 May 2021 08:18:20 GMT  
		Size: 310.5 KB (310531 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:nd-non-free`

```console
$ docker pull neurodebian@sha256:f5c6e4042009f687bade218a8f71a5dbcadc81d8fabbe809e7cf56e265fecaba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `neurodebian:nd-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:e37edbb41084fc7cad5cf7858111dbe5bafe96367d6c1442f7df28cac9c60468
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.5 MB (66518669 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:edee8c8f44dc50696cb75a754df72be810183d0b714da99792b61597250d3348`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 May 2021 01:22:07 GMT
ADD file:b00402c4b2c5828b18b251f8a057510f9f7da733f833cd147ed1a8fcb8d574db in / 
# Wed, 12 May 2021 01:22:08 GMT
CMD ["bash"]
# Wed, 12 May 2021 08:16:11 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Wed, 12 May 2021 08:16:12 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Wed, 12 May 2021 08:16:13 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian sid main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Wed, 12 May 2021 08:16:17 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Wed, 12 May 2021 08:16:23 GMT
RUN sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list /etc/apt/sources.list
```

-	Layers:
	-	`sha256:d2746b657344bbd3149c23794266413a61b32b44f53688f3619e485894c87b09`  
		Last Modified: Wed, 12 May 2021 01:28:33 GMT  
		Size: 54.9 MB (54896691 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db24a845c6c5719feb645b6c40fc3b9ad68b478ee8f445438bb62ff239ce8c70`  
		Last Modified: Wed, 12 May 2021 08:18:23 GMT  
		Size: 11.3 MB (11309128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c809501e4bc2c38d8a90b9796e38b490408f53254f3d5fe0193dc1ec1e21711b`  
		Last Modified: Wed, 12 May 2021 08:18:20 GMT  
		Size: 1.8 KB (1760 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bee38428ade9f57f57507e89a9f0528339d2c6272bf80b7731266137c46b5f0`  
		Last Modified: Wed, 12 May 2021 08:18:20 GMT  
		Size: 243.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6df1b9768570a2168e04e6ace7e4a069e395c92065be4a06b0f2151f1d5332e`  
		Last Modified: Wed, 12 May 2021 08:18:20 GMT  
		Size: 310.5 KB (310531 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8dece18eb17ef9146aa947cb890d9516a479b256caea0df9eb98bd9b27f9cd77`  
		Last Modified: Wed, 12 May 2021 08:18:33 GMT  
		Size: 316.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:nd100`

```console
$ docker pull neurodebian@sha256:be75a622593d46b0c85c0dc55774436eb29a9b7b205c4228aaadfc7fdbe5fe89
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `neurodebian:nd100` - linux; amd64

```console
$ docker pull neurodebian@sha256:b0fb9b986cdbacd0afaab5e742974bd3ef153dd73840d547ed841c41b5c4a768
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.2 MB (61237937 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a14430ab3dcd893dccbf9811e9c3825c96cc4fe29ed53702417e21f7324e4f77`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 May 2021 01:21:03 GMT
ADD file:1a1eae7a82c66d673971436ce2605e97d107e2934b7cdec876c64923ae6f4f85 in / 
# Wed, 12 May 2021 01:21:03 GMT
CMD ["bash"]
# Wed, 12 May 2021 08:15:25 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Wed, 12 May 2021 08:15:26 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Wed, 12 May 2021 08:15:27 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian buster main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel buster main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Wed, 12 May 2021 08:15:32 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:d960726af2bec62a87ceb07182f7b94c47be03909077e23d8226658f80b47f87`  
		Last Modified: Wed, 12 May 2021 01:26:49 GMT  
		Size: 50.4 MB (50433242 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a89553ed3a7797659596b70fac74c996633d5f2cecd4360db1b6bc5aa81131d`  
		Last Modified: Wed, 12 May 2021 08:17:32 GMT  
		Size: 10.5 MB (10499972 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32e2547b1380c9d77ce3ac458d0a28697a7064cda03c6239d421c365ab088738`  
		Last Modified: Wed, 12 May 2021 08:17:31 GMT  
		Size: 1.8 KB (1762 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40ba78ab5ae2bf7a1da1a747d895310235c2d28fa0a66c0eef0228e57d35e547`  
		Last Modified: Wed, 12 May 2021 08:17:31 GMT  
		Size: 246.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81703386770e4978fe71acaf5810bd4542e8e9fb5a7ed87bd780399f6885fddf`  
		Last Modified: Wed, 12 May 2021 08:17:32 GMT  
		Size: 302.7 KB (302715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:nd100-non-free`

```console
$ docker pull neurodebian@sha256:c50965f97971d78ba53f4987c2df17ced4c4d421fffaa849e9c5dce778aad9a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `neurodebian:nd100-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:595f1244408ebd2102c8e0c63f7adcb8c0d6a2a5cd77b68ea79925ee278a8b6a
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.2 MB (61238302 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de43c9d8833440ec409d45392795fe6df36f09be60f866657adc5672006e46e4`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 May 2021 01:21:03 GMT
ADD file:1a1eae7a82c66d673971436ce2605e97d107e2934b7cdec876c64923ae6f4f85 in / 
# Wed, 12 May 2021 01:21:03 GMT
CMD ["bash"]
# Wed, 12 May 2021 08:15:25 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Wed, 12 May 2021 08:15:26 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Wed, 12 May 2021 08:15:27 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian buster main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel buster main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Wed, 12 May 2021 08:15:32 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Wed, 12 May 2021 08:15:38 GMT
RUN sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list /etc/apt/sources.list
```

-	Layers:
	-	`sha256:d960726af2bec62a87ceb07182f7b94c47be03909077e23d8226658f80b47f87`  
		Last Modified: Wed, 12 May 2021 01:26:49 GMT  
		Size: 50.4 MB (50433242 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a89553ed3a7797659596b70fac74c996633d5f2cecd4360db1b6bc5aa81131d`  
		Last Modified: Wed, 12 May 2021 08:17:32 GMT  
		Size: 10.5 MB (10499972 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32e2547b1380c9d77ce3ac458d0a28697a7064cda03c6239d421c365ab088738`  
		Last Modified: Wed, 12 May 2021 08:17:31 GMT  
		Size: 1.8 KB (1762 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40ba78ab5ae2bf7a1da1a747d895310235c2d28fa0a66c0eef0228e57d35e547`  
		Last Modified: Wed, 12 May 2021 08:17:31 GMT  
		Size: 246.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81703386770e4978fe71acaf5810bd4542e8e9fb5a7ed87bd780399f6885fddf`  
		Last Modified: Wed, 12 May 2021 08:17:32 GMT  
		Size: 302.7 KB (302715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3269028ef6dfd1b263a7462e2cb26492f38f42e54fab284dba145e8dcd5806c`  
		Last Modified: Wed, 12 May 2021 08:17:45 GMT  
		Size: 365.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:nd110`

```console
$ docker pull neurodebian@sha256:37a70a1d18f74cc00a14aefd2e6f2fff9afd2b8d7e26ea63252422b95e77286f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `neurodebian:nd110` - linux; amd64

```console
$ docker pull neurodebian@sha256:d3f45dffd49a2b162a4e01edaa391cac11585ef1570f877d83cbc7c39c9d5c58
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.5 MB (66519150 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9956cb29636d21fc4de6593382fe3a75f61eb7e8811d2145baab1c230630a2a6`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 May 2021 01:20:32 GMT
ADD file:22ed184e421fcac775f322850c24589ef2e78ddd12900395d44b2ea74220a62e in / 
# Wed, 12 May 2021 01:20:33 GMT
CMD ["bash"]
# Wed, 12 May 2021 08:15:49 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Wed, 12 May 2021 08:15:50 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Wed, 12 May 2021 08:15:51 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bullseye main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Wed, 12 May 2021 08:15:55 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:ad4592a9cb6deb788f794c7bc60f66d77280e79869f13e9eccbf34e1d381b95d`  
		Last Modified: Wed, 12 May 2021 01:26:05 GMT  
		Size: 54.9 MB (54897696 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8542129608a42399bc292c1994a3f2340d165d1040e98a2bf563841e5a3eebb2`  
		Last Modified: Wed, 12 May 2021 08:18:00 GMT  
		Size: 11.3 MB (11308850 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f358d6314ea033af895f5aebc4724359a9aa401aa672cc401d584a2465387aac`  
		Last Modified: Wed, 12 May 2021 08:17:58 GMT  
		Size: 1.8 KB (1762 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e876a28d30789565f8fb5724aa6186e85e0ec5d722e4e45ad3d6ea02b2cb4fc8`  
		Last Modified: Wed, 12 May 2021 08:17:58 GMT  
		Size: 248.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bab1c0263bda33d4f321fe0ed47941aa2373f4d0a6068478b03cf7f78d9820c`  
		Last Modified: Wed, 12 May 2021 08:17:59 GMT  
		Size: 310.6 KB (310594 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:nd110-non-free`

```console
$ docker pull neurodebian@sha256:3c00f7abc74c5bbd7c80c41a5056a3b86f737b0bef1090404d3e6fc0602a9291
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `neurodebian:nd110-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:5ac0bd054e017dd1fdb6ad359e849c6b895a05010522d81c0cfe950f6e94ee43
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.5 MB (66519517 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ed86d8135cd289d5987ae2871c1cf8750f28e606e25a625a9627d58eb602a48`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 May 2021 01:20:32 GMT
ADD file:22ed184e421fcac775f322850c24589ef2e78ddd12900395d44b2ea74220a62e in / 
# Wed, 12 May 2021 01:20:33 GMT
CMD ["bash"]
# Wed, 12 May 2021 08:15:49 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Wed, 12 May 2021 08:15:50 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Wed, 12 May 2021 08:15:51 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bullseye main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Wed, 12 May 2021 08:15:55 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Wed, 12 May 2021 08:16:00 GMT
RUN sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list /etc/apt/sources.list
```

-	Layers:
	-	`sha256:ad4592a9cb6deb788f794c7bc60f66d77280e79869f13e9eccbf34e1d381b95d`  
		Last Modified: Wed, 12 May 2021 01:26:05 GMT  
		Size: 54.9 MB (54897696 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8542129608a42399bc292c1994a3f2340d165d1040e98a2bf563841e5a3eebb2`  
		Last Modified: Wed, 12 May 2021 08:18:00 GMT  
		Size: 11.3 MB (11308850 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f358d6314ea033af895f5aebc4724359a9aa401aa672cc401d584a2465387aac`  
		Last Modified: Wed, 12 May 2021 08:17:58 GMT  
		Size: 1.8 KB (1762 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e876a28d30789565f8fb5724aa6186e85e0ec5d722e4e45ad3d6ea02b2cb4fc8`  
		Last Modified: Wed, 12 May 2021 08:17:58 GMT  
		Size: 248.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bab1c0263bda33d4f321fe0ed47941aa2373f4d0a6068478b03cf7f78d9820c`  
		Last Modified: Wed, 12 May 2021 08:17:59 GMT  
		Size: 310.6 KB (310594 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d8e264ceb5b955edcc0b63ff38202b1f0ac04026f3f14b151f524409a442e09`  
		Last Modified: Wed, 12 May 2021 08:18:10 GMT  
		Size: 367.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:nd16.04`

```console
$ docker pull neurodebian@sha256:706422ad8751b16d4421f5c37474d10da64d708f89d0d19eae16587c32b2a0b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `neurodebian:nd16.04` - linux; amd64

```console
$ docker pull neurodebian@sha256:4471dff78eb2b61d7c0fe05c386984cee1ecffe25994d149995dd32d4c77900f
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.7 MB (46728844 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e81ebe285f4f396273f6e8f2b6ef3ef3f9e05f6fa87a6d16ffb9e12ce02da140`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 17 Jun 2021 23:32:06 GMT
ADD file:4dd75f16753c9c921fd05b1d0ed5b425d74d87405a76a0b3afcbf9723a50d1ce in / 
# Thu, 17 Jun 2021 23:32:07 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 17 Jun 2021 23:32:08 GMT
RUN rm -rf /var/lib/apt/lists/*
# Thu, 17 Jun 2021 23:32:09 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 17 Jun 2021 23:32:09 GMT
CMD ["/bin/bash"]
# Fri, 18 Jun 2021 04:51:46 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Fri, 18 Jun 2021 04:51:47 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Fri, 18 Jun 2021 04:51:48 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian xenial main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel xenial main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Fri, 18 Jun 2021 04:51:53 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:61e03ba1d4149ac4eb681c6bf75aef8ac4b3f0d6fbb08e9623c4089889396fc8`  
		Last Modified: Sat, 12 Jun 2021 00:25:16 GMT  
		Size: 46.5 MB (46496785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4afb39f216bd4e336f9b78584bae0f6bcb77150107471d8d67d3b8abfbdea46a`  
		Last Modified: Thu, 17 Jun 2021 23:34:09 GMT  
		Size: 849.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e489abdc9f902f737bfef2c0c7ff5c35ca9b3ca11e73405a472f31a25f2dcc69`  
		Last Modified: Thu, 17 Jun 2021 23:34:08 GMT  
		Size: 528.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:999fff7bcc2450fcf1210182802f3907e35cd7cf7569568bd2a179b9144d9c57`  
		Last Modified: Thu, 17 Jun 2021 23:34:08 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f27db3f87344ee4f403c5257877584f0b0319c19914fa2953e351715240aa547`  
		Last Modified: Fri, 18 Jun 2021 04:54:39 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05d325b9a44fc4bfd2ef838143c6afeeed1fbf4929cc69351b13790404151baf`  
		Last Modified: Fri, 18 Jun 2021 04:54:39 GMT  
		Size: 3.1 KB (3150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45a309011e84c623c2b39ed13ff0f62d5c0f40e9ae798cdf37fba510c34711c6`  
		Last Modified: Fri, 18 Jun 2021 04:54:39 GMT  
		Size: 248.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ea488f510caf428861b3edf4b32605992b348a0f4ec00ee2e81a581d8e80f80`  
		Last Modified: Fri, 18 Jun 2021 04:54:39 GMT  
		Size: 226.9 KB (226939 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:nd16.04-non-free`

```console
$ docker pull neurodebian@sha256:937cdaf8ad5054fd931a11a6bb0a8b4c0840a0a115540e98879ea449f69e1dbf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `neurodebian:nd16.04-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:0041163886c00bd41f9d9eaf5748fbc5b2e178e4d191beb751fb7e2659256870
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.7 MB (46729101 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:816d85192005dbf8618fa9b54d5b0ae148f0cf0104fb9268b604dad9648aa060`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 17 Jun 2021 23:32:06 GMT
ADD file:4dd75f16753c9c921fd05b1d0ed5b425d74d87405a76a0b3afcbf9723a50d1ce in / 
# Thu, 17 Jun 2021 23:32:07 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 17 Jun 2021 23:32:08 GMT
RUN rm -rf /var/lib/apt/lists/*
# Thu, 17 Jun 2021 23:32:09 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 17 Jun 2021 23:32:09 GMT
CMD ["/bin/bash"]
# Fri, 18 Jun 2021 04:51:46 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Fri, 18 Jun 2021 04:51:47 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Fri, 18 Jun 2021 04:51:48 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian xenial main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel xenial main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Fri, 18 Jun 2021 04:51:53 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Fri, 18 Jun 2021 04:51:57 GMT
RUN sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list; grep -q 'deb .* multiverse$' /etc/apt/sources.list || sed -i -e 's,universe *$,universe multiverse,g' /etc/apt/sources.list
```

-	Layers:
	-	`sha256:61e03ba1d4149ac4eb681c6bf75aef8ac4b3f0d6fbb08e9623c4089889396fc8`  
		Last Modified: Sat, 12 Jun 2021 00:25:16 GMT  
		Size: 46.5 MB (46496785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4afb39f216bd4e336f9b78584bae0f6bcb77150107471d8d67d3b8abfbdea46a`  
		Last Modified: Thu, 17 Jun 2021 23:34:09 GMT  
		Size: 849.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e489abdc9f902f737bfef2c0c7ff5c35ca9b3ca11e73405a472f31a25f2dcc69`  
		Last Modified: Thu, 17 Jun 2021 23:34:08 GMT  
		Size: 528.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:999fff7bcc2450fcf1210182802f3907e35cd7cf7569568bd2a179b9144d9c57`  
		Last Modified: Thu, 17 Jun 2021 23:34:08 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f27db3f87344ee4f403c5257877584f0b0319c19914fa2953e351715240aa547`  
		Last Modified: Fri, 18 Jun 2021 04:54:39 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05d325b9a44fc4bfd2ef838143c6afeeed1fbf4929cc69351b13790404151baf`  
		Last Modified: Fri, 18 Jun 2021 04:54:39 GMT  
		Size: 3.1 KB (3150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45a309011e84c623c2b39ed13ff0f62d5c0f40e9ae798cdf37fba510c34711c6`  
		Last Modified: Fri, 18 Jun 2021 04:54:39 GMT  
		Size: 248.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ea488f510caf428861b3edf4b32605992b348a0f4ec00ee2e81a581d8e80f80`  
		Last Modified: Fri, 18 Jun 2021 04:54:39 GMT  
		Size: 226.9 KB (226939 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e901921b5a6b1c35d7c4d2819f403cac6c89c2165b3d2c26ed9a7741007b3aae`  
		Last Modified: Fri, 18 Jun 2021 04:54:51 GMT  
		Size: 257.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:nd18.04`

```console
$ docker pull neurodebian@sha256:db216a15ee6f153fa278e74ec41018677ccd2e7b6601cae05b70ee12df8e5262
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `neurodebian:nd18.04` - linux; amd64

```console
$ docker pull neurodebian@sha256:4571610dba14a3148eab203c2968f8aa1b51a4cc11fdf4c0d6b705d46f2848bf
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.8 MB (31758477 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83cafc4228b65934b0fa1c7219c2807081de2aafb130446bf27e111327c35e30`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Jun 2021 23:31:22 GMT
ADD file:900f735ff138e5137cf25ddd85a32a01921ebec26d86704d24b5f12e73a832c2 in / 
# Thu, 17 Jun 2021 23:31:22 GMT
CMD ["bash"]
# Fri, 18 Jun 2021 04:52:11 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Fri, 18 Jun 2021 04:52:13 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Fri, 18 Jun 2021 04:52:14 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bionic main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bionic main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Fri, 18 Jun 2021 04:52:19 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:25fa05cd42bd8fabb25d2a6f3f8c9f7ab34637903d00fd2ed1c1d0fa980427dd`  
		Last Modified: Thu, 17 Jun 2021 23:32:41 GMT  
		Size: 26.7 MB (26700706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a372806eca722b9500ca1c252a350a3e0441d81be91618655d70abc45dad7d12`  
		Last Modified: Fri, 18 Jun 2021 04:55:02 GMT  
		Size: 4.8 MB (4813844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:182b5f8f7126262ff9cee76fb70a5d94c2164b9d04d38f3f4921426d6a808244`  
		Last Modified: Fri, 18 Jun 2021 04:55:01 GMT  
		Size: 3.2 KB (3152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3986bc512fe32c67789ba6b338b2c23b00719f03a9619bd4e5427b03ef79346`  
		Last Modified: Fri, 18 Jun 2021 04:55:01 GMT  
		Size: 244.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3285e935d5c30552d33396c6914b9f8181419e461b918cc75419eb56584526d3`  
		Last Modified: Fri, 18 Jun 2021 04:55:01 GMT  
		Size: 240.5 KB (240531 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:nd18.04-non-free`

```console
$ docker pull neurodebian@sha256:137643bf32def556edce8ffbba26060623f95319e4a2d74d96fc6c0bb30d1e30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `neurodebian:nd18.04-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:0cd189273525767046fb18bb92c66839ba0c8994c93f48d36fc8660e77503f59
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.8 MB (31758733 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d96912b660ca96bd8bbbe6a08237f9bd013262c9fc3db7a2a7900e424acc56d`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Jun 2021 23:31:22 GMT
ADD file:900f735ff138e5137cf25ddd85a32a01921ebec26d86704d24b5f12e73a832c2 in / 
# Thu, 17 Jun 2021 23:31:22 GMT
CMD ["bash"]
# Fri, 18 Jun 2021 04:52:11 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Fri, 18 Jun 2021 04:52:13 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Fri, 18 Jun 2021 04:52:14 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bionic main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bionic main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Fri, 18 Jun 2021 04:52:19 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Fri, 18 Jun 2021 04:52:27 GMT
RUN sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list; grep -q 'deb .* multiverse$' /etc/apt/sources.list || sed -i -e 's,universe *$,universe multiverse,g' /etc/apt/sources.list
```

-	Layers:
	-	`sha256:25fa05cd42bd8fabb25d2a6f3f8c9f7ab34637903d00fd2ed1c1d0fa980427dd`  
		Last Modified: Thu, 17 Jun 2021 23:32:41 GMT  
		Size: 26.7 MB (26700706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a372806eca722b9500ca1c252a350a3e0441d81be91618655d70abc45dad7d12`  
		Last Modified: Fri, 18 Jun 2021 04:55:02 GMT  
		Size: 4.8 MB (4813844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:182b5f8f7126262ff9cee76fb70a5d94c2164b9d04d38f3f4921426d6a808244`  
		Last Modified: Fri, 18 Jun 2021 04:55:01 GMT  
		Size: 3.2 KB (3152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3986bc512fe32c67789ba6b338b2c23b00719f03a9619bd4e5427b03ef79346`  
		Last Modified: Fri, 18 Jun 2021 04:55:01 GMT  
		Size: 244.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3285e935d5c30552d33396c6914b9f8181419e461b918cc75419eb56584526d3`  
		Last Modified: Fri, 18 Jun 2021 04:55:01 GMT  
		Size: 240.5 KB (240531 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1ca3f59ea90b8f2dae868601d0485c3d456b3f511ba70fe32d1c8ea82d12b0f`  
		Last Modified: Fri, 18 Jun 2021 04:55:12 GMT  
		Size: 256.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:nd20.04`

```console
$ docker pull neurodebian@sha256:4c455036d37f289095299df3a4bd0e8f300d4d0ee2c886062534ebb3442a9f7e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `neurodebian:nd20.04` - linux; amd64

```console
$ docker pull neurodebian@sha256:629c1e71294f3d83f64e640a5df834ca5c75274d36114803f07f7c273a721d4f
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.3 MB (34282594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a5707c344a0d6620e7086d356540cca35678d627c9ea94dae40997250bfc52b`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Jun 2021 23:31:29 GMT
ADD file:920cf788d1ba88f76c97e41e03e4dc2f3005b08d65b5e9da9dd1cbe20a74459b in / 
# Thu, 17 Jun 2021 23:31:29 GMT
CMD ["bash"]
# Fri, 18 Jun 2021 04:52:37 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Fri, 18 Jun 2021 04:52:38 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Fri, 18 Jun 2021 04:52:39 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian focal main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel focal main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Fri, 18 Jun 2021 04:52:44 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:c549ccf8d472c3bce9ce02e49c62b8f6cbc736ea2b8ba812a1ae9390c69d0b71`  
		Last Modified: Thu, 17 Jun 2021 23:32:58 GMT  
		Size: 28.6 MB (28553692 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc4a77e48a4e30ad5b9a0e8f57a8941b5e4afd803b768a118af1f4395e9af730`  
		Last Modified: Fri, 18 Jun 2021 04:55:23 GMT  
		Size: 5.5 MB (5488782 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2bc8c0b52966c29981f450a633c9e42cd66d2bc21ed88bdbb4bc8725848587c`  
		Last Modified: Fri, 18 Jun 2021 04:55:22 GMT  
		Size: 1.8 KB (1763 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c875b70270f67ed702580b6ff4c2fbcb6e07be3081b0884904af67c78aa811f`  
		Last Modified: Fri, 18 Jun 2021 04:55:22 GMT  
		Size: 245.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0629f8de5ae05b122171d9e1b056f0723c06414eef890d5630081aa0b06dcbe5`  
		Last Modified: Fri, 18 Jun 2021 04:55:22 GMT  
		Size: 238.1 KB (238112 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:nd20.04-non-free`

```console
$ docker pull neurodebian@sha256:839119d3149fdabb9757dba9e8c8d2e4da0f3d6ff2cf67b5235a059bc629bbec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `neurodebian:nd20.04-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:01e7915db023a737a56340dfe2fd95399210a85cc559374bc806d7bf55019d1b
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.3 MB (34282848 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f34fd1463d4c93e9554eb0926150b053f9b203c8d6b7451fb624faf1139dd84a`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Jun 2021 23:31:29 GMT
ADD file:920cf788d1ba88f76c97e41e03e4dc2f3005b08d65b5e9da9dd1cbe20a74459b in / 
# Thu, 17 Jun 2021 23:31:29 GMT
CMD ["bash"]
# Fri, 18 Jun 2021 04:52:37 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Fri, 18 Jun 2021 04:52:38 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Fri, 18 Jun 2021 04:52:39 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian focal main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel focal main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Fri, 18 Jun 2021 04:52:44 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Fri, 18 Jun 2021 04:52:49 GMT
RUN sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list; grep -q 'deb .* multiverse$' /etc/apt/sources.list || sed -i -e 's,universe *$,universe multiverse,g' /etc/apt/sources.list
```

-	Layers:
	-	`sha256:c549ccf8d472c3bce9ce02e49c62b8f6cbc736ea2b8ba812a1ae9390c69d0b71`  
		Last Modified: Thu, 17 Jun 2021 23:32:58 GMT  
		Size: 28.6 MB (28553692 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc4a77e48a4e30ad5b9a0e8f57a8941b5e4afd803b768a118af1f4395e9af730`  
		Last Modified: Fri, 18 Jun 2021 04:55:23 GMT  
		Size: 5.5 MB (5488782 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2bc8c0b52966c29981f450a633c9e42cd66d2bc21ed88bdbb4bc8725848587c`  
		Last Modified: Fri, 18 Jun 2021 04:55:22 GMT  
		Size: 1.8 KB (1763 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c875b70270f67ed702580b6ff4c2fbcb6e07be3081b0884904af67c78aa811f`  
		Last Modified: Fri, 18 Jun 2021 04:55:22 GMT  
		Size: 245.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0629f8de5ae05b122171d9e1b056f0723c06414eef890d5630081aa0b06dcbe5`  
		Last Modified: Fri, 18 Jun 2021 04:55:22 GMT  
		Size: 238.1 KB (238112 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c11f19f52782c866f0af53b6f977420b5fce2df64080ac5c2a1c45a7b530a39d`  
		Last Modified: Fri, 18 Jun 2021 04:55:32 GMT  
		Size: 254.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:nd20.10`

```console
$ docker pull neurodebian@sha256:52eef91cf9255c211253782c7e20ffa03412e4574a6e6f1c1d1363a613d9b10e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `neurodebian:nd20.10` - linux; amd64

```console
$ docker pull neurodebian@sha256:3d68604aebecfc0a701d12a8e822856e7488a783c5ff297d2632beed20ce03bd
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.2 MB (37195950 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49280897b29663747cd44465424ff0fe54a56cf77de43aa4930923cdad07e75b`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Jun 2021 23:31:36 GMT
ADD file:8fe6bbb03392c41fe275714978bd93f4c94d64366217e95415b50aa7edc3b7c8 in / 
# Thu, 17 Jun 2021 23:31:37 GMT
CMD ["bash"]
# Fri, 18 Jun 2021 04:53:26 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Fri, 18 Jun 2021 04:53:28 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Fri, 18 Jun 2021 04:53:28 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian groovy main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel groovy main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Fri, 18 Jun 2021 04:53:33 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:0166ff847fb08131d71f07d323c9814e7b7a658fabac8a5c3f07c7aa6e645460`  
		Last Modified: Thu, 17 Jun 2021 23:33:17 GMT  
		Size: 31.3 MB (31341655 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef5dc98630f1369b2b872c0f1433ee2264d024f77446e28c7ef0774320e53c72`  
		Last Modified: Fri, 18 Jun 2021 04:55:43 GMT  
		Size: 5.6 MB (5596604 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae632bbd84a049abf2e2b4c8de52b512d6a67261847ca558f1210f0cf549d49e`  
		Last Modified: Fri, 18 Jun 2021 04:55:42 GMT  
		Size: 1.8 KB (1764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:244285fe3e10b91f637478103b43cb3d726a844ea1fef7996911f74b75253171`  
		Last Modified: Fri, 18 Jun 2021 04:55:42 GMT  
		Size: 246.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b3df898e191dd5efbb4f30a12b4e1f94a74f1f6d0fdfd02b04d2322dee467e1`  
		Last Modified: Fri, 18 Jun 2021 04:55:42 GMT  
		Size: 255.7 KB (255681 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:nd20.10-non-free`

```console
$ docker pull neurodebian@sha256:d3ced1cd9e0a5f0e7621ca2ee50dce3f167c1609e44ed8f786f13a3e397726c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `neurodebian:nd20.10-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:89ba9aed80e6a2bd02ed99ae3b0fc1df099d4a148448dd17f4945cca583a9358
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.2 MB (37196210 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c162c7323f4dacbf0b562461152c03c25ea1abbf7bc42c8a92f19eb1a1278a9`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Jun 2021 23:31:36 GMT
ADD file:8fe6bbb03392c41fe275714978bd93f4c94d64366217e95415b50aa7edc3b7c8 in / 
# Thu, 17 Jun 2021 23:31:37 GMT
CMD ["bash"]
# Fri, 18 Jun 2021 04:53:26 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Fri, 18 Jun 2021 04:53:28 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Fri, 18 Jun 2021 04:53:28 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian groovy main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel groovy main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Fri, 18 Jun 2021 04:53:33 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Fri, 18 Jun 2021 04:53:43 GMT
RUN sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list; grep -q 'deb .* multiverse$' /etc/apt/sources.list || sed -i -e 's,universe *$,universe multiverse,g' /etc/apt/sources.list
```

-	Layers:
	-	`sha256:0166ff847fb08131d71f07d323c9814e7b7a658fabac8a5c3f07c7aa6e645460`  
		Last Modified: Thu, 17 Jun 2021 23:33:17 GMT  
		Size: 31.3 MB (31341655 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef5dc98630f1369b2b872c0f1433ee2264d024f77446e28c7ef0774320e53c72`  
		Last Modified: Fri, 18 Jun 2021 04:55:43 GMT  
		Size: 5.6 MB (5596604 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae632bbd84a049abf2e2b4c8de52b512d6a67261847ca558f1210f0cf549d49e`  
		Last Modified: Fri, 18 Jun 2021 04:55:42 GMT  
		Size: 1.8 KB (1764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:244285fe3e10b91f637478103b43cb3d726a844ea1fef7996911f74b75253171`  
		Last Modified: Fri, 18 Jun 2021 04:55:42 GMT  
		Size: 246.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b3df898e191dd5efbb4f30a12b4e1f94a74f1f6d0fdfd02b04d2322dee467e1`  
		Last Modified: Fri, 18 Jun 2021 04:55:42 GMT  
		Size: 255.7 KB (255681 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b6fb413d592ee23f758ed31d23e18e4415927a320ca525a6384358364051a76`  
		Last Modified: Fri, 18 Jun 2021 04:55:53 GMT  
		Size: 260.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:nd90`

```console
$ docker pull neurodebian@sha256:4b97c82deed72389c4052aa75eaaa048e5b28f636eceec1eb70776d0e7821f64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `neurodebian:nd90` - linux; amd64

```console
$ docker pull neurodebian@sha256:72eac05435998a7f359292c309d08a618dc2fbe26887ec1791b9e547d4907fcc
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.2 MB (52247359 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e03187edcef353908b2bdadd1e4b61d32d4484482b03d9c3f9f39d25f76c9cfa`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 May 2021 01:23:05 GMT
ADD file:d9e4f6f4fc33703b766642a5642cabb2b01675bb55cf6050f2e91507577ff570 in / 
# Wed, 12 May 2021 01:23:06 GMT
CMD ["bash"]
# Wed, 12 May 2021 08:15:03 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Wed, 12 May 2021 08:15:06 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Wed, 12 May 2021 08:15:07 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian stretch main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel stretch main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Wed, 12 May 2021 08:15:11 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:bfde2ec33fbca3c74c6e91bca3fbcb22ed2972671d49a1accb7089c9473cac12`  
		Last Modified: Wed, 12 May 2021 01:29:52 GMT  
		Size: 45.4 MB (45380083 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6afb019c2cdada5ced6a5d8c0e92dfc64a75015bf2ac0b9ca078302f587ad240`  
		Last Modified: Wed, 12 May 2021 08:17:11 GMT  
		Size: 6.6 MB (6571645 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c15c2225322e6cad8f224ae7e54efb1e0e3a1fa8cba02dcc371cb32257083edc`  
		Last Modified: Wed, 12 May 2021 08:17:10 GMT  
		Size: 3.2 KB (3151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:083f71a07bc9af9c5fe060d284067e7c04d3264e12d35949b42e946ba348ec00`  
		Last Modified: Wed, 12 May 2021 08:17:10 GMT  
		Size: 245.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71f0c8861a586ebc9c9262242826f9747b7f4c99d4c9088c58f973159b669427`  
		Last Modified: Wed, 12 May 2021 08:17:10 GMT  
		Size: 292.2 KB (292235 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:nd90-non-free`

```console
$ docker pull neurodebian@sha256:0b0033d72732c1732cf01b36b49eef5c43ad4c92dc0bcd84e887b7600d92a60b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `neurodebian:nd90-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:c706cf7f6632205ff94eb09cf3d596b16450c7b20e1862ae68241c1bce73c2f4
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.2 MB (52247721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17351213dba5262ccb5486d56e45f253090683cdbd2ed33cef0077eb28363c56`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 May 2021 01:23:05 GMT
ADD file:d9e4f6f4fc33703b766642a5642cabb2b01675bb55cf6050f2e91507577ff570 in / 
# Wed, 12 May 2021 01:23:06 GMT
CMD ["bash"]
# Wed, 12 May 2021 08:15:03 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Wed, 12 May 2021 08:15:06 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Wed, 12 May 2021 08:15:07 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian stretch main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel stretch main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Wed, 12 May 2021 08:15:11 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Wed, 12 May 2021 08:15:15 GMT
RUN sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list /etc/apt/sources.list
```

-	Layers:
	-	`sha256:bfde2ec33fbca3c74c6e91bca3fbcb22ed2972671d49a1accb7089c9473cac12`  
		Last Modified: Wed, 12 May 2021 01:29:52 GMT  
		Size: 45.4 MB (45380083 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6afb019c2cdada5ced6a5d8c0e92dfc64a75015bf2ac0b9ca078302f587ad240`  
		Last Modified: Wed, 12 May 2021 08:17:11 GMT  
		Size: 6.6 MB (6571645 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c15c2225322e6cad8f224ae7e54efb1e0e3a1fa8cba02dcc371cb32257083edc`  
		Last Modified: Wed, 12 May 2021 08:17:10 GMT  
		Size: 3.2 KB (3151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:083f71a07bc9af9c5fe060d284067e7c04d3264e12d35949b42e946ba348ec00`  
		Last Modified: Wed, 12 May 2021 08:17:10 GMT  
		Size: 245.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71f0c8861a586ebc9c9262242826f9747b7f4c99d4c9088c58f973159b669427`  
		Last Modified: Wed, 12 May 2021 08:17:10 GMT  
		Size: 292.2 KB (292235 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6277d2d8506189054a12ed80685e5ff526c601c8ba04c9a51f666b27cf824db8`  
		Last Modified: Wed, 12 May 2021 08:17:21 GMT  
		Size: 362.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:non-free`

```console
$ docker pull neurodebian@sha256:c50965f97971d78ba53f4987c2df17ced4c4d421fffaa849e9c5dce778aad9a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `neurodebian:non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:595f1244408ebd2102c8e0c63f7adcb8c0d6a2a5cd77b68ea79925ee278a8b6a
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.2 MB (61238302 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de43c9d8833440ec409d45392795fe6df36f09be60f866657adc5672006e46e4`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 May 2021 01:21:03 GMT
ADD file:1a1eae7a82c66d673971436ce2605e97d107e2934b7cdec876c64923ae6f4f85 in / 
# Wed, 12 May 2021 01:21:03 GMT
CMD ["bash"]
# Wed, 12 May 2021 08:15:25 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Wed, 12 May 2021 08:15:26 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Wed, 12 May 2021 08:15:27 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian buster main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel buster main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Wed, 12 May 2021 08:15:32 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Wed, 12 May 2021 08:15:38 GMT
RUN sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list /etc/apt/sources.list
```

-	Layers:
	-	`sha256:d960726af2bec62a87ceb07182f7b94c47be03909077e23d8226658f80b47f87`  
		Last Modified: Wed, 12 May 2021 01:26:49 GMT  
		Size: 50.4 MB (50433242 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a89553ed3a7797659596b70fac74c996633d5f2cecd4360db1b6bc5aa81131d`  
		Last Modified: Wed, 12 May 2021 08:17:32 GMT  
		Size: 10.5 MB (10499972 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32e2547b1380c9d77ce3ac458d0a28697a7064cda03c6239d421c365ab088738`  
		Last Modified: Wed, 12 May 2021 08:17:31 GMT  
		Size: 1.8 KB (1762 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40ba78ab5ae2bf7a1da1a747d895310235c2d28fa0a66c0eef0228e57d35e547`  
		Last Modified: Wed, 12 May 2021 08:17:31 GMT  
		Size: 246.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81703386770e4978fe71acaf5810bd4542e8e9fb5a7ed87bd780399f6885fddf`  
		Last Modified: Wed, 12 May 2021 08:17:32 GMT  
		Size: 302.7 KB (302715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3269028ef6dfd1b263a7462e2cb26492f38f42e54fab284dba145e8dcd5806c`  
		Last Modified: Wed, 12 May 2021 08:17:45 GMT  
		Size: 365.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:sid`

```console
$ docker pull neurodebian@sha256:a7837f3e1fa8ddb0e990ff95f60ef492335b704dc329d7e12bd68854399eb1e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `neurodebian:sid` - linux; amd64

```console
$ docker pull neurodebian@sha256:ddb092b2331787edfd0af3d4b4e528328da48691ae71b8b1baccbe8bbaebb0c9
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.5 MB (66518353 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:606f43da98b618c3f2d43c8187dccf688e86da2f44abe582bd1684592b4f9523`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 May 2021 01:22:07 GMT
ADD file:b00402c4b2c5828b18b251f8a057510f9f7da733f833cd147ed1a8fcb8d574db in / 
# Wed, 12 May 2021 01:22:08 GMT
CMD ["bash"]
# Wed, 12 May 2021 08:16:11 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Wed, 12 May 2021 08:16:12 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Wed, 12 May 2021 08:16:13 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian sid main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Wed, 12 May 2021 08:16:17 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:d2746b657344bbd3149c23794266413a61b32b44f53688f3619e485894c87b09`  
		Last Modified: Wed, 12 May 2021 01:28:33 GMT  
		Size: 54.9 MB (54896691 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db24a845c6c5719feb645b6c40fc3b9ad68b478ee8f445438bb62ff239ce8c70`  
		Last Modified: Wed, 12 May 2021 08:18:23 GMT  
		Size: 11.3 MB (11309128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c809501e4bc2c38d8a90b9796e38b490408f53254f3d5fe0193dc1ec1e21711b`  
		Last Modified: Wed, 12 May 2021 08:18:20 GMT  
		Size: 1.8 KB (1760 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bee38428ade9f57f57507e89a9f0528339d2c6272bf80b7731266137c46b5f0`  
		Last Modified: Wed, 12 May 2021 08:18:20 GMT  
		Size: 243.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6df1b9768570a2168e04e6ace7e4a069e395c92065be4a06b0f2151f1d5332e`  
		Last Modified: Wed, 12 May 2021 08:18:20 GMT  
		Size: 310.5 KB (310531 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:sid-non-free`

```console
$ docker pull neurodebian@sha256:f5c6e4042009f687bade218a8f71a5dbcadc81d8fabbe809e7cf56e265fecaba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `neurodebian:sid-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:e37edbb41084fc7cad5cf7858111dbe5bafe96367d6c1442f7df28cac9c60468
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.5 MB (66518669 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:edee8c8f44dc50696cb75a754df72be810183d0b714da99792b61597250d3348`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 May 2021 01:22:07 GMT
ADD file:b00402c4b2c5828b18b251f8a057510f9f7da733f833cd147ed1a8fcb8d574db in / 
# Wed, 12 May 2021 01:22:08 GMT
CMD ["bash"]
# Wed, 12 May 2021 08:16:11 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Wed, 12 May 2021 08:16:12 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Wed, 12 May 2021 08:16:13 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian sid main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Wed, 12 May 2021 08:16:17 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Wed, 12 May 2021 08:16:23 GMT
RUN sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list /etc/apt/sources.list
```

-	Layers:
	-	`sha256:d2746b657344bbd3149c23794266413a61b32b44f53688f3619e485894c87b09`  
		Last Modified: Wed, 12 May 2021 01:28:33 GMT  
		Size: 54.9 MB (54896691 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db24a845c6c5719feb645b6c40fc3b9ad68b478ee8f445438bb62ff239ce8c70`  
		Last Modified: Wed, 12 May 2021 08:18:23 GMT  
		Size: 11.3 MB (11309128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c809501e4bc2c38d8a90b9796e38b490408f53254f3d5fe0193dc1ec1e21711b`  
		Last Modified: Wed, 12 May 2021 08:18:20 GMT  
		Size: 1.8 KB (1760 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bee38428ade9f57f57507e89a9f0528339d2c6272bf80b7731266137c46b5f0`  
		Last Modified: Wed, 12 May 2021 08:18:20 GMT  
		Size: 243.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6df1b9768570a2168e04e6ace7e4a069e395c92065be4a06b0f2151f1d5332e`  
		Last Modified: Wed, 12 May 2021 08:18:20 GMT  
		Size: 310.5 KB (310531 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8dece18eb17ef9146aa947cb890d9516a479b256caea0df9eb98bd9b27f9cd77`  
		Last Modified: Wed, 12 May 2021 08:18:33 GMT  
		Size: 316.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:stretch`

```console
$ docker pull neurodebian@sha256:4b97c82deed72389c4052aa75eaaa048e5b28f636eceec1eb70776d0e7821f64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `neurodebian:stretch` - linux; amd64

```console
$ docker pull neurodebian@sha256:72eac05435998a7f359292c309d08a618dc2fbe26887ec1791b9e547d4907fcc
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.2 MB (52247359 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e03187edcef353908b2bdadd1e4b61d32d4484482b03d9c3f9f39d25f76c9cfa`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 May 2021 01:23:05 GMT
ADD file:d9e4f6f4fc33703b766642a5642cabb2b01675bb55cf6050f2e91507577ff570 in / 
# Wed, 12 May 2021 01:23:06 GMT
CMD ["bash"]
# Wed, 12 May 2021 08:15:03 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Wed, 12 May 2021 08:15:06 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Wed, 12 May 2021 08:15:07 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian stretch main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel stretch main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Wed, 12 May 2021 08:15:11 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:bfde2ec33fbca3c74c6e91bca3fbcb22ed2972671d49a1accb7089c9473cac12`  
		Last Modified: Wed, 12 May 2021 01:29:52 GMT  
		Size: 45.4 MB (45380083 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6afb019c2cdada5ced6a5d8c0e92dfc64a75015bf2ac0b9ca078302f587ad240`  
		Last Modified: Wed, 12 May 2021 08:17:11 GMT  
		Size: 6.6 MB (6571645 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c15c2225322e6cad8f224ae7e54efb1e0e3a1fa8cba02dcc371cb32257083edc`  
		Last Modified: Wed, 12 May 2021 08:17:10 GMT  
		Size: 3.2 KB (3151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:083f71a07bc9af9c5fe060d284067e7c04d3264e12d35949b42e946ba348ec00`  
		Last Modified: Wed, 12 May 2021 08:17:10 GMT  
		Size: 245.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71f0c8861a586ebc9c9262242826f9747b7f4c99d4c9088c58f973159b669427`  
		Last Modified: Wed, 12 May 2021 08:17:10 GMT  
		Size: 292.2 KB (292235 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:stretch-non-free`

```console
$ docker pull neurodebian@sha256:0b0033d72732c1732cf01b36b49eef5c43ad4c92dc0bcd84e887b7600d92a60b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `neurodebian:stretch-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:c706cf7f6632205ff94eb09cf3d596b16450c7b20e1862ae68241c1bce73c2f4
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.2 MB (52247721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17351213dba5262ccb5486d56e45f253090683cdbd2ed33cef0077eb28363c56`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 May 2021 01:23:05 GMT
ADD file:d9e4f6f4fc33703b766642a5642cabb2b01675bb55cf6050f2e91507577ff570 in / 
# Wed, 12 May 2021 01:23:06 GMT
CMD ["bash"]
# Wed, 12 May 2021 08:15:03 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Wed, 12 May 2021 08:15:06 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Wed, 12 May 2021 08:15:07 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian stretch main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel stretch main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Wed, 12 May 2021 08:15:11 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Wed, 12 May 2021 08:15:15 GMT
RUN sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list /etc/apt/sources.list
```

-	Layers:
	-	`sha256:bfde2ec33fbca3c74c6e91bca3fbcb22ed2972671d49a1accb7089c9473cac12`  
		Last Modified: Wed, 12 May 2021 01:29:52 GMT  
		Size: 45.4 MB (45380083 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6afb019c2cdada5ced6a5d8c0e92dfc64a75015bf2ac0b9ca078302f587ad240`  
		Last Modified: Wed, 12 May 2021 08:17:11 GMT  
		Size: 6.6 MB (6571645 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c15c2225322e6cad8f224ae7e54efb1e0e3a1fa8cba02dcc371cb32257083edc`  
		Last Modified: Wed, 12 May 2021 08:17:10 GMT  
		Size: 3.2 KB (3151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:083f71a07bc9af9c5fe060d284067e7c04d3264e12d35949b42e946ba348ec00`  
		Last Modified: Wed, 12 May 2021 08:17:10 GMT  
		Size: 245.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71f0c8861a586ebc9c9262242826f9747b7f4c99d4c9088c58f973159b669427`  
		Last Modified: Wed, 12 May 2021 08:17:10 GMT  
		Size: 292.2 KB (292235 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6277d2d8506189054a12ed80685e5ff526c601c8ba04c9a51f666b27cf824db8`  
		Last Modified: Wed, 12 May 2021 08:17:21 GMT  
		Size: 362.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:xenial`

```console
$ docker pull neurodebian@sha256:706422ad8751b16d4421f5c37474d10da64d708f89d0d19eae16587c32b2a0b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `neurodebian:xenial` - linux; amd64

```console
$ docker pull neurodebian@sha256:4471dff78eb2b61d7c0fe05c386984cee1ecffe25994d149995dd32d4c77900f
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.7 MB (46728844 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e81ebe285f4f396273f6e8f2b6ef3ef3f9e05f6fa87a6d16ffb9e12ce02da140`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 17 Jun 2021 23:32:06 GMT
ADD file:4dd75f16753c9c921fd05b1d0ed5b425d74d87405a76a0b3afcbf9723a50d1ce in / 
# Thu, 17 Jun 2021 23:32:07 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 17 Jun 2021 23:32:08 GMT
RUN rm -rf /var/lib/apt/lists/*
# Thu, 17 Jun 2021 23:32:09 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 17 Jun 2021 23:32:09 GMT
CMD ["/bin/bash"]
# Fri, 18 Jun 2021 04:51:46 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Fri, 18 Jun 2021 04:51:47 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Fri, 18 Jun 2021 04:51:48 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian xenial main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel xenial main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Fri, 18 Jun 2021 04:51:53 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:61e03ba1d4149ac4eb681c6bf75aef8ac4b3f0d6fbb08e9623c4089889396fc8`  
		Last Modified: Sat, 12 Jun 2021 00:25:16 GMT  
		Size: 46.5 MB (46496785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4afb39f216bd4e336f9b78584bae0f6bcb77150107471d8d67d3b8abfbdea46a`  
		Last Modified: Thu, 17 Jun 2021 23:34:09 GMT  
		Size: 849.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e489abdc9f902f737bfef2c0c7ff5c35ca9b3ca11e73405a472f31a25f2dcc69`  
		Last Modified: Thu, 17 Jun 2021 23:34:08 GMT  
		Size: 528.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:999fff7bcc2450fcf1210182802f3907e35cd7cf7569568bd2a179b9144d9c57`  
		Last Modified: Thu, 17 Jun 2021 23:34:08 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f27db3f87344ee4f403c5257877584f0b0319c19914fa2953e351715240aa547`  
		Last Modified: Fri, 18 Jun 2021 04:54:39 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05d325b9a44fc4bfd2ef838143c6afeeed1fbf4929cc69351b13790404151baf`  
		Last Modified: Fri, 18 Jun 2021 04:54:39 GMT  
		Size: 3.1 KB (3150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45a309011e84c623c2b39ed13ff0f62d5c0f40e9ae798cdf37fba510c34711c6`  
		Last Modified: Fri, 18 Jun 2021 04:54:39 GMT  
		Size: 248.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ea488f510caf428861b3edf4b32605992b348a0f4ec00ee2e81a581d8e80f80`  
		Last Modified: Fri, 18 Jun 2021 04:54:39 GMT  
		Size: 226.9 KB (226939 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:xenial-non-free`

```console
$ docker pull neurodebian@sha256:937cdaf8ad5054fd931a11a6bb0a8b4c0840a0a115540e98879ea449f69e1dbf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `neurodebian:xenial-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:0041163886c00bd41f9d9eaf5748fbc5b2e178e4d191beb751fb7e2659256870
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.7 MB (46729101 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:816d85192005dbf8618fa9b54d5b0ae148f0cf0104fb9268b604dad9648aa060`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 17 Jun 2021 23:32:06 GMT
ADD file:4dd75f16753c9c921fd05b1d0ed5b425d74d87405a76a0b3afcbf9723a50d1ce in / 
# Thu, 17 Jun 2021 23:32:07 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 17 Jun 2021 23:32:08 GMT
RUN rm -rf /var/lib/apt/lists/*
# Thu, 17 Jun 2021 23:32:09 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 17 Jun 2021 23:32:09 GMT
CMD ["/bin/bash"]
# Fri, 18 Jun 2021 04:51:46 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Fri, 18 Jun 2021 04:51:47 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Fri, 18 Jun 2021 04:51:48 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian xenial main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel xenial main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Fri, 18 Jun 2021 04:51:53 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Fri, 18 Jun 2021 04:51:57 GMT
RUN sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list; grep -q 'deb .* multiverse$' /etc/apt/sources.list || sed -i -e 's,universe *$,universe multiverse,g' /etc/apt/sources.list
```

-	Layers:
	-	`sha256:61e03ba1d4149ac4eb681c6bf75aef8ac4b3f0d6fbb08e9623c4089889396fc8`  
		Last Modified: Sat, 12 Jun 2021 00:25:16 GMT  
		Size: 46.5 MB (46496785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4afb39f216bd4e336f9b78584bae0f6bcb77150107471d8d67d3b8abfbdea46a`  
		Last Modified: Thu, 17 Jun 2021 23:34:09 GMT  
		Size: 849.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e489abdc9f902f737bfef2c0c7ff5c35ca9b3ca11e73405a472f31a25f2dcc69`  
		Last Modified: Thu, 17 Jun 2021 23:34:08 GMT  
		Size: 528.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:999fff7bcc2450fcf1210182802f3907e35cd7cf7569568bd2a179b9144d9c57`  
		Last Modified: Thu, 17 Jun 2021 23:34:08 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f27db3f87344ee4f403c5257877584f0b0319c19914fa2953e351715240aa547`  
		Last Modified: Fri, 18 Jun 2021 04:54:39 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05d325b9a44fc4bfd2ef838143c6afeeed1fbf4929cc69351b13790404151baf`  
		Last Modified: Fri, 18 Jun 2021 04:54:39 GMT  
		Size: 3.1 KB (3150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45a309011e84c623c2b39ed13ff0f62d5c0f40e9ae798cdf37fba510c34711c6`  
		Last Modified: Fri, 18 Jun 2021 04:54:39 GMT  
		Size: 248.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ea488f510caf428861b3edf4b32605992b348a0f4ec00ee2e81a581d8e80f80`  
		Last Modified: Fri, 18 Jun 2021 04:54:39 GMT  
		Size: 226.9 KB (226939 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e901921b5a6b1c35d7c4d2819f403cac6c89c2165b3d2c26ed9a7741007b3aae`  
		Last Modified: Fri, 18 Jun 2021 04:54:51 GMT  
		Size: 257.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
