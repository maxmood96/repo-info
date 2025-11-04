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
$ docker pull spiped@sha256:ae34dc5e1e750a9577c6c31b1bd458e953940df360d2129dcc6ab9ec76b97634
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
$ docker pull spiped@sha256:82a44171c51ca620ba3c3c03a99b52f52529674ec87bde43e9926f1d6ec0e009
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.8 MB (36828656 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe7422969ceb15f34c8bfad19efc9932626d64801cea01ac7adb6b48c80d31f5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 04:13:26 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Tue, 04 Nov 2025 04:13:28 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 04:13:49 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Tue, 04 Nov 2025 04:13:49 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 04 Nov 2025 04:13:49 GMT
VOLUME [/spiped]
# Tue, 04 Nov 2025 04:13:49 GMT
WORKDIR /spiped
# Tue, 04 Nov 2025 04:13:49 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 04:13:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Nov 2025 04:13:49 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:d7ecded7702a5dbf6d0f79a71edc34b534d08f3051980e2c948fba72db3197fc`  
		Last Modified: Tue, 04 Nov 2025 00:13:18 GMT  
		Size: 29.8 MB (29778104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04af94b2f2784b050748c0bc593d7625ed57d5cba186a5f086621574d0db770a`  
		Last Modified: Tue, 04 Nov 2025 04:14:00 GMT  
		Size: 1.1 KB (1105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:552c1418ed5f113e9eef0fa6687c45ff9cbffe5c42b756a669850fc73f345825`  
		Last Modified: Tue, 04 Nov 2025 04:14:00 GMT  
		Size: 826.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0261a8f67e930dd0ddf4233075edba351756a7d795a0e69a5855cb123372ba2`  
		Last Modified: Tue, 04 Nov 2025 04:14:02 GMT  
		Size: 7.0 MB (7048187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5ca2f62567ececa23586d454805f1453bfb20590012b083407cd012ee296eea`  
		Last Modified: Tue, 04 Nov 2025 04:14:00 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84431171e7f009a7782b98db778ea5e41991d25b73524432b73c55af5a67e4bf`  
		Last Modified: Tue, 04 Nov 2025 04:14:00 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1` - unknown; unknown

```console
$ docker pull spiped@sha256:fdc238e5b3be11018da12f326e986158a996ba0040c07e562493af76e56d252a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3641114 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6cee0fd107c9ef0ff2a206950205e6a145e94034a05e40a81d97bf9680015577`

```dockerfile
```

-	Layers:
	-	`sha256:e9a375eaa0ee407c9bf820a27a60ebfae8e1b0eca680a00e28bb2c1fe201e7dc`  
		Last Modified: Tue, 04 Nov 2025 14:04:42 GMT  
		Size: 3.6 MB (3626132 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:090acc34f1d66361f6d8fddabbc50d86e8f70632cdc1320e68686e3b27c23564`  
		Last Modified: Tue, 04 Nov 2025 14:04:43 GMT  
		Size: 15.0 KB (14982 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1` - linux; arm variant v5

```console
$ docker pull spiped@sha256:01018b8cd02af89ba30ae1bcf4e97855ab3bdf892659021c68cd6db582a4e82f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.7 MB (33738270 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8470079cfa5129c79d5f858dfab379f480768bc25217b8e0b6729b827bda73d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 01:26:44 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Tue, 04 Nov 2025 01:26:48 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 01:27:14 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Tue, 04 Nov 2025 01:27:14 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 04 Nov 2025 01:27:14 GMT
VOLUME [/spiped]
# Tue, 04 Nov 2025 01:27:14 GMT
WORKDIR /spiped
# Tue, 04 Nov 2025 01:27:15 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 01:27:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Nov 2025 01:27:15 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:453afc2258d7bc5729fed5672fb95bafa092e30a933b4377a12034be940a671b`  
		Last Modified: Tue, 04 Nov 2025 00:13:12 GMT  
		Size: 27.9 MB (27946438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca47efc60e8d395bb20127ab62f55376f6526f660fda2af48f332ab55a5db1de`  
		Last Modified: Tue, 04 Nov 2025 01:27:29 GMT  
		Size: 1.1 KB (1105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3087d5dadbd1a81bf4a6a89b5c5513e92c5267b062a5ad88f3714f4af65944f9`  
		Last Modified: Tue, 04 Nov 2025 01:27:29 GMT  
		Size: 830.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7844d897fb72d98b6d97c02c9aea425f239371a0383c9ddb897005ce9e32d8d`  
		Last Modified: Tue, 04 Nov 2025 01:27:31 GMT  
		Size: 5.8 MB (5789464 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bb6f08fbffea41432c882d7ca57574ca10f090cfc124102a57937cb13a1e8e4`  
		Last Modified: Tue, 04 Nov 2025 01:27:29 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd566239a0cc0043085f6f763357bcb82782f07ebf8d6d1cb77a81683614a813`  
		Last Modified: Tue, 04 Nov 2025 01:27:29 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1` - unknown; unknown

```console
$ docker pull spiped@sha256:acf598dd339fcabaa30ebe44d7595caa9299c0471756c6d4f51989a8e0ef9ca6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3634214 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d932b1acba0130144dcf23c7d242737a06b9e4ef9c5c435a2ed7d54042d30ec6`

```dockerfile
```

-	Layers:
	-	`sha256:e00221651b0ba4a1e38bf876ba3fba3f946d133c72200f5bab9b64d3e969ee42`  
		Last Modified: Tue, 04 Nov 2025 08:04:27 GMT  
		Size: 3.6 MB (3619126 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:59b7876f9d30572585cdd8c35b384ebd24d330f12217040dbea5e8cbd219456a`  
		Last Modified: Tue, 04 Nov 2025 08:04:28 GMT  
		Size: 15.1 KB (15088 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1` - linux; arm variant v7

```console
$ docker pull spiped@sha256:14c077460233a0891c8d77cba716c235993ec3531bc03dea2f45959b3387e049
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.8 MB (31800147 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12694eea0cdf2315ba4c0c3242b4e3501a38116b638d7239c5a46b6f6d61eef1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 02:17:27 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Tue, 04 Nov 2025 02:17:30 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 02:17:53 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Tue, 04 Nov 2025 02:17:53 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 04 Nov 2025 02:17:53 GMT
VOLUME [/spiped]
# Tue, 04 Nov 2025 02:17:53 GMT
WORKDIR /spiped
# Tue, 04 Nov 2025 02:17:53 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 02:17:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Nov 2025 02:17:53 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:8945aefb71bd942499dd072e2c7c869b6b74b7c4dd83bff59c209b7b95d52a9f`  
		Last Modified: Tue, 04 Nov 2025 00:13:33 GMT  
		Size: 26.2 MB (26213039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fda5ed53e0dbde40dfe076db326ecd295b0b1c6d680116701507afe281baba2f`  
		Last Modified: Tue, 04 Nov 2025 02:18:05 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97b35d897f0e9c8d74564913d30c18612c62876f021e52e682bccb7ca7aa7122`  
		Last Modified: Tue, 04 Nov 2025 02:18:05 GMT  
		Size: 824.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:880acbf14d869df07dc547c6546ace74066ceb671ee539f84c04b7aa6bd93d88`  
		Last Modified: Tue, 04 Nov 2025 02:18:06 GMT  
		Size: 5.6 MB (5584740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83ad84946a9a60a387ca7f2d49194aa08d4a4b00b6921b734ddd91ea47ec12fc`  
		Last Modified: Tue, 04 Nov 2025 02:18:05 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31948a9a6bd812479abcecaee071ca0adfc7ccb05075344aacb05afdde76c955`  
		Last Modified: Tue, 04 Nov 2025 02:18:05 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1` - unknown; unknown

```console
$ docker pull spiped@sha256:26e3b4b9812bd059487e9655a891858c085e662a2f0f9a3f0b298c3dfee41536
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3633335 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc044a3ebcd39fe3f2be39febd09774d0d90a07c0b0d2bd5c34d4ecb7efd8dbb`

```dockerfile
```

-	Layers:
	-	`sha256:15aab9c35b9929d5dd1efe22911175934126591da412018cbbfcf9cd3b909b71`  
		Last Modified: Tue, 04 Nov 2025 14:04:50 GMT  
		Size: 3.6 MB (3618247 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8c0fd76702563c822a41fb5417ecf0e5cc689f14a75561c58d94a7e9235c9058`  
		Last Modified: Tue, 04 Nov 2025 14:04:50 GMT  
		Size: 15.1 KB (15088 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1` - linux; arm64 variant v8

```console
$ docker pull spiped@sha256:b6b4508fea00b81da1ef86c3545f0570316acafb1741295cd5cb81b44d57983f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.4 MB (36376612 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b7e2bcd7f2a9a352a7c82c13dfc51a9cd1fb8b6951ecbebbd5caff5dba84b44`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 01:28:45 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Tue, 04 Nov 2025 01:28:48 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 01:29:10 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Tue, 04 Nov 2025 01:29:10 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 04 Nov 2025 01:29:10 GMT
VOLUME [/spiped]
# Tue, 04 Nov 2025 01:29:10 GMT
WORKDIR /spiped
# Tue, 04 Nov 2025 01:29:10 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 01:29:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Nov 2025 01:29:10 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:51365f04b68881c6fd3d04aa38cdb689fdee6efba2aa6afcf2da5385022cf475`  
		Last Modified: Tue, 04 Nov 2025 00:13:42 GMT  
		Size: 30.1 MB (30142298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da995b7386a81488a789551cb249fe6fea42d70c39ab8a87d627d805e7e0702f`  
		Last Modified: Tue, 04 Nov 2025 01:29:26 GMT  
		Size: 1.1 KB (1105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d22fea0cfbe83fade9a6807335d9620c018e1f013f30933686d89653b8f3751b`  
		Last Modified: Tue, 04 Nov 2025 01:29:26 GMT  
		Size: 827.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85524e1a2d9a76551e1de84299ffdf92ddd97e9d6f422b3e562dbc1a6ba6a50b`  
		Last Modified: Tue, 04 Nov 2025 01:29:27 GMT  
		Size: 6.2 MB (6231948 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c76200e3164e6d69e66e2534b38d35f0e16b4f2d64f70afd08c8457d373b835`  
		Last Modified: Tue, 04 Nov 2025 01:29:26 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c14c920bf38ff2c704eacb362443942ea2718f868f01e144eb2e3e04d96e2564`  
		Last Modified: Tue, 04 Nov 2025 01:29:26 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1` - unknown; unknown

```console
$ docker pull spiped@sha256:c779c8aee90a56c7378621b7fe346c3139be38eec6de2fa672f998c9fc4986de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3636284 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:555a5ae0e19d04ef7e45c6eec70472e7764fb60499c0675e4a6594e2241883b8`

```dockerfile
```

-	Layers:
	-	`sha256:8e1c42f1f18a6f283c053696b1e4ab1e61f688cebf405ec7e2eaa94d839d7fa0`  
		Last Modified: Tue, 04 Nov 2025 14:04:56 GMT  
		Size: 3.6 MB (3621168 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ff05626a27a8aaec468faef774708e79fad5edfdcfda16285d43c34ef591b620`  
		Last Modified: Tue, 04 Nov 2025 14:04:56 GMT  
		Size: 15.1 KB (15116 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1` - linux; 386

```console
$ docker pull spiped@sha256:a4b5da618ef9092d51d4526190bc5e118e9185b168ead3df69d42dff523191d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.7 MB (37739460 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04609af68ede4d313e06c3fabb8ba8d0a59f1b79b795df1e2cbe9a50cb5c0472`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 01:30:27 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Tue, 04 Nov 2025 01:30:30 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 01:30:55 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Tue, 04 Nov 2025 01:30:55 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 04 Nov 2025 01:30:55 GMT
VOLUME [/spiped]
# Tue, 04 Nov 2025 01:30:55 GMT
WORKDIR /spiped
# Tue, 04 Nov 2025 01:30:55 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 01:30:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Nov 2025 01:30:55 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:7f24a3a0c200106d0d9ab7b6264e50c689910154fb57bf08185b9eaf995db758`  
		Last Modified: Tue, 04 Nov 2025 00:13:54 GMT  
		Size: 31.3 MB (31294783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65859e510c2db85116bdd72bf3d9c7db20eb3aa26d9b1de16d5d468fac6e12b4`  
		Last Modified: Tue, 04 Nov 2025 01:31:07 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17425f70fc6396f91fe03abde4d6c062f561878471403b5e797512c012d0b58f`  
		Last Modified: Tue, 04 Nov 2025 01:31:08 GMT  
		Size: 826.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e92634046b1716dd52c3215f95a28867b3e64b689a52a66bc446570f7d3f915b`  
		Last Modified: Tue, 04 Nov 2025 01:31:08 GMT  
		Size: 6.4 MB (6442311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:082304266fac4680b67029584f056ab407e955eaaa5694d05580c08568183ba2`  
		Last Modified: Tue, 04 Nov 2025 01:31:08 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3f65e39b75028e66f2635520d73e70b21bb85c3574637ef9339d98b08cce418`  
		Last Modified: Tue, 04 Nov 2025 01:31:07 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1` - unknown; unknown

```console
$ docker pull spiped@sha256:8dfb3738f33f7909eb57ce11e1d4c3b9621b9bc19194c790528a58c917672527
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3635206 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ddfcb2680869fc3ee15b86cc93cba15353c8e2748cada861d826a1365663d62`

```dockerfile
```

-	Layers:
	-	`sha256:951cba86bfe9e094394aed88e6e4907c73131f7aa00df1f74494c86bc03df98e`  
		Last Modified: Tue, 04 Nov 2025 14:05:00 GMT  
		Size: 3.6 MB (3620261 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3b0ff7f7bd86aaafaa07c69914072c6f5ef7f94c5bb130d61e695b5f7cbb7461`  
		Last Modified: Tue, 04 Nov 2025 14:05:01 GMT  
		Size: 14.9 KB (14945 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1` - linux; ppc64le

```console
$ docker pull spiped@sha256:17a9f9c03a0c9c0b4845e576b4d50b32791c874660333d35e2f7713b5a4f9a54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.4 MB (40441436 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49d997c535004cfabfeb64a604cfa65a56f97d30072ca33d0813aad07018c58b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 06:08:31 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Tue, 04 Nov 2025 06:08:36 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 06:09:27 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Tue, 04 Nov 2025 06:09:27 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 04 Nov 2025 06:09:27 GMT
VOLUME [/spiped]
# Tue, 04 Nov 2025 06:09:27 GMT
WORKDIR /spiped
# Tue, 04 Nov 2025 06:09:28 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 06:09:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Nov 2025 06:09:28 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:eead2c4a2afd8217def9d0ca536e7e4108ac8a91745ca25e76eb059260c04aab`  
		Last Modified: Tue, 04 Nov 2025 00:20:53 GMT  
		Size: 33.6 MB (33598647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b2092794106fcd3e23337b489859b3eb0854104e16e57e5ec14f218338644be`  
		Last Modified: Tue, 04 Nov 2025 06:09:52 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca2ca52ff15c8f4ff8cb61e6ad4215e2632257624c0c417e70e3c3f6d7f234bb`  
		Last Modified: Tue, 04 Nov 2025 06:09:52 GMT  
		Size: 827.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5983f80493ffaac3089e1f7f8864ab8cc80507a20bbedfa2c3e2923e65b2c538`  
		Last Modified: Tue, 04 Nov 2025 06:09:52 GMT  
		Size: 6.8 MB (6840421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea2839f6c480bb68bf8aaeba58db823e5327791e68b29e0834b52e7458e069e5`  
		Last Modified: Tue, 04 Nov 2025 06:09:52 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e3df6a56753bd17d0ca244a384c7110325691bdb7f9bed0ef49ad1f9e29a8a4`  
		Last Modified: Tue, 04 Nov 2025 06:09:52 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1` - unknown; unknown

```console
$ docker pull spiped@sha256:b41008bcde4956aec3ad1ac3162aa82ac36e06cc052ee46b38c5de8e30d22b8c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3636899 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6faf5bf37b372ec100c4d596f350cf4eb6c850aebed6f26691d621fd6238977b`

```dockerfile
```

-	Layers:
	-	`sha256:9ea9bb8d6fdd4f34069789821b02e82da1ebf377c37ac65a8626ff7aafd83f54`  
		Last Modified: Tue, 04 Nov 2025 14:05:06 GMT  
		Size: 3.6 MB (3621869 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c37176c69bb122c01a898f0893b93e72adf3525b0accf60ac377a130c269a2d8`  
		Last Modified: Tue, 04 Nov 2025 14:05:07 GMT  
		Size: 15.0 KB (15030 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1` - linux; riscv64

```console
$ docker pull spiped@sha256:7004f59a14e65493d89d02012617e4685f705f645959559227290584c7da32b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.6 MB (37636275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57db3066c8da0560c596ad9830d9e9d916c732311869e057ec28751c6c95ea6e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Fri, 29 Aug 2025 17:20:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1760918400'
# Fri, 29 Aug 2025 17:20:00 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Fri, 29 Aug 2025 17:20:00 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 29 Aug 2025 17:20:00 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Fri, 29 Aug 2025 17:20:00 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Fri, 29 Aug 2025 17:20:00 GMT
VOLUME [/spiped]
# Fri, 29 Aug 2025 17:20:00 GMT
WORKDIR /spiped
# Fri, 29 Aug 2025 17:20:00 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Fri, 29 Aug 2025 17:20:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 29 Aug 2025 17:20:00 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:6d1567708d42906165204f9177d357cb6a2fd51f758da447f1743b00813f892f`  
		Last Modified: Tue, 21 Oct 2025 00:37:37 GMT  
		Size: 28.3 MB (28275650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d2eca7a0881779ed75b9a6df9e9c73f4e30a2545b324835ded643360d27d8cc`  
		Last Modified: Wed, 22 Oct 2025 17:58:55 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:189f2808be96be6277f0f38d8010c29a85c6383d14b6f87ab8b25267c049edb2`  
		Last Modified: Wed, 22 Oct 2025 17:58:55 GMT  
		Size: 823.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63ffa6796bebebbe0e033f44c2862905348b86b654f6796e30afac6e530d4277`  
		Last Modified: Wed, 22 Oct 2025 17:58:57 GMT  
		Size: 9.4 MB (9358258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fa6357568a94aa6f06730895e5dae1afb3df5610b097001d226a3f77165e34f`  
		Last Modified: Wed, 22 Oct 2025 17:58:55 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94b644b84d3f1a2b591c927fa6de5e0189e84eefcff0f41ec2a3f44187185c0d`  
		Last Modified: Wed, 22 Oct 2025 17:58:55 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1` - unknown; unknown

```console
$ docker pull spiped@sha256:5c5c3dac2a6b922d04f583d01b94567b074f27f995ce52ec74839d9912349909
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3628348 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a636dc3ff00c7130929694628709b79af7b1fee5b8a10375831363195b017596`

```dockerfile
```

-	Layers:
	-	`sha256:06533fa6c4fa5d87ac9aa9b94a962ef7605ef017f0c5582d776f1d8052627da7`  
		Last Modified: Wed, 22 Oct 2025 19:04:39 GMT  
		Size: 3.6 MB (3613275 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:83d421894b349a0bc498ac33059bfe41875507a74674a4b14aefd8a88b3e1a41`  
		Last Modified: Wed, 22 Oct 2025 19:04:40 GMT  
		Size: 15.1 KB (15073 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1` - linux; s390x

```console
$ docker pull spiped@sha256:0baf3a2f09f03f86b756f3144062ee4da868d648b33a12e0d36b82135d15915b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.0 MB (35961254 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e5f3f6eecc940670d5374d68bf8dfcde4b58c041506361c10c8a41c45108a1a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 09:44:46 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Tue, 04 Nov 2025 09:44:49 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 09:45:08 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Tue, 04 Nov 2025 09:45:08 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 04 Nov 2025 09:45:08 GMT
VOLUME [/spiped]
# Tue, 04 Nov 2025 09:45:08 GMT
WORKDIR /spiped
# Tue, 04 Nov 2025 09:45:09 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 09:45:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Nov 2025 09:45:09 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:ad0bc025a1766baba34dfa4dbb5713703de6595994d855ebf4689c0b161314ee`  
		Last Modified: Tue, 04 Nov 2025 00:20:17 GMT  
		Size: 29.8 MB (29837392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:413a343213dc776ef8ec8258f5d795654681dedb3c922a2300eb7ef7d73550e3`  
		Last Modified: Tue, 04 Nov 2025 09:45:31 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35418050ccaf1bb39b9fe282dc51e265bfb9549bbc54b3a04420b3009a5b9dc7`  
		Last Modified: Tue, 04 Nov 2025 09:45:30 GMT  
		Size: 826.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21ed93eeb8c99a4ac37aba7742f9400f88c3edb4f731713a63588cbff687b5a1`  
		Last Modified: Tue, 04 Nov 2025 09:45:31 GMT  
		Size: 6.1 MB (6121493 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:093c2dfb578dd5e22bde915b7aaf0b7a8664c98c82ec4e775d9cf87a8a39c074`  
		Last Modified: Tue, 04 Nov 2025 09:45:30 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5474616e30d2720bab7073b5cb8772b655fb03da212f01a6946c7777f26eda9`  
		Last Modified: Tue, 04 Nov 2025 09:45:30 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1` - unknown; unknown

```console
$ docker pull spiped@sha256:5ba27c04f04976a68826dba21d4d8065792b743fcdb70d57dec54f77b64c21c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3633475 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1ca1463694fb2e285ab976f084b9ac52e5c81410f43af1e039c67fb30e09338`

```dockerfile
```

-	Layers:
	-	`sha256:7e8ab82c8e759285edf28b13b88413a10ae662563b6de418f33f06c7c0bde122`  
		Last Modified: Tue, 04 Nov 2025 14:05:15 GMT  
		Size: 3.6 MB (3618495 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5a721785c314ac76a8f08022c6725ff60002127c2e5716b46279b371abd12af0`  
		Last Modified: Tue, 04 Nov 2025 14:05:16 GMT  
		Size: 15.0 KB (14980 bytes)  
		MIME: application/vnd.in-toto+json

## `spiped:1-alpine`

```console
$ docker pull spiped@sha256:7b9625a81e8db9045c4eaf8f9bf40b8ef8c78a666bb7201d8d7c80538a418f7a
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
$ docker pull spiped@sha256:7d011e9e579768cd749e2df95806a3b739ebbdd516385dac92f2e9cda3570e25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3919429 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc9d66303cac034d8960b8128b5967170028d350ecf6e131c4bf30b000a3f836`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Sun, 10 Aug 2025 19:07:57 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
CMD ["/bin/sh"]
# Sun, 10 Aug 2025 19:07:57 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
RUN apk add --no-cache libssl3 # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Sun, 10 Aug 2025 19:07:57 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
VOLUME [/spiped]
# Sun, 10 Aug 2025 19:07:57 GMT
WORKDIR /spiped
# Sun, 10 Aug 2025 19:07:57 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 10 Aug 2025 19:07:57 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7c041bc04e274276fc6a842ca20a0cf973af7c178bcfb6575c0d8203718fc91`  
		Last Modified: Wed, 08 Oct 2025 22:58:11 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f81b6f5c689713065e6b968619711a3bd698fd708594cc90dae3977d54ca24e`  
		Last Modified: Wed, 08 Oct 2025 22:58:11 GMT  
		Size: 8.0 KB (7950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a035501670b01c25e6d7ce231bae87ef493bb668e877be52618f03679b673c4f`  
		Last Modified: Wed, 08 Oct 2025 22:58:11 GMT  
		Size: 107.6 KB (107645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57f81362a47a6b65eaf0da33a0c61df7c9a874d76861e5ae8fa0bc16547593db`  
		Last Modified: Wed, 08 Oct 2025 22:58:12 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48ae81c7faaf7b0d0454b9d217085e8da2f5e5a72ead2527e67506b0d4834801`  
		Last Modified: Wed, 08 Oct 2025 22:58:11 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:ed8b2f715fbc09ab5fcc75433e022573fd8e46bded0d7dd791180a01b3d4a8dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.5 KB (96494 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b323748eb9cefd40fcfe67d6c7dd561a4f5c4498457b7739b98161ea53a531c`

```dockerfile
```

-	Layers:
	-	`sha256:64366b1f73c30d49b216afd6a2acb0a27ad6d69bbaf554934ef1fb5a1b8ae379`  
		Last Modified: Thu, 09 Oct 2025 01:04:34 GMT  
		Size: 82.2 KB (82192 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d77f4db066b7ca49f19231acfa8a9f30749e3884bc787f4fcb01d3cb8a54b848`  
		Last Modified: Thu, 09 Oct 2025 01:04:35 GMT  
		Size: 14.3 KB (14302 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1-alpine` - linux; arm variant v6

```console
$ docker pull spiped@sha256:07f6c1ec4d9a40087ba1fabf98ca259b39af58fe0aa3d1b5aff7a5c9c85aab9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3602562 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66830d62439293e746c3d4171b26eb7b060853f622562e26647e13254243d153`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Sun, 10 Aug 2025 19:07:57 GMT
ADD alpine-minirootfs-3.22.2-armhf.tar.gz / # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
CMD ["/bin/sh"]
# Sun, 10 Aug 2025 19:07:57 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
RUN apk add --no-cache libssl3 # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Sun, 10 Aug 2025 19:07:57 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
VOLUME [/spiped]
# Sun, 10 Aug 2025 19:07:57 GMT
WORKDIR /spiped
# Sun, 10 Aug 2025 19:07:57 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 10 Aug 2025 19:07:57 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:bb1da3d879939be7df9f182950d2fb201d4fc2e1043677da2037cd6afb084ce0`  
		Last Modified: Wed, 08 Oct 2025 21:00:16 GMT  
		Size: 3.5 MB (3504080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:153e87cee3c8273a66e75e0a084e6876c74329042a77778cc75c7865eafb5817`  
		Last Modified: Wed, 08 Oct 2025 22:09:30 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e054efed96e629a0c9a72dadd2a8d348aa66730afa5f59ce6e02a530b64b8d73`  
		Last Modified: Wed, 08 Oct 2025 22:09:30 GMT  
		Size: 7.9 KB (7943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17dbbcac13a86093cd5821deda5686d525abf33f1ffacea149ae0a0b642a332f`  
		Last Modified: Wed, 08 Oct 2025 22:09:30 GMT  
		Size: 89.2 KB (89158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6448f1d44fa11364cf66800119dd7e5e05fc9b9d8384cce8cc858006c0684aae`  
		Last Modified: Wed, 08 Oct 2025 22:09:30 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8fa931b05c23aa0b5927c5fc4bea0d9aa65908b7ac3e936a5a5888060a49337`  
		Last Modified: Wed, 08 Oct 2025 22:09:30 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:e083a00e19dd556e9a671f1709ffc708a0ab8d2a7373856218a44de2df24d462
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.2 KB (14190 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b47da3cb18e03a2142fd48220b0903336c0d8a799d804ac3b38780211559ba36`

```dockerfile
```

-	Layers:
	-	`sha256:069680ffcf03350d43ef8d45bcb21dafd37c1132acdfce2d83391a239a85d47e`  
		Last Modified: Thu, 09 Oct 2025 01:04:38 GMT  
		Size: 14.2 KB (14190 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1-alpine` - linux; arm variant v7

```console
$ docker pull spiped@sha256:742d7ee47c94e03887525e682c2614d90b9b1f43f674ce4407bcf06b787caa29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3312569 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6db7cd0fffd0a4f2c540dfe37e4c940cf5c7595aeffea1bf7acc4b1793c73d9a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Sun, 10 Aug 2025 19:07:57 GMT
ADD alpine-minirootfs-3.22.2-armv7.tar.gz / # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
CMD ["/bin/sh"]
# Sun, 10 Aug 2025 19:07:57 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
RUN apk add --no-cache libssl3 # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Sun, 10 Aug 2025 19:07:57 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
VOLUME [/spiped]
# Sun, 10 Aug 2025 19:07:57 GMT
WORKDIR /spiped
# Sun, 10 Aug 2025 19:07:57 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 10 Aug 2025 19:07:57 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:2763c7fc79b66030222442365f4a0f69d9dbaa11f7fd47a918d29d732d52996c`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.2 MB (3221555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6a85ed9579bf45ac1db2ef56f4067b84fe0c4d8e51e006ec1d925eb0c32bf22`  
		Last Modified: Wed, 08 Oct 2025 22:10:17 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a85621545c13dee2ff1d8660f7847266105703d040c19d1816e374881a3bdf6e`  
		Last Modified: Wed, 08 Oct 2025 22:10:17 GMT  
		Size: 7.9 KB (7944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8afad049c072c9b6d3ed2946f7d0c0782835979f90696b68ac6e4c0efff5bf4`  
		Last Modified: Wed, 08 Oct 2025 22:10:17 GMT  
		Size: 81.7 KB (81688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35464221f20a70de628e3018e70c13c2e8ed9970a791049f1ba3bae429355536`  
		Last Modified: Wed, 08 Oct 2025 22:10:17 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39d6fea506e0050596918141446ad53da32b5b3a4fc9c7a5d497caf9a7ec6390`  
		Last Modified: Wed, 08 Oct 2025 22:10:18 GMT  
		Size: 336.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:1db53d701cc5320b98ed95f8e8288e9c84ddb8ad31b517b42fe2faa626874b44
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.6 KB (96633 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f53816c0890232fc85b4017c83eabcfb11884aeab001b608b66e2a8c9e183e3`

```dockerfile
```

-	Layers:
	-	`sha256:f33fdb1fd07f91c527d8c950dcb81f1eea51882f51d66c0f4da88547240c6499`  
		Last Modified: Thu, 09 Oct 2025 01:04:42 GMT  
		Size: 82.2 KB (82228 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:20a9fe69db1d74bfbe4aa6a07c0fb4e0e59f4eff9e1636b7e0c486b6435b788b`  
		Last Modified: Thu, 09 Oct 2025 01:04:42 GMT  
		Size: 14.4 KB (14405 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1-alpine` - linux; arm64 variant v8

```console
$ docker pull spiped@sha256:1c2f38931ee0ff681a7c140bbc874fa1ff5837de4baf9a50a3498fbcb12a9668
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4248020 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26b0a53163c15fa0112f2865ee8a52cbed044f04fc7001f7bd1f5e407cd57237`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Sun, 10 Aug 2025 19:07:57 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
CMD ["/bin/sh"]
# Sun, 10 Aug 2025 19:07:57 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
RUN apk add --no-cache libssl3 # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Sun, 10 Aug 2025 19:07:57 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
VOLUME [/spiped]
# Sun, 10 Aug 2025 19:07:57 GMT
WORKDIR /spiped
# Sun, 10 Aug 2025 19:07:57 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 10 Aug 2025 19:07:57 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94547f3886a10ef8162a5d7fe9f4308e302dcfd48f5be2db3b1e5d4b5156d815`  
		Last Modified: Wed, 08 Oct 2025 22:29:31 GMT  
		Size: 949.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00ee5fd6e341869b5bcb70e517a1466b54c5191790816dd7956a41164690328b`  
		Last Modified: Wed, 08 Oct 2025 22:29:32 GMT  
		Size: 7.9 KB (7949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bba2ed7625e00fce702c1adbf90233532e0e4e98935a777f6bdffa076b1c3be2`  
		Last Modified: Wed, 08 Oct 2025 22:29:31 GMT  
		Size: 100.6 KB (100621 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1612c8ef14c84a7450d3ced7f152a93e533ffbb92d525fae7dde4c2988e230d7`  
		Last Modified: Wed, 08 Oct 2025 22:29:32 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:433ac69ec6618a756cde4ab30a4488c3f0f7b89df240ede5a7b0a29d66250444`  
		Last Modified: Wed, 08 Oct 2025 22:29:31 GMT  
		Size: 336.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:f599a056737cf26e2f1e5bfb25bf8cf6f92cea0ea27b040de42b2e4bf139168f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.7 KB (96684 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad1c665f9e5776de9d503dbefb3dccddb1d230d81716f5b086b02065d6f512d0`

```dockerfile
```

-	Layers:
	-	`sha256:8c6690f0ed02188be28287964aecbd171476e7e9484ec40d030c20c7b0e182c3`  
		Last Modified: Thu, 09 Oct 2025 01:04:46 GMT  
		Size: 82.2 KB (82248 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dde4ac6f12c825868630b75c268c91338db29a424c87e551c1153694da325c83`  
		Last Modified: Thu, 09 Oct 2025 01:04:46 GMT  
		Size: 14.4 KB (14436 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1-alpine` - linux; 386

```console
$ docker pull spiped@sha256:ac72ab4f716c2dabdad650618a34deccd477e31f604bf27a1f630a7a8433d994
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3748370 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf996beac99b6a5d8eae08ab4703a9cc11bccf3cb429e61a25bebf2947e4b519`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Sun, 10 Aug 2025 19:07:57 GMT
ADD alpine-minirootfs-3.22.2-x86.tar.gz / # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
CMD ["/bin/sh"]
# Sun, 10 Aug 2025 19:07:57 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
RUN apk add --no-cache libssl3 # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Sun, 10 Aug 2025 19:07:57 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
VOLUME [/spiped]
# Sun, 10 Aug 2025 19:07:57 GMT
WORKDIR /spiped
# Sun, 10 Aug 2025 19:07:57 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 10 Aug 2025 19:07:57 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:13c6e95c06ae06f126f5e940d6d88c2fec0da715c80878ad225c76ad48d0a31e`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.6 MB (3618931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:664f8e36f37724daee2260066812a0de8999a28949591daef235c15d49ca301a`  
		Last Modified: Wed, 08 Oct 2025 22:22:15 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ee281d18609c0bc414db88c7d17dd26aca0857610126d3e6d974952f5a414ab`  
		Last Modified: Wed, 08 Oct 2025 22:22:14 GMT  
		Size: 7.9 KB (7947 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20e8cb95edb963d4e91f7f5ea1c0881091c485846b9df554d3c11102b6a6a753`  
		Last Modified: Wed, 08 Oct 2025 22:22:14 GMT  
		Size: 120.1 KB (120110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:473aab810bb857acc1c39fc855966c0a2de5edd8a71287cf2183cea8dc6fdc4b`  
		Last Modified: Wed, 08 Oct 2025 22:22:14 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1968cadac684d87fbcd83e1d646d178ae33c9242a480ddbd04f8fdf77b5e2ed`  
		Last Modified: Wed, 08 Oct 2025 22:22:14 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:2e9fe75d8ecfc557edbdaa8476f159fdb286886f6212788ecb61cda153b3ee2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.4 KB (96433 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e13e74ee61a3719d708f5b8486f092d523816b5c47e960b60b25a5d76b1aaee`

```dockerfile
```

-	Layers:
	-	`sha256:565649aba2f7ebad36d4ce1a64e495876030406355bb0f7a99f41f82b8300791`  
		Last Modified: Thu, 09 Oct 2025 01:04:50 GMT  
		Size: 82.2 KB (82167 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8cf1923abaf687d0c1af4d1718e1e365a3359dbf3e5ff8c339291f60bb0fc220`  
		Last Modified: Thu, 09 Oct 2025 01:04:51 GMT  
		Size: 14.3 KB (14266 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1-alpine` - linux; ppc64le

```console
$ docker pull spiped@sha256:506cee7907557b7efa054dc1a4c3261e8956700c9f553e9eb8d9a3470a368431
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3854263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eca7a1787271596d011a96a2b5632780587dd9653d8b0410f93093e13ecb8fcf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Sun, 10 Aug 2025 19:07:57 GMT
ADD alpine-minirootfs-3.22.2-ppc64le.tar.gz / # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
CMD ["/bin/sh"]
# Sun, 10 Aug 2025 19:07:57 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
RUN apk add --no-cache libssl3 # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Sun, 10 Aug 2025 19:07:57 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
VOLUME [/spiped]
# Sun, 10 Aug 2025 19:07:57 GMT
WORKDIR /spiped
# Sun, 10 Aug 2025 19:07:57 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 10 Aug 2025 19:07:57 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:85a0f69f026b4a01420490809bed190217e05518f7b718c0bbc1ad4871e0dedf`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.7 MB (3732241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26cf524fa67a04db3aef99fc4ab2113633c6c1965d0f890616009377904a6284`  
		Last Modified: Thu, 09 Oct 2025 03:32:10 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecc9d95b7526b98e836dea8e7e9792130d0d6d71b1d6259e6f954ddffc64f5cc`  
		Last Modified: Thu, 09 Oct 2025 03:32:10 GMT  
		Size: 8.0 KB (7955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:011805850ee2924d217a7651762c507b895c90911b4151207fe8e82e4388fcce`  
		Last Modified: Thu, 09 Oct 2025 03:32:10 GMT  
		Size: 112.7 KB (112682 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcef441d2768884d48fcb3b73e59f27e5fe6fc1cb5484df89fd3db0df4ce9437`  
		Last Modified: Thu, 09 Oct 2025 03:32:10 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03005fd392da3ad1cd46c719335ac18f079118e761584617fe8c73405301647d`  
		Last Modified: Thu, 09 Oct 2025 03:32:10 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:55eac1eb38ff8ce12fb98d86fb70542b4620b4c59ff746effba30530ad8676de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.6 KB (94625 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0a3d2f7338bf8715707424b7b716c4498d4c3b844d2dc7387da9a1c64357879`

```dockerfile
```

-	Layers:
	-	`sha256:e3e6cde5a2631b7b9b782bb7fdfcf5de409ca1736416d9573c8888daf799d9e0`  
		Last Modified: Thu, 09 Oct 2025 07:04:30 GMT  
		Size: 80.3 KB (80275 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d9220e8aff0f38f3e237e21c128db8adfad10ae35fb9db4dc56ead1ff1235e9d`  
		Last Modified: Thu, 09 Oct 2025 07:04:31 GMT  
		Size: 14.3 KB (14350 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1-alpine` - linux; riscv64

```console
$ docker pull spiped@sha256:0f378090b0e02992217f4f2a73d59cfb8c76cf62d83fec92991b3a8b1f0bfcc7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3623434 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0a7d261c52ce9f797be48d32c37a2c3f66b54a18d3599dd071fefa04e588df9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Sun, 10 Aug 2025 19:07:57 GMT
ADD alpine-minirootfs-3.22.2-riscv64.tar.gz / # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
CMD ["/bin/sh"]
# Sun, 10 Aug 2025 19:07:57 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
RUN apk add --no-cache libssl3 # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Sun, 10 Aug 2025 19:07:57 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
VOLUME [/spiped]
# Sun, 10 Aug 2025 19:07:57 GMT
WORKDIR /spiped
# Sun, 10 Aug 2025 19:07:57 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 10 Aug 2025 19:07:57 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:139bee3c50b89b56dcbc72522ce83097d9beb59d9d3a5c19072ccd1ad54b11c8`  
		Last Modified: Wed, 08 Oct 2025 21:18:33 GMT  
		Size: 3.5 MB (3515240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3c352072eefdbb94e63d3787f16fac871ba719ed362861b9e97b581edd60548`  
		Last Modified: Fri, 10 Oct 2025 20:50:10 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9aaa05a9bc37f5bb35d75064bac3af035a1d3a82ac079befd8019359672cc322`  
		Last Modified: Fri, 10 Oct 2025 20:50:10 GMT  
		Size: 7.9 KB (7948 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c51a4b112c1b7e8d19565628602648b41c69109d0f16548d16e781b095481e4d`  
		Last Modified: Fri, 10 Oct 2025 20:50:10 GMT  
		Size: 98.9 KB (98862 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9971a3bdcb8df001e3163788a7484aea74c6bf79af7ec5c42ae330638a863112`  
		Last Modified: Fri, 10 Oct 2025 20:50:10 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36e689628a891ec93dec38687edd123814871319bfb552253a1ab8608d94fa74`  
		Last Modified: Fri, 10 Oct 2025 20:50:10 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:ef79fccc5586c74ed7a097a019247ca0f6644364c4e1b931202ce2f00cf4e38a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.6 KB (94617 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3c35fd6859715e249d4b311ca37e3e8e7886a7ce1788f0688877545e1f0fb2b`

```dockerfile
```

-	Layers:
	-	`sha256:624da72bc5bd15d76a69efe794516160d8151dc3f9b207f42a5b8b5165948a76`  
		Last Modified: Fri, 10 Oct 2025 22:04:34 GMT  
		Size: 80.3 KB (80271 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a83fb34ab49138178f6f97cf97ae672fc5e173707dec2895a8d5b36f2e7689a5`  
		Last Modified: Fri, 10 Oct 2025 22:04:35 GMT  
		Size: 14.3 KB (14346 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1-alpine` - linux; s390x

```console
$ docker pull spiped@sha256:be3e9a57eb9caa9fb853c68e3efdc680d9d441f399d676b7a437f56a46d71b59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3755528 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3eee68dd7eaa10392bbfe4c42a39adf582bc976bf97937637b807540ed7960af`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Sun, 10 Aug 2025 19:07:57 GMT
ADD alpine-minirootfs-3.22.2-s390x.tar.gz / # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
CMD ["/bin/sh"]
# Sun, 10 Aug 2025 19:07:57 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
RUN apk add --no-cache libssl3 # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Sun, 10 Aug 2025 19:07:57 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
VOLUME [/spiped]
# Sun, 10 Aug 2025 19:07:57 GMT
WORKDIR /spiped
# Sun, 10 Aug 2025 19:07:57 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 10 Aug 2025 19:07:57 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:e6b06613ca2e7cdf3e8ebbe71ca45137242628a4a3a4bfcb7a9f76d0d5b0e653`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.6 MB (3649244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5eca97998e3d4f083ea39c1b7e9bd8d771aaa888745b8a60d6baff87ab6f8f37`  
		Last Modified: Thu, 09 Oct 2025 02:26:07 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ae19bb237945d6597aced8fc4cd16e5d4f06869978f4f6eb5d90a8bc9be7f39`  
		Last Modified: Thu, 09 Oct 2025 02:26:07 GMT  
		Size: 8.0 KB (7957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ce433dda6c532473e5da602686ec5186ad28c43789f172a14efc1cd9e38093d`  
		Last Modified: Thu, 09 Oct 2025 02:26:07 GMT  
		Size: 96.9 KB (96944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:867b81ca187d86754818499befad84648bb33d900aa6c797f74f14d7f06589dd`  
		Last Modified: Thu, 09 Oct 2025 02:26:06 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de821656be3d9d0eadaa8bfe8c17052ce64308ac54b60bb962a59498810f549e`  
		Last Modified: Thu, 09 Oct 2025 02:26:07 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:daeef3e785369b94f4c3fec6e7b468c0aa8bcc71748eb82a5dcb98744d0c094a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.5 KB (94540 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ff814477e4912c3dbc0dc6c3b2d236588fe065252c86c9a2ed142e200619a8a`

```dockerfile
```

-	Layers:
	-	`sha256:3ccf297cff7eee80cdb3e7128fdeabdb48c58df324a049928273000e72eba72d`  
		Last Modified: Thu, 09 Oct 2025 04:04:35 GMT  
		Size: 80.2 KB (80241 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dcfca2be336420edbf2af734bab83d3864c289d0e61390ac2cfc5f6d7f183847`  
		Last Modified: Thu, 09 Oct 2025 04:04:36 GMT  
		Size: 14.3 KB (14299 bytes)  
		MIME: application/vnd.in-toto+json

## `spiped:1.6`

```console
$ docker pull spiped@sha256:ae34dc5e1e750a9577c6c31b1bd458e953940df360d2129dcc6ab9ec76b97634
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
$ docker pull spiped@sha256:82a44171c51ca620ba3c3c03a99b52f52529674ec87bde43e9926f1d6ec0e009
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.8 MB (36828656 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe7422969ceb15f34c8bfad19efc9932626d64801cea01ac7adb6b48c80d31f5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 04:13:26 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Tue, 04 Nov 2025 04:13:28 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 04:13:49 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Tue, 04 Nov 2025 04:13:49 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 04 Nov 2025 04:13:49 GMT
VOLUME [/spiped]
# Tue, 04 Nov 2025 04:13:49 GMT
WORKDIR /spiped
# Tue, 04 Nov 2025 04:13:49 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 04:13:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Nov 2025 04:13:49 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:d7ecded7702a5dbf6d0f79a71edc34b534d08f3051980e2c948fba72db3197fc`  
		Last Modified: Tue, 04 Nov 2025 00:13:18 GMT  
		Size: 29.8 MB (29778104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04af94b2f2784b050748c0bc593d7625ed57d5cba186a5f086621574d0db770a`  
		Last Modified: Tue, 04 Nov 2025 04:14:00 GMT  
		Size: 1.1 KB (1105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:552c1418ed5f113e9eef0fa6687c45ff9cbffe5c42b756a669850fc73f345825`  
		Last Modified: Tue, 04 Nov 2025 04:14:00 GMT  
		Size: 826.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0261a8f67e930dd0ddf4233075edba351756a7d795a0e69a5855cb123372ba2`  
		Last Modified: Tue, 04 Nov 2025 04:14:02 GMT  
		Size: 7.0 MB (7048187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5ca2f62567ececa23586d454805f1453bfb20590012b083407cd012ee296eea`  
		Last Modified: Tue, 04 Nov 2025 04:14:00 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84431171e7f009a7782b98db778ea5e41991d25b73524432b73c55af5a67e4bf`  
		Last Modified: Tue, 04 Nov 2025 04:14:00 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6` - unknown; unknown

```console
$ docker pull spiped@sha256:fdc238e5b3be11018da12f326e986158a996ba0040c07e562493af76e56d252a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3641114 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6cee0fd107c9ef0ff2a206950205e6a145e94034a05e40a81d97bf9680015577`

```dockerfile
```

-	Layers:
	-	`sha256:e9a375eaa0ee407c9bf820a27a60ebfae8e1b0eca680a00e28bb2c1fe201e7dc`  
		Last Modified: Tue, 04 Nov 2025 14:04:42 GMT  
		Size: 3.6 MB (3626132 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:090acc34f1d66361f6d8fddabbc50d86e8f70632cdc1320e68686e3b27c23564`  
		Last Modified: Tue, 04 Nov 2025 14:04:43 GMT  
		Size: 15.0 KB (14982 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6` - linux; arm variant v5

```console
$ docker pull spiped@sha256:01018b8cd02af89ba30ae1bcf4e97855ab3bdf892659021c68cd6db582a4e82f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.7 MB (33738270 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8470079cfa5129c79d5f858dfab379f480768bc25217b8e0b6729b827bda73d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 01:26:44 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Tue, 04 Nov 2025 01:26:48 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 01:27:14 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Tue, 04 Nov 2025 01:27:14 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 04 Nov 2025 01:27:14 GMT
VOLUME [/spiped]
# Tue, 04 Nov 2025 01:27:14 GMT
WORKDIR /spiped
# Tue, 04 Nov 2025 01:27:15 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 01:27:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Nov 2025 01:27:15 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:453afc2258d7bc5729fed5672fb95bafa092e30a933b4377a12034be940a671b`  
		Last Modified: Tue, 04 Nov 2025 00:13:12 GMT  
		Size: 27.9 MB (27946438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca47efc60e8d395bb20127ab62f55376f6526f660fda2af48f332ab55a5db1de`  
		Last Modified: Tue, 04 Nov 2025 01:27:29 GMT  
		Size: 1.1 KB (1105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3087d5dadbd1a81bf4a6a89b5c5513e92c5267b062a5ad88f3714f4af65944f9`  
		Last Modified: Tue, 04 Nov 2025 01:27:29 GMT  
		Size: 830.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7844d897fb72d98b6d97c02c9aea425f239371a0383c9ddb897005ce9e32d8d`  
		Last Modified: Tue, 04 Nov 2025 01:27:31 GMT  
		Size: 5.8 MB (5789464 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bb6f08fbffea41432c882d7ca57574ca10f090cfc124102a57937cb13a1e8e4`  
		Last Modified: Tue, 04 Nov 2025 01:27:29 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd566239a0cc0043085f6f763357bcb82782f07ebf8d6d1cb77a81683614a813`  
		Last Modified: Tue, 04 Nov 2025 01:27:29 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6` - unknown; unknown

```console
$ docker pull spiped@sha256:acf598dd339fcabaa30ebe44d7595caa9299c0471756c6d4f51989a8e0ef9ca6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3634214 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d932b1acba0130144dcf23c7d242737a06b9e4ef9c5c435a2ed7d54042d30ec6`

```dockerfile
```

-	Layers:
	-	`sha256:e00221651b0ba4a1e38bf876ba3fba3f946d133c72200f5bab9b64d3e969ee42`  
		Last Modified: Tue, 04 Nov 2025 08:04:27 GMT  
		Size: 3.6 MB (3619126 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:59b7876f9d30572585cdd8c35b384ebd24d330f12217040dbea5e8cbd219456a`  
		Last Modified: Tue, 04 Nov 2025 08:04:28 GMT  
		Size: 15.1 KB (15088 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6` - linux; arm variant v7

```console
$ docker pull spiped@sha256:14c077460233a0891c8d77cba716c235993ec3531bc03dea2f45959b3387e049
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.8 MB (31800147 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12694eea0cdf2315ba4c0c3242b4e3501a38116b638d7239c5a46b6f6d61eef1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 02:17:27 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Tue, 04 Nov 2025 02:17:30 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 02:17:53 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Tue, 04 Nov 2025 02:17:53 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 04 Nov 2025 02:17:53 GMT
VOLUME [/spiped]
# Tue, 04 Nov 2025 02:17:53 GMT
WORKDIR /spiped
# Tue, 04 Nov 2025 02:17:53 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 02:17:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Nov 2025 02:17:53 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:8945aefb71bd942499dd072e2c7c869b6b74b7c4dd83bff59c209b7b95d52a9f`  
		Last Modified: Tue, 04 Nov 2025 00:13:33 GMT  
		Size: 26.2 MB (26213039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fda5ed53e0dbde40dfe076db326ecd295b0b1c6d680116701507afe281baba2f`  
		Last Modified: Tue, 04 Nov 2025 02:18:05 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97b35d897f0e9c8d74564913d30c18612c62876f021e52e682bccb7ca7aa7122`  
		Last Modified: Tue, 04 Nov 2025 02:18:05 GMT  
		Size: 824.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:880acbf14d869df07dc547c6546ace74066ceb671ee539f84c04b7aa6bd93d88`  
		Last Modified: Tue, 04 Nov 2025 02:18:06 GMT  
		Size: 5.6 MB (5584740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83ad84946a9a60a387ca7f2d49194aa08d4a4b00b6921b734ddd91ea47ec12fc`  
		Last Modified: Tue, 04 Nov 2025 02:18:05 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31948a9a6bd812479abcecaee071ca0adfc7ccb05075344aacb05afdde76c955`  
		Last Modified: Tue, 04 Nov 2025 02:18:05 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6` - unknown; unknown

```console
$ docker pull spiped@sha256:26e3b4b9812bd059487e9655a891858c085e662a2f0f9a3f0b298c3dfee41536
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3633335 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc044a3ebcd39fe3f2be39febd09774d0d90a07c0b0d2bd5c34d4ecb7efd8dbb`

```dockerfile
```

-	Layers:
	-	`sha256:15aab9c35b9929d5dd1efe22911175934126591da412018cbbfcf9cd3b909b71`  
		Last Modified: Tue, 04 Nov 2025 14:04:50 GMT  
		Size: 3.6 MB (3618247 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8c0fd76702563c822a41fb5417ecf0e5cc689f14a75561c58d94a7e9235c9058`  
		Last Modified: Tue, 04 Nov 2025 14:04:50 GMT  
		Size: 15.1 KB (15088 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6` - linux; arm64 variant v8

```console
$ docker pull spiped@sha256:b6b4508fea00b81da1ef86c3545f0570316acafb1741295cd5cb81b44d57983f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.4 MB (36376612 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b7e2bcd7f2a9a352a7c82c13dfc51a9cd1fb8b6951ecbebbd5caff5dba84b44`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 01:28:45 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Tue, 04 Nov 2025 01:28:48 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 01:29:10 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Tue, 04 Nov 2025 01:29:10 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 04 Nov 2025 01:29:10 GMT
VOLUME [/spiped]
# Tue, 04 Nov 2025 01:29:10 GMT
WORKDIR /spiped
# Tue, 04 Nov 2025 01:29:10 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 01:29:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Nov 2025 01:29:10 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:51365f04b68881c6fd3d04aa38cdb689fdee6efba2aa6afcf2da5385022cf475`  
		Last Modified: Tue, 04 Nov 2025 00:13:42 GMT  
		Size: 30.1 MB (30142298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da995b7386a81488a789551cb249fe6fea42d70c39ab8a87d627d805e7e0702f`  
		Last Modified: Tue, 04 Nov 2025 01:29:26 GMT  
		Size: 1.1 KB (1105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d22fea0cfbe83fade9a6807335d9620c018e1f013f30933686d89653b8f3751b`  
		Last Modified: Tue, 04 Nov 2025 01:29:26 GMT  
		Size: 827.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85524e1a2d9a76551e1de84299ffdf92ddd97e9d6f422b3e562dbc1a6ba6a50b`  
		Last Modified: Tue, 04 Nov 2025 01:29:27 GMT  
		Size: 6.2 MB (6231948 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c76200e3164e6d69e66e2534b38d35f0e16b4f2d64f70afd08c8457d373b835`  
		Last Modified: Tue, 04 Nov 2025 01:29:26 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c14c920bf38ff2c704eacb362443942ea2718f868f01e144eb2e3e04d96e2564`  
		Last Modified: Tue, 04 Nov 2025 01:29:26 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6` - unknown; unknown

```console
$ docker pull spiped@sha256:c779c8aee90a56c7378621b7fe346c3139be38eec6de2fa672f998c9fc4986de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3636284 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:555a5ae0e19d04ef7e45c6eec70472e7764fb60499c0675e4a6594e2241883b8`

```dockerfile
```

-	Layers:
	-	`sha256:8e1c42f1f18a6f283c053696b1e4ab1e61f688cebf405ec7e2eaa94d839d7fa0`  
		Last Modified: Tue, 04 Nov 2025 14:04:56 GMT  
		Size: 3.6 MB (3621168 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ff05626a27a8aaec468faef774708e79fad5edfdcfda16285d43c34ef591b620`  
		Last Modified: Tue, 04 Nov 2025 14:04:56 GMT  
		Size: 15.1 KB (15116 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6` - linux; 386

```console
$ docker pull spiped@sha256:a4b5da618ef9092d51d4526190bc5e118e9185b168ead3df69d42dff523191d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.7 MB (37739460 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04609af68ede4d313e06c3fabb8ba8d0a59f1b79b795df1e2cbe9a50cb5c0472`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 01:30:27 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Tue, 04 Nov 2025 01:30:30 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 01:30:55 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Tue, 04 Nov 2025 01:30:55 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 04 Nov 2025 01:30:55 GMT
VOLUME [/spiped]
# Tue, 04 Nov 2025 01:30:55 GMT
WORKDIR /spiped
# Tue, 04 Nov 2025 01:30:55 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 01:30:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Nov 2025 01:30:55 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:7f24a3a0c200106d0d9ab7b6264e50c689910154fb57bf08185b9eaf995db758`  
		Last Modified: Tue, 04 Nov 2025 00:13:54 GMT  
		Size: 31.3 MB (31294783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65859e510c2db85116bdd72bf3d9c7db20eb3aa26d9b1de16d5d468fac6e12b4`  
		Last Modified: Tue, 04 Nov 2025 01:31:07 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17425f70fc6396f91fe03abde4d6c062f561878471403b5e797512c012d0b58f`  
		Last Modified: Tue, 04 Nov 2025 01:31:08 GMT  
		Size: 826.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e92634046b1716dd52c3215f95a28867b3e64b689a52a66bc446570f7d3f915b`  
		Last Modified: Tue, 04 Nov 2025 01:31:08 GMT  
		Size: 6.4 MB (6442311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:082304266fac4680b67029584f056ab407e955eaaa5694d05580c08568183ba2`  
		Last Modified: Tue, 04 Nov 2025 01:31:08 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3f65e39b75028e66f2635520d73e70b21bb85c3574637ef9339d98b08cce418`  
		Last Modified: Tue, 04 Nov 2025 01:31:07 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6` - unknown; unknown

```console
$ docker pull spiped@sha256:8dfb3738f33f7909eb57ce11e1d4c3b9621b9bc19194c790528a58c917672527
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3635206 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ddfcb2680869fc3ee15b86cc93cba15353c8e2748cada861d826a1365663d62`

```dockerfile
```

-	Layers:
	-	`sha256:951cba86bfe9e094394aed88e6e4907c73131f7aa00df1f74494c86bc03df98e`  
		Last Modified: Tue, 04 Nov 2025 14:05:00 GMT  
		Size: 3.6 MB (3620261 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3b0ff7f7bd86aaafaa07c69914072c6f5ef7f94c5bb130d61e695b5f7cbb7461`  
		Last Modified: Tue, 04 Nov 2025 14:05:01 GMT  
		Size: 14.9 KB (14945 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6` - linux; ppc64le

```console
$ docker pull spiped@sha256:17a9f9c03a0c9c0b4845e576b4d50b32791c874660333d35e2f7713b5a4f9a54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.4 MB (40441436 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49d997c535004cfabfeb64a604cfa65a56f97d30072ca33d0813aad07018c58b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 06:08:31 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Tue, 04 Nov 2025 06:08:36 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 06:09:27 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Tue, 04 Nov 2025 06:09:27 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 04 Nov 2025 06:09:27 GMT
VOLUME [/spiped]
# Tue, 04 Nov 2025 06:09:27 GMT
WORKDIR /spiped
# Tue, 04 Nov 2025 06:09:28 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 06:09:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Nov 2025 06:09:28 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:eead2c4a2afd8217def9d0ca536e7e4108ac8a91745ca25e76eb059260c04aab`  
		Last Modified: Tue, 04 Nov 2025 00:20:53 GMT  
		Size: 33.6 MB (33598647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b2092794106fcd3e23337b489859b3eb0854104e16e57e5ec14f218338644be`  
		Last Modified: Tue, 04 Nov 2025 06:09:52 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca2ca52ff15c8f4ff8cb61e6ad4215e2632257624c0c417e70e3c3f6d7f234bb`  
		Last Modified: Tue, 04 Nov 2025 06:09:52 GMT  
		Size: 827.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5983f80493ffaac3089e1f7f8864ab8cc80507a20bbedfa2c3e2923e65b2c538`  
		Last Modified: Tue, 04 Nov 2025 06:09:52 GMT  
		Size: 6.8 MB (6840421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea2839f6c480bb68bf8aaeba58db823e5327791e68b29e0834b52e7458e069e5`  
		Last Modified: Tue, 04 Nov 2025 06:09:52 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e3df6a56753bd17d0ca244a384c7110325691bdb7f9bed0ef49ad1f9e29a8a4`  
		Last Modified: Tue, 04 Nov 2025 06:09:52 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6` - unknown; unknown

```console
$ docker pull spiped@sha256:b41008bcde4956aec3ad1ac3162aa82ac36e06cc052ee46b38c5de8e30d22b8c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3636899 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6faf5bf37b372ec100c4d596f350cf4eb6c850aebed6f26691d621fd6238977b`

```dockerfile
```

-	Layers:
	-	`sha256:9ea9bb8d6fdd4f34069789821b02e82da1ebf377c37ac65a8626ff7aafd83f54`  
		Last Modified: Tue, 04 Nov 2025 14:05:06 GMT  
		Size: 3.6 MB (3621869 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c37176c69bb122c01a898f0893b93e72adf3525b0accf60ac377a130c269a2d8`  
		Last Modified: Tue, 04 Nov 2025 14:05:07 GMT  
		Size: 15.0 KB (15030 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6` - linux; riscv64

```console
$ docker pull spiped@sha256:7004f59a14e65493d89d02012617e4685f705f645959559227290584c7da32b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.6 MB (37636275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57db3066c8da0560c596ad9830d9e9d916c732311869e057ec28751c6c95ea6e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Fri, 29 Aug 2025 17:20:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1760918400'
# Fri, 29 Aug 2025 17:20:00 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Fri, 29 Aug 2025 17:20:00 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 29 Aug 2025 17:20:00 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Fri, 29 Aug 2025 17:20:00 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Fri, 29 Aug 2025 17:20:00 GMT
VOLUME [/spiped]
# Fri, 29 Aug 2025 17:20:00 GMT
WORKDIR /spiped
# Fri, 29 Aug 2025 17:20:00 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Fri, 29 Aug 2025 17:20:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 29 Aug 2025 17:20:00 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:6d1567708d42906165204f9177d357cb6a2fd51f758da447f1743b00813f892f`  
		Last Modified: Tue, 21 Oct 2025 00:37:37 GMT  
		Size: 28.3 MB (28275650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d2eca7a0881779ed75b9a6df9e9c73f4e30a2545b324835ded643360d27d8cc`  
		Last Modified: Wed, 22 Oct 2025 17:58:55 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:189f2808be96be6277f0f38d8010c29a85c6383d14b6f87ab8b25267c049edb2`  
		Last Modified: Wed, 22 Oct 2025 17:58:55 GMT  
		Size: 823.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63ffa6796bebebbe0e033f44c2862905348b86b654f6796e30afac6e530d4277`  
		Last Modified: Wed, 22 Oct 2025 17:58:57 GMT  
		Size: 9.4 MB (9358258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fa6357568a94aa6f06730895e5dae1afb3df5610b097001d226a3f77165e34f`  
		Last Modified: Wed, 22 Oct 2025 17:58:55 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94b644b84d3f1a2b591c927fa6de5e0189e84eefcff0f41ec2a3f44187185c0d`  
		Last Modified: Wed, 22 Oct 2025 17:58:55 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6` - unknown; unknown

```console
$ docker pull spiped@sha256:5c5c3dac2a6b922d04f583d01b94567b074f27f995ce52ec74839d9912349909
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3628348 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a636dc3ff00c7130929694628709b79af7b1fee5b8a10375831363195b017596`

```dockerfile
```

-	Layers:
	-	`sha256:06533fa6c4fa5d87ac9aa9b94a962ef7605ef017f0c5582d776f1d8052627da7`  
		Last Modified: Wed, 22 Oct 2025 19:04:39 GMT  
		Size: 3.6 MB (3613275 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:83d421894b349a0bc498ac33059bfe41875507a74674a4b14aefd8a88b3e1a41`  
		Last Modified: Wed, 22 Oct 2025 19:04:40 GMT  
		Size: 15.1 KB (15073 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6` - linux; s390x

```console
$ docker pull spiped@sha256:0baf3a2f09f03f86b756f3144062ee4da868d648b33a12e0d36b82135d15915b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.0 MB (35961254 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e5f3f6eecc940670d5374d68bf8dfcde4b58c041506361c10c8a41c45108a1a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 09:44:46 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Tue, 04 Nov 2025 09:44:49 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 09:45:08 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Tue, 04 Nov 2025 09:45:08 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 04 Nov 2025 09:45:08 GMT
VOLUME [/spiped]
# Tue, 04 Nov 2025 09:45:08 GMT
WORKDIR /spiped
# Tue, 04 Nov 2025 09:45:09 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 09:45:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Nov 2025 09:45:09 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:ad0bc025a1766baba34dfa4dbb5713703de6595994d855ebf4689c0b161314ee`  
		Last Modified: Tue, 04 Nov 2025 00:20:17 GMT  
		Size: 29.8 MB (29837392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:413a343213dc776ef8ec8258f5d795654681dedb3c922a2300eb7ef7d73550e3`  
		Last Modified: Tue, 04 Nov 2025 09:45:31 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35418050ccaf1bb39b9fe282dc51e265bfb9549bbc54b3a04420b3009a5b9dc7`  
		Last Modified: Tue, 04 Nov 2025 09:45:30 GMT  
		Size: 826.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21ed93eeb8c99a4ac37aba7742f9400f88c3edb4f731713a63588cbff687b5a1`  
		Last Modified: Tue, 04 Nov 2025 09:45:31 GMT  
		Size: 6.1 MB (6121493 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:093c2dfb578dd5e22bde915b7aaf0b7a8664c98c82ec4e775d9cf87a8a39c074`  
		Last Modified: Tue, 04 Nov 2025 09:45:30 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5474616e30d2720bab7073b5cb8772b655fb03da212f01a6946c7777f26eda9`  
		Last Modified: Tue, 04 Nov 2025 09:45:30 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6` - unknown; unknown

```console
$ docker pull spiped@sha256:5ba27c04f04976a68826dba21d4d8065792b743fcdb70d57dec54f77b64c21c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3633475 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1ca1463694fb2e285ab976f084b9ac52e5c81410f43af1e039c67fb30e09338`

```dockerfile
```

-	Layers:
	-	`sha256:7e8ab82c8e759285edf28b13b88413a10ae662563b6de418f33f06c7c0bde122`  
		Last Modified: Tue, 04 Nov 2025 14:05:15 GMT  
		Size: 3.6 MB (3618495 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5a721785c314ac76a8f08022c6725ff60002127c2e5716b46279b371abd12af0`  
		Last Modified: Tue, 04 Nov 2025 14:05:16 GMT  
		Size: 15.0 KB (14980 bytes)  
		MIME: application/vnd.in-toto+json

## `spiped:1.6-alpine`

```console
$ docker pull spiped@sha256:7b9625a81e8db9045c4eaf8f9bf40b8ef8c78a666bb7201d8d7c80538a418f7a
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
$ docker pull spiped@sha256:7d011e9e579768cd749e2df95806a3b739ebbdd516385dac92f2e9cda3570e25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3919429 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc9d66303cac034d8960b8128b5967170028d350ecf6e131c4bf30b000a3f836`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Sun, 10 Aug 2025 19:07:57 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
CMD ["/bin/sh"]
# Sun, 10 Aug 2025 19:07:57 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
RUN apk add --no-cache libssl3 # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Sun, 10 Aug 2025 19:07:57 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
VOLUME [/spiped]
# Sun, 10 Aug 2025 19:07:57 GMT
WORKDIR /spiped
# Sun, 10 Aug 2025 19:07:57 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 10 Aug 2025 19:07:57 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7c041bc04e274276fc6a842ca20a0cf973af7c178bcfb6575c0d8203718fc91`  
		Last Modified: Wed, 08 Oct 2025 22:58:11 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f81b6f5c689713065e6b968619711a3bd698fd708594cc90dae3977d54ca24e`  
		Last Modified: Wed, 08 Oct 2025 22:58:11 GMT  
		Size: 8.0 KB (7950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a035501670b01c25e6d7ce231bae87ef493bb668e877be52618f03679b673c4f`  
		Last Modified: Wed, 08 Oct 2025 22:58:11 GMT  
		Size: 107.6 KB (107645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57f81362a47a6b65eaf0da33a0c61df7c9a874d76861e5ae8fa0bc16547593db`  
		Last Modified: Wed, 08 Oct 2025 22:58:12 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48ae81c7faaf7b0d0454b9d217085e8da2f5e5a72ead2527e67506b0d4834801`  
		Last Modified: Wed, 08 Oct 2025 22:58:11 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:ed8b2f715fbc09ab5fcc75433e022573fd8e46bded0d7dd791180a01b3d4a8dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.5 KB (96494 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b323748eb9cefd40fcfe67d6c7dd561a4f5c4498457b7739b98161ea53a531c`

```dockerfile
```

-	Layers:
	-	`sha256:64366b1f73c30d49b216afd6a2acb0a27ad6d69bbaf554934ef1fb5a1b8ae379`  
		Last Modified: Thu, 09 Oct 2025 01:04:34 GMT  
		Size: 82.2 KB (82192 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d77f4db066b7ca49f19231acfa8a9f30749e3884bc787f4fcb01d3cb8a54b848`  
		Last Modified: Thu, 09 Oct 2025 01:04:35 GMT  
		Size: 14.3 KB (14302 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6-alpine` - linux; arm variant v6

```console
$ docker pull spiped@sha256:07f6c1ec4d9a40087ba1fabf98ca259b39af58fe0aa3d1b5aff7a5c9c85aab9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3602562 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66830d62439293e746c3d4171b26eb7b060853f622562e26647e13254243d153`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Sun, 10 Aug 2025 19:07:57 GMT
ADD alpine-minirootfs-3.22.2-armhf.tar.gz / # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
CMD ["/bin/sh"]
# Sun, 10 Aug 2025 19:07:57 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
RUN apk add --no-cache libssl3 # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Sun, 10 Aug 2025 19:07:57 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
VOLUME [/spiped]
# Sun, 10 Aug 2025 19:07:57 GMT
WORKDIR /spiped
# Sun, 10 Aug 2025 19:07:57 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 10 Aug 2025 19:07:57 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:bb1da3d879939be7df9f182950d2fb201d4fc2e1043677da2037cd6afb084ce0`  
		Last Modified: Wed, 08 Oct 2025 21:00:16 GMT  
		Size: 3.5 MB (3504080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:153e87cee3c8273a66e75e0a084e6876c74329042a77778cc75c7865eafb5817`  
		Last Modified: Wed, 08 Oct 2025 22:09:30 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e054efed96e629a0c9a72dadd2a8d348aa66730afa5f59ce6e02a530b64b8d73`  
		Last Modified: Wed, 08 Oct 2025 22:09:30 GMT  
		Size: 7.9 KB (7943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17dbbcac13a86093cd5821deda5686d525abf33f1ffacea149ae0a0b642a332f`  
		Last Modified: Wed, 08 Oct 2025 22:09:30 GMT  
		Size: 89.2 KB (89158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6448f1d44fa11364cf66800119dd7e5e05fc9b9d8384cce8cc858006c0684aae`  
		Last Modified: Wed, 08 Oct 2025 22:09:30 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8fa931b05c23aa0b5927c5fc4bea0d9aa65908b7ac3e936a5a5888060a49337`  
		Last Modified: Wed, 08 Oct 2025 22:09:30 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:e083a00e19dd556e9a671f1709ffc708a0ab8d2a7373856218a44de2df24d462
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.2 KB (14190 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b47da3cb18e03a2142fd48220b0903336c0d8a799d804ac3b38780211559ba36`

```dockerfile
```

-	Layers:
	-	`sha256:069680ffcf03350d43ef8d45bcb21dafd37c1132acdfce2d83391a239a85d47e`  
		Last Modified: Thu, 09 Oct 2025 01:04:38 GMT  
		Size: 14.2 KB (14190 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6-alpine` - linux; arm variant v7

```console
$ docker pull spiped@sha256:742d7ee47c94e03887525e682c2614d90b9b1f43f674ce4407bcf06b787caa29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3312569 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6db7cd0fffd0a4f2c540dfe37e4c940cf5c7595aeffea1bf7acc4b1793c73d9a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Sun, 10 Aug 2025 19:07:57 GMT
ADD alpine-minirootfs-3.22.2-armv7.tar.gz / # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
CMD ["/bin/sh"]
# Sun, 10 Aug 2025 19:07:57 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
RUN apk add --no-cache libssl3 # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Sun, 10 Aug 2025 19:07:57 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
VOLUME [/spiped]
# Sun, 10 Aug 2025 19:07:57 GMT
WORKDIR /spiped
# Sun, 10 Aug 2025 19:07:57 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 10 Aug 2025 19:07:57 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:2763c7fc79b66030222442365f4a0f69d9dbaa11f7fd47a918d29d732d52996c`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.2 MB (3221555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6a85ed9579bf45ac1db2ef56f4067b84fe0c4d8e51e006ec1d925eb0c32bf22`  
		Last Modified: Wed, 08 Oct 2025 22:10:17 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a85621545c13dee2ff1d8660f7847266105703d040c19d1816e374881a3bdf6e`  
		Last Modified: Wed, 08 Oct 2025 22:10:17 GMT  
		Size: 7.9 KB (7944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8afad049c072c9b6d3ed2946f7d0c0782835979f90696b68ac6e4c0efff5bf4`  
		Last Modified: Wed, 08 Oct 2025 22:10:17 GMT  
		Size: 81.7 KB (81688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35464221f20a70de628e3018e70c13c2e8ed9970a791049f1ba3bae429355536`  
		Last Modified: Wed, 08 Oct 2025 22:10:17 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39d6fea506e0050596918141446ad53da32b5b3a4fc9c7a5d497caf9a7ec6390`  
		Last Modified: Wed, 08 Oct 2025 22:10:18 GMT  
		Size: 336.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:1db53d701cc5320b98ed95f8e8288e9c84ddb8ad31b517b42fe2faa626874b44
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.6 KB (96633 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f53816c0890232fc85b4017c83eabcfb11884aeab001b608b66e2a8c9e183e3`

```dockerfile
```

-	Layers:
	-	`sha256:f33fdb1fd07f91c527d8c950dcb81f1eea51882f51d66c0f4da88547240c6499`  
		Last Modified: Thu, 09 Oct 2025 01:04:42 GMT  
		Size: 82.2 KB (82228 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:20a9fe69db1d74bfbe4aa6a07c0fb4e0e59f4eff9e1636b7e0c486b6435b788b`  
		Last Modified: Thu, 09 Oct 2025 01:04:42 GMT  
		Size: 14.4 KB (14405 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6-alpine` - linux; arm64 variant v8

```console
$ docker pull spiped@sha256:1c2f38931ee0ff681a7c140bbc874fa1ff5837de4baf9a50a3498fbcb12a9668
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4248020 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26b0a53163c15fa0112f2865ee8a52cbed044f04fc7001f7bd1f5e407cd57237`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Sun, 10 Aug 2025 19:07:57 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
CMD ["/bin/sh"]
# Sun, 10 Aug 2025 19:07:57 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
RUN apk add --no-cache libssl3 # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Sun, 10 Aug 2025 19:07:57 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
VOLUME [/spiped]
# Sun, 10 Aug 2025 19:07:57 GMT
WORKDIR /spiped
# Sun, 10 Aug 2025 19:07:57 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 10 Aug 2025 19:07:57 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94547f3886a10ef8162a5d7fe9f4308e302dcfd48f5be2db3b1e5d4b5156d815`  
		Last Modified: Wed, 08 Oct 2025 22:29:31 GMT  
		Size: 949.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00ee5fd6e341869b5bcb70e517a1466b54c5191790816dd7956a41164690328b`  
		Last Modified: Wed, 08 Oct 2025 22:29:32 GMT  
		Size: 7.9 KB (7949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bba2ed7625e00fce702c1adbf90233532e0e4e98935a777f6bdffa076b1c3be2`  
		Last Modified: Wed, 08 Oct 2025 22:29:31 GMT  
		Size: 100.6 KB (100621 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1612c8ef14c84a7450d3ced7f152a93e533ffbb92d525fae7dde4c2988e230d7`  
		Last Modified: Wed, 08 Oct 2025 22:29:32 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:433ac69ec6618a756cde4ab30a4488c3f0f7b89df240ede5a7b0a29d66250444`  
		Last Modified: Wed, 08 Oct 2025 22:29:31 GMT  
		Size: 336.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:f599a056737cf26e2f1e5bfb25bf8cf6f92cea0ea27b040de42b2e4bf139168f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.7 KB (96684 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad1c665f9e5776de9d503dbefb3dccddb1d230d81716f5b086b02065d6f512d0`

```dockerfile
```

-	Layers:
	-	`sha256:8c6690f0ed02188be28287964aecbd171476e7e9484ec40d030c20c7b0e182c3`  
		Last Modified: Thu, 09 Oct 2025 01:04:46 GMT  
		Size: 82.2 KB (82248 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dde4ac6f12c825868630b75c268c91338db29a424c87e551c1153694da325c83`  
		Last Modified: Thu, 09 Oct 2025 01:04:46 GMT  
		Size: 14.4 KB (14436 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6-alpine` - linux; 386

```console
$ docker pull spiped@sha256:ac72ab4f716c2dabdad650618a34deccd477e31f604bf27a1f630a7a8433d994
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3748370 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf996beac99b6a5d8eae08ab4703a9cc11bccf3cb429e61a25bebf2947e4b519`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Sun, 10 Aug 2025 19:07:57 GMT
ADD alpine-minirootfs-3.22.2-x86.tar.gz / # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
CMD ["/bin/sh"]
# Sun, 10 Aug 2025 19:07:57 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
RUN apk add --no-cache libssl3 # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Sun, 10 Aug 2025 19:07:57 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
VOLUME [/spiped]
# Sun, 10 Aug 2025 19:07:57 GMT
WORKDIR /spiped
# Sun, 10 Aug 2025 19:07:57 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 10 Aug 2025 19:07:57 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:13c6e95c06ae06f126f5e940d6d88c2fec0da715c80878ad225c76ad48d0a31e`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.6 MB (3618931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:664f8e36f37724daee2260066812a0de8999a28949591daef235c15d49ca301a`  
		Last Modified: Wed, 08 Oct 2025 22:22:15 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ee281d18609c0bc414db88c7d17dd26aca0857610126d3e6d974952f5a414ab`  
		Last Modified: Wed, 08 Oct 2025 22:22:14 GMT  
		Size: 7.9 KB (7947 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20e8cb95edb963d4e91f7f5ea1c0881091c485846b9df554d3c11102b6a6a753`  
		Last Modified: Wed, 08 Oct 2025 22:22:14 GMT  
		Size: 120.1 KB (120110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:473aab810bb857acc1c39fc855966c0a2de5edd8a71287cf2183cea8dc6fdc4b`  
		Last Modified: Wed, 08 Oct 2025 22:22:14 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1968cadac684d87fbcd83e1d646d178ae33c9242a480ddbd04f8fdf77b5e2ed`  
		Last Modified: Wed, 08 Oct 2025 22:22:14 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:2e9fe75d8ecfc557edbdaa8476f159fdb286886f6212788ecb61cda153b3ee2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.4 KB (96433 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e13e74ee61a3719d708f5b8486f092d523816b5c47e960b60b25a5d76b1aaee`

```dockerfile
```

-	Layers:
	-	`sha256:565649aba2f7ebad36d4ce1a64e495876030406355bb0f7a99f41f82b8300791`  
		Last Modified: Thu, 09 Oct 2025 01:04:50 GMT  
		Size: 82.2 KB (82167 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8cf1923abaf687d0c1af4d1718e1e365a3359dbf3e5ff8c339291f60bb0fc220`  
		Last Modified: Thu, 09 Oct 2025 01:04:51 GMT  
		Size: 14.3 KB (14266 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6-alpine` - linux; ppc64le

```console
$ docker pull spiped@sha256:506cee7907557b7efa054dc1a4c3261e8956700c9f553e9eb8d9a3470a368431
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3854263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eca7a1787271596d011a96a2b5632780587dd9653d8b0410f93093e13ecb8fcf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Sun, 10 Aug 2025 19:07:57 GMT
ADD alpine-minirootfs-3.22.2-ppc64le.tar.gz / # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
CMD ["/bin/sh"]
# Sun, 10 Aug 2025 19:07:57 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
RUN apk add --no-cache libssl3 # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Sun, 10 Aug 2025 19:07:57 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
VOLUME [/spiped]
# Sun, 10 Aug 2025 19:07:57 GMT
WORKDIR /spiped
# Sun, 10 Aug 2025 19:07:57 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 10 Aug 2025 19:07:57 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:85a0f69f026b4a01420490809bed190217e05518f7b718c0bbc1ad4871e0dedf`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.7 MB (3732241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26cf524fa67a04db3aef99fc4ab2113633c6c1965d0f890616009377904a6284`  
		Last Modified: Thu, 09 Oct 2025 03:32:10 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecc9d95b7526b98e836dea8e7e9792130d0d6d71b1d6259e6f954ddffc64f5cc`  
		Last Modified: Thu, 09 Oct 2025 03:32:10 GMT  
		Size: 8.0 KB (7955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:011805850ee2924d217a7651762c507b895c90911b4151207fe8e82e4388fcce`  
		Last Modified: Thu, 09 Oct 2025 03:32:10 GMT  
		Size: 112.7 KB (112682 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcef441d2768884d48fcb3b73e59f27e5fe6fc1cb5484df89fd3db0df4ce9437`  
		Last Modified: Thu, 09 Oct 2025 03:32:10 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03005fd392da3ad1cd46c719335ac18f079118e761584617fe8c73405301647d`  
		Last Modified: Thu, 09 Oct 2025 03:32:10 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:55eac1eb38ff8ce12fb98d86fb70542b4620b4c59ff746effba30530ad8676de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.6 KB (94625 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0a3d2f7338bf8715707424b7b716c4498d4c3b844d2dc7387da9a1c64357879`

```dockerfile
```

-	Layers:
	-	`sha256:e3e6cde5a2631b7b9b782bb7fdfcf5de409ca1736416d9573c8888daf799d9e0`  
		Last Modified: Thu, 09 Oct 2025 07:04:30 GMT  
		Size: 80.3 KB (80275 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d9220e8aff0f38f3e237e21c128db8adfad10ae35fb9db4dc56ead1ff1235e9d`  
		Last Modified: Thu, 09 Oct 2025 07:04:31 GMT  
		Size: 14.3 KB (14350 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6-alpine` - linux; riscv64

```console
$ docker pull spiped@sha256:0f378090b0e02992217f4f2a73d59cfb8c76cf62d83fec92991b3a8b1f0bfcc7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3623434 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0a7d261c52ce9f797be48d32c37a2c3f66b54a18d3599dd071fefa04e588df9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Sun, 10 Aug 2025 19:07:57 GMT
ADD alpine-minirootfs-3.22.2-riscv64.tar.gz / # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
CMD ["/bin/sh"]
# Sun, 10 Aug 2025 19:07:57 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
RUN apk add --no-cache libssl3 # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Sun, 10 Aug 2025 19:07:57 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
VOLUME [/spiped]
# Sun, 10 Aug 2025 19:07:57 GMT
WORKDIR /spiped
# Sun, 10 Aug 2025 19:07:57 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 10 Aug 2025 19:07:57 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:139bee3c50b89b56dcbc72522ce83097d9beb59d9d3a5c19072ccd1ad54b11c8`  
		Last Modified: Wed, 08 Oct 2025 21:18:33 GMT  
		Size: 3.5 MB (3515240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3c352072eefdbb94e63d3787f16fac871ba719ed362861b9e97b581edd60548`  
		Last Modified: Fri, 10 Oct 2025 20:50:10 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9aaa05a9bc37f5bb35d75064bac3af035a1d3a82ac079befd8019359672cc322`  
		Last Modified: Fri, 10 Oct 2025 20:50:10 GMT  
		Size: 7.9 KB (7948 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c51a4b112c1b7e8d19565628602648b41c69109d0f16548d16e781b095481e4d`  
		Last Modified: Fri, 10 Oct 2025 20:50:10 GMT  
		Size: 98.9 KB (98862 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9971a3bdcb8df001e3163788a7484aea74c6bf79af7ec5c42ae330638a863112`  
		Last Modified: Fri, 10 Oct 2025 20:50:10 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36e689628a891ec93dec38687edd123814871319bfb552253a1ab8608d94fa74`  
		Last Modified: Fri, 10 Oct 2025 20:50:10 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:ef79fccc5586c74ed7a097a019247ca0f6644364c4e1b931202ce2f00cf4e38a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.6 KB (94617 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3c35fd6859715e249d4b311ca37e3e8e7886a7ce1788f0688877545e1f0fb2b`

```dockerfile
```

-	Layers:
	-	`sha256:624da72bc5bd15d76a69efe794516160d8151dc3f9b207f42a5b8b5165948a76`  
		Last Modified: Fri, 10 Oct 2025 22:04:34 GMT  
		Size: 80.3 KB (80271 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a83fb34ab49138178f6f97cf97ae672fc5e173707dec2895a8d5b36f2e7689a5`  
		Last Modified: Fri, 10 Oct 2025 22:04:35 GMT  
		Size: 14.3 KB (14346 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6-alpine` - linux; s390x

```console
$ docker pull spiped@sha256:be3e9a57eb9caa9fb853c68e3efdc680d9d441f399d676b7a437f56a46d71b59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3755528 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3eee68dd7eaa10392bbfe4c42a39adf582bc976bf97937637b807540ed7960af`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Sun, 10 Aug 2025 19:07:57 GMT
ADD alpine-minirootfs-3.22.2-s390x.tar.gz / # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
CMD ["/bin/sh"]
# Sun, 10 Aug 2025 19:07:57 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
RUN apk add --no-cache libssl3 # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Sun, 10 Aug 2025 19:07:57 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
VOLUME [/spiped]
# Sun, 10 Aug 2025 19:07:57 GMT
WORKDIR /spiped
# Sun, 10 Aug 2025 19:07:57 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 10 Aug 2025 19:07:57 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:e6b06613ca2e7cdf3e8ebbe71ca45137242628a4a3a4bfcb7a9f76d0d5b0e653`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.6 MB (3649244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5eca97998e3d4f083ea39c1b7e9bd8d771aaa888745b8a60d6baff87ab6f8f37`  
		Last Modified: Thu, 09 Oct 2025 02:26:07 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ae19bb237945d6597aced8fc4cd16e5d4f06869978f4f6eb5d90a8bc9be7f39`  
		Last Modified: Thu, 09 Oct 2025 02:26:07 GMT  
		Size: 8.0 KB (7957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ce433dda6c532473e5da602686ec5186ad28c43789f172a14efc1cd9e38093d`  
		Last Modified: Thu, 09 Oct 2025 02:26:07 GMT  
		Size: 96.9 KB (96944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:867b81ca187d86754818499befad84648bb33d900aa6c797f74f14d7f06589dd`  
		Last Modified: Thu, 09 Oct 2025 02:26:06 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de821656be3d9d0eadaa8bfe8c17052ce64308ac54b60bb962a59498810f549e`  
		Last Modified: Thu, 09 Oct 2025 02:26:07 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:daeef3e785369b94f4c3fec6e7b468c0aa8bcc71748eb82a5dcb98744d0c094a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.5 KB (94540 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ff814477e4912c3dbc0dc6c3b2d236588fe065252c86c9a2ed142e200619a8a`

```dockerfile
```

-	Layers:
	-	`sha256:3ccf297cff7eee80cdb3e7128fdeabdb48c58df324a049928273000e72eba72d`  
		Last Modified: Thu, 09 Oct 2025 04:04:35 GMT  
		Size: 80.2 KB (80241 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dcfca2be336420edbf2af734bab83d3864c289d0e61390ac2cfc5f6d7f183847`  
		Last Modified: Thu, 09 Oct 2025 04:04:36 GMT  
		Size: 14.3 KB (14299 bytes)  
		MIME: application/vnd.in-toto+json

## `spiped:1.6.4`

```console
$ docker pull spiped@sha256:ae34dc5e1e750a9577c6c31b1bd458e953940df360d2129dcc6ab9ec76b97634
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
$ docker pull spiped@sha256:82a44171c51ca620ba3c3c03a99b52f52529674ec87bde43e9926f1d6ec0e009
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.8 MB (36828656 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe7422969ceb15f34c8bfad19efc9932626d64801cea01ac7adb6b48c80d31f5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 04:13:26 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Tue, 04 Nov 2025 04:13:28 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 04:13:49 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Tue, 04 Nov 2025 04:13:49 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 04 Nov 2025 04:13:49 GMT
VOLUME [/spiped]
# Tue, 04 Nov 2025 04:13:49 GMT
WORKDIR /spiped
# Tue, 04 Nov 2025 04:13:49 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 04:13:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Nov 2025 04:13:49 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:d7ecded7702a5dbf6d0f79a71edc34b534d08f3051980e2c948fba72db3197fc`  
		Last Modified: Tue, 04 Nov 2025 00:13:18 GMT  
		Size: 29.8 MB (29778104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04af94b2f2784b050748c0bc593d7625ed57d5cba186a5f086621574d0db770a`  
		Last Modified: Tue, 04 Nov 2025 04:14:00 GMT  
		Size: 1.1 KB (1105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:552c1418ed5f113e9eef0fa6687c45ff9cbffe5c42b756a669850fc73f345825`  
		Last Modified: Tue, 04 Nov 2025 04:14:00 GMT  
		Size: 826.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0261a8f67e930dd0ddf4233075edba351756a7d795a0e69a5855cb123372ba2`  
		Last Modified: Tue, 04 Nov 2025 04:14:02 GMT  
		Size: 7.0 MB (7048187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5ca2f62567ececa23586d454805f1453bfb20590012b083407cd012ee296eea`  
		Last Modified: Tue, 04 Nov 2025 04:14:00 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84431171e7f009a7782b98db778ea5e41991d25b73524432b73c55af5a67e4bf`  
		Last Modified: Tue, 04 Nov 2025 04:14:00 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6.4` - unknown; unknown

```console
$ docker pull spiped@sha256:fdc238e5b3be11018da12f326e986158a996ba0040c07e562493af76e56d252a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3641114 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6cee0fd107c9ef0ff2a206950205e6a145e94034a05e40a81d97bf9680015577`

```dockerfile
```

-	Layers:
	-	`sha256:e9a375eaa0ee407c9bf820a27a60ebfae8e1b0eca680a00e28bb2c1fe201e7dc`  
		Last Modified: Tue, 04 Nov 2025 14:04:42 GMT  
		Size: 3.6 MB (3626132 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:090acc34f1d66361f6d8fddabbc50d86e8f70632cdc1320e68686e3b27c23564`  
		Last Modified: Tue, 04 Nov 2025 14:04:43 GMT  
		Size: 15.0 KB (14982 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6.4` - linux; arm variant v5

```console
$ docker pull spiped@sha256:01018b8cd02af89ba30ae1bcf4e97855ab3bdf892659021c68cd6db582a4e82f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.7 MB (33738270 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8470079cfa5129c79d5f858dfab379f480768bc25217b8e0b6729b827bda73d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 01:26:44 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Tue, 04 Nov 2025 01:26:48 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 01:27:14 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Tue, 04 Nov 2025 01:27:14 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 04 Nov 2025 01:27:14 GMT
VOLUME [/spiped]
# Tue, 04 Nov 2025 01:27:14 GMT
WORKDIR /spiped
# Tue, 04 Nov 2025 01:27:15 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 01:27:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Nov 2025 01:27:15 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:453afc2258d7bc5729fed5672fb95bafa092e30a933b4377a12034be940a671b`  
		Last Modified: Tue, 04 Nov 2025 00:13:12 GMT  
		Size: 27.9 MB (27946438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca47efc60e8d395bb20127ab62f55376f6526f660fda2af48f332ab55a5db1de`  
		Last Modified: Tue, 04 Nov 2025 01:27:29 GMT  
		Size: 1.1 KB (1105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3087d5dadbd1a81bf4a6a89b5c5513e92c5267b062a5ad88f3714f4af65944f9`  
		Last Modified: Tue, 04 Nov 2025 01:27:29 GMT  
		Size: 830.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7844d897fb72d98b6d97c02c9aea425f239371a0383c9ddb897005ce9e32d8d`  
		Last Modified: Tue, 04 Nov 2025 01:27:31 GMT  
		Size: 5.8 MB (5789464 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bb6f08fbffea41432c882d7ca57574ca10f090cfc124102a57937cb13a1e8e4`  
		Last Modified: Tue, 04 Nov 2025 01:27:29 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd566239a0cc0043085f6f763357bcb82782f07ebf8d6d1cb77a81683614a813`  
		Last Modified: Tue, 04 Nov 2025 01:27:29 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6.4` - unknown; unknown

```console
$ docker pull spiped@sha256:acf598dd339fcabaa30ebe44d7595caa9299c0471756c6d4f51989a8e0ef9ca6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3634214 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d932b1acba0130144dcf23c7d242737a06b9e4ef9c5c435a2ed7d54042d30ec6`

```dockerfile
```

-	Layers:
	-	`sha256:e00221651b0ba4a1e38bf876ba3fba3f946d133c72200f5bab9b64d3e969ee42`  
		Last Modified: Tue, 04 Nov 2025 08:04:27 GMT  
		Size: 3.6 MB (3619126 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:59b7876f9d30572585cdd8c35b384ebd24d330f12217040dbea5e8cbd219456a`  
		Last Modified: Tue, 04 Nov 2025 08:04:28 GMT  
		Size: 15.1 KB (15088 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6.4` - linux; arm variant v7

```console
$ docker pull spiped@sha256:14c077460233a0891c8d77cba716c235993ec3531bc03dea2f45959b3387e049
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.8 MB (31800147 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12694eea0cdf2315ba4c0c3242b4e3501a38116b638d7239c5a46b6f6d61eef1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 02:17:27 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Tue, 04 Nov 2025 02:17:30 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 02:17:53 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Tue, 04 Nov 2025 02:17:53 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 04 Nov 2025 02:17:53 GMT
VOLUME [/spiped]
# Tue, 04 Nov 2025 02:17:53 GMT
WORKDIR /spiped
# Tue, 04 Nov 2025 02:17:53 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 02:17:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Nov 2025 02:17:53 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:8945aefb71bd942499dd072e2c7c869b6b74b7c4dd83bff59c209b7b95d52a9f`  
		Last Modified: Tue, 04 Nov 2025 00:13:33 GMT  
		Size: 26.2 MB (26213039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fda5ed53e0dbde40dfe076db326ecd295b0b1c6d680116701507afe281baba2f`  
		Last Modified: Tue, 04 Nov 2025 02:18:05 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97b35d897f0e9c8d74564913d30c18612c62876f021e52e682bccb7ca7aa7122`  
		Last Modified: Tue, 04 Nov 2025 02:18:05 GMT  
		Size: 824.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:880acbf14d869df07dc547c6546ace74066ceb671ee539f84c04b7aa6bd93d88`  
		Last Modified: Tue, 04 Nov 2025 02:18:06 GMT  
		Size: 5.6 MB (5584740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83ad84946a9a60a387ca7f2d49194aa08d4a4b00b6921b734ddd91ea47ec12fc`  
		Last Modified: Tue, 04 Nov 2025 02:18:05 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31948a9a6bd812479abcecaee071ca0adfc7ccb05075344aacb05afdde76c955`  
		Last Modified: Tue, 04 Nov 2025 02:18:05 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6.4` - unknown; unknown

```console
$ docker pull spiped@sha256:26e3b4b9812bd059487e9655a891858c085e662a2f0f9a3f0b298c3dfee41536
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3633335 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc044a3ebcd39fe3f2be39febd09774d0d90a07c0b0d2bd5c34d4ecb7efd8dbb`

```dockerfile
```

-	Layers:
	-	`sha256:15aab9c35b9929d5dd1efe22911175934126591da412018cbbfcf9cd3b909b71`  
		Last Modified: Tue, 04 Nov 2025 14:04:50 GMT  
		Size: 3.6 MB (3618247 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8c0fd76702563c822a41fb5417ecf0e5cc689f14a75561c58d94a7e9235c9058`  
		Last Modified: Tue, 04 Nov 2025 14:04:50 GMT  
		Size: 15.1 KB (15088 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6.4` - linux; arm64 variant v8

```console
$ docker pull spiped@sha256:b6b4508fea00b81da1ef86c3545f0570316acafb1741295cd5cb81b44d57983f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.4 MB (36376612 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b7e2bcd7f2a9a352a7c82c13dfc51a9cd1fb8b6951ecbebbd5caff5dba84b44`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 01:28:45 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Tue, 04 Nov 2025 01:28:48 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 01:29:10 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Tue, 04 Nov 2025 01:29:10 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 04 Nov 2025 01:29:10 GMT
VOLUME [/spiped]
# Tue, 04 Nov 2025 01:29:10 GMT
WORKDIR /spiped
# Tue, 04 Nov 2025 01:29:10 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 01:29:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Nov 2025 01:29:10 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:51365f04b68881c6fd3d04aa38cdb689fdee6efba2aa6afcf2da5385022cf475`  
		Last Modified: Tue, 04 Nov 2025 00:13:42 GMT  
		Size: 30.1 MB (30142298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da995b7386a81488a789551cb249fe6fea42d70c39ab8a87d627d805e7e0702f`  
		Last Modified: Tue, 04 Nov 2025 01:29:26 GMT  
		Size: 1.1 KB (1105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d22fea0cfbe83fade9a6807335d9620c018e1f013f30933686d89653b8f3751b`  
		Last Modified: Tue, 04 Nov 2025 01:29:26 GMT  
		Size: 827.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85524e1a2d9a76551e1de84299ffdf92ddd97e9d6f422b3e562dbc1a6ba6a50b`  
		Last Modified: Tue, 04 Nov 2025 01:29:27 GMT  
		Size: 6.2 MB (6231948 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c76200e3164e6d69e66e2534b38d35f0e16b4f2d64f70afd08c8457d373b835`  
		Last Modified: Tue, 04 Nov 2025 01:29:26 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c14c920bf38ff2c704eacb362443942ea2718f868f01e144eb2e3e04d96e2564`  
		Last Modified: Tue, 04 Nov 2025 01:29:26 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6.4` - unknown; unknown

```console
$ docker pull spiped@sha256:c779c8aee90a56c7378621b7fe346c3139be38eec6de2fa672f998c9fc4986de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3636284 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:555a5ae0e19d04ef7e45c6eec70472e7764fb60499c0675e4a6594e2241883b8`

```dockerfile
```

-	Layers:
	-	`sha256:8e1c42f1f18a6f283c053696b1e4ab1e61f688cebf405ec7e2eaa94d839d7fa0`  
		Last Modified: Tue, 04 Nov 2025 14:04:56 GMT  
		Size: 3.6 MB (3621168 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ff05626a27a8aaec468faef774708e79fad5edfdcfda16285d43c34ef591b620`  
		Last Modified: Tue, 04 Nov 2025 14:04:56 GMT  
		Size: 15.1 KB (15116 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6.4` - linux; 386

```console
$ docker pull spiped@sha256:a4b5da618ef9092d51d4526190bc5e118e9185b168ead3df69d42dff523191d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.7 MB (37739460 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04609af68ede4d313e06c3fabb8ba8d0a59f1b79b795df1e2cbe9a50cb5c0472`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 01:30:27 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Tue, 04 Nov 2025 01:30:30 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 01:30:55 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Tue, 04 Nov 2025 01:30:55 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 04 Nov 2025 01:30:55 GMT
VOLUME [/spiped]
# Tue, 04 Nov 2025 01:30:55 GMT
WORKDIR /spiped
# Tue, 04 Nov 2025 01:30:55 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 01:30:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Nov 2025 01:30:55 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:7f24a3a0c200106d0d9ab7b6264e50c689910154fb57bf08185b9eaf995db758`  
		Last Modified: Tue, 04 Nov 2025 00:13:54 GMT  
		Size: 31.3 MB (31294783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65859e510c2db85116bdd72bf3d9c7db20eb3aa26d9b1de16d5d468fac6e12b4`  
		Last Modified: Tue, 04 Nov 2025 01:31:07 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17425f70fc6396f91fe03abde4d6c062f561878471403b5e797512c012d0b58f`  
		Last Modified: Tue, 04 Nov 2025 01:31:08 GMT  
		Size: 826.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e92634046b1716dd52c3215f95a28867b3e64b689a52a66bc446570f7d3f915b`  
		Last Modified: Tue, 04 Nov 2025 01:31:08 GMT  
		Size: 6.4 MB (6442311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:082304266fac4680b67029584f056ab407e955eaaa5694d05580c08568183ba2`  
		Last Modified: Tue, 04 Nov 2025 01:31:08 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3f65e39b75028e66f2635520d73e70b21bb85c3574637ef9339d98b08cce418`  
		Last Modified: Tue, 04 Nov 2025 01:31:07 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6.4` - unknown; unknown

```console
$ docker pull spiped@sha256:8dfb3738f33f7909eb57ce11e1d4c3b9621b9bc19194c790528a58c917672527
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3635206 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ddfcb2680869fc3ee15b86cc93cba15353c8e2748cada861d826a1365663d62`

```dockerfile
```

-	Layers:
	-	`sha256:951cba86bfe9e094394aed88e6e4907c73131f7aa00df1f74494c86bc03df98e`  
		Last Modified: Tue, 04 Nov 2025 14:05:00 GMT  
		Size: 3.6 MB (3620261 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3b0ff7f7bd86aaafaa07c69914072c6f5ef7f94c5bb130d61e695b5f7cbb7461`  
		Last Modified: Tue, 04 Nov 2025 14:05:01 GMT  
		Size: 14.9 KB (14945 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6.4` - linux; ppc64le

```console
$ docker pull spiped@sha256:17a9f9c03a0c9c0b4845e576b4d50b32791c874660333d35e2f7713b5a4f9a54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.4 MB (40441436 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49d997c535004cfabfeb64a604cfa65a56f97d30072ca33d0813aad07018c58b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 06:08:31 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Tue, 04 Nov 2025 06:08:36 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 06:09:27 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Tue, 04 Nov 2025 06:09:27 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 04 Nov 2025 06:09:27 GMT
VOLUME [/spiped]
# Tue, 04 Nov 2025 06:09:27 GMT
WORKDIR /spiped
# Tue, 04 Nov 2025 06:09:28 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 06:09:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Nov 2025 06:09:28 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:eead2c4a2afd8217def9d0ca536e7e4108ac8a91745ca25e76eb059260c04aab`  
		Last Modified: Tue, 04 Nov 2025 00:20:53 GMT  
		Size: 33.6 MB (33598647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b2092794106fcd3e23337b489859b3eb0854104e16e57e5ec14f218338644be`  
		Last Modified: Tue, 04 Nov 2025 06:09:52 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca2ca52ff15c8f4ff8cb61e6ad4215e2632257624c0c417e70e3c3f6d7f234bb`  
		Last Modified: Tue, 04 Nov 2025 06:09:52 GMT  
		Size: 827.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5983f80493ffaac3089e1f7f8864ab8cc80507a20bbedfa2c3e2923e65b2c538`  
		Last Modified: Tue, 04 Nov 2025 06:09:52 GMT  
		Size: 6.8 MB (6840421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea2839f6c480bb68bf8aaeba58db823e5327791e68b29e0834b52e7458e069e5`  
		Last Modified: Tue, 04 Nov 2025 06:09:52 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e3df6a56753bd17d0ca244a384c7110325691bdb7f9bed0ef49ad1f9e29a8a4`  
		Last Modified: Tue, 04 Nov 2025 06:09:52 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6.4` - unknown; unknown

```console
$ docker pull spiped@sha256:b41008bcde4956aec3ad1ac3162aa82ac36e06cc052ee46b38c5de8e30d22b8c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3636899 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6faf5bf37b372ec100c4d596f350cf4eb6c850aebed6f26691d621fd6238977b`

```dockerfile
```

-	Layers:
	-	`sha256:9ea9bb8d6fdd4f34069789821b02e82da1ebf377c37ac65a8626ff7aafd83f54`  
		Last Modified: Tue, 04 Nov 2025 14:05:06 GMT  
		Size: 3.6 MB (3621869 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c37176c69bb122c01a898f0893b93e72adf3525b0accf60ac377a130c269a2d8`  
		Last Modified: Tue, 04 Nov 2025 14:05:07 GMT  
		Size: 15.0 KB (15030 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6.4` - linux; riscv64

```console
$ docker pull spiped@sha256:7004f59a14e65493d89d02012617e4685f705f645959559227290584c7da32b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.6 MB (37636275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57db3066c8da0560c596ad9830d9e9d916c732311869e057ec28751c6c95ea6e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Fri, 29 Aug 2025 17:20:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1760918400'
# Fri, 29 Aug 2025 17:20:00 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Fri, 29 Aug 2025 17:20:00 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 29 Aug 2025 17:20:00 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Fri, 29 Aug 2025 17:20:00 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Fri, 29 Aug 2025 17:20:00 GMT
VOLUME [/spiped]
# Fri, 29 Aug 2025 17:20:00 GMT
WORKDIR /spiped
# Fri, 29 Aug 2025 17:20:00 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Fri, 29 Aug 2025 17:20:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 29 Aug 2025 17:20:00 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:6d1567708d42906165204f9177d357cb6a2fd51f758da447f1743b00813f892f`  
		Last Modified: Tue, 21 Oct 2025 00:37:37 GMT  
		Size: 28.3 MB (28275650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d2eca7a0881779ed75b9a6df9e9c73f4e30a2545b324835ded643360d27d8cc`  
		Last Modified: Wed, 22 Oct 2025 17:58:55 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:189f2808be96be6277f0f38d8010c29a85c6383d14b6f87ab8b25267c049edb2`  
		Last Modified: Wed, 22 Oct 2025 17:58:55 GMT  
		Size: 823.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63ffa6796bebebbe0e033f44c2862905348b86b654f6796e30afac6e530d4277`  
		Last Modified: Wed, 22 Oct 2025 17:58:57 GMT  
		Size: 9.4 MB (9358258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fa6357568a94aa6f06730895e5dae1afb3df5610b097001d226a3f77165e34f`  
		Last Modified: Wed, 22 Oct 2025 17:58:55 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94b644b84d3f1a2b591c927fa6de5e0189e84eefcff0f41ec2a3f44187185c0d`  
		Last Modified: Wed, 22 Oct 2025 17:58:55 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6.4` - unknown; unknown

```console
$ docker pull spiped@sha256:5c5c3dac2a6b922d04f583d01b94567b074f27f995ce52ec74839d9912349909
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3628348 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a636dc3ff00c7130929694628709b79af7b1fee5b8a10375831363195b017596`

```dockerfile
```

-	Layers:
	-	`sha256:06533fa6c4fa5d87ac9aa9b94a962ef7605ef017f0c5582d776f1d8052627da7`  
		Last Modified: Wed, 22 Oct 2025 19:04:39 GMT  
		Size: 3.6 MB (3613275 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:83d421894b349a0bc498ac33059bfe41875507a74674a4b14aefd8a88b3e1a41`  
		Last Modified: Wed, 22 Oct 2025 19:04:40 GMT  
		Size: 15.1 KB (15073 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6.4` - linux; s390x

```console
$ docker pull spiped@sha256:0baf3a2f09f03f86b756f3144062ee4da868d648b33a12e0d36b82135d15915b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.0 MB (35961254 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e5f3f6eecc940670d5374d68bf8dfcde4b58c041506361c10c8a41c45108a1a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 09:44:46 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Tue, 04 Nov 2025 09:44:49 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 09:45:08 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Tue, 04 Nov 2025 09:45:08 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 04 Nov 2025 09:45:08 GMT
VOLUME [/spiped]
# Tue, 04 Nov 2025 09:45:08 GMT
WORKDIR /spiped
# Tue, 04 Nov 2025 09:45:09 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 09:45:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Nov 2025 09:45:09 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:ad0bc025a1766baba34dfa4dbb5713703de6595994d855ebf4689c0b161314ee`  
		Last Modified: Tue, 04 Nov 2025 00:20:17 GMT  
		Size: 29.8 MB (29837392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:413a343213dc776ef8ec8258f5d795654681dedb3c922a2300eb7ef7d73550e3`  
		Last Modified: Tue, 04 Nov 2025 09:45:31 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35418050ccaf1bb39b9fe282dc51e265bfb9549bbc54b3a04420b3009a5b9dc7`  
		Last Modified: Tue, 04 Nov 2025 09:45:30 GMT  
		Size: 826.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21ed93eeb8c99a4ac37aba7742f9400f88c3edb4f731713a63588cbff687b5a1`  
		Last Modified: Tue, 04 Nov 2025 09:45:31 GMT  
		Size: 6.1 MB (6121493 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:093c2dfb578dd5e22bde915b7aaf0b7a8664c98c82ec4e775d9cf87a8a39c074`  
		Last Modified: Tue, 04 Nov 2025 09:45:30 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5474616e30d2720bab7073b5cb8772b655fb03da212f01a6946c7777f26eda9`  
		Last Modified: Tue, 04 Nov 2025 09:45:30 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6.4` - unknown; unknown

```console
$ docker pull spiped@sha256:5ba27c04f04976a68826dba21d4d8065792b743fcdb70d57dec54f77b64c21c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3633475 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1ca1463694fb2e285ab976f084b9ac52e5c81410f43af1e039c67fb30e09338`

```dockerfile
```

-	Layers:
	-	`sha256:7e8ab82c8e759285edf28b13b88413a10ae662563b6de418f33f06c7c0bde122`  
		Last Modified: Tue, 04 Nov 2025 14:05:15 GMT  
		Size: 3.6 MB (3618495 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5a721785c314ac76a8f08022c6725ff60002127c2e5716b46279b371abd12af0`  
		Last Modified: Tue, 04 Nov 2025 14:05:16 GMT  
		Size: 15.0 KB (14980 bytes)  
		MIME: application/vnd.in-toto+json

## `spiped:1.6.4-alpine`

```console
$ docker pull spiped@sha256:7b9625a81e8db9045c4eaf8f9bf40b8ef8c78a666bb7201d8d7c80538a418f7a
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
$ docker pull spiped@sha256:7d011e9e579768cd749e2df95806a3b739ebbdd516385dac92f2e9cda3570e25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3919429 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc9d66303cac034d8960b8128b5967170028d350ecf6e131c4bf30b000a3f836`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Sun, 10 Aug 2025 19:07:57 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
CMD ["/bin/sh"]
# Sun, 10 Aug 2025 19:07:57 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
RUN apk add --no-cache libssl3 # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Sun, 10 Aug 2025 19:07:57 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
VOLUME [/spiped]
# Sun, 10 Aug 2025 19:07:57 GMT
WORKDIR /spiped
# Sun, 10 Aug 2025 19:07:57 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 10 Aug 2025 19:07:57 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7c041bc04e274276fc6a842ca20a0cf973af7c178bcfb6575c0d8203718fc91`  
		Last Modified: Wed, 08 Oct 2025 22:58:11 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f81b6f5c689713065e6b968619711a3bd698fd708594cc90dae3977d54ca24e`  
		Last Modified: Wed, 08 Oct 2025 22:58:11 GMT  
		Size: 8.0 KB (7950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a035501670b01c25e6d7ce231bae87ef493bb668e877be52618f03679b673c4f`  
		Last Modified: Wed, 08 Oct 2025 22:58:11 GMT  
		Size: 107.6 KB (107645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57f81362a47a6b65eaf0da33a0c61df7c9a874d76861e5ae8fa0bc16547593db`  
		Last Modified: Wed, 08 Oct 2025 22:58:12 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48ae81c7faaf7b0d0454b9d217085e8da2f5e5a72ead2527e67506b0d4834801`  
		Last Modified: Wed, 08 Oct 2025 22:58:11 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6.4-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:ed8b2f715fbc09ab5fcc75433e022573fd8e46bded0d7dd791180a01b3d4a8dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.5 KB (96494 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b323748eb9cefd40fcfe67d6c7dd561a4f5c4498457b7739b98161ea53a531c`

```dockerfile
```

-	Layers:
	-	`sha256:64366b1f73c30d49b216afd6a2acb0a27ad6d69bbaf554934ef1fb5a1b8ae379`  
		Last Modified: Thu, 09 Oct 2025 01:04:34 GMT  
		Size: 82.2 KB (82192 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d77f4db066b7ca49f19231acfa8a9f30749e3884bc787f4fcb01d3cb8a54b848`  
		Last Modified: Thu, 09 Oct 2025 01:04:35 GMT  
		Size: 14.3 KB (14302 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6.4-alpine` - linux; arm variant v6

```console
$ docker pull spiped@sha256:07f6c1ec4d9a40087ba1fabf98ca259b39af58fe0aa3d1b5aff7a5c9c85aab9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3602562 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66830d62439293e746c3d4171b26eb7b060853f622562e26647e13254243d153`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Sun, 10 Aug 2025 19:07:57 GMT
ADD alpine-minirootfs-3.22.2-armhf.tar.gz / # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
CMD ["/bin/sh"]
# Sun, 10 Aug 2025 19:07:57 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
RUN apk add --no-cache libssl3 # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Sun, 10 Aug 2025 19:07:57 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
VOLUME [/spiped]
# Sun, 10 Aug 2025 19:07:57 GMT
WORKDIR /spiped
# Sun, 10 Aug 2025 19:07:57 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 10 Aug 2025 19:07:57 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:bb1da3d879939be7df9f182950d2fb201d4fc2e1043677da2037cd6afb084ce0`  
		Last Modified: Wed, 08 Oct 2025 21:00:16 GMT  
		Size: 3.5 MB (3504080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:153e87cee3c8273a66e75e0a084e6876c74329042a77778cc75c7865eafb5817`  
		Last Modified: Wed, 08 Oct 2025 22:09:30 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e054efed96e629a0c9a72dadd2a8d348aa66730afa5f59ce6e02a530b64b8d73`  
		Last Modified: Wed, 08 Oct 2025 22:09:30 GMT  
		Size: 7.9 KB (7943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17dbbcac13a86093cd5821deda5686d525abf33f1ffacea149ae0a0b642a332f`  
		Last Modified: Wed, 08 Oct 2025 22:09:30 GMT  
		Size: 89.2 KB (89158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6448f1d44fa11364cf66800119dd7e5e05fc9b9d8384cce8cc858006c0684aae`  
		Last Modified: Wed, 08 Oct 2025 22:09:30 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8fa931b05c23aa0b5927c5fc4bea0d9aa65908b7ac3e936a5a5888060a49337`  
		Last Modified: Wed, 08 Oct 2025 22:09:30 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6.4-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:e083a00e19dd556e9a671f1709ffc708a0ab8d2a7373856218a44de2df24d462
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.2 KB (14190 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b47da3cb18e03a2142fd48220b0903336c0d8a799d804ac3b38780211559ba36`

```dockerfile
```

-	Layers:
	-	`sha256:069680ffcf03350d43ef8d45bcb21dafd37c1132acdfce2d83391a239a85d47e`  
		Last Modified: Thu, 09 Oct 2025 01:04:38 GMT  
		Size: 14.2 KB (14190 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6.4-alpine` - linux; arm variant v7

```console
$ docker pull spiped@sha256:742d7ee47c94e03887525e682c2614d90b9b1f43f674ce4407bcf06b787caa29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3312569 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6db7cd0fffd0a4f2c540dfe37e4c940cf5c7595aeffea1bf7acc4b1793c73d9a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Sun, 10 Aug 2025 19:07:57 GMT
ADD alpine-minirootfs-3.22.2-armv7.tar.gz / # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
CMD ["/bin/sh"]
# Sun, 10 Aug 2025 19:07:57 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
RUN apk add --no-cache libssl3 # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Sun, 10 Aug 2025 19:07:57 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
VOLUME [/spiped]
# Sun, 10 Aug 2025 19:07:57 GMT
WORKDIR /spiped
# Sun, 10 Aug 2025 19:07:57 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 10 Aug 2025 19:07:57 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:2763c7fc79b66030222442365f4a0f69d9dbaa11f7fd47a918d29d732d52996c`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.2 MB (3221555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6a85ed9579bf45ac1db2ef56f4067b84fe0c4d8e51e006ec1d925eb0c32bf22`  
		Last Modified: Wed, 08 Oct 2025 22:10:17 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a85621545c13dee2ff1d8660f7847266105703d040c19d1816e374881a3bdf6e`  
		Last Modified: Wed, 08 Oct 2025 22:10:17 GMT  
		Size: 7.9 KB (7944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8afad049c072c9b6d3ed2946f7d0c0782835979f90696b68ac6e4c0efff5bf4`  
		Last Modified: Wed, 08 Oct 2025 22:10:17 GMT  
		Size: 81.7 KB (81688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35464221f20a70de628e3018e70c13c2e8ed9970a791049f1ba3bae429355536`  
		Last Modified: Wed, 08 Oct 2025 22:10:17 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39d6fea506e0050596918141446ad53da32b5b3a4fc9c7a5d497caf9a7ec6390`  
		Last Modified: Wed, 08 Oct 2025 22:10:18 GMT  
		Size: 336.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6.4-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:1db53d701cc5320b98ed95f8e8288e9c84ddb8ad31b517b42fe2faa626874b44
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.6 KB (96633 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f53816c0890232fc85b4017c83eabcfb11884aeab001b608b66e2a8c9e183e3`

```dockerfile
```

-	Layers:
	-	`sha256:f33fdb1fd07f91c527d8c950dcb81f1eea51882f51d66c0f4da88547240c6499`  
		Last Modified: Thu, 09 Oct 2025 01:04:42 GMT  
		Size: 82.2 KB (82228 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:20a9fe69db1d74bfbe4aa6a07c0fb4e0e59f4eff9e1636b7e0c486b6435b788b`  
		Last Modified: Thu, 09 Oct 2025 01:04:42 GMT  
		Size: 14.4 KB (14405 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6.4-alpine` - linux; arm64 variant v8

```console
$ docker pull spiped@sha256:1c2f38931ee0ff681a7c140bbc874fa1ff5837de4baf9a50a3498fbcb12a9668
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4248020 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26b0a53163c15fa0112f2865ee8a52cbed044f04fc7001f7bd1f5e407cd57237`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Sun, 10 Aug 2025 19:07:57 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
CMD ["/bin/sh"]
# Sun, 10 Aug 2025 19:07:57 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
RUN apk add --no-cache libssl3 # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Sun, 10 Aug 2025 19:07:57 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
VOLUME [/spiped]
# Sun, 10 Aug 2025 19:07:57 GMT
WORKDIR /spiped
# Sun, 10 Aug 2025 19:07:57 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 10 Aug 2025 19:07:57 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94547f3886a10ef8162a5d7fe9f4308e302dcfd48f5be2db3b1e5d4b5156d815`  
		Last Modified: Wed, 08 Oct 2025 22:29:31 GMT  
		Size: 949.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00ee5fd6e341869b5bcb70e517a1466b54c5191790816dd7956a41164690328b`  
		Last Modified: Wed, 08 Oct 2025 22:29:32 GMT  
		Size: 7.9 KB (7949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bba2ed7625e00fce702c1adbf90233532e0e4e98935a777f6bdffa076b1c3be2`  
		Last Modified: Wed, 08 Oct 2025 22:29:31 GMT  
		Size: 100.6 KB (100621 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1612c8ef14c84a7450d3ced7f152a93e533ffbb92d525fae7dde4c2988e230d7`  
		Last Modified: Wed, 08 Oct 2025 22:29:32 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:433ac69ec6618a756cde4ab30a4488c3f0f7b89df240ede5a7b0a29d66250444`  
		Last Modified: Wed, 08 Oct 2025 22:29:31 GMT  
		Size: 336.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6.4-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:f599a056737cf26e2f1e5bfb25bf8cf6f92cea0ea27b040de42b2e4bf139168f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.7 KB (96684 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad1c665f9e5776de9d503dbefb3dccddb1d230d81716f5b086b02065d6f512d0`

```dockerfile
```

-	Layers:
	-	`sha256:8c6690f0ed02188be28287964aecbd171476e7e9484ec40d030c20c7b0e182c3`  
		Last Modified: Thu, 09 Oct 2025 01:04:46 GMT  
		Size: 82.2 KB (82248 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dde4ac6f12c825868630b75c268c91338db29a424c87e551c1153694da325c83`  
		Last Modified: Thu, 09 Oct 2025 01:04:46 GMT  
		Size: 14.4 KB (14436 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6.4-alpine` - linux; 386

```console
$ docker pull spiped@sha256:ac72ab4f716c2dabdad650618a34deccd477e31f604bf27a1f630a7a8433d994
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3748370 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf996beac99b6a5d8eae08ab4703a9cc11bccf3cb429e61a25bebf2947e4b519`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Sun, 10 Aug 2025 19:07:57 GMT
ADD alpine-minirootfs-3.22.2-x86.tar.gz / # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
CMD ["/bin/sh"]
# Sun, 10 Aug 2025 19:07:57 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
RUN apk add --no-cache libssl3 # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Sun, 10 Aug 2025 19:07:57 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
VOLUME [/spiped]
# Sun, 10 Aug 2025 19:07:57 GMT
WORKDIR /spiped
# Sun, 10 Aug 2025 19:07:57 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 10 Aug 2025 19:07:57 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:13c6e95c06ae06f126f5e940d6d88c2fec0da715c80878ad225c76ad48d0a31e`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.6 MB (3618931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:664f8e36f37724daee2260066812a0de8999a28949591daef235c15d49ca301a`  
		Last Modified: Wed, 08 Oct 2025 22:22:15 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ee281d18609c0bc414db88c7d17dd26aca0857610126d3e6d974952f5a414ab`  
		Last Modified: Wed, 08 Oct 2025 22:22:14 GMT  
		Size: 7.9 KB (7947 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20e8cb95edb963d4e91f7f5ea1c0881091c485846b9df554d3c11102b6a6a753`  
		Last Modified: Wed, 08 Oct 2025 22:22:14 GMT  
		Size: 120.1 KB (120110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:473aab810bb857acc1c39fc855966c0a2de5edd8a71287cf2183cea8dc6fdc4b`  
		Last Modified: Wed, 08 Oct 2025 22:22:14 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1968cadac684d87fbcd83e1d646d178ae33c9242a480ddbd04f8fdf77b5e2ed`  
		Last Modified: Wed, 08 Oct 2025 22:22:14 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6.4-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:2e9fe75d8ecfc557edbdaa8476f159fdb286886f6212788ecb61cda153b3ee2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.4 KB (96433 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e13e74ee61a3719d708f5b8486f092d523816b5c47e960b60b25a5d76b1aaee`

```dockerfile
```

-	Layers:
	-	`sha256:565649aba2f7ebad36d4ce1a64e495876030406355bb0f7a99f41f82b8300791`  
		Last Modified: Thu, 09 Oct 2025 01:04:50 GMT  
		Size: 82.2 KB (82167 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8cf1923abaf687d0c1af4d1718e1e365a3359dbf3e5ff8c339291f60bb0fc220`  
		Last Modified: Thu, 09 Oct 2025 01:04:51 GMT  
		Size: 14.3 KB (14266 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6.4-alpine` - linux; ppc64le

```console
$ docker pull spiped@sha256:506cee7907557b7efa054dc1a4c3261e8956700c9f553e9eb8d9a3470a368431
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3854263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eca7a1787271596d011a96a2b5632780587dd9653d8b0410f93093e13ecb8fcf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Sun, 10 Aug 2025 19:07:57 GMT
ADD alpine-minirootfs-3.22.2-ppc64le.tar.gz / # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
CMD ["/bin/sh"]
# Sun, 10 Aug 2025 19:07:57 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
RUN apk add --no-cache libssl3 # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Sun, 10 Aug 2025 19:07:57 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
VOLUME [/spiped]
# Sun, 10 Aug 2025 19:07:57 GMT
WORKDIR /spiped
# Sun, 10 Aug 2025 19:07:57 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 10 Aug 2025 19:07:57 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:85a0f69f026b4a01420490809bed190217e05518f7b718c0bbc1ad4871e0dedf`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.7 MB (3732241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26cf524fa67a04db3aef99fc4ab2113633c6c1965d0f890616009377904a6284`  
		Last Modified: Thu, 09 Oct 2025 03:32:10 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecc9d95b7526b98e836dea8e7e9792130d0d6d71b1d6259e6f954ddffc64f5cc`  
		Last Modified: Thu, 09 Oct 2025 03:32:10 GMT  
		Size: 8.0 KB (7955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:011805850ee2924d217a7651762c507b895c90911b4151207fe8e82e4388fcce`  
		Last Modified: Thu, 09 Oct 2025 03:32:10 GMT  
		Size: 112.7 KB (112682 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcef441d2768884d48fcb3b73e59f27e5fe6fc1cb5484df89fd3db0df4ce9437`  
		Last Modified: Thu, 09 Oct 2025 03:32:10 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03005fd392da3ad1cd46c719335ac18f079118e761584617fe8c73405301647d`  
		Last Modified: Thu, 09 Oct 2025 03:32:10 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6.4-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:55eac1eb38ff8ce12fb98d86fb70542b4620b4c59ff746effba30530ad8676de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.6 KB (94625 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0a3d2f7338bf8715707424b7b716c4498d4c3b844d2dc7387da9a1c64357879`

```dockerfile
```

-	Layers:
	-	`sha256:e3e6cde5a2631b7b9b782bb7fdfcf5de409ca1736416d9573c8888daf799d9e0`  
		Last Modified: Thu, 09 Oct 2025 07:04:30 GMT  
		Size: 80.3 KB (80275 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d9220e8aff0f38f3e237e21c128db8adfad10ae35fb9db4dc56ead1ff1235e9d`  
		Last Modified: Thu, 09 Oct 2025 07:04:31 GMT  
		Size: 14.3 KB (14350 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6.4-alpine` - linux; riscv64

```console
$ docker pull spiped@sha256:0f378090b0e02992217f4f2a73d59cfb8c76cf62d83fec92991b3a8b1f0bfcc7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3623434 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0a7d261c52ce9f797be48d32c37a2c3f66b54a18d3599dd071fefa04e588df9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Sun, 10 Aug 2025 19:07:57 GMT
ADD alpine-minirootfs-3.22.2-riscv64.tar.gz / # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
CMD ["/bin/sh"]
# Sun, 10 Aug 2025 19:07:57 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
RUN apk add --no-cache libssl3 # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Sun, 10 Aug 2025 19:07:57 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
VOLUME [/spiped]
# Sun, 10 Aug 2025 19:07:57 GMT
WORKDIR /spiped
# Sun, 10 Aug 2025 19:07:57 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 10 Aug 2025 19:07:57 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:139bee3c50b89b56dcbc72522ce83097d9beb59d9d3a5c19072ccd1ad54b11c8`  
		Last Modified: Wed, 08 Oct 2025 21:18:33 GMT  
		Size: 3.5 MB (3515240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3c352072eefdbb94e63d3787f16fac871ba719ed362861b9e97b581edd60548`  
		Last Modified: Fri, 10 Oct 2025 20:50:10 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9aaa05a9bc37f5bb35d75064bac3af035a1d3a82ac079befd8019359672cc322`  
		Last Modified: Fri, 10 Oct 2025 20:50:10 GMT  
		Size: 7.9 KB (7948 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c51a4b112c1b7e8d19565628602648b41c69109d0f16548d16e781b095481e4d`  
		Last Modified: Fri, 10 Oct 2025 20:50:10 GMT  
		Size: 98.9 KB (98862 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9971a3bdcb8df001e3163788a7484aea74c6bf79af7ec5c42ae330638a863112`  
		Last Modified: Fri, 10 Oct 2025 20:50:10 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36e689628a891ec93dec38687edd123814871319bfb552253a1ab8608d94fa74`  
		Last Modified: Fri, 10 Oct 2025 20:50:10 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6.4-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:ef79fccc5586c74ed7a097a019247ca0f6644364c4e1b931202ce2f00cf4e38a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.6 KB (94617 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3c35fd6859715e249d4b311ca37e3e8e7886a7ce1788f0688877545e1f0fb2b`

```dockerfile
```

-	Layers:
	-	`sha256:624da72bc5bd15d76a69efe794516160d8151dc3f9b207f42a5b8b5165948a76`  
		Last Modified: Fri, 10 Oct 2025 22:04:34 GMT  
		Size: 80.3 KB (80271 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a83fb34ab49138178f6f97cf97ae672fc5e173707dec2895a8d5b36f2e7689a5`  
		Last Modified: Fri, 10 Oct 2025 22:04:35 GMT  
		Size: 14.3 KB (14346 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6.4-alpine` - linux; s390x

```console
$ docker pull spiped@sha256:be3e9a57eb9caa9fb853c68e3efdc680d9d441f399d676b7a437f56a46d71b59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3755528 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3eee68dd7eaa10392bbfe4c42a39adf582bc976bf97937637b807540ed7960af`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Sun, 10 Aug 2025 19:07:57 GMT
ADD alpine-minirootfs-3.22.2-s390x.tar.gz / # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
CMD ["/bin/sh"]
# Sun, 10 Aug 2025 19:07:57 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
RUN apk add --no-cache libssl3 # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Sun, 10 Aug 2025 19:07:57 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
VOLUME [/spiped]
# Sun, 10 Aug 2025 19:07:57 GMT
WORKDIR /spiped
# Sun, 10 Aug 2025 19:07:57 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 10 Aug 2025 19:07:57 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:e6b06613ca2e7cdf3e8ebbe71ca45137242628a4a3a4bfcb7a9f76d0d5b0e653`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.6 MB (3649244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5eca97998e3d4f083ea39c1b7e9bd8d771aaa888745b8a60d6baff87ab6f8f37`  
		Last Modified: Thu, 09 Oct 2025 02:26:07 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ae19bb237945d6597aced8fc4cd16e5d4f06869978f4f6eb5d90a8bc9be7f39`  
		Last Modified: Thu, 09 Oct 2025 02:26:07 GMT  
		Size: 8.0 KB (7957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ce433dda6c532473e5da602686ec5186ad28c43789f172a14efc1cd9e38093d`  
		Last Modified: Thu, 09 Oct 2025 02:26:07 GMT  
		Size: 96.9 KB (96944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:867b81ca187d86754818499befad84648bb33d900aa6c797f74f14d7f06589dd`  
		Last Modified: Thu, 09 Oct 2025 02:26:06 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de821656be3d9d0eadaa8bfe8c17052ce64308ac54b60bb962a59498810f549e`  
		Last Modified: Thu, 09 Oct 2025 02:26:07 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6.4-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:daeef3e785369b94f4c3fec6e7b468c0aa8bcc71748eb82a5dcb98744d0c094a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.5 KB (94540 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ff814477e4912c3dbc0dc6c3b2d236588fe065252c86c9a2ed142e200619a8a`

```dockerfile
```

-	Layers:
	-	`sha256:3ccf297cff7eee80cdb3e7128fdeabdb48c58df324a049928273000e72eba72d`  
		Last Modified: Thu, 09 Oct 2025 04:04:35 GMT  
		Size: 80.2 KB (80241 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dcfca2be336420edbf2af734bab83d3864c289d0e61390ac2cfc5f6d7f183847`  
		Last Modified: Thu, 09 Oct 2025 04:04:36 GMT  
		Size: 14.3 KB (14299 bytes)  
		MIME: application/vnd.in-toto+json

## `spiped:alpine`

```console
$ docker pull spiped@sha256:7b9625a81e8db9045c4eaf8f9bf40b8ef8c78a666bb7201d8d7c80538a418f7a
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
$ docker pull spiped@sha256:7d011e9e579768cd749e2df95806a3b739ebbdd516385dac92f2e9cda3570e25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3919429 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc9d66303cac034d8960b8128b5967170028d350ecf6e131c4bf30b000a3f836`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Sun, 10 Aug 2025 19:07:57 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
CMD ["/bin/sh"]
# Sun, 10 Aug 2025 19:07:57 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
RUN apk add --no-cache libssl3 # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Sun, 10 Aug 2025 19:07:57 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
VOLUME [/spiped]
# Sun, 10 Aug 2025 19:07:57 GMT
WORKDIR /spiped
# Sun, 10 Aug 2025 19:07:57 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 10 Aug 2025 19:07:57 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7c041bc04e274276fc6a842ca20a0cf973af7c178bcfb6575c0d8203718fc91`  
		Last Modified: Wed, 08 Oct 2025 22:58:11 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f81b6f5c689713065e6b968619711a3bd698fd708594cc90dae3977d54ca24e`  
		Last Modified: Wed, 08 Oct 2025 22:58:11 GMT  
		Size: 8.0 KB (7950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a035501670b01c25e6d7ce231bae87ef493bb668e877be52618f03679b673c4f`  
		Last Modified: Wed, 08 Oct 2025 22:58:11 GMT  
		Size: 107.6 KB (107645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57f81362a47a6b65eaf0da33a0c61df7c9a874d76861e5ae8fa0bc16547593db`  
		Last Modified: Wed, 08 Oct 2025 22:58:12 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48ae81c7faaf7b0d0454b9d217085e8da2f5e5a72ead2527e67506b0d4834801`  
		Last Modified: Wed, 08 Oct 2025 22:58:11 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:ed8b2f715fbc09ab5fcc75433e022573fd8e46bded0d7dd791180a01b3d4a8dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.5 KB (96494 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b323748eb9cefd40fcfe67d6c7dd561a4f5c4498457b7739b98161ea53a531c`

```dockerfile
```

-	Layers:
	-	`sha256:64366b1f73c30d49b216afd6a2acb0a27ad6d69bbaf554934ef1fb5a1b8ae379`  
		Last Modified: Thu, 09 Oct 2025 01:04:34 GMT  
		Size: 82.2 KB (82192 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d77f4db066b7ca49f19231acfa8a9f30749e3884bc787f4fcb01d3cb8a54b848`  
		Last Modified: Thu, 09 Oct 2025 01:04:35 GMT  
		Size: 14.3 KB (14302 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:alpine` - linux; arm variant v6

```console
$ docker pull spiped@sha256:07f6c1ec4d9a40087ba1fabf98ca259b39af58fe0aa3d1b5aff7a5c9c85aab9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3602562 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66830d62439293e746c3d4171b26eb7b060853f622562e26647e13254243d153`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Sun, 10 Aug 2025 19:07:57 GMT
ADD alpine-minirootfs-3.22.2-armhf.tar.gz / # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
CMD ["/bin/sh"]
# Sun, 10 Aug 2025 19:07:57 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
RUN apk add --no-cache libssl3 # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Sun, 10 Aug 2025 19:07:57 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
VOLUME [/spiped]
# Sun, 10 Aug 2025 19:07:57 GMT
WORKDIR /spiped
# Sun, 10 Aug 2025 19:07:57 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 10 Aug 2025 19:07:57 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:bb1da3d879939be7df9f182950d2fb201d4fc2e1043677da2037cd6afb084ce0`  
		Last Modified: Wed, 08 Oct 2025 21:00:16 GMT  
		Size: 3.5 MB (3504080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:153e87cee3c8273a66e75e0a084e6876c74329042a77778cc75c7865eafb5817`  
		Last Modified: Wed, 08 Oct 2025 22:09:30 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e054efed96e629a0c9a72dadd2a8d348aa66730afa5f59ce6e02a530b64b8d73`  
		Last Modified: Wed, 08 Oct 2025 22:09:30 GMT  
		Size: 7.9 KB (7943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17dbbcac13a86093cd5821deda5686d525abf33f1ffacea149ae0a0b642a332f`  
		Last Modified: Wed, 08 Oct 2025 22:09:30 GMT  
		Size: 89.2 KB (89158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6448f1d44fa11364cf66800119dd7e5e05fc9b9d8384cce8cc858006c0684aae`  
		Last Modified: Wed, 08 Oct 2025 22:09:30 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8fa931b05c23aa0b5927c5fc4bea0d9aa65908b7ac3e936a5a5888060a49337`  
		Last Modified: Wed, 08 Oct 2025 22:09:30 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:e083a00e19dd556e9a671f1709ffc708a0ab8d2a7373856218a44de2df24d462
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.2 KB (14190 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b47da3cb18e03a2142fd48220b0903336c0d8a799d804ac3b38780211559ba36`

```dockerfile
```

-	Layers:
	-	`sha256:069680ffcf03350d43ef8d45bcb21dafd37c1132acdfce2d83391a239a85d47e`  
		Last Modified: Thu, 09 Oct 2025 01:04:38 GMT  
		Size: 14.2 KB (14190 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:alpine` - linux; arm variant v7

```console
$ docker pull spiped@sha256:742d7ee47c94e03887525e682c2614d90b9b1f43f674ce4407bcf06b787caa29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3312569 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6db7cd0fffd0a4f2c540dfe37e4c940cf5c7595aeffea1bf7acc4b1793c73d9a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Sun, 10 Aug 2025 19:07:57 GMT
ADD alpine-minirootfs-3.22.2-armv7.tar.gz / # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
CMD ["/bin/sh"]
# Sun, 10 Aug 2025 19:07:57 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
RUN apk add --no-cache libssl3 # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Sun, 10 Aug 2025 19:07:57 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
VOLUME [/spiped]
# Sun, 10 Aug 2025 19:07:57 GMT
WORKDIR /spiped
# Sun, 10 Aug 2025 19:07:57 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 10 Aug 2025 19:07:57 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:2763c7fc79b66030222442365f4a0f69d9dbaa11f7fd47a918d29d732d52996c`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.2 MB (3221555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6a85ed9579bf45ac1db2ef56f4067b84fe0c4d8e51e006ec1d925eb0c32bf22`  
		Last Modified: Wed, 08 Oct 2025 22:10:17 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a85621545c13dee2ff1d8660f7847266105703d040c19d1816e374881a3bdf6e`  
		Last Modified: Wed, 08 Oct 2025 22:10:17 GMT  
		Size: 7.9 KB (7944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8afad049c072c9b6d3ed2946f7d0c0782835979f90696b68ac6e4c0efff5bf4`  
		Last Modified: Wed, 08 Oct 2025 22:10:17 GMT  
		Size: 81.7 KB (81688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35464221f20a70de628e3018e70c13c2e8ed9970a791049f1ba3bae429355536`  
		Last Modified: Wed, 08 Oct 2025 22:10:17 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39d6fea506e0050596918141446ad53da32b5b3a4fc9c7a5d497caf9a7ec6390`  
		Last Modified: Wed, 08 Oct 2025 22:10:18 GMT  
		Size: 336.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:1db53d701cc5320b98ed95f8e8288e9c84ddb8ad31b517b42fe2faa626874b44
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.6 KB (96633 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f53816c0890232fc85b4017c83eabcfb11884aeab001b608b66e2a8c9e183e3`

```dockerfile
```

-	Layers:
	-	`sha256:f33fdb1fd07f91c527d8c950dcb81f1eea51882f51d66c0f4da88547240c6499`  
		Last Modified: Thu, 09 Oct 2025 01:04:42 GMT  
		Size: 82.2 KB (82228 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:20a9fe69db1d74bfbe4aa6a07c0fb4e0e59f4eff9e1636b7e0c486b6435b788b`  
		Last Modified: Thu, 09 Oct 2025 01:04:42 GMT  
		Size: 14.4 KB (14405 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:alpine` - linux; arm64 variant v8

```console
$ docker pull spiped@sha256:1c2f38931ee0ff681a7c140bbc874fa1ff5837de4baf9a50a3498fbcb12a9668
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4248020 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26b0a53163c15fa0112f2865ee8a52cbed044f04fc7001f7bd1f5e407cd57237`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Sun, 10 Aug 2025 19:07:57 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
CMD ["/bin/sh"]
# Sun, 10 Aug 2025 19:07:57 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
RUN apk add --no-cache libssl3 # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Sun, 10 Aug 2025 19:07:57 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
VOLUME [/spiped]
# Sun, 10 Aug 2025 19:07:57 GMT
WORKDIR /spiped
# Sun, 10 Aug 2025 19:07:57 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 10 Aug 2025 19:07:57 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94547f3886a10ef8162a5d7fe9f4308e302dcfd48f5be2db3b1e5d4b5156d815`  
		Last Modified: Wed, 08 Oct 2025 22:29:31 GMT  
		Size: 949.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00ee5fd6e341869b5bcb70e517a1466b54c5191790816dd7956a41164690328b`  
		Last Modified: Wed, 08 Oct 2025 22:29:32 GMT  
		Size: 7.9 KB (7949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bba2ed7625e00fce702c1adbf90233532e0e4e98935a777f6bdffa076b1c3be2`  
		Last Modified: Wed, 08 Oct 2025 22:29:31 GMT  
		Size: 100.6 KB (100621 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1612c8ef14c84a7450d3ced7f152a93e533ffbb92d525fae7dde4c2988e230d7`  
		Last Modified: Wed, 08 Oct 2025 22:29:32 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:433ac69ec6618a756cde4ab30a4488c3f0f7b89df240ede5a7b0a29d66250444`  
		Last Modified: Wed, 08 Oct 2025 22:29:31 GMT  
		Size: 336.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:f599a056737cf26e2f1e5bfb25bf8cf6f92cea0ea27b040de42b2e4bf139168f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.7 KB (96684 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad1c665f9e5776de9d503dbefb3dccddb1d230d81716f5b086b02065d6f512d0`

```dockerfile
```

-	Layers:
	-	`sha256:8c6690f0ed02188be28287964aecbd171476e7e9484ec40d030c20c7b0e182c3`  
		Last Modified: Thu, 09 Oct 2025 01:04:46 GMT  
		Size: 82.2 KB (82248 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dde4ac6f12c825868630b75c268c91338db29a424c87e551c1153694da325c83`  
		Last Modified: Thu, 09 Oct 2025 01:04:46 GMT  
		Size: 14.4 KB (14436 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:alpine` - linux; 386

```console
$ docker pull spiped@sha256:ac72ab4f716c2dabdad650618a34deccd477e31f604bf27a1f630a7a8433d994
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3748370 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf996beac99b6a5d8eae08ab4703a9cc11bccf3cb429e61a25bebf2947e4b519`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Sun, 10 Aug 2025 19:07:57 GMT
ADD alpine-minirootfs-3.22.2-x86.tar.gz / # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
CMD ["/bin/sh"]
# Sun, 10 Aug 2025 19:07:57 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
RUN apk add --no-cache libssl3 # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Sun, 10 Aug 2025 19:07:57 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
VOLUME [/spiped]
# Sun, 10 Aug 2025 19:07:57 GMT
WORKDIR /spiped
# Sun, 10 Aug 2025 19:07:57 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 10 Aug 2025 19:07:57 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:13c6e95c06ae06f126f5e940d6d88c2fec0da715c80878ad225c76ad48d0a31e`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.6 MB (3618931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:664f8e36f37724daee2260066812a0de8999a28949591daef235c15d49ca301a`  
		Last Modified: Wed, 08 Oct 2025 22:22:15 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ee281d18609c0bc414db88c7d17dd26aca0857610126d3e6d974952f5a414ab`  
		Last Modified: Wed, 08 Oct 2025 22:22:14 GMT  
		Size: 7.9 KB (7947 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20e8cb95edb963d4e91f7f5ea1c0881091c485846b9df554d3c11102b6a6a753`  
		Last Modified: Wed, 08 Oct 2025 22:22:14 GMT  
		Size: 120.1 KB (120110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:473aab810bb857acc1c39fc855966c0a2de5edd8a71287cf2183cea8dc6fdc4b`  
		Last Modified: Wed, 08 Oct 2025 22:22:14 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1968cadac684d87fbcd83e1d646d178ae33c9242a480ddbd04f8fdf77b5e2ed`  
		Last Modified: Wed, 08 Oct 2025 22:22:14 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:2e9fe75d8ecfc557edbdaa8476f159fdb286886f6212788ecb61cda153b3ee2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.4 KB (96433 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e13e74ee61a3719d708f5b8486f092d523816b5c47e960b60b25a5d76b1aaee`

```dockerfile
```

-	Layers:
	-	`sha256:565649aba2f7ebad36d4ce1a64e495876030406355bb0f7a99f41f82b8300791`  
		Last Modified: Thu, 09 Oct 2025 01:04:50 GMT  
		Size: 82.2 KB (82167 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8cf1923abaf687d0c1af4d1718e1e365a3359dbf3e5ff8c339291f60bb0fc220`  
		Last Modified: Thu, 09 Oct 2025 01:04:51 GMT  
		Size: 14.3 KB (14266 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:alpine` - linux; ppc64le

```console
$ docker pull spiped@sha256:506cee7907557b7efa054dc1a4c3261e8956700c9f553e9eb8d9a3470a368431
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3854263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eca7a1787271596d011a96a2b5632780587dd9653d8b0410f93093e13ecb8fcf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Sun, 10 Aug 2025 19:07:57 GMT
ADD alpine-minirootfs-3.22.2-ppc64le.tar.gz / # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
CMD ["/bin/sh"]
# Sun, 10 Aug 2025 19:07:57 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
RUN apk add --no-cache libssl3 # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Sun, 10 Aug 2025 19:07:57 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
VOLUME [/spiped]
# Sun, 10 Aug 2025 19:07:57 GMT
WORKDIR /spiped
# Sun, 10 Aug 2025 19:07:57 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 10 Aug 2025 19:07:57 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:85a0f69f026b4a01420490809bed190217e05518f7b718c0bbc1ad4871e0dedf`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.7 MB (3732241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26cf524fa67a04db3aef99fc4ab2113633c6c1965d0f890616009377904a6284`  
		Last Modified: Thu, 09 Oct 2025 03:32:10 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecc9d95b7526b98e836dea8e7e9792130d0d6d71b1d6259e6f954ddffc64f5cc`  
		Last Modified: Thu, 09 Oct 2025 03:32:10 GMT  
		Size: 8.0 KB (7955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:011805850ee2924d217a7651762c507b895c90911b4151207fe8e82e4388fcce`  
		Last Modified: Thu, 09 Oct 2025 03:32:10 GMT  
		Size: 112.7 KB (112682 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcef441d2768884d48fcb3b73e59f27e5fe6fc1cb5484df89fd3db0df4ce9437`  
		Last Modified: Thu, 09 Oct 2025 03:32:10 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03005fd392da3ad1cd46c719335ac18f079118e761584617fe8c73405301647d`  
		Last Modified: Thu, 09 Oct 2025 03:32:10 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:55eac1eb38ff8ce12fb98d86fb70542b4620b4c59ff746effba30530ad8676de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.6 KB (94625 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0a3d2f7338bf8715707424b7b716c4498d4c3b844d2dc7387da9a1c64357879`

```dockerfile
```

-	Layers:
	-	`sha256:e3e6cde5a2631b7b9b782bb7fdfcf5de409ca1736416d9573c8888daf799d9e0`  
		Last Modified: Thu, 09 Oct 2025 07:04:30 GMT  
		Size: 80.3 KB (80275 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d9220e8aff0f38f3e237e21c128db8adfad10ae35fb9db4dc56ead1ff1235e9d`  
		Last Modified: Thu, 09 Oct 2025 07:04:31 GMT  
		Size: 14.3 KB (14350 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:alpine` - linux; riscv64

```console
$ docker pull spiped@sha256:0f378090b0e02992217f4f2a73d59cfb8c76cf62d83fec92991b3a8b1f0bfcc7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3623434 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0a7d261c52ce9f797be48d32c37a2c3f66b54a18d3599dd071fefa04e588df9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Sun, 10 Aug 2025 19:07:57 GMT
ADD alpine-minirootfs-3.22.2-riscv64.tar.gz / # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
CMD ["/bin/sh"]
# Sun, 10 Aug 2025 19:07:57 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
RUN apk add --no-cache libssl3 # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Sun, 10 Aug 2025 19:07:57 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
VOLUME [/spiped]
# Sun, 10 Aug 2025 19:07:57 GMT
WORKDIR /spiped
# Sun, 10 Aug 2025 19:07:57 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 10 Aug 2025 19:07:57 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:139bee3c50b89b56dcbc72522ce83097d9beb59d9d3a5c19072ccd1ad54b11c8`  
		Last Modified: Wed, 08 Oct 2025 21:18:33 GMT  
		Size: 3.5 MB (3515240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3c352072eefdbb94e63d3787f16fac871ba719ed362861b9e97b581edd60548`  
		Last Modified: Fri, 10 Oct 2025 20:50:10 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9aaa05a9bc37f5bb35d75064bac3af035a1d3a82ac079befd8019359672cc322`  
		Last Modified: Fri, 10 Oct 2025 20:50:10 GMT  
		Size: 7.9 KB (7948 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c51a4b112c1b7e8d19565628602648b41c69109d0f16548d16e781b095481e4d`  
		Last Modified: Fri, 10 Oct 2025 20:50:10 GMT  
		Size: 98.9 KB (98862 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9971a3bdcb8df001e3163788a7484aea74c6bf79af7ec5c42ae330638a863112`  
		Last Modified: Fri, 10 Oct 2025 20:50:10 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36e689628a891ec93dec38687edd123814871319bfb552253a1ab8608d94fa74`  
		Last Modified: Fri, 10 Oct 2025 20:50:10 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:ef79fccc5586c74ed7a097a019247ca0f6644364c4e1b931202ce2f00cf4e38a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.6 KB (94617 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3c35fd6859715e249d4b311ca37e3e8e7886a7ce1788f0688877545e1f0fb2b`

```dockerfile
```

-	Layers:
	-	`sha256:624da72bc5bd15d76a69efe794516160d8151dc3f9b207f42a5b8b5165948a76`  
		Last Modified: Fri, 10 Oct 2025 22:04:34 GMT  
		Size: 80.3 KB (80271 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a83fb34ab49138178f6f97cf97ae672fc5e173707dec2895a8d5b36f2e7689a5`  
		Last Modified: Fri, 10 Oct 2025 22:04:35 GMT  
		Size: 14.3 KB (14346 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:alpine` - linux; s390x

```console
$ docker pull spiped@sha256:be3e9a57eb9caa9fb853c68e3efdc680d9d441f399d676b7a437f56a46d71b59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3755528 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3eee68dd7eaa10392bbfe4c42a39adf582bc976bf97937637b807540ed7960af`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Sun, 10 Aug 2025 19:07:57 GMT
ADD alpine-minirootfs-3.22.2-s390x.tar.gz / # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
CMD ["/bin/sh"]
# Sun, 10 Aug 2025 19:07:57 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
RUN apk add --no-cache libssl3 # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Sun, 10 Aug 2025 19:07:57 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
VOLUME [/spiped]
# Sun, 10 Aug 2025 19:07:57 GMT
WORKDIR /spiped
# Sun, 10 Aug 2025 19:07:57 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 10 Aug 2025 19:07:57 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:e6b06613ca2e7cdf3e8ebbe71ca45137242628a4a3a4bfcb7a9f76d0d5b0e653`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.6 MB (3649244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5eca97998e3d4f083ea39c1b7e9bd8d771aaa888745b8a60d6baff87ab6f8f37`  
		Last Modified: Thu, 09 Oct 2025 02:26:07 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ae19bb237945d6597aced8fc4cd16e5d4f06869978f4f6eb5d90a8bc9be7f39`  
		Last Modified: Thu, 09 Oct 2025 02:26:07 GMT  
		Size: 8.0 KB (7957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ce433dda6c532473e5da602686ec5186ad28c43789f172a14efc1cd9e38093d`  
		Last Modified: Thu, 09 Oct 2025 02:26:07 GMT  
		Size: 96.9 KB (96944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:867b81ca187d86754818499befad84648bb33d900aa6c797f74f14d7f06589dd`  
		Last Modified: Thu, 09 Oct 2025 02:26:06 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de821656be3d9d0eadaa8bfe8c17052ce64308ac54b60bb962a59498810f549e`  
		Last Modified: Thu, 09 Oct 2025 02:26:07 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:daeef3e785369b94f4c3fec6e7b468c0aa8bcc71748eb82a5dcb98744d0c094a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.5 KB (94540 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ff814477e4912c3dbc0dc6c3b2d236588fe065252c86c9a2ed142e200619a8a`

```dockerfile
```

-	Layers:
	-	`sha256:3ccf297cff7eee80cdb3e7128fdeabdb48c58df324a049928273000e72eba72d`  
		Last Modified: Thu, 09 Oct 2025 04:04:35 GMT  
		Size: 80.2 KB (80241 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dcfca2be336420edbf2af734bab83d3864c289d0e61390ac2cfc5f6d7f183847`  
		Last Modified: Thu, 09 Oct 2025 04:04:36 GMT  
		Size: 14.3 KB (14299 bytes)  
		MIME: application/vnd.in-toto+json

## `spiped:latest`

```console
$ docker pull spiped@sha256:ae34dc5e1e750a9577c6c31b1bd458e953940df360d2129dcc6ab9ec76b97634
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
$ docker pull spiped@sha256:82a44171c51ca620ba3c3c03a99b52f52529674ec87bde43e9926f1d6ec0e009
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.8 MB (36828656 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe7422969ceb15f34c8bfad19efc9932626d64801cea01ac7adb6b48c80d31f5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 04:13:26 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Tue, 04 Nov 2025 04:13:28 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 04:13:49 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Tue, 04 Nov 2025 04:13:49 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 04 Nov 2025 04:13:49 GMT
VOLUME [/spiped]
# Tue, 04 Nov 2025 04:13:49 GMT
WORKDIR /spiped
# Tue, 04 Nov 2025 04:13:49 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 04:13:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Nov 2025 04:13:49 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:d7ecded7702a5dbf6d0f79a71edc34b534d08f3051980e2c948fba72db3197fc`  
		Last Modified: Tue, 04 Nov 2025 00:13:18 GMT  
		Size: 29.8 MB (29778104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04af94b2f2784b050748c0bc593d7625ed57d5cba186a5f086621574d0db770a`  
		Last Modified: Tue, 04 Nov 2025 04:14:00 GMT  
		Size: 1.1 KB (1105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:552c1418ed5f113e9eef0fa6687c45ff9cbffe5c42b756a669850fc73f345825`  
		Last Modified: Tue, 04 Nov 2025 04:14:00 GMT  
		Size: 826.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0261a8f67e930dd0ddf4233075edba351756a7d795a0e69a5855cb123372ba2`  
		Last Modified: Tue, 04 Nov 2025 04:14:02 GMT  
		Size: 7.0 MB (7048187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5ca2f62567ececa23586d454805f1453bfb20590012b083407cd012ee296eea`  
		Last Modified: Tue, 04 Nov 2025 04:14:00 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84431171e7f009a7782b98db778ea5e41991d25b73524432b73c55af5a67e4bf`  
		Last Modified: Tue, 04 Nov 2025 04:14:00 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:latest` - unknown; unknown

```console
$ docker pull spiped@sha256:fdc238e5b3be11018da12f326e986158a996ba0040c07e562493af76e56d252a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3641114 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6cee0fd107c9ef0ff2a206950205e6a145e94034a05e40a81d97bf9680015577`

```dockerfile
```

-	Layers:
	-	`sha256:e9a375eaa0ee407c9bf820a27a60ebfae8e1b0eca680a00e28bb2c1fe201e7dc`  
		Last Modified: Tue, 04 Nov 2025 14:04:42 GMT  
		Size: 3.6 MB (3626132 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:090acc34f1d66361f6d8fddabbc50d86e8f70632cdc1320e68686e3b27c23564`  
		Last Modified: Tue, 04 Nov 2025 14:04:43 GMT  
		Size: 15.0 KB (14982 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:latest` - linux; arm variant v5

```console
$ docker pull spiped@sha256:01018b8cd02af89ba30ae1bcf4e97855ab3bdf892659021c68cd6db582a4e82f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.7 MB (33738270 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8470079cfa5129c79d5f858dfab379f480768bc25217b8e0b6729b827bda73d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 01:26:44 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Tue, 04 Nov 2025 01:26:48 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 01:27:14 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Tue, 04 Nov 2025 01:27:14 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 04 Nov 2025 01:27:14 GMT
VOLUME [/spiped]
# Tue, 04 Nov 2025 01:27:14 GMT
WORKDIR /spiped
# Tue, 04 Nov 2025 01:27:15 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 01:27:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Nov 2025 01:27:15 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:453afc2258d7bc5729fed5672fb95bafa092e30a933b4377a12034be940a671b`  
		Last Modified: Tue, 04 Nov 2025 00:13:12 GMT  
		Size: 27.9 MB (27946438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca47efc60e8d395bb20127ab62f55376f6526f660fda2af48f332ab55a5db1de`  
		Last Modified: Tue, 04 Nov 2025 01:27:29 GMT  
		Size: 1.1 KB (1105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3087d5dadbd1a81bf4a6a89b5c5513e92c5267b062a5ad88f3714f4af65944f9`  
		Last Modified: Tue, 04 Nov 2025 01:27:29 GMT  
		Size: 830.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7844d897fb72d98b6d97c02c9aea425f239371a0383c9ddb897005ce9e32d8d`  
		Last Modified: Tue, 04 Nov 2025 01:27:31 GMT  
		Size: 5.8 MB (5789464 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bb6f08fbffea41432c882d7ca57574ca10f090cfc124102a57937cb13a1e8e4`  
		Last Modified: Tue, 04 Nov 2025 01:27:29 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd566239a0cc0043085f6f763357bcb82782f07ebf8d6d1cb77a81683614a813`  
		Last Modified: Tue, 04 Nov 2025 01:27:29 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:latest` - unknown; unknown

```console
$ docker pull spiped@sha256:acf598dd339fcabaa30ebe44d7595caa9299c0471756c6d4f51989a8e0ef9ca6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3634214 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d932b1acba0130144dcf23c7d242737a06b9e4ef9c5c435a2ed7d54042d30ec6`

```dockerfile
```

-	Layers:
	-	`sha256:e00221651b0ba4a1e38bf876ba3fba3f946d133c72200f5bab9b64d3e969ee42`  
		Last Modified: Tue, 04 Nov 2025 08:04:27 GMT  
		Size: 3.6 MB (3619126 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:59b7876f9d30572585cdd8c35b384ebd24d330f12217040dbea5e8cbd219456a`  
		Last Modified: Tue, 04 Nov 2025 08:04:28 GMT  
		Size: 15.1 KB (15088 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:latest` - linux; arm variant v7

```console
$ docker pull spiped@sha256:14c077460233a0891c8d77cba716c235993ec3531bc03dea2f45959b3387e049
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.8 MB (31800147 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12694eea0cdf2315ba4c0c3242b4e3501a38116b638d7239c5a46b6f6d61eef1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 02:17:27 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Tue, 04 Nov 2025 02:17:30 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 02:17:53 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Tue, 04 Nov 2025 02:17:53 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 04 Nov 2025 02:17:53 GMT
VOLUME [/spiped]
# Tue, 04 Nov 2025 02:17:53 GMT
WORKDIR /spiped
# Tue, 04 Nov 2025 02:17:53 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 02:17:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Nov 2025 02:17:53 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:8945aefb71bd942499dd072e2c7c869b6b74b7c4dd83bff59c209b7b95d52a9f`  
		Last Modified: Tue, 04 Nov 2025 00:13:33 GMT  
		Size: 26.2 MB (26213039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fda5ed53e0dbde40dfe076db326ecd295b0b1c6d680116701507afe281baba2f`  
		Last Modified: Tue, 04 Nov 2025 02:18:05 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97b35d897f0e9c8d74564913d30c18612c62876f021e52e682bccb7ca7aa7122`  
		Last Modified: Tue, 04 Nov 2025 02:18:05 GMT  
		Size: 824.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:880acbf14d869df07dc547c6546ace74066ceb671ee539f84c04b7aa6bd93d88`  
		Last Modified: Tue, 04 Nov 2025 02:18:06 GMT  
		Size: 5.6 MB (5584740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83ad84946a9a60a387ca7f2d49194aa08d4a4b00b6921b734ddd91ea47ec12fc`  
		Last Modified: Tue, 04 Nov 2025 02:18:05 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31948a9a6bd812479abcecaee071ca0adfc7ccb05075344aacb05afdde76c955`  
		Last Modified: Tue, 04 Nov 2025 02:18:05 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:latest` - unknown; unknown

```console
$ docker pull spiped@sha256:26e3b4b9812bd059487e9655a891858c085e662a2f0f9a3f0b298c3dfee41536
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3633335 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc044a3ebcd39fe3f2be39febd09774d0d90a07c0b0d2bd5c34d4ecb7efd8dbb`

```dockerfile
```

-	Layers:
	-	`sha256:15aab9c35b9929d5dd1efe22911175934126591da412018cbbfcf9cd3b909b71`  
		Last Modified: Tue, 04 Nov 2025 14:04:50 GMT  
		Size: 3.6 MB (3618247 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8c0fd76702563c822a41fb5417ecf0e5cc689f14a75561c58d94a7e9235c9058`  
		Last Modified: Tue, 04 Nov 2025 14:04:50 GMT  
		Size: 15.1 KB (15088 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:latest` - linux; arm64 variant v8

```console
$ docker pull spiped@sha256:b6b4508fea00b81da1ef86c3545f0570316acafb1741295cd5cb81b44d57983f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.4 MB (36376612 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b7e2bcd7f2a9a352a7c82c13dfc51a9cd1fb8b6951ecbebbd5caff5dba84b44`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 01:28:45 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Tue, 04 Nov 2025 01:28:48 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 01:29:10 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Tue, 04 Nov 2025 01:29:10 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 04 Nov 2025 01:29:10 GMT
VOLUME [/spiped]
# Tue, 04 Nov 2025 01:29:10 GMT
WORKDIR /spiped
# Tue, 04 Nov 2025 01:29:10 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 01:29:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Nov 2025 01:29:10 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:51365f04b68881c6fd3d04aa38cdb689fdee6efba2aa6afcf2da5385022cf475`  
		Last Modified: Tue, 04 Nov 2025 00:13:42 GMT  
		Size: 30.1 MB (30142298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da995b7386a81488a789551cb249fe6fea42d70c39ab8a87d627d805e7e0702f`  
		Last Modified: Tue, 04 Nov 2025 01:29:26 GMT  
		Size: 1.1 KB (1105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d22fea0cfbe83fade9a6807335d9620c018e1f013f30933686d89653b8f3751b`  
		Last Modified: Tue, 04 Nov 2025 01:29:26 GMT  
		Size: 827.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85524e1a2d9a76551e1de84299ffdf92ddd97e9d6f422b3e562dbc1a6ba6a50b`  
		Last Modified: Tue, 04 Nov 2025 01:29:27 GMT  
		Size: 6.2 MB (6231948 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c76200e3164e6d69e66e2534b38d35f0e16b4f2d64f70afd08c8457d373b835`  
		Last Modified: Tue, 04 Nov 2025 01:29:26 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c14c920bf38ff2c704eacb362443942ea2718f868f01e144eb2e3e04d96e2564`  
		Last Modified: Tue, 04 Nov 2025 01:29:26 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:latest` - unknown; unknown

```console
$ docker pull spiped@sha256:c779c8aee90a56c7378621b7fe346c3139be38eec6de2fa672f998c9fc4986de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3636284 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:555a5ae0e19d04ef7e45c6eec70472e7764fb60499c0675e4a6594e2241883b8`

```dockerfile
```

-	Layers:
	-	`sha256:8e1c42f1f18a6f283c053696b1e4ab1e61f688cebf405ec7e2eaa94d839d7fa0`  
		Last Modified: Tue, 04 Nov 2025 14:04:56 GMT  
		Size: 3.6 MB (3621168 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ff05626a27a8aaec468faef774708e79fad5edfdcfda16285d43c34ef591b620`  
		Last Modified: Tue, 04 Nov 2025 14:04:56 GMT  
		Size: 15.1 KB (15116 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:latest` - linux; 386

```console
$ docker pull spiped@sha256:a4b5da618ef9092d51d4526190bc5e118e9185b168ead3df69d42dff523191d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.7 MB (37739460 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04609af68ede4d313e06c3fabb8ba8d0a59f1b79b795df1e2cbe9a50cb5c0472`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 01:30:27 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Tue, 04 Nov 2025 01:30:30 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 01:30:55 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Tue, 04 Nov 2025 01:30:55 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 04 Nov 2025 01:30:55 GMT
VOLUME [/spiped]
# Tue, 04 Nov 2025 01:30:55 GMT
WORKDIR /spiped
# Tue, 04 Nov 2025 01:30:55 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 01:30:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Nov 2025 01:30:55 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:7f24a3a0c200106d0d9ab7b6264e50c689910154fb57bf08185b9eaf995db758`  
		Last Modified: Tue, 04 Nov 2025 00:13:54 GMT  
		Size: 31.3 MB (31294783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65859e510c2db85116bdd72bf3d9c7db20eb3aa26d9b1de16d5d468fac6e12b4`  
		Last Modified: Tue, 04 Nov 2025 01:31:07 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17425f70fc6396f91fe03abde4d6c062f561878471403b5e797512c012d0b58f`  
		Last Modified: Tue, 04 Nov 2025 01:31:08 GMT  
		Size: 826.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e92634046b1716dd52c3215f95a28867b3e64b689a52a66bc446570f7d3f915b`  
		Last Modified: Tue, 04 Nov 2025 01:31:08 GMT  
		Size: 6.4 MB (6442311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:082304266fac4680b67029584f056ab407e955eaaa5694d05580c08568183ba2`  
		Last Modified: Tue, 04 Nov 2025 01:31:08 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3f65e39b75028e66f2635520d73e70b21bb85c3574637ef9339d98b08cce418`  
		Last Modified: Tue, 04 Nov 2025 01:31:07 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:latest` - unknown; unknown

```console
$ docker pull spiped@sha256:8dfb3738f33f7909eb57ce11e1d4c3b9621b9bc19194c790528a58c917672527
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3635206 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ddfcb2680869fc3ee15b86cc93cba15353c8e2748cada861d826a1365663d62`

```dockerfile
```

-	Layers:
	-	`sha256:951cba86bfe9e094394aed88e6e4907c73131f7aa00df1f74494c86bc03df98e`  
		Last Modified: Tue, 04 Nov 2025 14:05:00 GMT  
		Size: 3.6 MB (3620261 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3b0ff7f7bd86aaafaa07c69914072c6f5ef7f94c5bb130d61e695b5f7cbb7461`  
		Last Modified: Tue, 04 Nov 2025 14:05:01 GMT  
		Size: 14.9 KB (14945 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:latest` - linux; ppc64le

```console
$ docker pull spiped@sha256:17a9f9c03a0c9c0b4845e576b4d50b32791c874660333d35e2f7713b5a4f9a54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.4 MB (40441436 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49d997c535004cfabfeb64a604cfa65a56f97d30072ca33d0813aad07018c58b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 06:08:31 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Tue, 04 Nov 2025 06:08:36 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 06:09:27 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Tue, 04 Nov 2025 06:09:27 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 04 Nov 2025 06:09:27 GMT
VOLUME [/spiped]
# Tue, 04 Nov 2025 06:09:27 GMT
WORKDIR /spiped
# Tue, 04 Nov 2025 06:09:28 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 06:09:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Nov 2025 06:09:28 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:eead2c4a2afd8217def9d0ca536e7e4108ac8a91745ca25e76eb059260c04aab`  
		Last Modified: Tue, 04 Nov 2025 00:20:53 GMT  
		Size: 33.6 MB (33598647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b2092794106fcd3e23337b489859b3eb0854104e16e57e5ec14f218338644be`  
		Last Modified: Tue, 04 Nov 2025 06:09:52 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca2ca52ff15c8f4ff8cb61e6ad4215e2632257624c0c417e70e3c3f6d7f234bb`  
		Last Modified: Tue, 04 Nov 2025 06:09:52 GMT  
		Size: 827.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5983f80493ffaac3089e1f7f8864ab8cc80507a20bbedfa2c3e2923e65b2c538`  
		Last Modified: Tue, 04 Nov 2025 06:09:52 GMT  
		Size: 6.8 MB (6840421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea2839f6c480bb68bf8aaeba58db823e5327791e68b29e0834b52e7458e069e5`  
		Last Modified: Tue, 04 Nov 2025 06:09:52 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e3df6a56753bd17d0ca244a384c7110325691bdb7f9bed0ef49ad1f9e29a8a4`  
		Last Modified: Tue, 04 Nov 2025 06:09:52 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:latest` - unknown; unknown

```console
$ docker pull spiped@sha256:b41008bcde4956aec3ad1ac3162aa82ac36e06cc052ee46b38c5de8e30d22b8c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3636899 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6faf5bf37b372ec100c4d596f350cf4eb6c850aebed6f26691d621fd6238977b`

```dockerfile
```

-	Layers:
	-	`sha256:9ea9bb8d6fdd4f34069789821b02e82da1ebf377c37ac65a8626ff7aafd83f54`  
		Last Modified: Tue, 04 Nov 2025 14:05:06 GMT  
		Size: 3.6 MB (3621869 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c37176c69bb122c01a898f0893b93e72adf3525b0accf60ac377a130c269a2d8`  
		Last Modified: Tue, 04 Nov 2025 14:05:07 GMT  
		Size: 15.0 KB (15030 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:latest` - linux; riscv64

```console
$ docker pull spiped@sha256:7004f59a14e65493d89d02012617e4685f705f645959559227290584c7da32b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.6 MB (37636275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57db3066c8da0560c596ad9830d9e9d916c732311869e057ec28751c6c95ea6e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Fri, 29 Aug 2025 17:20:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1760918400'
# Fri, 29 Aug 2025 17:20:00 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Fri, 29 Aug 2025 17:20:00 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 29 Aug 2025 17:20:00 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Fri, 29 Aug 2025 17:20:00 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Fri, 29 Aug 2025 17:20:00 GMT
VOLUME [/spiped]
# Fri, 29 Aug 2025 17:20:00 GMT
WORKDIR /spiped
# Fri, 29 Aug 2025 17:20:00 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Fri, 29 Aug 2025 17:20:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 29 Aug 2025 17:20:00 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:6d1567708d42906165204f9177d357cb6a2fd51f758da447f1743b00813f892f`  
		Last Modified: Tue, 21 Oct 2025 00:37:37 GMT  
		Size: 28.3 MB (28275650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d2eca7a0881779ed75b9a6df9e9c73f4e30a2545b324835ded643360d27d8cc`  
		Last Modified: Wed, 22 Oct 2025 17:58:55 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:189f2808be96be6277f0f38d8010c29a85c6383d14b6f87ab8b25267c049edb2`  
		Last Modified: Wed, 22 Oct 2025 17:58:55 GMT  
		Size: 823.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63ffa6796bebebbe0e033f44c2862905348b86b654f6796e30afac6e530d4277`  
		Last Modified: Wed, 22 Oct 2025 17:58:57 GMT  
		Size: 9.4 MB (9358258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fa6357568a94aa6f06730895e5dae1afb3df5610b097001d226a3f77165e34f`  
		Last Modified: Wed, 22 Oct 2025 17:58:55 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94b644b84d3f1a2b591c927fa6de5e0189e84eefcff0f41ec2a3f44187185c0d`  
		Last Modified: Wed, 22 Oct 2025 17:58:55 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:latest` - unknown; unknown

```console
$ docker pull spiped@sha256:5c5c3dac2a6b922d04f583d01b94567b074f27f995ce52ec74839d9912349909
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3628348 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a636dc3ff00c7130929694628709b79af7b1fee5b8a10375831363195b017596`

```dockerfile
```

-	Layers:
	-	`sha256:06533fa6c4fa5d87ac9aa9b94a962ef7605ef017f0c5582d776f1d8052627da7`  
		Last Modified: Wed, 22 Oct 2025 19:04:39 GMT  
		Size: 3.6 MB (3613275 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:83d421894b349a0bc498ac33059bfe41875507a74674a4b14aefd8a88b3e1a41`  
		Last Modified: Wed, 22 Oct 2025 19:04:40 GMT  
		Size: 15.1 KB (15073 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:latest` - linux; s390x

```console
$ docker pull spiped@sha256:0baf3a2f09f03f86b756f3144062ee4da868d648b33a12e0d36b82135d15915b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.0 MB (35961254 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e5f3f6eecc940670d5374d68bf8dfcde4b58c041506361c10c8a41c45108a1a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 09:44:46 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Tue, 04 Nov 2025 09:44:49 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 09:45:08 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Tue, 04 Nov 2025 09:45:08 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 04 Nov 2025 09:45:08 GMT
VOLUME [/spiped]
# Tue, 04 Nov 2025 09:45:08 GMT
WORKDIR /spiped
# Tue, 04 Nov 2025 09:45:09 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 09:45:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Nov 2025 09:45:09 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:ad0bc025a1766baba34dfa4dbb5713703de6595994d855ebf4689c0b161314ee`  
		Last Modified: Tue, 04 Nov 2025 00:20:17 GMT  
		Size: 29.8 MB (29837392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:413a343213dc776ef8ec8258f5d795654681dedb3c922a2300eb7ef7d73550e3`  
		Last Modified: Tue, 04 Nov 2025 09:45:31 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35418050ccaf1bb39b9fe282dc51e265bfb9549bbc54b3a04420b3009a5b9dc7`  
		Last Modified: Tue, 04 Nov 2025 09:45:30 GMT  
		Size: 826.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21ed93eeb8c99a4ac37aba7742f9400f88c3edb4f731713a63588cbff687b5a1`  
		Last Modified: Tue, 04 Nov 2025 09:45:31 GMT  
		Size: 6.1 MB (6121493 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:093c2dfb578dd5e22bde915b7aaf0b7a8664c98c82ec4e775d9cf87a8a39c074`  
		Last Modified: Tue, 04 Nov 2025 09:45:30 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5474616e30d2720bab7073b5cb8772b655fb03da212f01a6946c7777f26eda9`  
		Last Modified: Tue, 04 Nov 2025 09:45:30 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:latest` - unknown; unknown

```console
$ docker pull spiped@sha256:5ba27c04f04976a68826dba21d4d8065792b743fcdb70d57dec54f77b64c21c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3633475 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1ca1463694fb2e285ab976f084b9ac52e5c81410f43af1e039c67fb30e09338`

```dockerfile
```

-	Layers:
	-	`sha256:7e8ab82c8e759285edf28b13b88413a10ae662563b6de418f33f06c7c0bde122`  
		Last Modified: Tue, 04 Nov 2025 14:05:15 GMT  
		Size: 3.6 MB (3618495 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5a721785c314ac76a8f08022c6725ff60002127c2e5716b46279b371abd12af0`  
		Last Modified: Tue, 04 Nov 2025 14:05:16 GMT  
		Size: 15.0 KB (14980 bytes)  
		MIME: application/vnd.in-toto+json
