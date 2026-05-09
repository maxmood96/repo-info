<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `spiped`

-	[`spiped:1`](#spiped1)
-	[`spiped:1-alpine`](#spiped1-alpine)
-	[`spiped:1.6`](#spiped16)
-	[`spiped:1.6-alpine`](#spiped16-alpine)
-	[`spiped:1.6.4`](#spiped164)
-	[`spiped:1.6.4-alpine`](#spiped164-alpine)
-	[`spiped:alpine`](#spipedalpine)
-	[`spiped:latest`](#spipedlatest)

## `spiped:1`

```console
$ docker pull spiped@sha256:88bc77b7f493281dc8a9e59dc2520bc581437fda4955fe72e186b89e6f5fcc51
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 16
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v5
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `spiped:1` - linux; amd64

```console
$ docker pull spiped@sha256:6efd769d805f600ba739d18173542643175bc85a275a6c2b774507b866215473
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.8 MB (36830428 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3193b704891a8a18ac61ecedd914fc9f5bd4f08bcb9f49c1bf5d515f1d635642`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 19:35:11 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Fri, 08 May 2026 19:35:13 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:35:34 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Fri, 08 May 2026 19:35:34 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Fri, 08 May 2026 19:35:34 GMT
VOLUME [/spiped]
# Fri, 08 May 2026 19:35:35 GMT
WORKDIR /spiped
# Fri, 08 May 2026 19:35:35 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Fri, 08 May 2026 19:35:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 08 May 2026 19:35:35 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:57fb71246055257a374deb7564ceca10f43c2352572b501efc08add5d24ebb61`  
		Last Modified: Fri, 08 May 2026 18:24:13 GMT  
		Size: 29.8 MB (29780226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d57dde26e20eb068bd1c6070f0dd034bd2fd4bb74b1da82102adef70cdfed8b`  
		Last Modified: Fri, 08 May 2026 19:35:41 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00bc21a8189b7a94c8796b3a7235e2b6031c3bb5c38a32e6dd145ecc6bbf04b7`  
		Last Modified: Fri, 08 May 2026 19:35:41 GMT  
		Size: 829.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e86acbd1889987e9e18c2f14f31b0434706f81121130868eda3c8c530a20af8`  
		Last Modified: Fri, 08 May 2026 19:35:42 GMT  
		Size: 7.0 MB (7047830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8465fa5d80692f7b30c835d41e84147136800e2c926a318e6f844e8aa3836bac`  
		Last Modified: Fri, 08 May 2026 19:35:41 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c80c6cb3750ff6c08d0efb53fca666dfb8b02730a76835cddd23324fdb9c8a50`  
		Last Modified: Fri, 08 May 2026 19:35:42 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1` - unknown; unknown

```console
$ docker pull spiped@sha256:487c3ee9e344c1a378f97678431d3e69821f86c4eda6453de29af68a08d68173
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3641240 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc31b2a2f275eaf7500af7747def58d03e41f11827d308adb17d72a49c616aac`

```dockerfile
```

-	Layers:
	-	`sha256:4b40916ec2afebb3f0a5a2048230524b2afb160289fc9744212b19b511be425d`  
		Last Modified: Fri, 08 May 2026 19:35:41 GMT  
		Size: 3.6 MB (3626260 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:50c2e4615b4f2b4e4ffd2810f21ba67d9914c2f032810327b3488715ae97a747`  
		Last Modified: Fri, 08 May 2026 19:35:41 GMT  
		Size: 15.0 KB (14980 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1` - linux; arm variant v5

```console
$ docker pull spiped@sha256:6cbedd59e1b9ab471903f2f35a283d6f759be7121323441a6ca11573d8ae1cc4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.7 MB (33739804 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d990d2ba40ebc977000d42cedd17ab74640ddafe3cdee97d15362100231d6383`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 20:56:49 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Fri, 08 May 2026 20:56:54 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 20:57:21 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Fri, 08 May 2026 20:57:21 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Fri, 08 May 2026 20:57:21 GMT
VOLUME [/spiped]
# Fri, 08 May 2026 20:57:21 GMT
WORKDIR /spiped
# Fri, 08 May 2026 20:57:21 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Fri, 08 May 2026 20:57:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 08 May 2026 20:57:21 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:8f774e9b92b540806fc05167db7ce09a3e1b12abdb9d496f7b8c82138656065a`  
		Last Modified: Fri, 08 May 2026 18:33:49 GMT  
		Size: 27.9 MB (27948200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a147b3e27022cec78f27ab492347bf10b38fbc6c422c905e72f65841af2c2d35`  
		Last Modified: Fri, 08 May 2026 20:57:28 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f6f9b4d53a44c3aa0c748c56ea7420bc6a2ab57d31e476283c807a478c52a3b`  
		Last Modified: Fri, 08 May 2026 20:57:28 GMT  
		Size: 834.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7292710fe7c3115e3ec777cbaae5e736fe457c7abb0b37105d16f3dd0e6aa0d0`  
		Last Modified: Fri, 08 May 2026 20:57:28 GMT  
		Size: 5.8 MB (5789227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1be583d842fa62ff531b016e5bcc500de7cb8e354eddd92a4d45dc6617a54826`  
		Last Modified: Fri, 08 May 2026 20:57:28 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e608db2fba73f6cd7cc5367f133a6f818229089838eec0abce963f0960c957e`  
		Last Modified: Fri, 08 May 2026 20:57:29 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1` - unknown; unknown

```console
$ docker pull spiped@sha256:ee5c5f8032a4007863cf92bf644d1f00091054b2afe7ed6c0a2abd05eabee240
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3634341 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:713b5a387e4efd3ea171616d9b76dcad6c85e7fd7c9406dc19495e279cbaebbd`

```dockerfile
```

-	Layers:
	-	`sha256:c1b655131c2f9a200d94f4a9833890220f71e30981b4064d2f16f8a833f997bb`  
		Last Modified: Fri, 08 May 2026 20:57:28 GMT  
		Size: 3.6 MB (3619254 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:49ddef005c38ab7a29e8f27a8e717e4f7c45fbf16cf5484b232c46b7d559ff7c`  
		Last Modified: Fri, 08 May 2026 20:57:28 GMT  
		Size: 15.1 KB (15087 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1` - linux; arm variant v7

```console
$ docker pull spiped@sha256:4ff1f64955f0baac28dd640dfec3eb6e7155387c14a4c6857815f04a5019ffc2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.8 MB (31802065 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3c7a8a4fd74a9ea680b4826c71ad4261c1b369234cf1e5a1af74de4f0f02780`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 19:43:48 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Fri, 08 May 2026 19:43:51 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:44:15 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Fri, 08 May 2026 19:44:15 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Fri, 08 May 2026 19:44:15 GMT
VOLUME [/spiped]
# Fri, 08 May 2026 19:44:15 GMT
WORKDIR /spiped
# Fri, 08 May 2026 19:44:15 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Fri, 08 May 2026 19:44:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 08 May 2026 19:44:15 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:f1433620eadfdfe016c8054b954f619ae5bca159f35a9459c36a76d9ef4d39c3`  
		Last Modified: Fri, 08 May 2026 18:37:58 GMT  
		Size: 26.2 MB (26214912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f160c4481d462904aa24778c4b01da7a50dd3330da0f3146ecd0fa1750b36e3`  
		Last Modified: Fri, 08 May 2026 19:44:22 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:004f6312484a065cbbbc3f38cbdcd14f9d0d288af4570dc95d0b422521d5a4e9`  
		Last Modified: Fri, 08 May 2026 19:44:22 GMT  
		Size: 828.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7cfb1c37acf55579035e448653f38eb6ee097fa7f5c76c63e12e4b73e6bed7e`  
		Last Modified: Fri, 08 May 2026 19:44:22 GMT  
		Size: 5.6 MB (5584782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55a95cb661cfcd83f6253fbdfda5fdca5527107bcaceb6cd297381b4a90ff390`  
		Last Modified: Fri, 08 May 2026 19:44:22 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d438e2f2f47da106abfac0e9680692ac80d185181f12e690966a0581ad54dd02`  
		Last Modified: Fri, 08 May 2026 19:44:23 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1` - unknown; unknown

```console
$ docker pull spiped@sha256:26f57e59b1a522ae1a687b8df8cf930ddf2c1d699112e21280421a49ca910972
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3633462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b2c0796641018c39128df86b179e33a156dcb32c5541d96e2972f2e703e151b`

```dockerfile
```

-	Layers:
	-	`sha256:418008c48573eba24e549885dce4ad96fd0a220792017aeb5f7acce11418e708`  
		Last Modified: Fri, 08 May 2026 19:44:22 GMT  
		Size: 3.6 MB (3618375 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0d6e39d76bd241efe3b0b538efe61306d7f2392070a38f4c7231ff87fb17c6fc`  
		Last Modified: Fri, 08 May 2026 19:44:22 GMT  
		Size: 15.1 KB (15087 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1` - linux; arm64 variant v8

```console
$ docker pull spiped@sha256:f4d2c7ba22fbdd4c39d643fc06400642b6d479a7dfc684a3939b41bd69392c60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.4 MB (36379770 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:076b678a615cd6adb58ebf5f146ff8d89909b5200fed70f6093a1252adb559d0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 19:36:49 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Fri, 08 May 2026 19:36:52 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:37:14 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Fri, 08 May 2026 19:37:14 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Fri, 08 May 2026 19:37:14 GMT
VOLUME [/spiped]
# Fri, 08 May 2026 19:37:14 GMT
WORKDIR /spiped
# Fri, 08 May 2026 19:37:14 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Fri, 08 May 2026 19:37:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 08 May 2026 19:37:14 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:9ebf9a1d0c9ca1bcb377e9dba38a3fdd3e89cf37164f4245286c24f8cd50a39e`  
		Last Modified: Fri, 08 May 2026 18:26:50 GMT  
		Size: 30.1 MB (30143642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab68b1d288c6fda5c3d291b76142d35c7ec90bba49f2f7e249984ab5030b2a8a`  
		Last Modified: Fri, 08 May 2026 19:37:21 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72258c478f2f0cacc665dd483d41ad5142247c03f899d55173f931b7e1127ccd`  
		Last Modified: Fri, 08 May 2026 19:37:21 GMT  
		Size: 829.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bff059afbb00a8d0c47938a8cd83a2cb69138df7c613c1ff73877639d5839980`  
		Last Modified: Fri, 08 May 2026 19:37:22 GMT  
		Size: 6.2 MB (6233755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45a3566292154189efcb23707ad78ae15514dc0e956d1fb5b4f10ca4fe927840`  
		Last Modified: Fri, 08 May 2026 19:37:22 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:290e4c2f5ef9aaf2f014d15a44512a40b25b7bc0cac6db9b8ae073550aadfd21`  
		Last Modified: Fri, 08 May 2026 19:37:23 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1` - unknown; unknown

```console
$ docker pull spiped@sha256:b8025f0910028dd9817f393058197a8d68cf5196c0a4e130126c5b48c10cb344
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3636412 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39ab8802b871f6dee336412a2abb98089de33fd8aaab9762c3cda2637371d0f2`

```dockerfile
```

-	Layers:
	-	`sha256:1778e062fea4855a339744af921af7d4db3810975c7e16ccd96cf39b1c6b1c2c`  
		Last Modified: Fri, 08 May 2026 19:37:22 GMT  
		Size: 3.6 MB (3621296 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5180c5ea69da7069bfd3b17dcadb7c91742ce10c5bb6bedca95126234abc14a7`  
		Last Modified: Fri, 08 May 2026 19:37:21 GMT  
		Size: 15.1 KB (15116 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1` - linux; 386

```console
$ docker pull spiped@sha256:d981618a0d9c00684e6abf3d84a440dd8149f059c1fa1770e74b57656b7d1660
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.7 MB (37741286 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a5cb61d1ba1a94f11c6345a5fdb6fea544260c32c6125120a8872687fa142f3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 19:42:56 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Fri, 08 May 2026 19:42:59 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:43:23 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Fri, 08 May 2026 19:43:23 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Fri, 08 May 2026 19:43:23 GMT
VOLUME [/spiped]
# Fri, 08 May 2026 19:43:24 GMT
WORKDIR /spiped
# Fri, 08 May 2026 19:43:24 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Fri, 08 May 2026 19:43:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 08 May 2026 19:43:24 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:43e2ffbaa23260ffb4e3de716920f2ed9e6af56e465ca1233a2d84c2cc1cf005`  
		Last Modified: Fri, 08 May 2026 18:32:48 GMT  
		Size: 31.3 MB (31296400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c17b41ec4f852447201aeb965c3aa2bafdee78fd8912e91f0b7978c569be5e2f`  
		Last Modified: Fri, 08 May 2026 19:43:31 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d70e5c72cd4936724086c00ec89429bded5df26b92391c2566ed2fb716f18aa7`  
		Last Modified: Fri, 08 May 2026 19:43:31 GMT  
		Size: 828.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:709085b6edd21ce82957d908045c521464897a7c5aa9403a2dd9fd0f92d5140e`  
		Last Modified: Fri, 08 May 2026 19:43:31 GMT  
		Size: 6.4 MB (6442518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b14de3e13da7ff3cc57333aab9a6a05e63d3b95b75b2817946da6be54d9c921`  
		Last Modified: Fri, 08 May 2026 19:43:31 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82008a569b9479b56a58f4f85ce555a0023f34e26440b092f1cf31191ce34456`  
		Last Modified: Fri, 08 May 2026 19:43:32 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1` - unknown; unknown

```console
$ docker pull spiped@sha256:3408744cec174cbb267a63b72e71e41b4e396fdbf4d8b29a489532fce7271e94
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3635335 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a172af2f2faf106a865ab5dc37e0b74df8c431777dbc521aa563779b97a0365`

```dockerfile
```

-	Layers:
	-	`sha256:aedee6e6a52a08621420305a03eeabe6aaa0173b995b54b09f9326e9c235f2be`  
		Last Modified: Fri, 08 May 2026 19:43:31 GMT  
		Size: 3.6 MB (3620389 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b58a647b7d7db8950d4a473142cb3d7427b419850101f376d98d507d3a374200`  
		Last Modified: Fri, 08 May 2026 19:43:30 GMT  
		Size: 14.9 KB (14946 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1` - linux; ppc64le

```console
$ docker pull spiped@sha256:2e4bd458122e32e6d0dabd95f38757741b801a99e93c50b9e645fa87eb51102a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.4 MB (40441188 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa385580deb2b8dcbc058025f53221c9c9a13ba6d0e1d1fcea983d0d8004f717`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 22:25:38 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Fri, 08 May 2026 22:25:44 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 22:26:31 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Fri, 08 May 2026 22:26:31 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Fri, 08 May 2026 22:26:31 GMT
VOLUME [/spiped]
# Fri, 08 May 2026 22:26:31 GMT
WORKDIR /spiped
# Fri, 08 May 2026 22:26:31 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Fri, 08 May 2026 22:26:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 08 May 2026 22:26:31 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:b9baa45d89920bd180d7551ccc5bc535e0c5f55b863ddebddfdc06f9436dfe91`  
		Last Modified: Fri, 08 May 2026 19:46:53 GMT  
		Size: 33.6 MB (33598087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:680ca9add7a30a7a7a02b373e65419c55c156f59ab37259115ead4b9683e755f`  
		Last Modified: Fri, 08 May 2026 22:26:46 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6fbd88296e83b0fe34af0d7aea8feb0ab152c24009771728138ab8ea6a3c7e3`  
		Last Modified: Fri, 08 May 2026 22:26:46 GMT  
		Size: 829.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:427b4091434bcad2400a705856ffbc391e8edb99ddd0244020ab8e87b8fb0029`  
		Last Modified: Fri, 08 May 2026 22:26:46 GMT  
		Size: 6.8 MB (6840726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5761c60db3e29874e7a761fb091b3a0716e00845ff60b44aed197905641f8201`  
		Last Modified: Fri, 08 May 2026 22:26:46 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d979fa4083e9e6936395a7aa0bbee2b7b6a8cc7f4e41e6234afe21c2ef4653e`  
		Last Modified: Fri, 08 May 2026 22:26:47 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1` - unknown; unknown

```console
$ docker pull spiped@sha256:05648be86c583500baf9a23fc752f751b17a45b3a93ce072b80d2c560c492e45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3637027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:527ae0828e720ab8c7f87f091c2295b3dcd1df2f39af33c2ebf4a290bf2b6a83`

```dockerfile
```

-	Layers:
	-	`sha256:5d43283d3f5718ce69f0dd46023d5abd6439b1b618e1f306799c06fe849aea01`  
		Last Modified: Fri, 08 May 2026 22:26:46 GMT  
		Size: 3.6 MB (3621997 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:917814349a2d8dd15ccd6b0a739bb88131cfd61f1a5b110c16b85cb164e6d7bb`  
		Last Modified: Fri, 08 May 2026 22:26:46 GMT  
		Size: 15.0 KB (15030 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1` - linux; riscv64

```console
$ docker pull spiped@sha256:4b71cf53987a9707a16131c1318e249b3fd3d6ce9a82cb42cc7f49e072e18fd7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.6 MB (37638423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f26a4b86552c1e9439f4f551a02d1d47a8a09b1564576e2077689ea60ed92ca7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1776729600'
# Thu, 23 Apr 2026 16:08:31 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Thu, 23 Apr 2026 16:09:01 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 23 Apr 2026 16:12:07 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Thu, 23 Apr 2026 16:12:07 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Thu, 23 Apr 2026 16:12:07 GMT
VOLUME [/spiped]
# Thu, 23 Apr 2026 16:12:07 GMT
WORKDIR /spiped
# Thu, 23 Apr 2026 16:12:08 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Thu, 23 Apr 2026 16:12:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 Apr 2026 16:12:08 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:c59e3a1f334be9f0528643dd07d69319f75f877f83be33ec1eff872a489985a0`  
		Last Modified: Wed, 22 Apr 2026 02:30:51 GMT  
		Size: 28.3 MB (28280195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65c3fe48b86e812e3913e5d13d1a9629869d202426b9c61e1715fa21c49eefb0`  
		Last Modified: Thu, 23 Apr 2026 16:13:20 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b34a84840c5fe62bd145180a478a04eb839e8ebc46151483b24496cb9f4a91f`  
		Last Modified: Thu, 23 Apr 2026 16:13:20 GMT  
		Size: 819.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d24129e4ff9e3418ef7a713edd9546c25c9b66ed26f8d5aa09e53f0c443a147`  
		Last Modified: Thu, 23 Apr 2026 16:13:23 GMT  
		Size: 9.4 MB (9355868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c9de411851378c843f1fa5367128062cec83a39214793d042c62249d045708d`  
		Last Modified: Thu, 23 Apr 2026 16:13:20 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e45064277bc4d512497c03c09b867eecba1e9f36520600b1b7cf50ccf931c314`  
		Last Modified: Thu, 23 Apr 2026 16:13:22 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1` - unknown; unknown

```console
$ docker pull spiped@sha256:8f1fdb09a20e86779bcd22247e4e7dc45779eadf380ed22541529e1f7c49f080
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3628433 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30611531e32494ce7228fad7644d17d3b521a5eb65e2cab640541ec507a3ccff`

```dockerfile
```

-	Layers:
	-	`sha256:28e7945cedc25231eedc0925db8b02ae1dfc5c3c41f66ebd1d3a8ef39e217551`  
		Last Modified: Thu, 23 Apr 2026 16:13:22 GMT  
		Size: 3.6 MB (3613403 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0b3f06dd63e825c9c98e9b4bfdc4f7087ec431640aee8976c15796ae26a216eb`  
		Last Modified: Thu, 23 Apr 2026 16:13:20 GMT  
		Size: 15.0 KB (15030 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1` - linux; s390x

```console
$ docker pull spiped@sha256:bd86a35901c83fdbe0b1dd9ab57c28d30a6565052dbe1ae0ef315fc89adffc00
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.0 MB (35964636 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90e9eead17c9f5aa0363836fa2a870f271ca50be7e2f1899fb3e7e0c17e6add5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 20:52:18 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Fri, 08 May 2026 20:52:21 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 20:52:41 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Fri, 08 May 2026 20:52:41 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Fri, 08 May 2026 20:52:41 GMT
VOLUME [/spiped]
# Fri, 08 May 2026 20:52:41 GMT
WORKDIR /spiped
# Fri, 08 May 2026 20:52:41 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Fri, 08 May 2026 20:52:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 08 May 2026 20:52:41 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:2fbbc68c452b3ba3a496488f38159dac53afe693311bee1c04f555d854ff4a2e`  
		Last Modified: Fri, 08 May 2026 18:29:20 GMT  
		Size: 29.8 MB (29840347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:379c83725970f21bcd83cf3380670f0ea271dd1fc30bc3e9568c083f2580ba55`  
		Last Modified: Fri, 08 May 2026 20:52:53 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3b3284a3de5bccf5d6b269c2b7bf9b319d15f9bebd9af7f1c95123337f82ffc`  
		Last Modified: Fri, 08 May 2026 20:52:53 GMT  
		Size: 829.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78ee74470711143892631998b06f797b17b8f24c199e31160dbad3fa3f9f4b1b`  
		Last Modified: Fri, 08 May 2026 20:52:53 GMT  
		Size: 6.1 MB (6121916 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5efe750c150333b99cd25f27597baa8d209228b9898aac1c0a7355a41ab17040`  
		Last Modified: Fri, 08 May 2026 20:52:53 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31b3234d867e10e2e459de5bd4cf9e1156a19cf24d495f2dfc7415071ae5715f`  
		Last Modified: Fri, 08 May 2026 20:52:54 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1` - unknown; unknown

```console
$ docker pull spiped@sha256:7c6bfdf45b3649d1b3f9001e65846a9f9c95d3e42d468a4d78f4b4419a680bf5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3633605 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5894b164eadfcc36f173a9f50f9038140f4fd57fd4528d5251f9f417819c1e0c`

```dockerfile
```

-	Layers:
	-	`sha256:117c16ab57c2ffc82accce55a8dd174232910aa2a2d2f4121a9924747a140c28`  
		Last Modified: Fri, 08 May 2026 20:52:53 GMT  
		Size: 3.6 MB (3618623 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b7501e35b7a1f23c01cc4fa7d7fe477f7d1e791f6af13d52b1b0b27d654c13a4`  
		Last Modified: Fri, 08 May 2026 20:52:53 GMT  
		Size: 15.0 KB (14982 bytes)  
		MIME: application/vnd.in-toto+json

## `spiped:1-alpine`

```console
$ docker pull spiped@sha256:10785aa58079387363e472d7e20eb96bd01f12b9850476a066e124d57be1a8cc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 16
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `spiped:1-alpine` - linux; amd64

```console
$ docker pull spiped@sha256:6a78a135961dde77e0a3e9171928717694804d7cfb3d6aedbebfadb42bf4f3e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3925151 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06f599634d068048f3fcd01d27356e8cc57fb8937f8bbf03cfccaebddd3b1e24`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:02 GMT
ADD alpine-minirootfs-3.22.4-x86_64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:02 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 00:14:35 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Fri, 17 Apr 2026 00:14:36 GMT
RUN apk add --no-cache libssl3 # buildkit
# Fri, 17 Apr 2026 00:14:45 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Fri, 17 Apr 2026 00:14:45 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Fri, 17 Apr 2026 00:14:45 GMT
VOLUME [/spiped]
# Fri, 17 Apr 2026 00:14:45 GMT
WORKDIR /spiped
# Fri, 17 Apr 2026 00:14:45 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Fri, 17 Apr 2026 00:14:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 17 Apr 2026 00:14:45 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:84f5eff04246b56d48d1ed6cbd82d6bc7e53f7e790db6a467f92571c69f3289e`  
		Last Modified: Thu, 16 Apr 2026 23:53:07 GMT  
		Size: 3.8 MB (3808189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09629d4032ef7ab1ef9db974170b9cf0e98f6c5d68cb9f3d0e21a37889d50030`  
		Last Modified: Fri, 17 Apr 2026 00:14:50 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cad68e6c6d9b805cb5d27e526a335f55ae1e22e51fb78ed5cd842984966ec752`  
		Last Modified: Fri, 17 Apr 2026 00:14:50 GMT  
		Size: 7.9 KB (7942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0097cdb4e276728ffaa69c00b45edf54d761118176e68ef12d68092b7417f986`  
		Last Modified: Fri, 17 Apr 2026 00:14:50 GMT  
		Size: 107.6 KB (107638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9bc806c3d4f80593516df4d73efec6cd1cf16dfd200d5fd6adda41910072975`  
		Last Modified: Fri, 17 Apr 2026 00:14:50 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d250500ebc740f642b6509ef0a3f0576fe4b93cb687a514ceede64292cd717f`  
		Last Modified: Fri, 17 Apr 2026 00:14:51 GMT  
		Size: 336.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:dcf1f88cd35b0648a36b53371be8057efc788150c247273946f22f226c8922f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.5 KB (96450 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b695771cd59164f79af4e3d51a194af63f71274fa2ca45642700481f66706680`

```dockerfile
```

-	Layers:
	-	`sha256:9047c6064b6fcd9efa90aa0c959722cd5d0677dd3e15d576484c71664c66a025`  
		Last Modified: Fri, 17 Apr 2026 00:14:50 GMT  
		Size: 82.2 KB (82192 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b1ebf9604f23105cb6660c6767d301a937a4b9d6d85433f32e35ffb2ba1e86d8`  
		Last Modified: Fri, 17 Apr 2026 00:14:50 GMT  
		Size: 14.3 KB (14258 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1-alpine` - linux; arm variant v6

```console
$ docker pull spiped@sha256:e61a3952e5718375c379136684659c21136328808a6c3f88e9585943251e9a16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3605859 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c576e8f7269c2ef4826f92b4a22494225a6cd470d17d9f30f01d9cc229e696f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:27 GMT
ADD alpine-minirootfs-3.22.4-armhf.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:27 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 00:28:09 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Fri, 17 Apr 2026 00:28:10 GMT
RUN apk add --no-cache libssl3 # buildkit
# Fri, 17 Apr 2026 00:28:20 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Fri, 17 Apr 2026 00:28:20 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Fri, 17 Apr 2026 00:28:20 GMT
VOLUME [/spiped]
# Fri, 17 Apr 2026 00:28:20 GMT
WORKDIR /spiped
# Fri, 17 Apr 2026 00:28:20 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Fri, 17 Apr 2026 00:28:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 17 Apr 2026 00:28:20 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:08c654e9a4409dbbeb5faba9659360f33dbc6f7a6d79ebebe08f57d22a1b76fc`  
		Last Modified: Thu, 16 Apr 2026 23:53:31 GMT  
		Size: 3.5 MB (3507383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a28595f303e8390d8534900bd78b38647a907732d3d3e842c7b3a9caf747dfa`  
		Last Modified: Fri, 17 Apr 2026 00:28:24 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04a2d882259c543692d98198b2c8f098f64b95d9b8018fbe3daf4bce16ccdea8`  
		Last Modified: Fri, 17 Apr 2026 00:28:24 GMT  
		Size: 7.9 KB (7941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:750bf6b03a38c9f5493952dd7c83dba844fa70e86926b54303c228f996e864fb`  
		Last Modified: Fri, 17 Apr 2026 00:28:24 GMT  
		Size: 89.2 KB (89153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bb0b56fb727ea9f7a3dad23a396c81b60139284396a263e6658329c844b5dad`  
		Last Modified: Fri, 17 Apr 2026 00:28:23 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20e6b266845306bbbcbee6801a12889b7c152b510808934deb45a090cedc3a06`  
		Last Modified: Fri, 17 Apr 2026 00:28:25 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:e8ab0469cf1a0658dd7f777f120002189b116eedc60e2d13004809373539fd11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.1 KB (14144 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cfbd38bcf39cf976d74f4ea0d61a864e9b890815035438f477a99caff10eae99`

```dockerfile
```

-	Layers:
	-	`sha256:acf29d68d1e7fa30dc5742c4211ffe81430df68660be1f3d0207d5a94d98bc39`  
		Last Modified: Fri, 17 Apr 2026 00:28:23 GMT  
		Size: 14.1 KB (14144 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1-alpine` - linux; arm variant v7

```console
$ docker pull spiped@sha256:147fe0124aa237fa168a69becb6a2db57f4a9ad7144beb44a52a7735a75ed88f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3316848 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1fac8ff5e55f7bb423942ebc9a0dcfe62ab45560df8acbf81f20fce40adfb0d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 16 Apr 2026 23:54:02 GMT
ADD alpine-minirootfs-3.22.4-armv7.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:54:02 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 00:13:44 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Fri, 17 Apr 2026 00:13:45 GMT
RUN apk add --no-cache libssl3 # buildkit
# Fri, 17 Apr 2026 00:13:54 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Fri, 17 Apr 2026 00:13:54 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Fri, 17 Apr 2026 00:13:54 GMT
VOLUME [/spiped]
# Fri, 17 Apr 2026 00:13:54 GMT
WORKDIR /spiped
# Fri, 17 Apr 2026 00:13:54 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Fri, 17 Apr 2026 00:13:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 17 Apr 2026 00:13:54 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:99e8c7f1cf08d3156a369084c1a1fd745878aa29f4a0f55d73e953b93f0b7a93`  
		Last Modified: Thu, 16 Apr 2026 23:54:07 GMT  
		Size: 3.2 MB (3225830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e48112adbff0844ea29be59655ce36bdc68db268960b43349a213160861be5b`  
		Last Modified: Fri, 17 Apr 2026 00:13:59 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62b71c7a3ae36749950f95514df7064116e47fac5d0e8f2b2a7465a08ec730b1`  
		Last Modified: Fri, 17 Apr 2026 00:13:59 GMT  
		Size: 7.9 KB (7949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90dbc42fa35611c27c8478a77677c7599958f859178a2ae432cdeea23ff283fe`  
		Last Modified: Fri, 17 Apr 2026 00:13:59 GMT  
		Size: 81.7 KB (81682 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d17f9759dca0bc64327214acbd9fd3deb78375c7afd7010e30d54ffe9eafdb6`  
		Last Modified: Fri, 17 Apr 2026 00:13:59 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87eff9de0017984f4c4aceb50f22ba5600d01062af116b4a3d8666f104982e79`  
		Last Modified: Fri, 17 Apr 2026 00:14:00 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:87b16d20b49f4fd531d2a7882ebf70ab433c78455a68ecb63229df2b111b80e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.6 KB (96590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4db1828da7718e04747ebb0f602b5974b0a7a0da76481d2a933ecbb6b1869fd9`

```dockerfile
```

-	Layers:
	-	`sha256:32fd82b374cd8966ecaddf73d35913d341f1bf089acec4758b0eddc9ae15bf6c`  
		Last Modified: Fri, 17 Apr 2026 00:13:59 GMT  
		Size: 82.2 KB (82228 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:451cb443bac28fadec04af355b08de89c30845228bcead9735b3be6a627381f6`  
		Last Modified: Fri, 17 Apr 2026 00:13:59 GMT  
		Size: 14.4 KB (14362 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1-alpine` - linux; arm64 variant v8

```console
$ docker pull spiped@sha256:1fd688a89197aa9ec5aa2ecf456f856d56b46639e5d0733ee167c8e1f1f67c29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4251815 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3e3a3494482e2c117fe69680a253048739b96db6b666e0ba693d69f12f3cffa`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:00 GMT
ADD alpine-minirootfs-3.22.4-aarch64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:00 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 00:23:30 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Fri, 17 Apr 2026 00:23:30 GMT
RUN apk add --no-cache libssl3 # buildkit
# Fri, 17 Apr 2026 00:23:40 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Fri, 17 Apr 2026 00:23:40 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Fri, 17 Apr 2026 00:23:40 GMT
VOLUME [/spiped]
# Fri, 17 Apr 2026 00:23:40 GMT
WORKDIR /spiped
# Fri, 17 Apr 2026 00:23:40 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Fri, 17 Apr 2026 00:23:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 17 Apr 2026 00:23:40 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:58e777220c395c319866c5d73ea32a5ea574bbd12f4eb289b392f584d0cd953e`  
		Last Modified: Thu, 16 Apr 2026 23:53:05 GMT  
		Size: 4.1 MB (4141894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3b70cf46309ade34c5a66991fc83a20e95c2a2ca7662393d07532b98169b897`  
		Last Modified: Fri, 17 Apr 2026 00:23:45 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4aa5fdf2c2bb57fb12d420f1ebc379b73a6a07a076dd649edbdfb2ec65e9b52f`  
		Last Modified: Fri, 17 Apr 2026 00:23:45 GMT  
		Size: 7.9 KB (7939 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62bde94e8b5d108bfaf26624adc0087452e38a2a8176cc98ece876fe2117fc72`  
		Last Modified: Fri, 17 Apr 2026 00:23:45 GMT  
		Size: 100.6 KB (100601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec5b88c8155b1bdcaf3ceb67be1cd60eac4d053dbde4189b58b41e709ce71a5d`  
		Last Modified: Fri, 17 Apr 2026 00:23:45 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bb330bcfc9ca5ba0cfa2155b2866b977ad2c3ce1d9ae151d07e639bbada8ed2`  
		Last Modified: Fri, 17 Apr 2026 00:23:46 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:fc73de67fe7f5bcda008d343140166980bf4176b3096a535d83f3dcd2d534e5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.6 KB (96641 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a18fe2b2319a581866e1c86ace119888f0e7b9a60b55a3ce6b779f28fe92710`

```dockerfile
```

-	Layers:
	-	`sha256:a96c2085f2ac76644e77254bfa9bf6d1b56c67d9d9405eaa8416f74fcba97701`  
		Last Modified: Fri, 17 Apr 2026 00:23:45 GMT  
		Size: 82.2 KB (82248 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a7d5f7f4737f85a0e24460592078844c64dafe02803bdf87581c20f597e952bb`  
		Last Modified: Fri, 17 Apr 2026 00:23:45 GMT  
		Size: 14.4 KB (14393 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1-alpine` - linux; 386

```console
$ docker pull spiped@sha256:60c2f83afdec0385615a7286994daa8f205766ef71d83fa8ddc2e700ac81936f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3754157 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fdc7573391c8c621e1b2f987722ca168aebbe555b0499e62e86738da10c96e58`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Fri, 17 Apr 2026 02:42:29 GMT
ADD alpine-minirootfs-3.22.4-x86.tar.gz / # buildkit
# Fri, 17 Apr 2026 02:42:29 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 05:54:58 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Fri, 17 Apr 2026 05:54:58 GMT
RUN apk add --no-cache libssl3 # buildkit
# Fri, 17 Apr 2026 05:55:09 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Fri, 17 Apr 2026 05:55:09 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Fri, 17 Apr 2026 05:55:09 GMT
VOLUME [/spiped]
# Fri, 17 Apr 2026 05:55:09 GMT
WORKDIR /spiped
# Fri, 17 Apr 2026 05:55:09 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Fri, 17 Apr 2026 05:55:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 17 Apr 2026 05:55:09 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:481dba1f7704181ddc1e2b499675e9651a93f972d4cd141a4933d44622cdc88a`  
		Last Modified: Fri, 17 Apr 2026 02:42:34 GMT  
		Size: 3.6 MB (3624721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2f934ad8efa54d7383ed1d7daf8f07d69a316c785b55e29d855f59724767ac5`  
		Last Modified: Fri, 17 Apr 2026 05:55:13 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fad6a50d64bebedb5b11ecc9dbad14debf2baa30235c5ed093775151dd20c5f`  
		Last Modified: Fri, 17 Apr 2026 05:55:13 GMT  
		Size: 7.9 KB (7947 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4e9ad205a738e9a190290cb841b91a7516b90d39ccefc8a464803a80e5d3bf2`  
		Last Modified: Fri, 17 Apr 2026 05:55:14 GMT  
		Size: 120.1 KB (120105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b13bce07410da4d5d2d2271580461ed3ae19008e5249df3c1003a06c213c180b`  
		Last Modified: Fri, 17 Apr 2026 05:55:14 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d30a682d686a1255ac7f31b311acf6f01b819da6af05a18bb59cf9285441247`  
		Last Modified: Fri, 17 Apr 2026 05:55:14 GMT  
		Size: 336.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:499b7ec7b9c4e4eec426321c8934ac7fac003aeff1b6247ccf002c546cd6a262
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.4 KB (96390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9072722cf70bdbdd1bd5420a6744bc8ca176440a12571a40e33ce18862067a55`

```dockerfile
```

-	Layers:
	-	`sha256:dd1f08b2c21c938da19a9533a1b9dcb5f15e078dab41c9a4bd4ab244cd979858`  
		Last Modified: Fri, 17 Apr 2026 05:55:13 GMT  
		Size: 82.2 KB (82167 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:517f76f905b9dca96e65eec9ad79a6211e1b541723537e827a226d4839aa2649`  
		Last Modified: Fri, 17 Apr 2026 05:55:14 GMT  
		Size: 14.2 KB (14223 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1-alpine` - linux; ppc64le

```console
$ docker pull spiped@sha256:cd9ed7a248ccd86ed221ed62ccb5fccc85d88f92bb07eacf32a54aa285d3baef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3858669 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01b17425a87a9b3f6cf310b87ae46b1234772bd0b80ea164489da909a148229e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Fri, 17 Apr 2026 00:00:29 GMT
ADD alpine-minirootfs-3.22.4-ppc64le.tar.gz / # buildkit
# Fri, 17 Apr 2026 00:00:29 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 01:13:47 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Fri, 17 Apr 2026 01:13:49 GMT
RUN apk add --no-cache libssl3 # buildkit
# Fri, 17 Apr 2026 01:14:13 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Fri, 17 Apr 2026 01:14:13 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Fri, 17 Apr 2026 01:14:13 GMT
VOLUME [/spiped]
# Fri, 17 Apr 2026 01:14:15 GMT
WORKDIR /spiped
# Fri, 17 Apr 2026 01:14:15 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Fri, 17 Apr 2026 01:14:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 17 Apr 2026 01:14:15 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:9d65ab042d46bde09babe9a9587237000067c332d24fd9ca516fea7bdfb77c80`  
		Last Modified: Fri, 17 Apr 2026 00:00:38 GMT  
		Size: 3.7 MB (3736656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d4eb2b31b373fa4117e61ee4973c717af31bc2e3376684ddf64780f6a0cfbf2`  
		Last Modified: Fri, 17 Apr 2026 01:14:36 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e5bc892fe10dffc5824aa6f02e4a3fd2d8872fcc548dc32d8271fbeda871d54`  
		Last Modified: Fri, 17 Apr 2026 01:14:36 GMT  
		Size: 8.0 KB (7951 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a0f69169c64986eaf44f560100f0ace1b79586cff5d1f517fcf6f2810fcf476`  
		Last Modified: Fri, 17 Apr 2026 01:14:36 GMT  
		Size: 112.7 KB (112676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ecc1153f644e2e26a00aa90bf9b03917ab7f9ec331b32bd9bc295281cee7151`  
		Last Modified: Fri, 17 Apr 2026 01:14:36 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94785087e434424ecd2b2a79b34d04d7aa53bdc943265138216cadd6badf5495`  
		Last Modified: Fri, 17 Apr 2026 01:14:37 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:42b060f58ef29347aa95f2a95a49a750c85e6dc1283a7429bdbd08cbb35d8c90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.6 KB (94582 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1aeddc4f5e06133647f4d77b87d5471240c741e9ac4581ee0469cd5e684bde41`

```dockerfile
```

-	Layers:
	-	`sha256:8054970ddb854b9dbe87ad8cc6cb52f8ac69bae6393895a2cc0ec179d9890648`  
		Last Modified: Fri, 17 Apr 2026 01:14:36 GMT  
		Size: 80.3 KB (80275 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5cf789792086c7df442c741fa726e1c634b400a002527085dcc36c87a5bdd724`  
		Last Modified: Fri, 17 Apr 2026 01:14:36 GMT  
		Size: 14.3 KB (14307 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1-alpine` - linux; riscv64

```console
$ docker pull spiped@sha256:eaf86ffaae6edde3dcb5bc958a07fa09bfe7cf9bcd05be9ace676e83efe5f761
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3629050 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:508a25834d52056b9c731fc2100ea35e54d563c093104a90eef8c05cb0cd1cf9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Fri, 17 Apr 2026 07:18:45 GMT
ADD alpine-minirootfs-3.22.4-riscv64.tar.gz / # buildkit
# Fri, 17 Apr 2026 07:18:45 GMT
CMD ["/bin/sh"]
# Sun, 19 Apr 2026 03:43:32 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Sun, 19 Apr 2026 03:43:36 GMT
RUN apk add --no-cache libssl3 # buildkit
# Sun, 19 Apr 2026 03:45:16 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Sun, 19 Apr 2026 03:45:16 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Sun, 19 Apr 2026 03:45:16 GMT
VOLUME [/spiped]
# Sun, 19 Apr 2026 03:45:16 GMT
WORKDIR /spiped
# Sun, 19 Apr 2026 03:45:17 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 19 Apr 2026 03:45:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 19 Apr 2026 03:45:17 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:fbc07c8b85a3c60e503ffd0cbe3e1b3947fd65764784e1bd9d943ac21097cce7`  
		Last Modified: Fri, 17 Apr 2026 07:19:08 GMT  
		Size: 3.5 MB (3520880 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62f6ee73726995fef9f6ea4faf4767bcea48e04bfd71f1eea0bd05f9534d43f8`  
		Last Modified: Sun, 19 Apr 2026 03:45:37 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ce2dd3bcf1d4c6316b374da1b2790b7de4b60cf8e6512e5f30f8d7b2d7a3b38`  
		Last Modified: Sun, 19 Apr 2026 03:45:37 GMT  
		Size: 7.9 KB (7940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8e66ca15c2a84ed0ad5aac95f1257383ec006115c07282942c1fd6f06bc2b26`  
		Last Modified: Sun, 19 Apr 2026 03:45:37 GMT  
		Size: 98.8 KB (98844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04a854d7ad8f0e7a7a6274e5c362b1a896bd76e462c14408778ba02dff83d37b`  
		Last Modified: Sun, 19 Apr 2026 03:45:37 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5ff5f61469b0ef7c1c8bf56662d9b762181e909bc3c749eacbaaecf7bb475ab`  
		Last Modified: Sun, 19 Apr 2026 03:45:39 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:f21b45950838bc0c80c8410cc4f2814b68f96ecad1e19be90b06994c99afbf58
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.6 KB (94574 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1abe71f567ae68daf6e6dfeaafd74f8104d7a6958082dd986f64838b44c12b9f`

```dockerfile
```

-	Layers:
	-	`sha256:e9f4f6fe1bacdcf68608f4eb99bf2115bae97f39b1056b72d36c08b63e32ef42`  
		Last Modified: Sun, 19 Apr 2026 03:45:37 GMT  
		Size: 80.3 KB (80271 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d5e5c1e0a1d68c8bdb360c97f9072a3c973409b2f9afe7ff5795d523cae5119b`  
		Last Modified: Sun, 19 Apr 2026 03:45:38 GMT  
		Size: 14.3 KB (14303 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1-alpine` - linux; s390x

```console
$ docker pull spiped@sha256:d63a333156f14c550016968b48b61e03d6ffa7cdadeb4dc11994993be83c667f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3760132 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:425f883e0aba651c328e78b42abc6210940d11022f1ee5d1ff5258ebca42e51f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:56 GMT
ADD alpine-minirootfs-3.22.4-s390x.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:56 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 00:41:11 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Fri, 17 Apr 2026 00:41:12 GMT
RUN apk add --no-cache libssl3 # buildkit
# Fri, 17 Apr 2026 00:41:19 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Fri, 17 Apr 2026 00:41:19 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Fri, 17 Apr 2026 00:41:19 GMT
VOLUME [/spiped]
# Fri, 17 Apr 2026 00:41:19 GMT
WORKDIR /spiped
# Fri, 17 Apr 2026 00:41:19 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Fri, 17 Apr 2026 00:41:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 17 Apr 2026 00:41:19 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:54b429821fc7436a26fe07d9038b86e2bef4ef3bf03e43e9ae5e91ab8e4b37a9`  
		Last Modified: Thu, 16 Apr 2026 23:54:12 GMT  
		Size: 3.7 MB (3653873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98c5658f716398e67bcdf451aa62d9268badc01207fb2761dde286827e782131`  
		Last Modified: Fri, 17 Apr 2026 00:41:28 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d837fc0069a0ae8449bb0adb9f65b43fff5ff059948bf845ea728a30d3eaca0`  
		Last Modified: Fri, 17 Apr 2026 00:41:28 GMT  
		Size: 7.9 KB (7947 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:669f2f936af1acb505aa131fbad0547df0d36ff3dc9c4f8c3a396c9877b87798`  
		Last Modified: Fri, 17 Apr 2026 00:41:28 GMT  
		Size: 96.9 KB (96930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33930e4a86d8157d355b84eecf720d4f20b38ee3502ab3baa6329d6c6acac811`  
		Last Modified: Fri, 17 Apr 2026 00:41:28 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27970db5cca98e64b9bdffc3b4445e18a503e3e0dc858c6ae91eff10bccd50bd`  
		Last Modified: Fri, 17 Apr 2026 00:41:29 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:3a63421a60ad516e8ae99df7c008ce97158220da99f3e592d9090f762eb254c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.5 KB (94497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03ae27771b3c7505fb78b0f0546a7416b11e879220de4dc6090bf643dedf8614`

```dockerfile
```

-	Layers:
	-	`sha256:c6abf9efd631a7212221f0b771ec35e734885be3d3a6755a004bba8bd46cc068`  
		Last Modified: Fri, 17 Apr 2026 00:41:28 GMT  
		Size: 80.2 KB (80241 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:033e56e9f47fa0453060710502d5ab3daddcba0cc4e51e5e138a57faf3e873d6`  
		Last Modified: Fri, 17 Apr 2026 00:41:28 GMT  
		Size: 14.3 KB (14256 bytes)  
		MIME: application/vnd.in-toto+json

## `spiped:1.6`

```console
$ docker pull spiped@sha256:88bc77b7f493281dc8a9e59dc2520bc581437fda4955fe72e186b89e6f5fcc51
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 16
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v5
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `spiped:1.6` - linux; amd64

```console
$ docker pull spiped@sha256:6efd769d805f600ba739d18173542643175bc85a275a6c2b774507b866215473
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.8 MB (36830428 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3193b704891a8a18ac61ecedd914fc9f5bd4f08bcb9f49c1bf5d515f1d635642`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 19:35:11 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Fri, 08 May 2026 19:35:13 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:35:34 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Fri, 08 May 2026 19:35:34 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Fri, 08 May 2026 19:35:34 GMT
VOLUME [/spiped]
# Fri, 08 May 2026 19:35:35 GMT
WORKDIR /spiped
# Fri, 08 May 2026 19:35:35 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Fri, 08 May 2026 19:35:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 08 May 2026 19:35:35 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:57fb71246055257a374deb7564ceca10f43c2352572b501efc08add5d24ebb61`  
		Last Modified: Fri, 08 May 2026 18:24:13 GMT  
		Size: 29.8 MB (29780226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d57dde26e20eb068bd1c6070f0dd034bd2fd4bb74b1da82102adef70cdfed8b`  
		Last Modified: Fri, 08 May 2026 19:35:41 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00bc21a8189b7a94c8796b3a7235e2b6031c3bb5c38a32e6dd145ecc6bbf04b7`  
		Last Modified: Fri, 08 May 2026 19:35:41 GMT  
		Size: 829.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e86acbd1889987e9e18c2f14f31b0434706f81121130868eda3c8c530a20af8`  
		Last Modified: Fri, 08 May 2026 19:35:42 GMT  
		Size: 7.0 MB (7047830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8465fa5d80692f7b30c835d41e84147136800e2c926a318e6f844e8aa3836bac`  
		Last Modified: Fri, 08 May 2026 19:35:41 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c80c6cb3750ff6c08d0efb53fca666dfb8b02730a76835cddd23324fdb9c8a50`  
		Last Modified: Fri, 08 May 2026 19:35:42 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6` - unknown; unknown

```console
$ docker pull spiped@sha256:487c3ee9e344c1a378f97678431d3e69821f86c4eda6453de29af68a08d68173
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3641240 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc31b2a2f275eaf7500af7747def58d03e41f11827d308adb17d72a49c616aac`

```dockerfile
```

-	Layers:
	-	`sha256:4b40916ec2afebb3f0a5a2048230524b2afb160289fc9744212b19b511be425d`  
		Last Modified: Fri, 08 May 2026 19:35:41 GMT  
		Size: 3.6 MB (3626260 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:50c2e4615b4f2b4e4ffd2810f21ba67d9914c2f032810327b3488715ae97a747`  
		Last Modified: Fri, 08 May 2026 19:35:41 GMT  
		Size: 15.0 KB (14980 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6` - linux; arm variant v5

```console
$ docker pull spiped@sha256:6cbedd59e1b9ab471903f2f35a283d6f759be7121323441a6ca11573d8ae1cc4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.7 MB (33739804 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d990d2ba40ebc977000d42cedd17ab74640ddafe3cdee97d15362100231d6383`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 20:56:49 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Fri, 08 May 2026 20:56:54 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 20:57:21 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Fri, 08 May 2026 20:57:21 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Fri, 08 May 2026 20:57:21 GMT
VOLUME [/spiped]
# Fri, 08 May 2026 20:57:21 GMT
WORKDIR /spiped
# Fri, 08 May 2026 20:57:21 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Fri, 08 May 2026 20:57:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 08 May 2026 20:57:21 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:8f774e9b92b540806fc05167db7ce09a3e1b12abdb9d496f7b8c82138656065a`  
		Last Modified: Fri, 08 May 2026 18:33:49 GMT  
		Size: 27.9 MB (27948200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a147b3e27022cec78f27ab492347bf10b38fbc6c422c905e72f65841af2c2d35`  
		Last Modified: Fri, 08 May 2026 20:57:28 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f6f9b4d53a44c3aa0c748c56ea7420bc6a2ab57d31e476283c807a478c52a3b`  
		Last Modified: Fri, 08 May 2026 20:57:28 GMT  
		Size: 834.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7292710fe7c3115e3ec777cbaae5e736fe457c7abb0b37105d16f3dd0e6aa0d0`  
		Last Modified: Fri, 08 May 2026 20:57:28 GMT  
		Size: 5.8 MB (5789227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1be583d842fa62ff531b016e5bcc500de7cb8e354eddd92a4d45dc6617a54826`  
		Last Modified: Fri, 08 May 2026 20:57:28 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e608db2fba73f6cd7cc5367f133a6f818229089838eec0abce963f0960c957e`  
		Last Modified: Fri, 08 May 2026 20:57:29 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6` - unknown; unknown

```console
$ docker pull spiped@sha256:ee5c5f8032a4007863cf92bf644d1f00091054b2afe7ed6c0a2abd05eabee240
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3634341 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:713b5a387e4efd3ea171616d9b76dcad6c85e7fd7c9406dc19495e279cbaebbd`

```dockerfile
```

-	Layers:
	-	`sha256:c1b655131c2f9a200d94f4a9833890220f71e30981b4064d2f16f8a833f997bb`  
		Last Modified: Fri, 08 May 2026 20:57:28 GMT  
		Size: 3.6 MB (3619254 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:49ddef005c38ab7a29e8f27a8e717e4f7c45fbf16cf5484b232c46b7d559ff7c`  
		Last Modified: Fri, 08 May 2026 20:57:28 GMT  
		Size: 15.1 KB (15087 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6` - linux; arm variant v7

```console
$ docker pull spiped@sha256:4ff1f64955f0baac28dd640dfec3eb6e7155387c14a4c6857815f04a5019ffc2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.8 MB (31802065 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3c7a8a4fd74a9ea680b4826c71ad4261c1b369234cf1e5a1af74de4f0f02780`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 19:43:48 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Fri, 08 May 2026 19:43:51 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:44:15 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Fri, 08 May 2026 19:44:15 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Fri, 08 May 2026 19:44:15 GMT
VOLUME [/spiped]
# Fri, 08 May 2026 19:44:15 GMT
WORKDIR /spiped
# Fri, 08 May 2026 19:44:15 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Fri, 08 May 2026 19:44:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 08 May 2026 19:44:15 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:f1433620eadfdfe016c8054b954f619ae5bca159f35a9459c36a76d9ef4d39c3`  
		Last Modified: Fri, 08 May 2026 18:37:58 GMT  
		Size: 26.2 MB (26214912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f160c4481d462904aa24778c4b01da7a50dd3330da0f3146ecd0fa1750b36e3`  
		Last Modified: Fri, 08 May 2026 19:44:22 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:004f6312484a065cbbbc3f38cbdcd14f9d0d288af4570dc95d0b422521d5a4e9`  
		Last Modified: Fri, 08 May 2026 19:44:22 GMT  
		Size: 828.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7cfb1c37acf55579035e448653f38eb6ee097fa7f5c76c63e12e4b73e6bed7e`  
		Last Modified: Fri, 08 May 2026 19:44:22 GMT  
		Size: 5.6 MB (5584782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55a95cb661cfcd83f6253fbdfda5fdca5527107bcaceb6cd297381b4a90ff390`  
		Last Modified: Fri, 08 May 2026 19:44:22 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d438e2f2f47da106abfac0e9680692ac80d185181f12e690966a0581ad54dd02`  
		Last Modified: Fri, 08 May 2026 19:44:23 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6` - unknown; unknown

```console
$ docker pull spiped@sha256:26f57e59b1a522ae1a687b8df8cf930ddf2c1d699112e21280421a49ca910972
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3633462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b2c0796641018c39128df86b179e33a156dcb32c5541d96e2972f2e703e151b`

```dockerfile
```

-	Layers:
	-	`sha256:418008c48573eba24e549885dce4ad96fd0a220792017aeb5f7acce11418e708`  
		Last Modified: Fri, 08 May 2026 19:44:22 GMT  
		Size: 3.6 MB (3618375 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0d6e39d76bd241efe3b0b538efe61306d7f2392070a38f4c7231ff87fb17c6fc`  
		Last Modified: Fri, 08 May 2026 19:44:22 GMT  
		Size: 15.1 KB (15087 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6` - linux; arm64 variant v8

```console
$ docker pull spiped@sha256:f4d2c7ba22fbdd4c39d643fc06400642b6d479a7dfc684a3939b41bd69392c60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.4 MB (36379770 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:076b678a615cd6adb58ebf5f146ff8d89909b5200fed70f6093a1252adb559d0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 19:36:49 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Fri, 08 May 2026 19:36:52 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:37:14 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Fri, 08 May 2026 19:37:14 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Fri, 08 May 2026 19:37:14 GMT
VOLUME [/spiped]
# Fri, 08 May 2026 19:37:14 GMT
WORKDIR /spiped
# Fri, 08 May 2026 19:37:14 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Fri, 08 May 2026 19:37:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 08 May 2026 19:37:14 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:9ebf9a1d0c9ca1bcb377e9dba38a3fdd3e89cf37164f4245286c24f8cd50a39e`  
		Last Modified: Fri, 08 May 2026 18:26:50 GMT  
		Size: 30.1 MB (30143642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab68b1d288c6fda5c3d291b76142d35c7ec90bba49f2f7e249984ab5030b2a8a`  
		Last Modified: Fri, 08 May 2026 19:37:21 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72258c478f2f0cacc665dd483d41ad5142247c03f899d55173f931b7e1127ccd`  
		Last Modified: Fri, 08 May 2026 19:37:21 GMT  
		Size: 829.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bff059afbb00a8d0c47938a8cd83a2cb69138df7c613c1ff73877639d5839980`  
		Last Modified: Fri, 08 May 2026 19:37:22 GMT  
		Size: 6.2 MB (6233755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45a3566292154189efcb23707ad78ae15514dc0e956d1fb5b4f10ca4fe927840`  
		Last Modified: Fri, 08 May 2026 19:37:22 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:290e4c2f5ef9aaf2f014d15a44512a40b25b7bc0cac6db9b8ae073550aadfd21`  
		Last Modified: Fri, 08 May 2026 19:37:23 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6` - unknown; unknown

```console
$ docker pull spiped@sha256:b8025f0910028dd9817f393058197a8d68cf5196c0a4e130126c5b48c10cb344
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3636412 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39ab8802b871f6dee336412a2abb98089de33fd8aaab9762c3cda2637371d0f2`

```dockerfile
```

-	Layers:
	-	`sha256:1778e062fea4855a339744af921af7d4db3810975c7e16ccd96cf39b1c6b1c2c`  
		Last Modified: Fri, 08 May 2026 19:37:22 GMT  
		Size: 3.6 MB (3621296 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5180c5ea69da7069bfd3b17dcadb7c91742ce10c5bb6bedca95126234abc14a7`  
		Last Modified: Fri, 08 May 2026 19:37:21 GMT  
		Size: 15.1 KB (15116 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6` - linux; 386

```console
$ docker pull spiped@sha256:d981618a0d9c00684e6abf3d84a440dd8149f059c1fa1770e74b57656b7d1660
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.7 MB (37741286 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a5cb61d1ba1a94f11c6345a5fdb6fea544260c32c6125120a8872687fa142f3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 19:42:56 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Fri, 08 May 2026 19:42:59 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:43:23 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Fri, 08 May 2026 19:43:23 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Fri, 08 May 2026 19:43:23 GMT
VOLUME [/spiped]
# Fri, 08 May 2026 19:43:24 GMT
WORKDIR /spiped
# Fri, 08 May 2026 19:43:24 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Fri, 08 May 2026 19:43:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 08 May 2026 19:43:24 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:43e2ffbaa23260ffb4e3de716920f2ed9e6af56e465ca1233a2d84c2cc1cf005`  
		Last Modified: Fri, 08 May 2026 18:32:48 GMT  
		Size: 31.3 MB (31296400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c17b41ec4f852447201aeb965c3aa2bafdee78fd8912e91f0b7978c569be5e2f`  
		Last Modified: Fri, 08 May 2026 19:43:31 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d70e5c72cd4936724086c00ec89429bded5df26b92391c2566ed2fb716f18aa7`  
		Last Modified: Fri, 08 May 2026 19:43:31 GMT  
		Size: 828.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:709085b6edd21ce82957d908045c521464897a7c5aa9403a2dd9fd0f92d5140e`  
		Last Modified: Fri, 08 May 2026 19:43:31 GMT  
		Size: 6.4 MB (6442518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b14de3e13da7ff3cc57333aab9a6a05e63d3b95b75b2817946da6be54d9c921`  
		Last Modified: Fri, 08 May 2026 19:43:31 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82008a569b9479b56a58f4f85ce555a0023f34e26440b092f1cf31191ce34456`  
		Last Modified: Fri, 08 May 2026 19:43:32 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6` - unknown; unknown

```console
$ docker pull spiped@sha256:3408744cec174cbb267a63b72e71e41b4e396fdbf4d8b29a489532fce7271e94
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3635335 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a172af2f2faf106a865ab5dc37e0b74df8c431777dbc521aa563779b97a0365`

```dockerfile
```

-	Layers:
	-	`sha256:aedee6e6a52a08621420305a03eeabe6aaa0173b995b54b09f9326e9c235f2be`  
		Last Modified: Fri, 08 May 2026 19:43:31 GMT  
		Size: 3.6 MB (3620389 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b58a647b7d7db8950d4a473142cb3d7427b419850101f376d98d507d3a374200`  
		Last Modified: Fri, 08 May 2026 19:43:30 GMT  
		Size: 14.9 KB (14946 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6` - linux; ppc64le

```console
$ docker pull spiped@sha256:2e4bd458122e32e6d0dabd95f38757741b801a99e93c50b9e645fa87eb51102a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.4 MB (40441188 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa385580deb2b8dcbc058025f53221c9c9a13ba6d0e1d1fcea983d0d8004f717`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 22:25:38 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Fri, 08 May 2026 22:25:44 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 22:26:31 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Fri, 08 May 2026 22:26:31 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Fri, 08 May 2026 22:26:31 GMT
VOLUME [/spiped]
# Fri, 08 May 2026 22:26:31 GMT
WORKDIR /spiped
# Fri, 08 May 2026 22:26:31 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Fri, 08 May 2026 22:26:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 08 May 2026 22:26:31 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:b9baa45d89920bd180d7551ccc5bc535e0c5f55b863ddebddfdc06f9436dfe91`  
		Last Modified: Fri, 08 May 2026 19:46:53 GMT  
		Size: 33.6 MB (33598087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:680ca9add7a30a7a7a02b373e65419c55c156f59ab37259115ead4b9683e755f`  
		Last Modified: Fri, 08 May 2026 22:26:46 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6fbd88296e83b0fe34af0d7aea8feb0ab152c24009771728138ab8ea6a3c7e3`  
		Last Modified: Fri, 08 May 2026 22:26:46 GMT  
		Size: 829.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:427b4091434bcad2400a705856ffbc391e8edb99ddd0244020ab8e87b8fb0029`  
		Last Modified: Fri, 08 May 2026 22:26:46 GMT  
		Size: 6.8 MB (6840726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5761c60db3e29874e7a761fb091b3a0716e00845ff60b44aed197905641f8201`  
		Last Modified: Fri, 08 May 2026 22:26:46 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d979fa4083e9e6936395a7aa0bbee2b7b6a8cc7f4e41e6234afe21c2ef4653e`  
		Last Modified: Fri, 08 May 2026 22:26:47 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6` - unknown; unknown

```console
$ docker pull spiped@sha256:05648be86c583500baf9a23fc752f751b17a45b3a93ce072b80d2c560c492e45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3637027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:527ae0828e720ab8c7f87f091c2295b3dcd1df2f39af33c2ebf4a290bf2b6a83`

```dockerfile
```

-	Layers:
	-	`sha256:5d43283d3f5718ce69f0dd46023d5abd6439b1b618e1f306799c06fe849aea01`  
		Last Modified: Fri, 08 May 2026 22:26:46 GMT  
		Size: 3.6 MB (3621997 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:917814349a2d8dd15ccd6b0a739bb88131cfd61f1a5b110c16b85cb164e6d7bb`  
		Last Modified: Fri, 08 May 2026 22:26:46 GMT  
		Size: 15.0 KB (15030 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6` - linux; riscv64

```console
$ docker pull spiped@sha256:4b71cf53987a9707a16131c1318e249b3fd3d6ce9a82cb42cc7f49e072e18fd7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.6 MB (37638423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f26a4b86552c1e9439f4f551a02d1d47a8a09b1564576e2077689ea60ed92ca7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1776729600'
# Thu, 23 Apr 2026 16:08:31 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Thu, 23 Apr 2026 16:09:01 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 23 Apr 2026 16:12:07 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Thu, 23 Apr 2026 16:12:07 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Thu, 23 Apr 2026 16:12:07 GMT
VOLUME [/spiped]
# Thu, 23 Apr 2026 16:12:07 GMT
WORKDIR /spiped
# Thu, 23 Apr 2026 16:12:08 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Thu, 23 Apr 2026 16:12:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 Apr 2026 16:12:08 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:c59e3a1f334be9f0528643dd07d69319f75f877f83be33ec1eff872a489985a0`  
		Last Modified: Wed, 22 Apr 2026 02:30:51 GMT  
		Size: 28.3 MB (28280195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65c3fe48b86e812e3913e5d13d1a9629869d202426b9c61e1715fa21c49eefb0`  
		Last Modified: Thu, 23 Apr 2026 16:13:20 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b34a84840c5fe62bd145180a478a04eb839e8ebc46151483b24496cb9f4a91f`  
		Last Modified: Thu, 23 Apr 2026 16:13:20 GMT  
		Size: 819.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d24129e4ff9e3418ef7a713edd9546c25c9b66ed26f8d5aa09e53f0c443a147`  
		Last Modified: Thu, 23 Apr 2026 16:13:23 GMT  
		Size: 9.4 MB (9355868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c9de411851378c843f1fa5367128062cec83a39214793d042c62249d045708d`  
		Last Modified: Thu, 23 Apr 2026 16:13:20 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e45064277bc4d512497c03c09b867eecba1e9f36520600b1b7cf50ccf931c314`  
		Last Modified: Thu, 23 Apr 2026 16:13:22 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6` - unknown; unknown

```console
$ docker pull spiped@sha256:8f1fdb09a20e86779bcd22247e4e7dc45779eadf380ed22541529e1f7c49f080
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3628433 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30611531e32494ce7228fad7644d17d3b521a5eb65e2cab640541ec507a3ccff`

```dockerfile
```

-	Layers:
	-	`sha256:28e7945cedc25231eedc0925db8b02ae1dfc5c3c41f66ebd1d3a8ef39e217551`  
		Last Modified: Thu, 23 Apr 2026 16:13:22 GMT  
		Size: 3.6 MB (3613403 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0b3f06dd63e825c9c98e9b4bfdc4f7087ec431640aee8976c15796ae26a216eb`  
		Last Modified: Thu, 23 Apr 2026 16:13:20 GMT  
		Size: 15.0 KB (15030 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6` - linux; s390x

```console
$ docker pull spiped@sha256:bd86a35901c83fdbe0b1dd9ab57c28d30a6565052dbe1ae0ef315fc89adffc00
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.0 MB (35964636 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90e9eead17c9f5aa0363836fa2a870f271ca50be7e2f1899fb3e7e0c17e6add5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 20:52:18 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Fri, 08 May 2026 20:52:21 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 20:52:41 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Fri, 08 May 2026 20:52:41 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Fri, 08 May 2026 20:52:41 GMT
VOLUME [/spiped]
# Fri, 08 May 2026 20:52:41 GMT
WORKDIR /spiped
# Fri, 08 May 2026 20:52:41 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Fri, 08 May 2026 20:52:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 08 May 2026 20:52:41 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:2fbbc68c452b3ba3a496488f38159dac53afe693311bee1c04f555d854ff4a2e`  
		Last Modified: Fri, 08 May 2026 18:29:20 GMT  
		Size: 29.8 MB (29840347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:379c83725970f21bcd83cf3380670f0ea271dd1fc30bc3e9568c083f2580ba55`  
		Last Modified: Fri, 08 May 2026 20:52:53 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3b3284a3de5bccf5d6b269c2b7bf9b319d15f9bebd9af7f1c95123337f82ffc`  
		Last Modified: Fri, 08 May 2026 20:52:53 GMT  
		Size: 829.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78ee74470711143892631998b06f797b17b8f24c199e31160dbad3fa3f9f4b1b`  
		Last Modified: Fri, 08 May 2026 20:52:53 GMT  
		Size: 6.1 MB (6121916 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5efe750c150333b99cd25f27597baa8d209228b9898aac1c0a7355a41ab17040`  
		Last Modified: Fri, 08 May 2026 20:52:53 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31b3234d867e10e2e459de5bd4cf9e1156a19cf24d495f2dfc7415071ae5715f`  
		Last Modified: Fri, 08 May 2026 20:52:54 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6` - unknown; unknown

```console
$ docker pull spiped@sha256:7c6bfdf45b3649d1b3f9001e65846a9f9c95d3e42d468a4d78f4b4419a680bf5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3633605 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5894b164eadfcc36f173a9f50f9038140f4fd57fd4528d5251f9f417819c1e0c`

```dockerfile
```

-	Layers:
	-	`sha256:117c16ab57c2ffc82accce55a8dd174232910aa2a2d2f4121a9924747a140c28`  
		Last Modified: Fri, 08 May 2026 20:52:53 GMT  
		Size: 3.6 MB (3618623 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b7501e35b7a1f23c01cc4fa7d7fe477f7d1e791f6af13d52b1b0b27d654c13a4`  
		Last Modified: Fri, 08 May 2026 20:52:53 GMT  
		Size: 15.0 KB (14982 bytes)  
		MIME: application/vnd.in-toto+json

## `spiped:1.6-alpine`

```console
$ docker pull spiped@sha256:10785aa58079387363e472d7e20eb96bd01f12b9850476a066e124d57be1a8cc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 16
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `spiped:1.6-alpine` - linux; amd64

```console
$ docker pull spiped@sha256:6a78a135961dde77e0a3e9171928717694804d7cfb3d6aedbebfadb42bf4f3e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3925151 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06f599634d068048f3fcd01d27356e8cc57fb8937f8bbf03cfccaebddd3b1e24`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:02 GMT
ADD alpine-minirootfs-3.22.4-x86_64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:02 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 00:14:35 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Fri, 17 Apr 2026 00:14:36 GMT
RUN apk add --no-cache libssl3 # buildkit
# Fri, 17 Apr 2026 00:14:45 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Fri, 17 Apr 2026 00:14:45 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Fri, 17 Apr 2026 00:14:45 GMT
VOLUME [/spiped]
# Fri, 17 Apr 2026 00:14:45 GMT
WORKDIR /spiped
# Fri, 17 Apr 2026 00:14:45 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Fri, 17 Apr 2026 00:14:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 17 Apr 2026 00:14:45 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:84f5eff04246b56d48d1ed6cbd82d6bc7e53f7e790db6a467f92571c69f3289e`  
		Last Modified: Thu, 16 Apr 2026 23:53:07 GMT  
		Size: 3.8 MB (3808189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09629d4032ef7ab1ef9db974170b9cf0e98f6c5d68cb9f3d0e21a37889d50030`  
		Last Modified: Fri, 17 Apr 2026 00:14:50 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cad68e6c6d9b805cb5d27e526a335f55ae1e22e51fb78ed5cd842984966ec752`  
		Last Modified: Fri, 17 Apr 2026 00:14:50 GMT  
		Size: 7.9 KB (7942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0097cdb4e276728ffaa69c00b45edf54d761118176e68ef12d68092b7417f986`  
		Last Modified: Fri, 17 Apr 2026 00:14:50 GMT  
		Size: 107.6 KB (107638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9bc806c3d4f80593516df4d73efec6cd1cf16dfd200d5fd6adda41910072975`  
		Last Modified: Fri, 17 Apr 2026 00:14:50 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d250500ebc740f642b6509ef0a3f0576fe4b93cb687a514ceede64292cd717f`  
		Last Modified: Fri, 17 Apr 2026 00:14:51 GMT  
		Size: 336.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:dcf1f88cd35b0648a36b53371be8057efc788150c247273946f22f226c8922f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.5 KB (96450 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b695771cd59164f79af4e3d51a194af63f71274fa2ca45642700481f66706680`

```dockerfile
```

-	Layers:
	-	`sha256:9047c6064b6fcd9efa90aa0c959722cd5d0677dd3e15d576484c71664c66a025`  
		Last Modified: Fri, 17 Apr 2026 00:14:50 GMT  
		Size: 82.2 KB (82192 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b1ebf9604f23105cb6660c6767d301a937a4b9d6d85433f32e35ffb2ba1e86d8`  
		Last Modified: Fri, 17 Apr 2026 00:14:50 GMT  
		Size: 14.3 KB (14258 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6-alpine` - linux; arm variant v6

```console
$ docker pull spiped@sha256:e61a3952e5718375c379136684659c21136328808a6c3f88e9585943251e9a16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3605859 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c576e8f7269c2ef4826f92b4a22494225a6cd470d17d9f30f01d9cc229e696f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:27 GMT
ADD alpine-minirootfs-3.22.4-armhf.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:27 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 00:28:09 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Fri, 17 Apr 2026 00:28:10 GMT
RUN apk add --no-cache libssl3 # buildkit
# Fri, 17 Apr 2026 00:28:20 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Fri, 17 Apr 2026 00:28:20 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Fri, 17 Apr 2026 00:28:20 GMT
VOLUME [/spiped]
# Fri, 17 Apr 2026 00:28:20 GMT
WORKDIR /spiped
# Fri, 17 Apr 2026 00:28:20 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Fri, 17 Apr 2026 00:28:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 17 Apr 2026 00:28:20 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:08c654e9a4409dbbeb5faba9659360f33dbc6f7a6d79ebebe08f57d22a1b76fc`  
		Last Modified: Thu, 16 Apr 2026 23:53:31 GMT  
		Size: 3.5 MB (3507383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a28595f303e8390d8534900bd78b38647a907732d3d3e842c7b3a9caf747dfa`  
		Last Modified: Fri, 17 Apr 2026 00:28:24 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04a2d882259c543692d98198b2c8f098f64b95d9b8018fbe3daf4bce16ccdea8`  
		Last Modified: Fri, 17 Apr 2026 00:28:24 GMT  
		Size: 7.9 KB (7941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:750bf6b03a38c9f5493952dd7c83dba844fa70e86926b54303c228f996e864fb`  
		Last Modified: Fri, 17 Apr 2026 00:28:24 GMT  
		Size: 89.2 KB (89153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bb0b56fb727ea9f7a3dad23a396c81b60139284396a263e6658329c844b5dad`  
		Last Modified: Fri, 17 Apr 2026 00:28:23 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20e6b266845306bbbcbee6801a12889b7c152b510808934deb45a090cedc3a06`  
		Last Modified: Fri, 17 Apr 2026 00:28:25 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:e8ab0469cf1a0658dd7f777f120002189b116eedc60e2d13004809373539fd11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.1 KB (14144 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cfbd38bcf39cf976d74f4ea0d61a864e9b890815035438f477a99caff10eae99`

```dockerfile
```

-	Layers:
	-	`sha256:acf29d68d1e7fa30dc5742c4211ffe81430df68660be1f3d0207d5a94d98bc39`  
		Last Modified: Fri, 17 Apr 2026 00:28:23 GMT  
		Size: 14.1 KB (14144 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6-alpine` - linux; arm variant v7

```console
$ docker pull spiped@sha256:147fe0124aa237fa168a69becb6a2db57f4a9ad7144beb44a52a7735a75ed88f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3316848 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1fac8ff5e55f7bb423942ebc9a0dcfe62ab45560df8acbf81f20fce40adfb0d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 16 Apr 2026 23:54:02 GMT
ADD alpine-minirootfs-3.22.4-armv7.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:54:02 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 00:13:44 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Fri, 17 Apr 2026 00:13:45 GMT
RUN apk add --no-cache libssl3 # buildkit
# Fri, 17 Apr 2026 00:13:54 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Fri, 17 Apr 2026 00:13:54 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Fri, 17 Apr 2026 00:13:54 GMT
VOLUME [/spiped]
# Fri, 17 Apr 2026 00:13:54 GMT
WORKDIR /spiped
# Fri, 17 Apr 2026 00:13:54 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Fri, 17 Apr 2026 00:13:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 17 Apr 2026 00:13:54 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:99e8c7f1cf08d3156a369084c1a1fd745878aa29f4a0f55d73e953b93f0b7a93`  
		Last Modified: Thu, 16 Apr 2026 23:54:07 GMT  
		Size: 3.2 MB (3225830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e48112adbff0844ea29be59655ce36bdc68db268960b43349a213160861be5b`  
		Last Modified: Fri, 17 Apr 2026 00:13:59 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62b71c7a3ae36749950f95514df7064116e47fac5d0e8f2b2a7465a08ec730b1`  
		Last Modified: Fri, 17 Apr 2026 00:13:59 GMT  
		Size: 7.9 KB (7949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90dbc42fa35611c27c8478a77677c7599958f859178a2ae432cdeea23ff283fe`  
		Last Modified: Fri, 17 Apr 2026 00:13:59 GMT  
		Size: 81.7 KB (81682 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d17f9759dca0bc64327214acbd9fd3deb78375c7afd7010e30d54ffe9eafdb6`  
		Last Modified: Fri, 17 Apr 2026 00:13:59 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87eff9de0017984f4c4aceb50f22ba5600d01062af116b4a3d8666f104982e79`  
		Last Modified: Fri, 17 Apr 2026 00:14:00 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:87b16d20b49f4fd531d2a7882ebf70ab433c78455a68ecb63229df2b111b80e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.6 KB (96590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4db1828da7718e04747ebb0f602b5974b0a7a0da76481d2a933ecbb6b1869fd9`

```dockerfile
```

-	Layers:
	-	`sha256:32fd82b374cd8966ecaddf73d35913d341f1bf089acec4758b0eddc9ae15bf6c`  
		Last Modified: Fri, 17 Apr 2026 00:13:59 GMT  
		Size: 82.2 KB (82228 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:451cb443bac28fadec04af355b08de89c30845228bcead9735b3be6a627381f6`  
		Last Modified: Fri, 17 Apr 2026 00:13:59 GMT  
		Size: 14.4 KB (14362 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6-alpine` - linux; arm64 variant v8

```console
$ docker pull spiped@sha256:1fd688a89197aa9ec5aa2ecf456f856d56b46639e5d0733ee167c8e1f1f67c29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4251815 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3e3a3494482e2c117fe69680a253048739b96db6b666e0ba693d69f12f3cffa`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:00 GMT
ADD alpine-minirootfs-3.22.4-aarch64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:00 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 00:23:30 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Fri, 17 Apr 2026 00:23:30 GMT
RUN apk add --no-cache libssl3 # buildkit
# Fri, 17 Apr 2026 00:23:40 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Fri, 17 Apr 2026 00:23:40 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Fri, 17 Apr 2026 00:23:40 GMT
VOLUME [/spiped]
# Fri, 17 Apr 2026 00:23:40 GMT
WORKDIR /spiped
# Fri, 17 Apr 2026 00:23:40 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Fri, 17 Apr 2026 00:23:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 17 Apr 2026 00:23:40 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:58e777220c395c319866c5d73ea32a5ea574bbd12f4eb289b392f584d0cd953e`  
		Last Modified: Thu, 16 Apr 2026 23:53:05 GMT  
		Size: 4.1 MB (4141894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3b70cf46309ade34c5a66991fc83a20e95c2a2ca7662393d07532b98169b897`  
		Last Modified: Fri, 17 Apr 2026 00:23:45 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4aa5fdf2c2bb57fb12d420f1ebc379b73a6a07a076dd649edbdfb2ec65e9b52f`  
		Last Modified: Fri, 17 Apr 2026 00:23:45 GMT  
		Size: 7.9 KB (7939 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62bde94e8b5d108bfaf26624adc0087452e38a2a8176cc98ece876fe2117fc72`  
		Last Modified: Fri, 17 Apr 2026 00:23:45 GMT  
		Size: 100.6 KB (100601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec5b88c8155b1bdcaf3ceb67be1cd60eac4d053dbde4189b58b41e709ce71a5d`  
		Last Modified: Fri, 17 Apr 2026 00:23:45 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bb330bcfc9ca5ba0cfa2155b2866b977ad2c3ce1d9ae151d07e639bbada8ed2`  
		Last Modified: Fri, 17 Apr 2026 00:23:46 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:fc73de67fe7f5bcda008d343140166980bf4176b3096a535d83f3dcd2d534e5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.6 KB (96641 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a18fe2b2319a581866e1c86ace119888f0e7b9a60b55a3ce6b779f28fe92710`

```dockerfile
```

-	Layers:
	-	`sha256:a96c2085f2ac76644e77254bfa9bf6d1b56c67d9d9405eaa8416f74fcba97701`  
		Last Modified: Fri, 17 Apr 2026 00:23:45 GMT  
		Size: 82.2 KB (82248 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a7d5f7f4737f85a0e24460592078844c64dafe02803bdf87581c20f597e952bb`  
		Last Modified: Fri, 17 Apr 2026 00:23:45 GMT  
		Size: 14.4 KB (14393 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6-alpine` - linux; 386

```console
$ docker pull spiped@sha256:60c2f83afdec0385615a7286994daa8f205766ef71d83fa8ddc2e700ac81936f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3754157 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fdc7573391c8c621e1b2f987722ca168aebbe555b0499e62e86738da10c96e58`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Fri, 17 Apr 2026 02:42:29 GMT
ADD alpine-minirootfs-3.22.4-x86.tar.gz / # buildkit
# Fri, 17 Apr 2026 02:42:29 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 05:54:58 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Fri, 17 Apr 2026 05:54:58 GMT
RUN apk add --no-cache libssl3 # buildkit
# Fri, 17 Apr 2026 05:55:09 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Fri, 17 Apr 2026 05:55:09 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Fri, 17 Apr 2026 05:55:09 GMT
VOLUME [/spiped]
# Fri, 17 Apr 2026 05:55:09 GMT
WORKDIR /spiped
# Fri, 17 Apr 2026 05:55:09 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Fri, 17 Apr 2026 05:55:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 17 Apr 2026 05:55:09 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:481dba1f7704181ddc1e2b499675e9651a93f972d4cd141a4933d44622cdc88a`  
		Last Modified: Fri, 17 Apr 2026 02:42:34 GMT  
		Size: 3.6 MB (3624721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2f934ad8efa54d7383ed1d7daf8f07d69a316c785b55e29d855f59724767ac5`  
		Last Modified: Fri, 17 Apr 2026 05:55:13 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fad6a50d64bebedb5b11ecc9dbad14debf2baa30235c5ed093775151dd20c5f`  
		Last Modified: Fri, 17 Apr 2026 05:55:13 GMT  
		Size: 7.9 KB (7947 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4e9ad205a738e9a190290cb841b91a7516b90d39ccefc8a464803a80e5d3bf2`  
		Last Modified: Fri, 17 Apr 2026 05:55:14 GMT  
		Size: 120.1 KB (120105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b13bce07410da4d5d2d2271580461ed3ae19008e5249df3c1003a06c213c180b`  
		Last Modified: Fri, 17 Apr 2026 05:55:14 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d30a682d686a1255ac7f31b311acf6f01b819da6af05a18bb59cf9285441247`  
		Last Modified: Fri, 17 Apr 2026 05:55:14 GMT  
		Size: 336.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:499b7ec7b9c4e4eec426321c8934ac7fac003aeff1b6247ccf002c546cd6a262
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.4 KB (96390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9072722cf70bdbdd1bd5420a6744bc8ca176440a12571a40e33ce18862067a55`

```dockerfile
```

-	Layers:
	-	`sha256:dd1f08b2c21c938da19a9533a1b9dcb5f15e078dab41c9a4bd4ab244cd979858`  
		Last Modified: Fri, 17 Apr 2026 05:55:13 GMT  
		Size: 82.2 KB (82167 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:517f76f905b9dca96e65eec9ad79a6211e1b541723537e827a226d4839aa2649`  
		Last Modified: Fri, 17 Apr 2026 05:55:14 GMT  
		Size: 14.2 KB (14223 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6-alpine` - linux; ppc64le

```console
$ docker pull spiped@sha256:cd9ed7a248ccd86ed221ed62ccb5fccc85d88f92bb07eacf32a54aa285d3baef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3858669 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01b17425a87a9b3f6cf310b87ae46b1234772bd0b80ea164489da909a148229e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Fri, 17 Apr 2026 00:00:29 GMT
ADD alpine-minirootfs-3.22.4-ppc64le.tar.gz / # buildkit
# Fri, 17 Apr 2026 00:00:29 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 01:13:47 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Fri, 17 Apr 2026 01:13:49 GMT
RUN apk add --no-cache libssl3 # buildkit
# Fri, 17 Apr 2026 01:14:13 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Fri, 17 Apr 2026 01:14:13 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Fri, 17 Apr 2026 01:14:13 GMT
VOLUME [/spiped]
# Fri, 17 Apr 2026 01:14:15 GMT
WORKDIR /spiped
# Fri, 17 Apr 2026 01:14:15 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Fri, 17 Apr 2026 01:14:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 17 Apr 2026 01:14:15 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:9d65ab042d46bde09babe9a9587237000067c332d24fd9ca516fea7bdfb77c80`  
		Last Modified: Fri, 17 Apr 2026 00:00:38 GMT  
		Size: 3.7 MB (3736656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d4eb2b31b373fa4117e61ee4973c717af31bc2e3376684ddf64780f6a0cfbf2`  
		Last Modified: Fri, 17 Apr 2026 01:14:36 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e5bc892fe10dffc5824aa6f02e4a3fd2d8872fcc548dc32d8271fbeda871d54`  
		Last Modified: Fri, 17 Apr 2026 01:14:36 GMT  
		Size: 8.0 KB (7951 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a0f69169c64986eaf44f560100f0ace1b79586cff5d1f517fcf6f2810fcf476`  
		Last Modified: Fri, 17 Apr 2026 01:14:36 GMT  
		Size: 112.7 KB (112676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ecc1153f644e2e26a00aa90bf9b03917ab7f9ec331b32bd9bc295281cee7151`  
		Last Modified: Fri, 17 Apr 2026 01:14:36 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94785087e434424ecd2b2a79b34d04d7aa53bdc943265138216cadd6badf5495`  
		Last Modified: Fri, 17 Apr 2026 01:14:37 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:42b060f58ef29347aa95f2a95a49a750c85e6dc1283a7429bdbd08cbb35d8c90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.6 KB (94582 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1aeddc4f5e06133647f4d77b87d5471240c741e9ac4581ee0469cd5e684bde41`

```dockerfile
```

-	Layers:
	-	`sha256:8054970ddb854b9dbe87ad8cc6cb52f8ac69bae6393895a2cc0ec179d9890648`  
		Last Modified: Fri, 17 Apr 2026 01:14:36 GMT  
		Size: 80.3 KB (80275 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5cf789792086c7df442c741fa726e1c634b400a002527085dcc36c87a5bdd724`  
		Last Modified: Fri, 17 Apr 2026 01:14:36 GMT  
		Size: 14.3 KB (14307 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6-alpine` - linux; riscv64

```console
$ docker pull spiped@sha256:eaf86ffaae6edde3dcb5bc958a07fa09bfe7cf9bcd05be9ace676e83efe5f761
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3629050 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:508a25834d52056b9c731fc2100ea35e54d563c093104a90eef8c05cb0cd1cf9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Fri, 17 Apr 2026 07:18:45 GMT
ADD alpine-minirootfs-3.22.4-riscv64.tar.gz / # buildkit
# Fri, 17 Apr 2026 07:18:45 GMT
CMD ["/bin/sh"]
# Sun, 19 Apr 2026 03:43:32 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Sun, 19 Apr 2026 03:43:36 GMT
RUN apk add --no-cache libssl3 # buildkit
# Sun, 19 Apr 2026 03:45:16 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Sun, 19 Apr 2026 03:45:16 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Sun, 19 Apr 2026 03:45:16 GMT
VOLUME [/spiped]
# Sun, 19 Apr 2026 03:45:16 GMT
WORKDIR /spiped
# Sun, 19 Apr 2026 03:45:17 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 19 Apr 2026 03:45:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 19 Apr 2026 03:45:17 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:fbc07c8b85a3c60e503ffd0cbe3e1b3947fd65764784e1bd9d943ac21097cce7`  
		Last Modified: Fri, 17 Apr 2026 07:19:08 GMT  
		Size: 3.5 MB (3520880 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62f6ee73726995fef9f6ea4faf4767bcea48e04bfd71f1eea0bd05f9534d43f8`  
		Last Modified: Sun, 19 Apr 2026 03:45:37 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ce2dd3bcf1d4c6316b374da1b2790b7de4b60cf8e6512e5f30f8d7b2d7a3b38`  
		Last Modified: Sun, 19 Apr 2026 03:45:37 GMT  
		Size: 7.9 KB (7940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8e66ca15c2a84ed0ad5aac95f1257383ec006115c07282942c1fd6f06bc2b26`  
		Last Modified: Sun, 19 Apr 2026 03:45:37 GMT  
		Size: 98.8 KB (98844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04a854d7ad8f0e7a7a6274e5c362b1a896bd76e462c14408778ba02dff83d37b`  
		Last Modified: Sun, 19 Apr 2026 03:45:37 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5ff5f61469b0ef7c1c8bf56662d9b762181e909bc3c749eacbaaecf7bb475ab`  
		Last Modified: Sun, 19 Apr 2026 03:45:39 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:f21b45950838bc0c80c8410cc4f2814b68f96ecad1e19be90b06994c99afbf58
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.6 KB (94574 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1abe71f567ae68daf6e6dfeaafd74f8104d7a6958082dd986f64838b44c12b9f`

```dockerfile
```

-	Layers:
	-	`sha256:e9f4f6fe1bacdcf68608f4eb99bf2115bae97f39b1056b72d36c08b63e32ef42`  
		Last Modified: Sun, 19 Apr 2026 03:45:37 GMT  
		Size: 80.3 KB (80271 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d5e5c1e0a1d68c8bdb360c97f9072a3c973409b2f9afe7ff5795d523cae5119b`  
		Last Modified: Sun, 19 Apr 2026 03:45:38 GMT  
		Size: 14.3 KB (14303 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6-alpine` - linux; s390x

```console
$ docker pull spiped@sha256:d63a333156f14c550016968b48b61e03d6ffa7cdadeb4dc11994993be83c667f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3760132 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:425f883e0aba651c328e78b42abc6210940d11022f1ee5d1ff5258ebca42e51f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:56 GMT
ADD alpine-minirootfs-3.22.4-s390x.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:56 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 00:41:11 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Fri, 17 Apr 2026 00:41:12 GMT
RUN apk add --no-cache libssl3 # buildkit
# Fri, 17 Apr 2026 00:41:19 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Fri, 17 Apr 2026 00:41:19 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Fri, 17 Apr 2026 00:41:19 GMT
VOLUME [/spiped]
# Fri, 17 Apr 2026 00:41:19 GMT
WORKDIR /spiped
# Fri, 17 Apr 2026 00:41:19 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Fri, 17 Apr 2026 00:41:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 17 Apr 2026 00:41:19 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:54b429821fc7436a26fe07d9038b86e2bef4ef3bf03e43e9ae5e91ab8e4b37a9`  
		Last Modified: Thu, 16 Apr 2026 23:54:12 GMT  
		Size: 3.7 MB (3653873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98c5658f716398e67bcdf451aa62d9268badc01207fb2761dde286827e782131`  
		Last Modified: Fri, 17 Apr 2026 00:41:28 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d837fc0069a0ae8449bb0adb9f65b43fff5ff059948bf845ea728a30d3eaca0`  
		Last Modified: Fri, 17 Apr 2026 00:41:28 GMT  
		Size: 7.9 KB (7947 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:669f2f936af1acb505aa131fbad0547df0d36ff3dc9c4f8c3a396c9877b87798`  
		Last Modified: Fri, 17 Apr 2026 00:41:28 GMT  
		Size: 96.9 KB (96930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33930e4a86d8157d355b84eecf720d4f20b38ee3502ab3baa6329d6c6acac811`  
		Last Modified: Fri, 17 Apr 2026 00:41:28 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27970db5cca98e64b9bdffc3b4445e18a503e3e0dc858c6ae91eff10bccd50bd`  
		Last Modified: Fri, 17 Apr 2026 00:41:29 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:3a63421a60ad516e8ae99df7c008ce97158220da99f3e592d9090f762eb254c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.5 KB (94497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03ae27771b3c7505fb78b0f0546a7416b11e879220de4dc6090bf643dedf8614`

```dockerfile
```

-	Layers:
	-	`sha256:c6abf9efd631a7212221f0b771ec35e734885be3d3a6755a004bba8bd46cc068`  
		Last Modified: Fri, 17 Apr 2026 00:41:28 GMT  
		Size: 80.2 KB (80241 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:033e56e9f47fa0453060710502d5ab3daddcba0cc4e51e5e138a57faf3e873d6`  
		Last Modified: Fri, 17 Apr 2026 00:41:28 GMT  
		Size: 14.3 KB (14256 bytes)  
		MIME: application/vnd.in-toto+json

## `spiped:1.6.4`

```console
$ docker pull spiped@sha256:88bc77b7f493281dc8a9e59dc2520bc581437fda4955fe72e186b89e6f5fcc51
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 16
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v5
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `spiped:1.6.4` - linux; amd64

```console
$ docker pull spiped@sha256:6efd769d805f600ba739d18173542643175bc85a275a6c2b774507b866215473
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.8 MB (36830428 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3193b704891a8a18ac61ecedd914fc9f5bd4f08bcb9f49c1bf5d515f1d635642`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 19:35:11 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Fri, 08 May 2026 19:35:13 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:35:34 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Fri, 08 May 2026 19:35:34 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Fri, 08 May 2026 19:35:34 GMT
VOLUME [/spiped]
# Fri, 08 May 2026 19:35:35 GMT
WORKDIR /spiped
# Fri, 08 May 2026 19:35:35 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Fri, 08 May 2026 19:35:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 08 May 2026 19:35:35 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:57fb71246055257a374deb7564ceca10f43c2352572b501efc08add5d24ebb61`  
		Last Modified: Fri, 08 May 2026 18:24:13 GMT  
		Size: 29.8 MB (29780226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d57dde26e20eb068bd1c6070f0dd034bd2fd4bb74b1da82102adef70cdfed8b`  
		Last Modified: Fri, 08 May 2026 19:35:41 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00bc21a8189b7a94c8796b3a7235e2b6031c3bb5c38a32e6dd145ecc6bbf04b7`  
		Last Modified: Fri, 08 May 2026 19:35:41 GMT  
		Size: 829.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e86acbd1889987e9e18c2f14f31b0434706f81121130868eda3c8c530a20af8`  
		Last Modified: Fri, 08 May 2026 19:35:42 GMT  
		Size: 7.0 MB (7047830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8465fa5d80692f7b30c835d41e84147136800e2c926a318e6f844e8aa3836bac`  
		Last Modified: Fri, 08 May 2026 19:35:41 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c80c6cb3750ff6c08d0efb53fca666dfb8b02730a76835cddd23324fdb9c8a50`  
		Last Modified: Fri, 08 May 2026 19:35:42 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6.4` - unknown; unknown

```console
$ docker pull spiped@sha256:487c3ee9e344c1a378f97678431d3e69821f86c4eda6453de29af68a08d68173
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3641240 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc31b2a2f275eaf7500af7747def58d03e41f11827d308adb17d72a49c616aac`

```dockerfile
```

-	Layers:
	-	`sha256:4b40916ec2afebb3f0a5a2048230524b2afb160289fc9744212b19b511be425d`  
		Last Modified: Fri, 08 May 2026 19:35:41 GMT  
		Size: 3.6 MB (3626260 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:50c2e4615b4f2b4e4ffd2810f21ba67d9914c2f032810327b3488715ae97a747`  
		Last Modified: Fri, 08 May 2026 19:35:41 GMT  
		Size: 15.0 KB (14980 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6.4` - linux; arm variant v5

```console
$ docker pull spiped@sha256:6cbedd59e1b9ab471903f2f35a283d6f759be7121323441a6ca11573d8ae1cc4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.7 MB (33739804 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d990d2ba40ebc977000d42cedd17ab74640ddafe3cdee97d15362100231d6383`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 20:56:49 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Fri, 08 May 2026 20:56:54 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 20:57:21 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Fri, 08 May 2026 20:57:21 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Fri, 08 May 2026 20:57:21 GMT
VOLUME [/spiped]
# Fri, 08 May 2026 20:57:21 GMT
WORKDIR /spiped
# Fri, 08 May 2026 20:57:21 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Fri, 08 May 2026 20:57:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 08 May 2026 20:57:21 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:8f774e9b92b540806fc05167db7ce09a3e1b12abdb9d496f7b8c82138656065a`  
		Last Modified: Fri, 08 May 2026 18:33:49 GMT  
		Size: 27.9 MB (27948200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a147b3e27022cec78f27ab492347bf10b38fbc6c422c905e72f65841af2c2d35`  
		Last Modified: Fri, 08 May 2026 20:57:28 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f6f9b4d53a44c3aa0c748c56ea7420bc6a2ab57d31e476283c807a478c52a3b`  
		Last Modified: Fri, 08 May 2026 20:57:28 GMT  
		Size: 834.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7292710fe7c3115e3ec777cbaae5e736fe457c7abb0b37105d16f3dd0e6aa0d0`  
		Last Modified: Fri, 08 May 2026 20:57:28 GMT  
		Size: 5.8 MB (5789227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1be583d842fa62ff531b016e5bcc500de7cb8e354eddd92a4d45dc6617a54826`  
		Last Modified: Fri, 08 May 2026 20:57:28 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e608db2fba73f6cd7cc5367f133a6f818229089838eec0abce963f0960c957e`  
		Last Modified: Fri, 08 May 2026 20:57:29 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6.4` - unknown; unknown

```console
$ docker pull spiped@sha256:ee5c5f8032a4007863cf92bf644d1f00091054b2afe7ed6c0a2abd05eabee240
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3634341 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:713b5a387e4efd3ea171616d9b76dcad6c85e7fd7c9406dc19495e279cbaebbd`

```dockerfile
```

-	Layers:
	-	`sha256:c1b655131c2f9a200d94f4a9833890220f71e30981b4064d2f16f8a833f997bb`  
		Last Modified: Fri, 08 May 2026 20:57:28 GMT  
		Size: 3.6 MB (3619254 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:49ddef005c38ab7a29e8f27a8e717e4f7c45fbf16cf5484b232c46b7d559ff7c`  
		Last Modified: Fri, 08 May 2026 20:57:28 GMT  
		Size: 15.1 KB (15087 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6.4` - linux; arm variant v7

```console
$ docker pull spiped@sha256:4ff1f64955f0baac28dd640dfec3eb6e7155387c14a4c6857815f04a5019ffc2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.8 MB (31802065 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3c7a8a4fd74a9ea680b4826c71ad4261c1b369234cf1e5a1af74de4f0f02780`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 19:43:48 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Fri, 08 May 2026 19:43:51 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:44:15 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Fri, 08 May 2026 19:44:15 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Fri, 08 May 2026 19:44:15 GMT
VOLUME [/spiped]
# Fri, 08 May 2026 19:44:15 GMT
WORKDIR /spiped
# Fri, 08 May 2026 19:44:15 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Fri, 08 May 2026 19:44:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 08 May 2026 19:44:15 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:f1433620eadfdfe016c8054b954f619ae5bca159f35a9459c36a76d9ef4d39c3`  
		Last Modified: Fri, 08 May 2026 18:37:58 GMT  
		Size: 26.2 MB (26214912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f160c4481d462904aa24778c4b01da7a50dd3330da0f3146ecd0fa1750b36e3`  
		Last Modified: Fri, 08 May 2026 19:44:22 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:004f6312484a065cbbbc3f38cbdcd14f9d0d288af4570dc95d0b422521d5a4e9`  
		Last Modified: Fri, 08 May 2026 19:44:22 GMT  
		Size: 828.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7cfb1c37acf55579035e448653f38eb6ee097fa7f5c76c63e12e4b73e6bed7e`  
		Last Modified: Fri, 08 May 2026 19:44:22 GMT  
		Size: 5.6 MB (5584782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55a95cb661cfcd83f6253fbdfda5fdca5527107bcaceb6cd297381b4a90ff390`  
		Last Modified: Fri, 08 May 2026 19:44:22 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d438e2f2f47da106abfac0e9680692ac80d185181f12e690966a0581ad54dd02`  
		Last Modified: Fri, 08 May 2026 19:44:23 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6.4` - unknown; unknown

```console
$ docker pull spiped@sha256:26f57e59b1a522ae1a687b8df8cf930ddf2c1d699112e21280421a49ca910972
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3633462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b2c0796641018c39128df86b179e33a156dcb32c5541d96e2972f2e703e151b`

```dockerfile
```

-	Layers:
	-	`sha256:418008c48573eba24e549885dce4ad96fd0a220792017aeb5f7acce11418e708`  
		Last Modified: Fri, 08 May 2026 19:44:22 GMT  
		Size: 3.6 MB (3618375 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0d6e39d76bd241efe3b0b538efe61306d7f2392070a38f4c7231ff87fb17c6fc`  
		Last Modified: Fri, 08 May 2026 19:44:22 GMT  
		Size: 15.1 KB (15087 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6.4` - linux; arm64 variant v8

```console
$ docker pull spiped@sha256:f4d2c7ba22fbdd4c39d643fc06400642b6d479a7dfc684a3939b41bd69392c60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.4 MB (36379770 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:076b678a615cd6adb58ebf5f146ff8d89909b5200fed70f6093a1252adb559d0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 19:36:49 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Fri, 08 May 2026 19:36:52 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:37:14 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Fri, 08 May 2026 19:37:14 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Fri, 08 May 2026 19:37:14 GMT
VOLUME [/spiped]
# Fri, 08 May 2026 19:37:14 GMT
WORKDIR /spiped
# Fri, 08 May 2026 19:37:14 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Fri, 08 May 2026 19:37:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 08 May 2026 19:37:14 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:9ebf9a1d0c9ca1bcb377e9dba38a3fdd3e89cf37164f4245286c24f8cd50a39e`  
		Last Modified: Fri, 08 May 2026 18:26:50 GMT  
		Size: 30.1 MB (30143642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab68b1d288c6fda5c3d291b76142d35c7ec90bba49f2f7e249984ab5030b2a8a`  
		Last Modified: Fri, 08 May 2026 19:37:21 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72258c478f2f0cacc665dd483d41ad5142247c03f899d55173f931b7e1127ccd`  
		Last Modified: Fri, 08 May 2026 19:37:21 GMT  
		Size: 829.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bff059afbb00a8d0c47938a8cd83a2cb69138df7c613c1ff73877639d5839980`  
		Last Modified: Fri, 08 May 2026 19:37:22 GMT  
		Size: 6.2 MB (6233755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45a3566292154189efcb23707ad78ae15514dc0e956d1fb5b4f10ca4fe927840`  
		Last Modified: Fri, 08 May 2026 19:37:22 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:290e4c2f5ef9aaf2f014d15a44512a40b25b7bc0cac6db9b8ae073550aadfd21`  
		Last Modified: Fri, 08 May 2026 19:37:23 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6.4` - unknown; unknown

```console
$ docker pull spiped@sha256:b8025f0910028dd9817f393058197a8d68cf5196c0a4e130126c5b48c10cb344
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3636412 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39ab8802b871f6dee336412a2abb98089de33fd8aaab9762c3cda2637371d0f2`

```dockerfile
```

-	Layers:
	-	`sha256:1778e062fea4855a339744af921af7d4db3810975c7e16ccd96cf39b1c6b1c2c`  
		Last Modified: Fri, 08 May 2026 19:37:22 GMT  
		Size: 3.6 MB (3621296 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5180c5ea69da7069bfd3b17dcadb7c91742ce10c5bb6bedca95126234abc14a7`  
		Last Modified: Fri, 08 May 2026 19:37:21 GMT  
		Size: 15.1 KB (15116 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6.4` - linux; 386

```console
$ docker pull spiped@sha256:d981618a0d9c00684e6abf3d84a440dd8149f059c1fa1770e74b57656b7d1660
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.7 MB (37741286 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a5cb61d1ba1a94f11c6345a5fdb6fea544260c32c6125120a8872687fa142f3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 19:42:56 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Fri, 08 May 2026 19:42:59 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:43:23 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Fri, 08 May 2026 19:43:23 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Fri, 08 May 2026 19:43:23 GMT
VOLUME [/spiped]
# Fri, 08 May 2026 19:43:24 GMT
WORKDIR /spiped
# Fri, 08 May 2026 19:43:24 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Fri, 08 May 2026 19:43:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 08 May 2026 19:43:24 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:43e2ffbaa23260ffb4e3de716920f2ed9e6af56e465ca1233a2d84c2cc1cf005`  
		Last Modified: Fri, 08 May 2026 18:32:48 GMT  
		Size: 31.3 MB (31296400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c17b41ec4f852447201aeb965c3aa2bafdee78fd8912e91f0b7978c569be5e2f`  
		Last Modified: Fri, 08 May 2026 19:43:31 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d70e5c72cd4936724086c00ec89429bded5df26b92391c2566ed2fb716f18aa7`  
		Last Modified: Fri, 08 May 2026 19:43:31 GMT  
		Size: 828.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:709085b6edd21ce82957d908045c521464897a7c5aa9403a2dd9fd0f92d5140e`  
		Last Modified: Fri, 08 May 2026 19:43:31 GMT  
		Size: 6.4 MB (6442518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b14de3e13da7ff3cc57333aab9a6a05e63d3b95b75b2817946da6be54d9c921`  
		Last Modified: Fri, 08 May 2026 19:43:31 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82008a569b9479b56a58f4f85ce555a0023f34e26440b092f1cf31191ce34456`  
		Last Modified: Fri, 08 May 2026 19:43:32 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6.4` - unknown; unknown

```console
$ docker pull spiped@sha256:3408744cec174cbb267a63b72e71e41b4e396fdbf4d8b29a489532fce7271e94
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3635335 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a172af2f2faf106a865ab5dc37e0b74df8c431777dbc521aa563779b97a0365`

```dockerfile
```

-	Layers:
	-	`sha256:aedee6e6a52a08621420305a03eeabe6aaa0173b995b54b09f9326e9c235f2be`  
		Last Modified: Fri, 08 May 2026 19:43:31 GMT  
		Size: 3.6 MB (3620389 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b58a647b7d7db8950d4a473142cb3d7427b419850101f376d98d507d3a374200`  
		Last Modified: Fri, 08 May 2026 19:43:30 GMT  
		Size: 14.9 KB (14946 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6.4` - linux; ppc64le

```console
$ docker pull spiped@sha256:2e4bd458122e32e6d0dabd95f38757741b801a99e93c50b9e645fa87eb51102a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.4 MB (40441188 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa385580deb2b8dcbc058025f53221c9c9a13ba6d0e1d1fcea983d0d8004f717`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 22:25:38 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Fri, 08 May 2026 22:25:44 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 22:26:31 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Fri, 08 May 2026 22:26:31 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Fri, 08 May 2026 22:26:31 GMT
VOLUME [/spiped]
# Fri, 08 May 2026 22:26:31 GMT
WORKDIR /spiped
# Fri, 08 May 2026 22:26:31 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Fri, 08 May 2026 22:26:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 08 May 2026 22:26:31 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:b9baa45d89920bd180d7551ccc5bc535e0c5f55b863ddebddfdc06f9436dfe91`  
		Last Modified: Fri, 08 May 2026 19:46:53 GMT  
		Size: 33.6 MB (33598087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:680ca9add7a30a7a7a02b373e65419c55c156f59ab37259115ead4b9683e755f`  
		Last Modified: Fri, 08 May 2026 22:26:46 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6fbd88296e83b0fe34af0d7aea8feb0ab152c24009771728138ab8ea6a3c7e3`  
		Last Modified: Fri, 08 May 2026 22:26:46 GMT  
		Size: 829.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:427b4091434bcad2400a705856ffbc391e8edb99ddd0244020ab8e87b8fb0029`  
		Last Modified: Fri, 08 May 2026 22:26:46 GMT  
		Size: 6.8 MB (6840726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5761c60db3e29874e7a761fb091b3a0716e00845ff60b44aed197905641f8201`  
		Last Modified: Fri, 08 May 2026 22:26:46 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d979fa4083e9e6936395a7aa0bbee2b7b6a8cc7f4e41e6234afe21c2ef4653e`  
		Last Modified: Fri, 08 May 2026 22:26:47 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6.4` - unknown; unknown

```console
$ docker pull spiped@sha256:05648be86c583500baf9a23fc752f751b17a45b3a93ce072b80d2c560c492e45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3637027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:527ae0828e720ab8c7f87f091c2295b3dcd1df2f39af33c2ebf4a290bf2b6a83`

```dockerfile
```

-	Layers:
	-	`sha256:5d43283d3f5718ce69f0dd46023d5abd6439b1b618e1f306799c06fe849aea01`  
		Last Modified: Fri, 08 May 2026 22:26:46 GMT  
		Size: 3.6 MB (3621997 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:917814349a2d8dd15ccd6b0a739bb88131cfd61f1a5b110c16b85cb164e6d7bb`  
		Last Modified: Fri, 08 May 2026 22:26:46 GMT  
		Size: 15.0 KB (15030 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6.4` - linux; riscv64

```console
$ docker pull spiped@sha256:4b71cf53987a9707a16131c1318e249b3fd3d6ce9a82cb42cc7f49e072e18fd7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.6 MB (37638423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f26a4b86552c1e9439f4f551a02d1d47a8a09b1564576e2077689ea60ed92ca7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1776729600'
# Thu, 23 Apr 2026 16:08:31 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Thu, 23 Apr 2026 16:09:01 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 23 Apr 2026 16:12:07 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Thu, 23 Apr 2026 16:12:07 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Thu, 23 Apr 2026 16:12:07 GMT
VOLUME [/spiped]
# Thu, 23 Apr 2026 16:12:07 GMT
WORKDIR /spiped
# Thu, 23 Apr 2026 16:12:08 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Thu, 23 Apr 2026 16:12:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 Apr 2026 16:12:08 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:c59e3a1f334be9f0528643dd07d69319f75f877f83be33ec1eff872a489985a0`  
		Last Modified: Wed, 22 Apr 2026 02:30:51 GMT  
		Size: 28.3 MB (28280195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65c3fe48b86e812e3913e5d13d1a9629869d202426b9c61e1715fa21c49eefb0`  
		Last Modified: Thu, 23 Apr 2026 16:13:20 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b34a84840c5fe62bd145180a478a04eb839e8ebc46151483b24496cb9f4a91f`  
		Last Modified: Thu, 23 Apr 2026 16:13:20 GMT  
		Size: 819.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d24129e4ff9e3418ef7a713edd9546c25c9b66ed26f8d5aa09e53f0c443a147`  
		Last Modified: Thu, 23 Apr 2026 16:13:23 GMT  
		Size: 9.4 MB (9355868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c9de411851378c843f1fa5367128062cec83a39214793d042c62249d045708d`  
		Last Modified: Thu, 23 Apr 2026 16:13:20 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e45064277bc4d512497c03c09b867eecba1e9f36520600b1b7cf50ccf931c314`  
		Last Modified: Thu, 23 Apr 2026 16:13:22 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6.4` - unknown; unknown

```console
$ docker pull spiped@sha256:8f1fdb09a20e86779bcd22247e4e7dc45779eadf380ed22541529e1f7c49f080
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3628433 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30611531e32494ce7228fad7644d17d3b521a5eb65e2cab640541ec507a3ccff`

```dockerfile
```

-	Layers:
	-	`sha256:28e7945cedc25231eedc0925db8b02ae1dfc5c3c41f66ebd1d3a8ef39e217551`  
		Last Modified: Thu, 23 Apr 2026 16:13:22 GMT  
		Size: 3.6 MB (3613403 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0b3f06dd63e825c9c98e9b4bfdc4f7087ec431640aee8976c15796ae26a216eb`  
		Last Modified: Thu, 23 Apr 2026 16:13:20 GMT  
		Size: 15.0 KB (15030 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6.4` - linux; s390x

```console
$ docker pull spiped@sha256:bd86a35901c83fdbe0b1dd9ab57c28d30a6565052dbe1ae0ef315fc89adffc00
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.0 MB (35964636 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90e9eead17c9f5aa0363836fa2a870f271ca50be7e2f1899fb3e7e0c17e6add5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 20:52:18 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Fri, 08 May 2026 20:52:21 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 20:52:41 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Fri, 08 May 2026 20:52:41 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Fri, 08 May 2026 20:52:41 GMT
VOLUME [/spiped]
# Fri, 08 May 2026 20:52:41 GMT
WORKDIR /spiped
# Fri, 08 May 2026 20:52:41 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Fri, 08 May 2026 20:52:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 08 May 2026 20:52:41 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:2fbbc68c452b3ba3a496488f38159dac53afe693311bee1c04f555d854ff4a2e`  
		Last Modified: Fri, 08 May 2026 18:29:20 GMT  
		Size: 29.8 MB (29840347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:379c83725970f21bcd83cf3380670f0ea271dd1fc30bc3e9568c083f2580ba55`  
		Last Modified: Fri, 08 May 2026 20:52:53 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3b3284a3de5bccf5d6b269c2b7bf9b319d15f9bebd9af7f1c95123337f82ffc`  
		Last Modified: Fri, 08 May 2026 20:52:53 GMT  
		Size: 829.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78ee74470711143892631998b06f797b17b8f24c199e31160dbad3fa3f9f4b1b`  
		Last Modified: Fri, 08 May 2026 20:52:53 GMT  
		Size: 6.1 MB (6121916 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5efe750c150333b99cd25f27597baa8d209228b9898aac1c0a7355a41ab17040`  
		Last Modified: Fri, 08 May 2026 20:52:53 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31b3234d867e10e2e459de5bd4cf9e1156a19cf24d495f2dfc7415071ae5715f`  
		Last Modified: Fri, 08 May 2026 20:52:54 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6.4` - unknown; unknown

```console
$ docker pull spiped@sha256:7c6bfdf45b3649d1b3f9001e65846a9f9c95d3e42d468a4d78f4b4419a680bf5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3633605 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5894b164eadfcc36f173a9f50f9038140f4fd57fd4528d5251f9f417819c1e0c`

```dockerfile
```

-	Layers:
	-	`sha256:117c16ab57c2ffc82accce55a8dd174232910aa2a2d2f4121a9924747a140c28`  
		Last Modified: Fri, 08 May 2026 20:52:53 GMT  
		Size: 3.6 MB (3618623 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b7501e35b7a1f23c01cc4fa7d7fe477f7d1e791f6af13d52b1b0b27d654c13a4`  
		Last Modified: Fri, 08 May 2026 20:52:53 GMT  
		Size: 15.0 KB (14982 bytes)  
		MIME: application/vnd.in-toto+json

## `spiped:1.6.4-alpine`

```console
$ docker pull spiped@sha256:10785aa58079387363e472d7e20eb96bd01f12b9850476a066e124d57be1a8cc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 16
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `spiped:1.6.4-alpine` - linux; amd64

```console
$ docker pull spiped@sha256:6a78a135961dde77e0a3e9171928717694804d7cfb3d6aedbebfadb42bf4f3e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3925151 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06f599634d068048f3fcd01d27356e8cc57fb8937f8bbf03cfccaebddd3b1e24`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:02 GMT
ADD alpine-minirootfs-3.22.4-x86_64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:02 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 00:14:35 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Fri, 17 Apr 2026 00:14:36 GMT
RUN apk add --no-cache libssl3 # buildkit
# Fri, 17 Apr 2026 00:14:45 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Fri, 17 Apr 2026 00:14:45 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Fri, 17 Apr 2026 00:14:45 GMT
VOLUME [/spiped]
# Fri, 17 Apr 2026 00:14:45 GMT
WORKDIR /spiped
# Fri, 17 Apr 2026 00:14:45 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Fri, 17 Apr 2026 00:14:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 17 Apr 2026 00:14:45 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:84f5eff04246b56d48d1ed6cbd82d6bc7e53f7e790db6a467f92571c69f3289e`  
		Last Modified: Thu, 16 Apr 2026 23:53:07 GMT  
		Size: 3.8 MB (3808189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09629d4032ef7ab1ef9db974170b9cf0e98f6c5d68cb9f3d0e21a37889d50030`  
		Last Modified: Fri, 17 Apr 2026 00:14:50 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cad68e6c6d9b805cb5d27e526a335f55ae1e22e51fb78ed5cd842984966ec752`  
		Last Modified: Fri, 17 Apr 2026 00:14:50 GMT  
		Size: 7.9 KB (7942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0097cdb4e276728ffaa69c00b45edf54d761118176e68ef12d68092b7417f986`  
		Last Modified: Fri, 17 Apr 2026 00:14:50 GMT  
		Size: 107.6 KB (107638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9bc806c3d4f80593516df4d73efec6cd1cf16dfd200d5fd6adda41910072975`  
		Last Modified: Fri, 17 Apr 2026 00:14:50 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d250500ebc740f642b6509ef0a3f0576fe4b93cb687a514ceede64292cd717f`  
		Last Modified: Fri, 17 Apr 2026 00:14:51 GMT  
		Size: 336.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6.4-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:dcf1f88cd35b0648a36b53371be8057efc788150c247273946f22f226c8922f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.5 KB (96450 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b695771cd59164f79af4e3d51a194af63f71274fa2ca45642700481f66706680`

```dockerfile
```

-	Layers:
	-	`sha256:9047c6064b6fcd9efa90aa0c959722cd5d0677dd3e15d576484c71664c66a025`  
		Last Modified: Fri, 17 Apr 2026 00:14:50 GMT  
		Size: 82.2 KB (82192 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b1ebf9604f23105cb6660c6767d301a937a4b9d6d85433f32e35ffb2ba1e86d8`  
		Last Modified: Fri, 17 Apr 2026 00:14:50 GMT  
		Size: 14.3 KB (14258 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6.4-alpine` - linux; arm variant v6

```console
$ docker pull spiped@sha256:e61a3952e5718375c379136684659c21136328808a6c3f88e9585943251e9a16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3605859 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c576e8f7269c2ef4826f92b4a22494225a6cd470d17d9f30f01d9cc229e696f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:27 GMT
ADD alpine-minirootfs-3.22.4-armhf.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:27 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 00:28:09 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Fri, 17 Apr 2026 00:28:10 GMT
RUN apk add --no-cache libssl3 # buildkit
# Fri, 17 Apr 2026 00:28:20 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Fri, 17 Apr 2026 00:28:20 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Fri, 17 Apr 2026 00:28:20 GMT
VOLUME [/spiped]
# Fri, 17 Apr 2026 00:28:20 GMT
WORKDIR /spiped
# Fri, 17 Apr 2026 00:28:20 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Fri, 17 Apr 2026 00:28:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 17 Apr 2026 00:28:20 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:08c654e9a4409dbbeb5faba9659360f33dbc6f7a6d79ebebe08f57d22a1b76fc`  
		Last Modified: Thu, 16 Apr 2026 23:53:31 GMT  
		Size: 3.5 MB (3507383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a28595f303e8390d8534900bd78b38647a907732d3d3e842c7b3a9caf747dfa`  
		Last Modified: Fri, 17 Apr 2026 00:28:24 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04a2d882259c543692d98198b2c8f098f64b95d9b8018fbe3daf4bce16ccdea8`  
		Last Modified: Fri, 17 Apr 2026 00:28:24 GMT  
		Size: 7.9 KB (7941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:750bf6b03a38c9f5493952dd7c83dba844fa70e86926b54303c228f996e864fb`  
		Last Modified: Fri, 17 Apr 2026 00:28:24 GMT  
		Size: 89.2 KB (89153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bb0b56fb727ea9f7a3dad23a396c81b60139284396a263e6658329c844b5dad`  
		Last Modified: Fri, 17 Apr 2026 00:28:23 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20e6b266845306bbbcbee6801a12889b7c152b510808934deb45a090cedc3a06`  
		Last Modified: Fri, 17 Apr 2026 00:28:25 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6.4-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:e8ab0469cf1a0658dd7f777f120002189b116eedc60e2d13004809373539fd11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.1 KB (14144 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cfbd38bcf39cf976d74f4ea0d61a864e9b890815035438f477a99caff10eae99`

```dockerfile
```

-	Layers:
	-	`sha256:acf29d68d1e7fa30dc5742c4211ffe81430df68660be1f3d0207d5a94d98bc39`  
		Last Modified: Fri, 17 Apr 2026 00:28:23 GMT  
		Size: 14.1 KB (14144 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6.4-alpine` - linux; arm variant v7

```console
$ docker pull spiped@sha256:147fe0124aa237fa168a69becb6a2db57f4a9ad7144beb44a52a7735a75ed88f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3316848 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1fac8ff5e55f7bb423942ebc9a0dcfe62ab45560df8acbf81f20fce40adfb0d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 16 Apr 2026 23:54:02 GMT
ADD alpine-minirootfs-3.22.4-armv7.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:54:02 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 00:13:44 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Fri, 17 Apr 2026 00:13:45 GMT
RUN apk add --no-cache libssl3 # buildkit
# Fri, 17 Apr 2026 00:13:54 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Fri, 17 Apr 2026 00:13:54 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Fri, 17 Apr 2026 00:13:54 GMT
VOLUME [/spiped]
# Fri, 17 Apr 2026 00:13:54 GMT
WORKDIR /spiped
# Fri, 17 Apr 2026 00:13:54 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Fri, 17 Apr 2026 00:13:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 17 Apr 2026 00:13:54 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:99e8c7f1cf08d3156a369084c1a1fd745878aa29f4a0f55d73e953b93f0b7a93`  
		Last Modified: Thu, 16 Apr 2026 23:54:07 GMT  
		Size: 3.2 MB (3225830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e48112adbff0844ea29be59655ce36bdc68db268960b43349a213160861be5b`  
		Last Modified: Fri, 17 Apr 2026 00:13:59 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62b71c7a3ae36749950f95514df7064116e47fac5d0e8f2b2a7465a08ec730b1`  
		Last Modified: Fri, 17 Apr 2026 00:13:59 GMT  
		Size: 7.9 KB (7949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90dbc42fa35611c27c8478a77677c7599958f859178a2ae432cdeea23ff283fe`  
		Last Modified: Fri, 17 Apr 2026 00:13:59 GMT  
		Size: 81.7 KB (81682 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d17f9759dca0bc64327214acbd9fd3deb78375c7afd7010e30d54ffe9eafdb6`  
		Last Modified: Fri, 17 Apr 2026 00:13:59 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87eff9de0017984f4c4aceb50f22ba5600d01062af116b4a3d8666f104982e79`  
		Last Modified: Fri, 17 Apr 2026 00:14:00 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6.4-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:87b16d20b49f4fd531d2a7882ebf70ab433c78455a68ecb63229df2b111b80e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.6 KB (96590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4db1828da7718e04747ebb0f602b5974b0a7a0da76481d2a933ecbb6b1869fd9`

```dockerfile
```

-	Layers:
	-	`sha256:32fd82b374cd8966ecaddf73d35913d341f1bf089acec4758b0eddc9ae15bf6c`  
		Last Modified: Fri, 17 Apr 2026 00:13:59 GMT  
		Size: 82.2 KB (82228 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:451cb443bac28fadec04af355b08de89c30845228bcead9735b3be6a627381f6`  
		Last Modified: Fri, 17 Apr 2026 00:13:59 GMT  
		Size: 14.4 KB (14362 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6.4-alpine` - linux; arm64 variant v8

```console
$ docker pull spiped@sha256:1fd688a89197aa9ec5aa2ecf456f856d56b46639e5d0733ee167c8e1f1f67c29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4251815 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3e3a3494482e2c117fe69680a253048739b96db6b666e0ba693d69f12f3cffa`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:00 GMT
ADD alpine-minirootfs-3.22.4-aarch64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:00 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 00:23:30 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Fri, 17 Apr 2026 00:23:30 GMT
RUN apk add --no-cache libssl3 # buildkit
# Fri, 17 Apr 2026 00:23:40 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Fri, 17 Apr 2026 00:23:40 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Fri, 17 Apr 2026 00:23:40 GMT
VOLUME [/spiped]
# Fri, 17 Apr 2026 00:23:40 GMT
WORKDIR /spiped
# Fri, 17 Apr 2026 00:23:40 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Fri, 17 Apr 2026 00:23:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 17 Apr 2026 00:23:40 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:58e777220c395c319866c5d73ea32a5ea574bbd12f4eb289b392f584d0cd953e`  
		Last Modified: Thu, 16 Apr 2026 23:53:05 GMT  
		Size: 4.1 MB (4141894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3b70cf46309ade34c5a66991fc83a20e95c2a2ca7662393d07532b98169b897`  
		Last Modified: Fri, 17 Apr 2026 00:23:45 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4aa5fdf2c2bb57fb12d420f1ebc379b73a6a07a076dd649edbdfb2ec65e9b52f`  
		Last Modified: Fri, 17 Apr 2026 00:23:45 GMT  
		Size: 7.9 KB (7939 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62bde94e8b5d108bfaf26624adc0087452e38a2a8176cc98ece876fe2117fc72`  
		Last Modified: Fri, 17 Apr 2026 00:23:45 GMT  
		Size: 100.6 KB (100601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec5b88c8155b1bdcaf3ceb67be1cd60eac4d053dbde4189b58b41e709ce71a5d`  
		Last Modified: Fri, 17 Apr 2026 00:23:45 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bb330bcfc9ca5ba0cfa2155b2866b977ad2c3ce1d9ae151d07e639bbada8ed2`  
		Last Modified: Fri, 17 Apr 2026 00:23:46 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6.4-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:fc73de67fe7f5bcda008d343140166980bf4176b3096a535d83f3dcd2d534e5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.6 KB (96641 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a18fe2b2319a581866e1c86ace119888f0e7b9a60b55a3ce6b779f28fe92710`

```dockerfile
```

-	Layers:
	-	`sha256:a96c2085f2ac76644e77254bfa9bf6d1b56c67d9d9405eaa8416f74fcba97701`  
		Last Modified: Fri, 17 Apr 2026 00:23:45 GMT  
		Size: 82.2 KB (82248 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a7d5f7f4737f85a0e24460592078844c64dafe02803bdf87581c20f597e952bb`  
		Last Modified: Fri, 17 Apr 2026 00:23:45 GMT  
		Size: 14.4 KB (14393 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6.4-alpine` - linux; 386

```console
$ docker pull spiped@sha256:60c2f83afdec0385615a7286994daa8f205766ef71d83fa8ddc2e700ac81936f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3754157 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fdc7573391c8c621e1b2f987722ca168aebbe555b0499e62e86738da10c96e58`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Fri, 17 Apr 2026 02:42:29 GMT
ADD alpine-minirootfs-3.22.4-x86.tar.gz / # buildkit
# Fri, 17 Apr 2026 02:42:29 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 05:54:58 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Fri, 17 Apr 2026 05:54:58 GMT
RUN apk add --no-cache libssl3 # buildkit
# Fri, 17 Apr 2026 05:55:09 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Fri, 17 Apr 2026 05:55:09 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Fri, 17 Apr 2026 05:55:09 GMT
VOLUME [/spiped]
# Fri, 17 Apr 2026 05:55:09 GMT
WORKDIR /spiped
# Fri, 17 Apr 2026 05:55:09 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Fri, 17 Apr 2026 05:55:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 17 Apr 2026 05:55:09 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:481dba1f7704181ddc1e2b499675e9651a93f972d4cd141a4933d44622cdc88a`  
		Last Modified: Fri, 17 Apr 2026 02:42:34 GMT  
		Size: 3.6 MB (3624721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2f934ad8efa54d7383ed1d7daf8f07d69a316c785b55e29d855f59724767ac5`  
		Last Modified: Fri, 17 Apr 2026 05:55:13 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fad6a50d64bebedb5b11ecc9dbad14debf2baa30235c5ed093775151dd20c5f`  
		Last Modified: Fri, 17 Apr 2026 05:55:13 GMT  
		Size: 7.9 KB (7947 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4e9ad205a738e9a190290cb841b91a7516b90d39ccefc8a464803a80e5d3bf2`  
		Last Modified: Fri, 17 Apr 2026 05:55:14 GMT  
		Size: 120.1 KB (120105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b13bce07410da4d5d2d2271580461ed3ae19008e5249df3c1003a06c213c180b`  
		Last Modified: Fri, 17 Apr 2026 05:55:14 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d30a682d686a1255ac7f31b311acf6f01b819da6af05a18bb59cf9285441247`  
		Last Modified: Fri, 17 Apr 2026 05:55:14 GMT  
		Size: 336.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6.4-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:499b7ec7b9c4e4eec426321c8934ac7fac003aeff1b6247ccf002c546cd6a262
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.4 KB (96390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9072722cf70bdbdd1bd5420a6744bc8ca176440a12571a40e33ce18862067a55`

```dockerfile
```

-	Layers:
	-	`sha256:dd1f08b2c21c938da19a9533a1b9dcb5f15e078dab41c9a4bd4ab244cd979858`  
		Last Modified: Fri, 17 Apr 2026 05:55:13 GMT  
		Size: 82.2 KB (82167 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:517f76f905b9dca96e65eec9ad79a6211e1b541723537e827a226d4839aa2649`  
		Last Modified: Fri, 17 Apr 2026 05:55:14 GMT  
		Size: 14.2 KB (14223 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6.4-alpine` - linux; ppc64le

```console
$ docker pull spiped@sha256:cd9ed7a248ccd86ed221ed62ccb5fccc85d88f92bb07eacf32a54aa285d3baef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3858669 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01b17425a87a9b3f6cf310b87ae46b1234772bd0b80ea164489da909a148229e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Fri, 17 Apr 2026 00:00:29 GMT
ADD alpine-minirootfs-3.22.4-ppc64le.tar.gz / # buildkit
# Fri, 17 Apr 2026 00:00:29 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 01:13:47 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Fri, 17 Apr 2026 01:13:49 GMT
RUN apk add --no-cache libssl3 # buildkit
# Fri, 17 Apr 2026 01:14:13 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Fri, 17 Apr 2026 01:14:13 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Fri, 17 Apr 2026 01:14:13 GMT
VOLUME [/spiped]
# Fri, 17 Apr 2026 01:14:15 GMT
WORKDIR /spiped
# Fri, 17 Apr 2026 01:14:15 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Fri, 17 Apr 2026 01:14:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 17 Apr 2026 01:14:15 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:9d65ab042d46bde09babe9a9587237000067c332d24fd9ca516fea7bdfb77c80`  
		Last Modified: Fri, 17 Apr 2026 00:00:38 GMT  
		Size: 3.7 MB (3736656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d4eb2b31b373fa4117e61ee4973c717af31bc2e3376684ddf64780f6a0cfbf2`  
		Last Modified: Fri, 17 Apr 2026 01:14:36 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e5bc892fe10dffc5824aa6f02e4a3fd2d8872fcc548dc32d8271fbeda871d54`  
		Last Modified: Fri, 17 Apr 2026 01:14:36 GMT  
		Size: 8.0 KB (7951 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a0f69169c64986eaf44f560100f0ace1b79586cff5d1f517fcf6f2810fcf476`  
		Last Modified: Fri, 17 Apr 2026 01:14:36 GMT  
		Size: 112.7 KB (112676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ecc1153f644e2e26a00aa90bf9b03917ab7f9ec331b32bd9bc295281cee7151`  
		Last Modified: Fri, 17 Apr 2026 01:14:36 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94785087e434424ecd2b2a79b34d04d7aa53bdc943265138216cadd6badf5495`  
		Last Modified: Fri, 17 Apr 2026 01:14:37 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6.4-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:42b060f58ef29347aa95f2a95a49a750c85e6dc1283a7429bdbd08cbb35d8c90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.6 KB (94582 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1aeddc4f5e06133647f4d77b87d5471240c741e9ac4581ee0469cd5e684bde41`

```dockerfile
```

-	Layers:
	-	`sha256:8054970ddb854b9dbe87ad8cc6cb52f8ac69bae6393895a2cc0ec179d9890648`  
		Last Modified: Fri, 17 Apr 2026 01:14:36 GMT  
		Size: 80.3 KB (80275 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5cf789792086c7df442c741fa726e1c634b400a002527085dcc36c87a5bdd724`  
		Last Modified: Fri, 17 Apr 2026 01:14:36 GMT  
		Size: 14.3 KB (14307 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6.4-alpine` - linux; riscv64

```console
$ docker pull spiped@sha256:eaf86ffaae6edde3dcb5bc958a07fa09bfe7cf9bcd05be9ace676e83efe5f761
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3629050 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:508a25834d52056b9c731fc2100ea35e54d563c093104a90eef8c05cb0cd1cf9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Fri, 17 Apr 2026 07:18:45 GMT
ADD alpine-minirootfs-3.22.4-riscv64.tar.gz / # buildkit
# Fri, 17 Apr 2026 07:18:45 GMT
CMD ["/bin/sh"]
# Sun, 19 Apr 2026 03:43:32 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Sun, 19 Apr 2026 03:43:36 GMT
RUN apk add --no-cache libssl3 # buildkit
# Sun, 19 Apr 2026 03:45:16 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Sun, 19 Apr 2026 03:45:16 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Sun, 19 Apr 2026 03:45:16 GMT
VOLUME [/spiped]
# Sun, 19 Apr 2026 03:45:16 GMT
WORKDIR /spiped
# Sun, 19 Apr 2026 03:45:17 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 19 Apr 2026 03:45:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 19 Apr 2026 03:45:17 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:fbc07c8b85a3c60e503ffd0cbe3e1b3947fd65764784e1bd9d943ac21097cce7`  
		Last Modified: Fri, 17 Apr 2026 07:19:08 GMT  
		Size: 3.5 MB (3520880 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62f6ee73726995fef9f6ea4faf4767bcea48e04bfd71f1eea0bd05f9534d43f8`  
		Last Modified: Sun, 19 Apr 2026 03:45:37 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ce2dd3bcf1d4c6316b374da1b2790b7de4b60cf8e6512e5f30f8d7b2d7a3b38`  
		Last Modified: Sun, 19 Apr 2026 03:45:37 GMT  
		Size: 7.9 KB (7940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8e66ca15c2a84ed0ad5aac95f1257383ec006115c07282942c1fd6f06bc2b26`  
		Last Modified: Sun, 19 Apr 2026 03:45:37 GMT  
		Size: 98.8 KB (98844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04a854d7ad8f0e7a7a6274e5c362b1a896bd76e462c14408778ba02dff83d37b`  
		Last Modified: Sun, 19 Apr 2026 03:45:37 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5ff5f61469b0ef7c1c8bf56662d9b762181e909bc3c749eacbaaecf7bb475ab`  
		Last Modified: Sun, 19 Apr 2026 03:45:39 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6.4-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:f21b45950838bc0c80c8410cc4f2814b68f96ecad1e19be90b06994c99afbf58
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.6 KB (94574 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1abe71f567ae68daf6e6dfeaafd74f8104d7a6958082dd986f64838b44c12b9f`

```dockerfile
```

-	Layers:
	-	`sha256:e9f4f6fe1bacdcf68608f4eb99bf2115bae97f39b1056b72d36c08b63e32ef42`  
		Last Modified: Sun, 19 Apr 2026 03:45:37 GMT  
		Size: 80.3 KB (80271 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d5e5c1e0a1d68c8bdb360c97f9072a3c973409b2f9afe7ff5795d523cae5119b`  
		Last Modified: Sun, 19 Apr 2026 03:45:38 GMT  
		Size: 14.3 KB (14303 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6.4-alpine` - linux; s390x

```console
$ docker pull spiped@sha256:d63a333156f14c550016968b48b61e03d6ffa7cdadeb4dc11994993be83c667f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3760132 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:425f883e0aba651c328e78b42abc6210940d11022f1ee5d1ff5258ebca42e51f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:56 GMT
ADD alpine-minirootfs-3.22.4-s390x.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:56 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 00:41:11 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Fri, 17 Apr 2026 00:41:12 GMT
RUN apk add --no-cache libssl3 # buildkit
# Fri, 17 Apr 2026 00:41:19 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Fri, 17 Apr 2026 00:41:19 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Fri, 17 Apr 2026 00:41:19 GMT
VOLUME [/spiped]
# Fri, 17 Apr 2026 00:41:19 GMT
WORKDIR /spiped
# Fri, 17 Apr 2026 00:41:19 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Fri, 17 Apr 2026 00:41:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 17 Apr 2026 00:41:19 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:54b429821fc7436a26fe07d9038b86e2bef4ef3bf03e43e9ae5e91ab8e4b37a9`  
		Last Modified: Thu, 16 Apr 2026 23:54:12 GMT  
		Size: 3.7 MB (3653873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98c5658f716398e67bcdf451aa62d9268badc01207fb2761dde286827e782131`  
		Last Modified: Fri, 17 Apr 2026 00:41:28 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d837fc0069a0ae8449bb0adb9f65b43fff5ff059948bf845ea728a30d3eaca0`  
		Last Modified: Fri, 17 Apr 2026 00:41:28 GMT  
		Size: 7.9 KB (7947 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:669f2f936af1acb505aa131fbad0547df0d36ff3dc9c4f8c3a396c9877b87798`  
		Last Modified: Fri, 17 Apr 2026 00:41:28 GMT  
		Size: 96.9 KB (96930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33930e4a86d8157d355b84eecf720d4f20b38ee3502ab3baa6329d6c6acac811`  
		Last Modified: Fri, 17 Apr 2026 00:41:28 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27970db5cca98e64b9bdffc3b4445e18a503e3e0dc858c6ae91eff10bccd50bd`  
		Last Modified: Fri, 17 Apr 2026 00:41:29 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6.4-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:3a63421a60ad516e8ae99df7c008ce97158220da99f3e592d9090f762eb254c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.5 KB (94497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03ae27771b3c7505fb78b0f0546a7416b11e879220de4dc6090bf643dedf8614`

```dockerfile
```

-	Layers:
	-	`sha256:c6abf9efd631a7212221f0b771ec35e734885be3d3a6755a004bba8bd46cc068`  
		Last Modified: Fri, 17 Apr 2026 00:41:28 GMT  
		Size: 80.2 KB (80241 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:033e56e9f47fa0453060710502d5ab3daddcba0cc4e51e5e138a57faf3e873d6`  
		Last Modified: Fri, 17 Apr 2026 00:41:28 GMT  
		Size: 14.3 KB (14256 bytes)  
		MIME: application/vnd.in-toto+json

## `spiped:alpine`

```console
$ docker pull spiped@sha256:10785aa58079387363e472d7e20eb96bd01f12b9850476a066e124d57be1a8cc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 16
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `spiped:alpine` - linux; amd64

```console
$ docker pull spiped@sha256:6a78a135961dde77e0a3e9171928717694804d7cfb3d6aedbebfadb42bf4f3e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3925151 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06f599634d068048f3fcd01d27356e8cc57fb8937f8bbf03cfccaebddd3b1e24`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:02 GMT
ADD alpine-minirootfs-3.22.4-x86_64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:02 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 00:14:35 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Fri, 17 Apr 2026 00:14:36 GMT
RUN apk add --no-cache libssl3 # buildkit
# Fri, 17 Apr 2026 00:14:45 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Fri, 17 Apr 2026 00:14:45 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Fri, 17 Apr 2026 00:14:45 GMT
VOLUME [/spiped]
# Fri, 17 Apr 2026 00:14:45 GMT
WORKDIR /spiped
# Fri, 17 Apr 2026 00:14:45 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Fri, 17 Apr 2026 00:14:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 17 Apr 2026 00:14:45 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:84f5eff04246b56d48d1ed6cbd82d6bc7e53f7e790db6a467f92571c69f3289e`  
		Last Modified: Thu, 16 Apr 2026 23:53:07 GMT  
		Size: 3.8 MB (3808189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09629d4032ef7ab1ef9db974170b9cf0e98f6c5d68cb9f3d0e21a37889d50030`  
		Last Modified: Fri, 17 Apr 2026 00:14:50 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cad68e6c6d9b805cb5d27e526a335f55ae1e22e51fb78ed5cd842984966ec752`  
		Last Modified: Fri, 17 Apr 2026 00:14:50 GMT  
		Size: 7.9 KB (7942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0097cdb4e276728ffaa69c00b45edf54d761118176e68ef12d68092b7417f986`  
		Last Modified: Fri, 17 Apr 2026 00:14:50 GMT  
		Size: 107.6 KB (107638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9bc806c3d4f80593516df4d73efec6cd1cf16dfd200d5fd6adda41910072975`  
		Last Modified: Fri, 17 Apr 2026 00:14:50 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d250500ebc740f642b6509ef0a3f0576fe4b93cb687a514ceede64292cd717f`  
		Last Modified: Fri, 17 Apr 2026 00:14:51 GMT  
		Size: 336.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:dcf1f88cd35b0648a36b53371be8057efc788150c247273946f22f226c8922f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.5 KB (96450 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b695771cd59164f79af4e3d51a194af63f71274fa2ca45642700481f66706680`

```dockerfile
```

-	Layers:
	-	`sha256:9047c6064b6fcd9efa90aa0c959722cd5d0677dd3e15d576484c71664c66a025`  
		Last Modified: Fri, 17 Apr 2026 00:14:50 GMT  
		Size: 82.2 KB (82192 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b1ebf9604f23105cb6660c6767d301a937a4b9d6d85433f32e35ffb2ba1e86d8`  
		Last Modified: Fri, 17 Apr 2026 00:14:50 GMT  
		Size: 14.3 KB (14258 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:alpine` - linux; arm variant v6

```console
$ docker pull spiped@sha256:e61a3952e5718375c379136684659c21136328808a6c3f88e9585943251e9a16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3605859 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c576e8f7269c2ef4826f92b4a22494225a6cd470d17d9f30f01d9cc229e696f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:27 GMT
ADD alpine-minirootfs-3.22.4-armhf.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:27 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 00:28:09 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Fri, 17 Apr 2026 00:28:10 GMT
RUN apk add --no-cache libssl3 # buildkit
# Fri, 17 Apr 2026 00:28:20 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Fri, 17 Apr 2026 00:28:20 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Fri, 17 Apr 2026 00:28:20 GMT
VOLUME [/spiped]
# Fri, 17 Apr 2026 00:28:20 GMT
WORKDIR /spiped
# Fri, 17 Apr 2026 00:28:20 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Fri, 17 Apr 2026 00:28:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 17 Apr 2026 00:28:20 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:08c654e9a4409dbbeb5faba9659360f33dbc6f7a6d79ebebe08f57d22a1b76fc`  
		Last Modified: Thu, 16 Apr 2026 23:53:31 GMT  
		Size: 3.5 MB (3507383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a28595f303e8390d8534900bd78b38647a907732d3d3e842c7b3a9caf747dfa`  
		Last Modified: Fri, 17 Apr 2026 00:28:24 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04a2d882259c543692d98198b2c8f098f64b95d9b8018fbe3daf4bce16ccdea8`  
		Last Modified: Fri, 17 Apr 2026 00:28:24 GMT  
		Size: 7.9 KB (7941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:750bf6b03a38c9f5493952dd7c83dba844fa70e86926b54303c228f996e864fb`  
		Last Modified: Fri, 17 Apr 2026 00:28:24 GMT  
		Size: 89.2 KB (89153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bb0b56fb727ea9f7a3dad23a396c81b60139284396a263e6658329c844b5dad`  
		Last Modified: Fri, 17 Apr 2026 00:28:23 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20e6b266845306bbbcbee6801a12889b7c152b510808934deb45a090cedc3a06`  
		Last Modified: Fri, 17 Apr 2026 00:28:25 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:e8ab0469cf1a0658dd7f777f120002189b116eedc60e2d13004809373539fd11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.1 KB (14144 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cfbd38bcf39cf976d74f4ea0d61a864e9b890815035438f477a99caff10eae99`

```dockerfile
```

-	Layers:
	-	`sha256:acf29d68d1e7fa30dc5742c4211ffe81430df68660be1f3d0207d5a94d98bc39`  
		Last Modified: Fri, 17 Apr 2026 00:28:23 GMT  
		Size: 14.1 KB (14144 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:alpine` - linux; arm variant v7

```console
$ docker pull spiped@sha256:147fe0124aa237fa168a69becb6a2db57f4a9ad7144beb44a52a7735a75ed88f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3316848 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1fac8ff5e55f7bb423942ebc9a0dcfe62ab45560df8acbf81f20fce40adfb0d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 16 Apr 2026 23:54:02 GMT
ADD alpine-minirootfs-3.22.4-armv7.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:54:02 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 00:13:44 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Fri, 17 Apr 2026 00:13:45 GMT
RUN apk add --no-cache libssl3 # buildkit
# Fri, 17 Apr 2026 00:13:54 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Fri, 17 Apr 2026 00:13:54 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Fri, 17 Apr 2026 00:13:54 GMT
VOLUME [/spiped]
# Fri, 17 Apr 2026 00:13:54 GMT
WORKDIR /spiped
# Fri, 17 Apr 2026 00:13:54 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Fri, 17 Apr 2026 00:13:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 17 Apr 2026 00:13:54 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:99e8c7f1cf08d3156a369084c1a1fd745878aa29f4a0f55d73e953b93f0b7a93`  
		Last Modified: Thu, 16 Apr 2026 23:54:07 GMT  
		Size: 3.2 MB (3225830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e48112adbff0844ea29be59655ce36bdc68db268960b43349a213160861be5b`  
		Last Modified: Fri, 17 Apr 2026 00:13:59 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62b71c7a3ae36749950f95514df7064116e47fac5d0e8f2b2a7465a08ec730b1`  
		Last Modified: Fri, 17 Apr 2026 00:13:59 GMT  
		Size: 7.9 KB (7949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90dbc42fa35611c27c8478a77677c7599958f859178a2ae432cdeea23ff283fe`  
		Last Modified: Fri, 17 Apr 2026 00:13:59 GMT  
		Size: 81.7 KB (81682 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d17f9759dca0bc64327214acbd9fd3deb78375c7afd7010e30d54ffe9eafdb6`  
		Last Modified: Fri, 17 Apr 2026 00:13:59 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87eff9de0017984f4c4aceb50f22ba5600d01062af116b4a3d8666f104982e79`  
		Last Modified: Fri, 17 Apr 2026 00:14:00 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:87b16d20b49f4fd531d2a7882ebf70ab433c78455a68ecb63229df2b111b80e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.6 KB (96590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4db1828da7718e04747ebb0f602b5974b0a7a0da76481d2a933ecbb6b1869fd9`

```dockerfile
```

-	Layers:
	-	`sha256:32fd82b374cd8966ecaddf73d35913d341f1bf089acec4758b0eddc9ae15bf6c`  
		Last Modified: Fri, 17 Apr 2026 00:13:59 GMT  
		Size: 82.2 KB (82228 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:451cb443bac28fadec04af355b08de89c30845228bcead9735b3be6a627381f6`  
		Last Modified: Fri, 17 Apr 2026 00:13:59 GMT  
		Size: 14.4 KB (14362 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:alpine` - linux; arm64 variant v8

```console
$ docker pull spiped@sha256:1fd688a89197aa9ec5aa2ecf456f856d56b46639e5d0733ee167c8e1f1f67c29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4251815 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3e3a3494482e2c117fe69680a253048739b96db6b666e0ba693d69f12f3cffa`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:00 GMT
ADD alpine-minirootfs-3.22.4-aarch64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:00 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 00:23:30 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Fri, 17 Apr 2026 00:23:30 GMT
RUN apk add --no-cache libssl3 # buildkit
# Fri, 17 Apr 2026 00:23:40 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Fri, 17 Apr 2026 00:23:40 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Fri, 17 Apr 2026 00:23:40 GMT
VOLUME [/spiped]
# Fri, 17 Apr 2026 00:23:40 GMT
WORKDIR /spiped
# Fri, 17 Apr 2026 00:23:40 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Fri, 17 Apr 2026 00:23:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 17 Apr 2026 00:23:40 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:58e777220c395c319866c5d73ea32a5ea574bbd12f4eb289b392f584d0cd953e`  
		Last Modified: Thu, 16 Apr 2026 23:53:05 GMT  
		Size: 4.1 MB (4141894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3b70cf46309ade34c5a66991fc83a20e95c2a2ca7662393d07532b98169b897`  
		Last Modified: Fri, 17 Apr 2026 00:23:45 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4aa5fdf2c2bb57fb12d420f1ebc379b73a6a07a076dd649edbdfb2ec65e9b52f`  
		Last Modified: Fri, 17 Apr 2026 00:23:45 GMT  
		Size: 7.9 KB (7939 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62bde94e8b5d108bfaf26624adc0087452e38a2a8176cc98ece876fe2117fc72`  
		Last Modified: Fri, 17 Apr 2026 00:23:45 GMT  
		Size: 100.6 KB (100601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec5b88c8155b1bdcaf3ceb67be1cd60eac4d053dbde4189b58b41e709ce71a5d`  
		Last Modified: Fri, 17 Apr 2026 00:23:45 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bb330bcfc9ca5ba0cfa2155b2866b977ad2c3ce1d9ae151d07e639bbada8ed2`  
		Last Modified: Fri, 17 Apr 2026 00:23:46 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:fc73de67fe7f5bcda008d343140166980bf4176b3096a535d83f3dcd2d534e5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.6 KB (96641 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a18fe2b2319a581866e1c86ace119888f0e7b9a60b55a3ce6b779f28fe92710`

```dockerfile
```

-	Layers:
	-	`sha256:a96c2085f2ac76644e77254bfa9bf6d1b56c67d9d9405eaa8416f74fcba97701`  
		Last Modified: Fri, 17 Apr 2026 00:23:45 GMT  
		Size: 82.2 KB (82248 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a7d5f7f4737f85a0e24460592078844c64dafe02803bdf87581c20f597e952bb`  
		Last Modified: Fri, 17 Apr 2026 00:23:45 GMT  
		Size: 14.4 KB (14393 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:alpine` - linux; 386

```console
$ docker pull spiped@sha256:60c2f83afdec0385615a7286994daa8f205766ef71d83fa8ddc2e700ac81936f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3754157 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fdc7573391c8c621e1b2f987722ca168aebbe555b0499e62e86738da10c96e58`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Fri, 17 Apr 2026 02:42:29 GMT
ADD alpine-minirootfs-3.22.4-x86.tar.gz / # buildkit
# Fri, 17 Apr 2026 02:42:29 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 05:54:58 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Fri, 17 Apr 2026 05:54:58 GMT
RUN apk add --no-cache libssl3 # buildkit
# Fri, 17 Apr 2026 05:55:09 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Fri, 17 Apr 2026 05:55:09 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Fri, 17 Apr 2026 05:55:09 GMT
VOLUME [/spiped]
# Fri, 17 Apr 2026 05:55:09 GMT
WORKDIR /spiped
# Fri, 17 Apr 2026 05:55:09 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Fri, 17 Apr 2026 05:55:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 17 Apr 2026 05:55:09 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:481dba1f7704181ddc1e2b499675e9651a93f972d4cd141a4933d44622cdc88a`  
		Last Modified: Fri, 17 Apr 2026 02:42:34 GMT  
		Size: 3.6 MB (3624721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2f934ad8efa54d7383ed1d7daf8f07d69a316c785b55e29d855f59724767ac5`  
		Last Modified: Fri, 17 Apr 2026 05:55:13 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fad6a50d64bebedb5b11ecc9dbad14debf2baa30235c5ed093775151dd20c5f`  
		Last Modified: Fri, 17 Apr 2026 05:55:13 GMT  
		Size: 7.9 KB (7947 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4e9ad205a738e9a190290cb841b91a7516b90d39ccefc8a464803a80e5d3bf2`  
		Last Modified: Fri, 17 Apr 2026 05:55:14 GMT  
		Size: 120.1 KB (120105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b13bce07410da4d5d2d2271580461ed3ae19008e5249df3c1003a06c213c180b`  
		Last Modified: Fri, 17 Apr 2026 05:55:14 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d30a682d686a1255ac7f31b311acf6f01b819da6af05a18bb59cf9285441247`  
		Last Modified: Fri, 17 Apr 2026 05:55:14 GMT  
		Size: 336.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:499b7ec7b9c4e4eec426321c8934ac7fac003aeff1b6247ccf002c546cd6a262
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.4 KB (96390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9072722cf70bdbdd1bd5420a6744bc8ca176440a12571a40e33ce18862067a55`

```dockerfile
```

-	Layers:
	-	`sha256:dd1f08b2c21c938da19a9533a1b9dcb5f15e078dab41c9a4bd4ab244cd979858`  
		Last Modified: Fri, 17 Apr 2026 05:55:13 GMT  
		Size: 82.2 KB (82167 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:517f76f905b9dca96e65eec9ad79a6211e1b541723537e827a226d4839aa2649`  
		Last Modified: Fri, 17 Apr 2026 05:55:14 GMT  
		Size: 14.2 KB (14223 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:alpine` - linux; ppc64le

```console
$ docker pull spiped@sha256:cd9ed7a248ccd86ed221ed62ccb5fccc85d88f92bb07eacf32a54aa285d3baef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3858669 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01b17425a87a9b3f6cf310b87ae46b1234772bd0b80ea164489da909a148229e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Fri, 17 Apr 2026 00:00:29 GMT
ADD alpine-minirootfs-3.22.4-ppc64le.tar.gz / # buildkit
# Fri, 17 Apr 2026 00:00:29 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 01:13:47 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Fri, 17 Apr 2026 01:13:49 GMT
RUN apk add --no-cache libssl3 # buildkit
# Fri, 17 Apr 2026 01:14:13 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Fri, 17 Apr 2026 01:14:13 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Fri, 17 Apr 2026 01:14:13 GMT
VOLUME [/spiped]
# Fri, 17 Apr 2026 01:14:15 GMT
WORKDIR /spiped
# Fri, 17 Apr 2026 01:14:15 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Fri, 17 Apr 2026 01:14:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 17 Apr 2026 01:14:15 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:9d65ab042d46bde09babe9a9587237000067c332d24fd9ca516fea7bdfb77c80`  
		Last Modified: Fri, 17 Apr 2026 00:00:38 GMT  
		Size: 3.7 MB (3736656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d4eb2b31b373fa4117e61ee4973c717af31bc2e3376684ddf64780f6a0cfbf2`  
		Last Modified: Fri, 17 Apr 2026 01:14:36 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e5bc892fe10dffc5824aa6f02e4a3fd2d8872fcc548dc32d8271fbeda871d54`  
		Last Modified: Fri, 17 Apr 2026 01:14:36 GMT  
		Size: 8.0 KB (7951 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a0f69169c64986eaf44f560100f0ace1b79586cff5d1f517fcf6f2810fcf476`  
		Last Modified: Fri, 17 Apr 2026 01:14:36 GMT  
		Size: 112.7 KB (112676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ecc1153f644e2e26a00aa90bf9b03917ab7f9ec331b32bd9bc295281cee7151`  
		Last Modified: Fri, 17 Apr 2026 01:14:36 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94785087e434424ecd2b2a79b34d04d7aa53bdc943265138216cadd6badf5495`  
		Last Modified: Fri, 17 Apr 2026 01:14:37 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:42b060f58ef29347aa95f2a95a49a750c85e6dc1283a7429bdbd08cbb35d8c90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.6 KB (94582 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1aeddc4f5e06133647f4d77b87d5471240c741e9ac4581ee0469cd5e684bde41`

```dockerfile
```

-	Layers:
	-	`sha256:8054970ddb854b9dbe87ad8cc6cb52f8ac69bae6393895a2cc0ec179d9890648`  
		Last Modified: Fri, 17 Apr 2026 01:14:36 GMT  
		Size: 80.3 KB (80275 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5cf789792086c7df442c741fa726e1c634b400a002527085dcc36c87a5bdd724`  
		Last Modified: Fri, 17 Apr 2026 01:14:36 GMT  
		Size: 14.3 KB (14307 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:alpine` - linux; riscv64

```console
$ docker pull spiped@sha256:eaf86ffaae6edde3dcb5bc958a07fa09bfe7cf9bcd05be9ace676e83efe5f761
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3629050 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:508a25834d52056b9c731fc2100ea35e54d563c093104a90eef8c05cb0cd1cf9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Fri, 17 Apr 2026 07:18:45 GMT
ADD alpine-minirootfs-3.22.4-riscv64.tar.gz / # buildkit
# Fri, 17 Apr 2026 07:18:45 GMT
CMD ["/bin/sh"]
# Sun, 19 Apr 2026 03:43:32 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Sun, 19 Apr 2026 03:43:36 GMT
RUN apk add --no-cache libssl3 # buildkit
# Sun, 19 Apr 2026 03:45:16 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Sun, 19 Apr 2026 03:45:16 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Sun, 19 Apr 2026 03:45:16 GMT
VOLUME [/spiped]
# Sun, 19 Apr 2026 03:45:16 GMT
WORKDIR /spiped
# Sun, 19 Apr 2026 03:45:17 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 19 Apr 2026 03:45:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 19 Apr 2026 03:45:17 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:fbc07c8b85a3c60e503ffd0cbe3e1b3947fd65764784e1bd9d943ac21097cce7`  
		Last Modified: Fri, 17 Apr 2026 07:19:08 GMT  
		Size: 3.5 MB (3520880 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62f6ee73726995fef9f6ea4faf4767bcea48e04bfd71f1eea0bd05f9534d43f8`  
		Last Modified: Sun, 19 Apr 2026 03:45:37 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ce2dd3bcf1d4c6316b374da1b2790b7de4b60cf8e6512e5f30f8d7b2d7a3b38`  
		Last Modified: Sun, 19 Apr 2026 03:45:37 GMT  
		Size: 7.9 KB (7940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8e66ca15c2a84ed0ad5aac95f1257383ec006115c07282942c1fd6f06bc2b26`  
		Last Modified: Sun, 19 Apr 2026 03:45:37 GMT  
		Size: 98.8 KB (98844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04a854d7ad8f0e7a7a6274e5c362b1a896bd76e462c14408778ba02dff83d37b`  
		Last Modified: Sun, 19 Apr 2026 03:45:37 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5ff5f61469b0ef7c1c8bf56662d9b762181e909bc3c749eacbaaecf7bb475ab`  
		Last Modified: Sun, 19 Apr 2026 03:45:39 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:f21b45950838bc0c80c8410cc4f2814b68f96ecad1e19be90b06994c99afbf58
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.6 KB (94574 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1abe71f567ae68daf6e6dfeaafd74f8104d7a6958082dd986f64838b44c12b9f`

```dockerfile
```

-	Layers:
	-	`sha256:e9f4f6fe1bacdcf68608f4eb99bf2115bae97f39b1056b72d36c08b63e32ef42`  
		Last Modified: Sun, 19 Apr 2026 03:45:37 GMT  
		Size: 80.3 KB (80271 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d5e5c1e0a1d68c8bdb360c97f9072a3c973409b2f9afe7ff5795d523cae5119b`  
		Last Modified: Sun, 19 Apr 2026 03:45:38 GMT  
		Size: 14.3 KB (14303 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:alpine` - linux; s390x

```console
$ docker pull spiped@sha256:d63a333156f14c550016968b48b61e03d6ffa7cdadeb4dc11994993be83c667f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3760132 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:425f883e0aba651c328e78b42abc6210940d11022f1ee5d1ff5258ebca42e51f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:56 GMT
ADD alpine-minirootfs-3.22.4-s390x.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:56 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 00:41:11 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Fri, 17 Apr 2026 00:41:12 GMT
RUN apk add --no-cache libssl3 # buildkit
# Fri, 17 Apr 2026 00:41:19 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Fri, 17 Apr 2026 00:41:19 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Fri, 17 Apr 2026 00:41:19 GMT
VOLUME [/spiped]
# Fri, 17 Apr 2026 00:41:19 GMT
WORKDIR /spiped
# Fri, 17 Apr 2026 00:41:19 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Fri, 17 Apr 2026 00:41:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 17 Apr 2026 00:41:19 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:54b429821fc7436a26fe07d9038b86e2bef4ef3bf03e43e9ae5e91ab8e4b37a9`  
		Last Modified: Thu, 16 Apr 2026 23:54:12 GMT  
		Size: 3.7 MB (3653873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98c5658f716398e67bcdf451aa62d9268badc01207fb2761dde286827e782131`  
		Last Modified: Fri, 17 Apr 2026 00:41:28 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d837fc0069a0ae8449bb0adb9f65b43fff5ff059948bf845ea728a30d3eaca0`  
		Last Modified: Fri, 17 Apr 2026 00:41:28 GMT  
		Size: 7.9 KB (7947 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:669f2f936af1acb505aa131fbad0547df0d36ff3dc9c4f8c3a396c9877b87798`  
		Last Modified: Fri, 17 Apr 2026 00:41:28 GMT  
		Size: 96.9 KB (96930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33930e4a86d8157d355b84eecf720d4f20b38ee3502ab3baa6329d6c6acac811`  
		Last Modified: Fri, 17 Apr 2026 00:41:28 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27970db5cca98e64b9bdffc3b4445e18a503e3e0dc858c6ae91eff10bccd50bd`  
		Last Modified: Fri, 17 Apr 2026 00:41:29 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:3a63421a60ad516e8ae99df7c008ce97158220da99f3e592d9090f762eb254c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.5 KB (94497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03ae27771b3c7505fb78b0f0546a7416b11e879220de4dc6090bf643dedf8614`

```dockerfile
```

-	Layers:
	-	`sha256:c6abf9efd631a7212221f0b771ec35e734885be3d3a6755a004bba8bd46cc068`  
		Last Modified: Fri, 17 Apr 2026 00:41:28 GMT  
		Size: 80.2 KB (80241 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:033e56e9f47fa0453060710502d5ab3daddcba0cc4e51e5e138a57faf3e873d6`  
		Last Modified: Fri, 17 Apr 2026 00:41:28 GMT  
		Size: 14.3 KB (14256 bytes)  
		MIME: application/vnd.in-toto+json

## `spiped:latest`

```console
$ docker pull spiped@sha256:88bc77b7f493281dc8a9e59dc2520bc581437fda4955fe72e186b89e6f5fcc51
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 16
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v5
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `spiped:latest` - linux; amd64

```console
$ docker pull spiped@sha256:6efd769d805f600ba739d18173542643175bc85a275a6c2b774507b866215473
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.8 MB (36830428 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3193b704891a8a18ac61ecedd914fc9f5bd4f08bcb9f49c1bf5d515f1d635642`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 19:35:11 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Fri, 08 May 2026 19:35:13 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:35:34 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Fri, 08 May 2026 19:35:34 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Fri, 08 May 2026 19:35:34 GMT
VOLUME [/spiped]
# Fri, 08 May 2026 19:35:35 GMT
WORKDIR /spiped
# Fri, 08 May 2026 19:35:35 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Fri, 08 May 2026 19:35:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 08 May 2026 19:35:35 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:57fb71246055257a374deb7564ceca10f43c2352572b501efc08add5d24ebb61`  
		Last Modified: Fri, 08 May 2026 18:24:13 GMT  
		Size: 29.8 MB (29780226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d57dde26e20eb068bd1c6070f0dd034bd2fd4bb74b1da82102adef70cdfed8b`  
		Last Modified: Fri, 08 May 2026 19:35:41 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00bc21a8189b7a94c8796b3a7235e2b6031c3bb5c38a32e6dd145ecc6bbf04b7`  
		Last Modified: Fri, 08 May 2026 19:35:41 GMT  
		Size: 829.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e86acbd1889987e9e18c2f14f31b0434706f81121130868eda3c8c530a20af8`  
		Last Modified: Fri, 08 May 2026 19:35:42 GMT  
		Size: 7.0 MB (7047830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8465fa5d80692f7b30c835d41e84147136800e2c926a318e6f844e8aa3836bac`  
		Last Modified: Fri, 08 May 2026 19:35:41 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c80c6cb3750ff6c08d0efb53fca666dfb8b02730a76835cddd23324fdb9c8a50`  
		Last Modified: Fri, 08 May 2026 19:35:42 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:latest` - unknown; unknown

```console
$ docker pull spiped@sha256:487c3ee9e344c1a378f97678431d3e69821f86c4eda6453de29af68a08d68173
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3641240 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc31b2a2f275eaf7500af7747def58d03e41f11827d308adb17d72a49c616aac`

```dockerfile
```

-	Layers:
	-	`sha256:4b40916ec2afebb3f0a5a2048230524b2afb160289fc9744212b19b511be425d`  
		Last Modified: Fri, 08 May 2026 19:35:41 GMT  
		Size: 3.6 MB (3626260 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:50c2e4615b4f2b4e4ffd2810f21ba67d9914c2f032810327b3488715ae97a747`  
		Last Modified: Fri, 08 May 2026 19:35:41 GMT  
		Size: 15.0 KB (14980 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:latest` - linux; arm variant v5

```console
$ docker pull spiped@sha256:6cbedd59e1b9ab471903f2f35a283d6f759be7121323441a6ca11573d8ae1cc4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.7 MB (33739804 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d990d2ba40ebc977000d42cedd17ab74640ddafe3cdee97d15362100231d6383`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 20:56:49 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Fri, 08 May 2026 20:56:54 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 20:57:21 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Fri, 08 May 2026 20:57:21 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Fri, 08 May 2026 20:57:21 GMT
VOLUME [/spiped]
# Fri, 08 May 2026 20:57:21 GMT
WORKDIR /spiped
# Fri, 08 May 2026 20:57:21 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Fri, 08 May 2026 20:57:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 08 May 2026 20:57:21 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:8f774e9b92b540806fc05167db7ce09a3e1b12abdb9d496f7b8c82138656065a`  
		Last Modified: Fri, 08 May 2026 18:33:49 GMT  
		Size: 27.9 MB (27948200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a147b3e27022cec78f27ab492347bf10b38fbc6c422c905e72f65841af2c2d35`  
		Last Modified: Fri, 08 May 2026 20:57:28 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f6f9b4d53a44c3aa0c748c56ea7420bc6a2ab57d31e476283c807a478c52a3b`  
		Last Modified: Fri, 08 May 2026 20:57:28 GMT  
		Size: 834.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7292710fe7c3115e3ec777cbaae5e736fe457c7abb0b37105d16f3dd0e6aa0d0`  
		Last Modified: Fri, 08 May 2026 20:57:28 GMT  
		Size: 5.8 MB (5789227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1be583d842fa62ff531b016e5bcc500de7cb8e354eddd92a4d45dc6617a54826`  
		Last Modified: Fri, 08 May 2026 20:57:28 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e608db2fba73f6cd7cc5367f133a6f818229089838eec0abce963f0960c957e`  
		Last Modified: Fri, 08 May 2026 20:57:29 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:latest` - unknown; unknown

```console
$ docker pull spiped@sha256:ee5c5f8032a4007863cf92bf644d1f00091054b2afe7ed6c0a2abd05eabee240
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3634341 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:713b5a387e4efd3ea171616d9b76dcad6c85e7fd7c9406dc19495e279cbaebbd`

```dockerfile
```

-	Layers:
	-	`sha256:c1b655131c2f9a200d94f4a9833890220f71e30981b4064d2f16f8a833f997bb`  
		Last Modified: Fri, 08 May 2026 20:57:28 GMT  
		Size: 3.6 MB (3619254 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:49ddef005c38ab7a29e8f27a8e717e4f7c45fbf16cf5484b232c46b7d559ff7c`  
		Last Modified: Fri, 08 May 2026 20:57:28 GMT  
		Size: 15.1 KB (15087 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:latest` - linux; arm variant v7

```console
$ docker pull spiped@sha256:4ff1f64955f0baac28dd640dfec3eb6e7155387c14a4c6857815f04a5019ffc2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.8 MB (31802065 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3c7a8a4fd74a9ea680b4826c71ad4261c1b369234cf1e5a1af74de4f0f02780`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 19:43:48 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Fri, 08 May 2026 19:43:51 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:44:15 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Fri, 08 May 2026 19:44:15 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Fri, 08 May 2026 19:44:15 GMT
VOLUME [/spiped]
# Fri, 08 May 2026 19:44:15 GMT
WORKDIR /spiped
# Fri, 08 May 2026 19:44:15 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Fri, 08 May 2026 19:44:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 08 May 2026 19:44:15 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:f1433620eadfdfe016c8054b954f619ae5bca159f35a9459c36a76d9ef4d39c3`  
		Last Modified: Fri, 08 May 2026 18:37:58 GMT  
		Size: 26.2 MB (26214912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f160c4481d462904aa24778c4b01da7a50dd3330da0f3146ecd0fa1750b36e3`  
		Last Modified: Fri, 08 May 2026 19:44:22 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:004f6312484a065cbbbc3f38cbdcd14f9d0d288af4570dc95d0b422521d5a4e9`  
		Last Modified: Fri, 08 May 2026 19:44:22 GMT  
		Size: 828.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7cfb1c37acf55579035e448653f38eb6ee097fa7f5c76c63e12e4b73e6bed7e`  
		Last Modified: Fri, 08 May 2026 19:44:22 GMT  
		Size: 5.6 MB (5584782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55a95cb661cfcd83f6253fbdfda5fdca5527107bcaceb6cd297381b4a90ff390`  
		Last Modified: Fri, 08 May 2026 19:44:22 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d438e2f2f47da106abfac0e9680692ac80d185181f12e690966a0581ad54dd02`  
		Last Modified: Fri, 08 May 2026 19:44:23 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:latest` - unknown; unknown

```console
$ docker pull spiped@sha256:26f57e59b1a522ae1a687b8df8cf930ddf2c1d699112e21280421a49ca910972
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3633462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b2c0796641018c39128df86b179e33a156dcb32c5541d96e2972f2e703e151b`

```dockerfile
```

-	Layers:
	-	`sha256:418008c48573eba24e549885dce4ad96fd0a220792017aeb5f7acce11418e708`  
		Last Modified: Fri, 08 May 2026 19:44:22 GMT  
		Size: 3.6 MB (3618375 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0d6e39d76bd241efe3b0b538efe61306d7f2392070a38f4c7231ff87fb17c6fc`  
		Last Modified: Fri, 08 May 2026 19:44:22 GMT  
		Size: 15.1 KB (15087 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:latest` - linux; arm64 variant v8

```console
$ docker pull spiped@sha256:f4d2c7ba22fbdd4c39d643fc06400642b6d479a7dfc684a3939b41bd69392c60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.4 MB (36379770 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:076b678a615cd6adb58ebf5f146ff8d89909b5200fed70f6093a1252adb559d0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 19:36:49 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Fri, 08 May 2026 19:36:52 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:37:14 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Fri, 08 May 2026 19:37:14 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Fri, 08 May 2026 19:37:14 GMT
VOLUME [/spiped]
# Fri, 08 May 2026 19:37:14 GMT
WORKDIR /spiped
# Fri, 08 May 2026 19:37:14 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Fri, 08 May 2026 19:37:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 08 May 2026 19:37:14 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:9ebf9a1d0c9ca1bcb377e9dba38a3fdd3e89cf37164f4245286c24f8cd50a39e`  
		Last Modified: Fri, 08 May 2026 18:26:50 GMT  
		Size: 30.1 MB (30143642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab68b1d288c6fda5c3d291b76142d35c7ec90bba49f2f7e249984ab5030b2a8a`  
		Last Modified: Fri, 08 May 2026 19:37:21 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72258c478f2f0cacc665dd483d41ad5142247c03f899d55173f931b7e1127ccd`  
		Last Modified: Fri, 08 May 2026 19:37:21 GMT  
		Size: 829.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bff059afbb00a8d0c47938a8cd83a2cb69138df7c613c1ff73877639d5839980`  
		Last Modified: Fri, 08 May 2026 19:37:22 GMT  
		Size: 6.2 MB (6233755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45a3566292154189efcb23707ad78ae15514dc0e956d1fb5b4f10ca4fe927840`  
		Last Modified: Fri, 08 May 2026 19:37:22 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:290e4c2f5ef9aaf2f014d15a44512a40b25b7bc0cac6db9b8ae073550aadfd21`  
		Last Modified: Fri, 08 May 2026 19:37:23 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:latest` - unknown; unknown

```console
$ docker pull spiped@sha256:b8025f0910028dd9817f393058197a8d68cf5196c0a4e130126c5b48c10cb344
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3636412 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39ab8802b871f6dee336412a2abb98089de33fd8aaab9762c3cda2637371d0f2`

```dockerfile
```

-	Layers:
	-	`sha256:1778e062fea4855a339744af921af7d4db3810975c7e16ccd96cf39b1c6b1c2c`  
		Last Modified: Fri, 08 May 2026 19:37:22 GMT  
		Size: 3.6 MB (3621296 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5180c5ea69da7069bfd3b17dcadb7c91742ce10c5bb6bedca95126234abc14a7`  
		Last Modified: Fri, 08 May 2026 19:37:21 GMT  
		Size: 15.1 KB (15116 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:latest` - linux; 386

```console
$ docker pull spiped@sha256:d981618a0d9c00684e6abf3d84a440dd8149f059c1fa1770e74b57656b7d1660
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.7 MB (37741286 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a5cb61d1ba1a94f11c6345a5fdb6fea544260c32c6125120a8872687fa142f3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 19:42:56 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Fri, 08 May 2026 19:42:59 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:43:23 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Fri, 08 May 2026 19:43:23 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Fri, 08 May 2026 19:43:23 GMT
VOLUME [/spiped]
# Fri, 08 May 2026 19:43:24 GMT
WORKDIR /spiped
# Fri, 08 May 2026 19:43:24 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Fri, 08 May 2026 19:43:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 08 May 2026 19:43:24 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:43e2ffbaa23260ffb4e3de716920f2ed9e6af56e465ca1233a2d84c2cc1cf005`  
		Last Modified: Fri, 08 May 2026 18:32:48 GMT  
		Size: 31.3 MB (31296400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c17b41ec4f852447201aeb965c3aa2bafdee78fd8912e91f0b7978c569be5e2f`  
		Last Modified: Fri, 08 May 2026 19:43:31 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d70e5c72cd4936724086c00ec89429bded5df26b92391c2566ed2fb716f18aa7`  
		Last Modified: Fri, 08 May 2026 19:43:31 GMT  
		Size: 828.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:709085b6edd21ce82957d908045c521464897a7c5aa9403a2dd9fd0f92d5140e`  
		Last Modified: Fri, 08 May 2026 19:43:31 GMT  
		Size: 6.4 MB (6442518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b14de3e13da7ff3cc57333aab9a6a05e63d3b95b75b2817946da6be54d9c921`  
		Last Modified: Fri, 08 May 2026 19:43:31 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82008a569b9479b56a58f4f85ce555a0023f34e26440b092f1cf31191ce34456`  
		Last Modified: Fri, 08 May 2026 19:43:32 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:latest` - unknown; unknown

```console
$ docker pull spiped@sha256:3408744cec174cbb267a63b72e71e41b4e396fdbf4d8b29a489532fce7271e94
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3635335 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a172af2f2faf106a865ab5dc37e0b74df8c431777dbc521aa563779b97a0365`

```dockerfile
```

-	Layers:
	-	`sha256:aedee6e6a52a08621420305a03eeabe6aaa0173b995b54b09f9326e9c235f2be`  
		Last Modified: Fri, 08 May 2026 19:43:31 GMT  
		Size: 3.6 MB (3620389 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b58a647b7d7db8950d4a473142cb3d7427b419850101f376d98d507d3a374200`  
		Last Modified: Fri, 08 May 2026 19:43:30 GMT  
		Size: 14.9 KB (14946 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:latest` - linux; ppc64le

```console
$ docker pull spiped@sha256:2e4bd458122e32e6d0dabd95f38757741b801a99e93c50b9e645fa87eb51102a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.4 MB (40441188 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa385580deb2b8dcbc058025f53221c9c9a13ba6d0e1d1fcea983d0d8004f717`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 22:25:38 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Fri, 08 May 2026 22:25:44 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 22:26:31 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Fri, 08 May 2026 22:26:31 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Fri, 08 May 2026 22:26:31 GMT
VOLUME [/spiped]
# Fri, 08 May 2026 22:26:31 GMT
WORKDIR /spiped
# Fri, 08 May 2026 22:26:31 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Fri, 08 May 2026 22:26:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 08 May 2026 22:26:31 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:b9baa45d89920bd180d7551ccc5bc535e0c5f55b863ddebddfdc06f9436dfe91`  
		Last Modified: Fri, 08 May 2026 19:46:53 GMT  
		Size: 33.6 MB (33598087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:680ca9add7a30a7a7a02b373e65419c55c156f59ab37259115ead4b9683e755f`  
		Last Modified: Fri, 08 May 2026 22:26:46 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6fbd88296e83b0fe34af0d7aea8feb0ab152c24009771728138ab8ea6a3c7e3`  
		Last Modified: Fri, 08 May 2026 22:26:46 GMT  
		Size: 829.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:427b4091434bcad2400a705856ffbc391e8edb99ddd0244020ab8e87b8fb0029`  
		Last Modified: Fri, 08 May 2026 22:26:46 GMT  
		Size: 6.8 MB (6840726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5761c60db3e29874e7a761fb091b3a0716e00845ff60b44aed197905641f8201`  
		Last Modified: Fri, 08 May 2026 22:26:46 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d979fa4083e9e6936395a7aa0bbee2b7b6a8cc7f4e41e6234afe21c2ef4653e`  
		Last Modified: Fri, 08 May 2026 22:26:47 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:latest` - unknown; unknown

```console
$ docker pull spiped@sha256:05648be86c583500baf9a23fc752f751b17a45b3a93ce072b80d2c560c492e45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3637027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:527ae0828e720ab8c7f87f091c2295b3dcd1df2f39af33c2ebf4a290bf2b6a83`

```dockerfile
```

-	Layers:
	-	`sha256:5d43283d3f5718ce69f0dd46023d5abd6439b1b618e1f306799c06fe849aea01`  
		Last Modified: Fri, 08 May 2026 22:26:46 GMT  
		Size: 3.6 MB (3621997 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:917814349a2d8dd15ccd6b0a739bb88131cfd61f1a5b110c16b85cb164e6d7bb`  
		Last Modified: Fri, 08 May 2026 22:26:46 GMT  
		Size: 15.0 KB (15030 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:latest` - linux; riscv64

```console
$ docker pull spiped@sha256:4b71cf53987a9707a16131c1318e249b3fd3d6ce9a82cb42cc7f49e072e18fd7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.6 MB (37638423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f26a4b86552c1e9439f4f551a02d1d47a8a09b1564576e2077689ea60ed92ca7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1776729600'
# Thu, 23 Apr 2026 16:08:31 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Thu, 23 Apr 2026 16:09:01 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 23 Apr 2026 16:12:07 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Thu, 23 Apr 2026 16:12:07 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Thu, 23 Apr 2026 16:12:07 GMT
VOLUME [/spiped]
# Thu, 23 Apr 2026 16:12:07 GMT
WORKDIR /spiped
# Thu, 23 Apr 2026 16:12:08 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Thu, 23 Apr 2026 16:12:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 Apr 2026 16:12:08 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:c59e3a1f334be9f0528643dd07d69319f75f877f83be33ec1eff872a489985a0`  
		Last Modified: Wed, 22 Apr 2026 02:30:51 GMT  
		Size: 28.3 MB (28280195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65c3fe48b86e812e3913e5d13d1a9629869d202426b9c61e1715fa21c49eefb0`  
		Last Modified: Thu, 23 Apr 2026 16:13:20 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b34a84840c5fe62bd145180a478a04eb839e8ebc46151483b24496cb9f4a91f`  
		Last Modified: Thu, 23 Apr 2026 16:13:20 GMT  
		Size: 819.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d24129e4ff9e3418ef7a713edd9546c25c9b66ed26f8d5aa09e53f0c443a147`  
		Last Modified: Thu, 23 Apr 2026 16:13:23 GMT  
		Size: 9.4 MB (9355868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c9de411851378c843f1fa5367128062cec83a39214793d042c62249d045708d`  
		Last Modified: Thu, 23 Apr 2026 16:13:20 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e45064277bc4d512497c03c09b867eecba1e9f36520600b1b7cf50ccf931c314`  
		Last Modified: Thu, 23 Apr 2026 16:13:22 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:latest` - unknown; unknown

```console
$ docker pull spiped@sha256:8f1fdb09a20e86779bcd22247e4e7dc45779eadf380ed22541529e1f7c49f080
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3628433 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30611531e32494ce7228fad7644d17d3b521a5eb65e2cab640541ec507a3ccff`

```dockerfile
```

-	Layers:
	-	`sha256:28e7945cedc25231eedc0925db8b02ae1dfc5c3c41f66ebd1d3a8ef39e217551`  
		Last Modified: Thu, 23 Apr 2026 16:13:22 GMT  
		Size: 3.6 MB (3613403 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0b3f06dd63e825c9c98e9b4bfdc4f7087ec431640aee8976c15796ae26a216eb`  
		Last Modified: Thu, 23 Apr 2026 16:13:20 GMT  
		Size: 15.0 KB (15030 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:latest` - linux; s390x

```console
$ docker pull spiped@sha256:bd86a35901c83fdbe0b1dd9ab57c28d30a6565052dbe1ae0ef315fc89adffc00
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.0 MB (35964636 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90e9eead17c9f5aa0363836fa2a870f271ca50be7e2f1899fb3e7e0c17e6add5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 20:52:18 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Fri, 08 May 2026 20:52:21 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 20:52:41 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Fri, 08 May 2026 20:52:41 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Fri, 08 May 2026 20:52:41 GMT
VOLUME [/spiped]
# Fri, 08 May 2026 20:52:41 GMT
WORKDIR /spiped
# Fri, 08 May 2026 20:52:41 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Fri, 08 May 2026 20:52:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 08 May 2026 20:52:41 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:2fbbc68c452b3ba3a496488f38159dac53afe693311bee1c04f555d854ff4a2e`  
		Last Modified: Fri, 08 May 2026 18:29:20 GMT  
		Size: 29.8 MB (29840347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:379c83725970f21bcd83cf3380670f0ea271dd1fc30bc3e9568c083f2580ba55`  
		Last Modified: Fri, 08 May 2026 20:52:53 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3b3284a3de5bccf5d6b269c2b7bf9b319d15f9bebd9af7f1c95123337f82ffc`  
		Last Modified: Fri, 08 May 2026 20:52:53 GMT  
		Size: 829.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78ee74470711143892631998b06f797b17b8f24c199e31160dbad3fa3f9f4b1b`  
		Last Modified: Fri, 08 May 2026 20:52:53 GMT  
		Size: 6.1 MB (6121916 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5efe750c150333b99cd25f27597baa8d209228b9898aac1c0a7355a41ab17040`  
		Last Modified: Fri, 08 May 2026 20:52:53 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31b3234d867e10e2e459de5bd4cf9e1156a19cf24d495f2dfc7415071ae5715f`  
		Last Modified: Fri, 08 May 2026 20:52:54 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:latest` - unknown; unknown

```console
$ docker pull spiped@sha256:7c6bfdf45b3649d1b3f9001e65846a9f9c95d3e42d468a4d78f4b4419a680bf5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3633605 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5894b164eadfcc36f173a9f50f9038140f4fd57fd4528d5251f9f417819c1e0c`

```dockerfile
```

-	Layers:
	-	`sha256:117c16ab57c2ffc82accce55a8dd174232910aa2a2d2f4121a9924747a140c28`  
		Last Modified: Fri, 08 May 2026 20:52:53 GMT  
		Size: 3.6 MB (3618623 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b7501e35b7a1f23c01cc4fa7d7fe477f7d1e791f6af13d52b1b0b27d654c13a4`  
		Last Modified: Fri, 08 May 2026 20:52:53 GMT  
		Size: 15.0 KB (14982 bytes)  
		MIME: application/vnd.in-toto+json
