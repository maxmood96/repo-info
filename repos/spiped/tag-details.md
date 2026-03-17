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
$ docker pull spiped@sha256:86bfe9d75887a0c865ca400bce9556e55f0100324ab12cea4182325b4538c9d3
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
$ docker pull spiped@sha256:1dadd78b37a53143babab424620b268d0e87665451c7e0b19ee714350efeb0aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.8 MB (36825645 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6aec690f0b7647a2b707058d20c805804b9d29cdd158eb3109584ae64c2e9c96`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1773619200'
# Mon, 16 Mar 2026 22:35:50 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Mon, 16 Mar 2026 22:35:52 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:36:17 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Mon, 16 Mar 2026 22:36:17 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Mon, 16 Mar 2026 22:36:17 GMT
VOLUME [/spiped]
# Mon, 16 Mar 2026 22:36:17 GMT
WORKDIR /spiped
# Mon, 16 Mar 2026 22:36:17 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Mon, 16 Mar 2026 22:36:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 16 Mar 2026 22:36:17 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:ec781dee3f4719c2ca0dd9e73cb1d4ed834ed1a406495eb6e44b6dfaad5d1f8f`  
		Last Modified: Mon, 16 Mar 2026 21:53:19 GMT  
		Size: 29.8 MB (29775500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32ceac9107a69b7bfdee6e7660e1eff3feb8d0fd5d6f681f2a6ad1905d93ba0a`  
		Last Modified: Mon, 16 Mar 2026 22:36:24 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1aa4948bacb0a02611ec173cb9f157bd247587fd13cb63e407219ba6dd87af7d`  
		Last Modified: Mon, 16 Mar 2026 22:36:24 GMT  
		Size: 828.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50f472851b739f36f98249e60dba4ceb8a571cbd9f18c3e6b9639215d2c6dcfa`  
		Last Modified: Mon, 16 Mar 2026 22:36:24 GMT  
		Size: 7.0 MB (7047777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7dda7601460289f11e5d3db99f3c14ac9bf518a829bc22ae224a96c8c3a4d4d9`  
		Last Modified: Mon, 16 Mar 2026 22:36:24 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:597b8eb9fa679d5997894aab7d18f62d615b6cc715de0c0a98c8bddef96e43ee`  
		Last Modified: Mon, 16 Mar 2026 22:36:25 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1` - unknown; unknown

```console
$ docker pull spiped@sha256:24038ff42b84801b0e2af5de324e185ffb9b47e091947a1d6ead4da071277394
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3641241 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:204d83d1b596e75d2d7efdfccf8e0ab85c3bf694d7310417d68e3add5e86a10f`

```dockerfile
```

-	Layers:
	-	`sha256:1f60bdfcbc8114aba716d733f2c08d28946d1d47510ef32f11fe773e7efbba8c`  
		Last Modified: Mon, 16 Mar 2026 22:36:24 GMT  
		Size: 3.6 MB (3626260 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b07a02dacfe5fad817dc8acef6300290b65922a87b426e54f70d87798a0696f5`  
		Last Modified: Mon, 16 Mar 2026 22:36:24 GMT  
		Size: 15.0 KB (14981 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1` - linux; arm variant v5

```console
$ docker pull spiped@sha256:d76bab68c9ba80d6bde9b766de2f4b524b29b2e06796dea03aa1f86973b6e402
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.7 MB (33735071 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e9ce3fe44b3195308782999982dffb0e0324f65968051303e6d0ccb5e46710e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1773619200'
# Mon, 16 Mar 2026 23:15:44 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Mon, 16 Mar 2026 23:15:49 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 23:16:15 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Mon, 16 Mar 2026 23:16:15 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Mon, 16 Mar 2026 23:16:15 GMT
VOLUME [/spiped]
# Mon, 16 Mar 2026 23:16:15 GMT
WORKDIR /spiped
# Mon, 16 Mar 2026 23:16:15 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Mon, 16 Mar 2026 23:16:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 16 Mar 2026 23:16:15 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:eb1defba38d0de4655b895d4763345b3ab078983d3385db43c308a7caca13f2a`  
		Last Modified: Mon, 16 Mar 2026 21:52:26 GMT  
		Size: 27.9 MB (27943649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9cfc1da50f0fc66e4696a6b249cf2c9f19d773fda1096f22c619e19221b8de7`  
		Last Modified: Mon, 16 Mar 2026 23:16:22 GMT  
		Size: 1.1 KB (1105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a98c3d3f9d3a820c9fbfddae7bba53067abc005cb4837355fd2fe02be5159fda`  
		Last Modified: Mon, 16 Mar 2026 23:16:22 GMT  
		Size: 831.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:981177ab397ef56ea1a515604977b4812a8bccc0e0ae76b96ba1a148b66278c5`  
		Last Modified: Mon, 16 Mar 2026 23:16:22 GMT  
		Size: 5.8 MB (5789053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8116b26167b41dbbadb8f30d9738528a34e2436086fd1d12d6d83af070f87911`  
		Last Modified: Mon, 16 Mar 2026 23:16:22 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8f7d349acecae8a4190b1310446bb378d3edc921d84f55ac12cf5202b8df556`  
		Last Modified: Mon, 16 Mar 2026 23:16:23 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1` - unknown; unknown

```console
$ docker pull spiped@sha256:1ef3cb6065e7ec1c89ec491fd9bfd3dc5b3221edc45b98e1d076dc81f408837e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3634342 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6758a2f7ff038f8df9fc87c6f4130ff4358acd576e0e39211c178068863796cc`

```dockerfile
```

-	Layers:
	-	`sha256:5a7c54557652f62feaed177546a18b57a4e82674763bde13f27b1dab19e00b9d`  
		Last Modified: Mon, 16 Mar 2026 23:16:23 GMT  
		Size: 3.6 MB (3619254 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:647540c448bfbe8c1ba0711adf24d3a530725e84f4fd25c88632cf2510d9c007`  
		Last Modified: Mon, 16 Mar 2026 23:16:22 GMT  
		Size: 15.1 KB (15088 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1` - linux; arm variant v7

```console
$ docker pull spiped@sha256:723ba9f91b55f3576b2113c495e19f93cb621ee72fabcaff1531301fbcaa4b1a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.8 MB (31796429 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5cb0e019fca22ad836d890087ee6d2a180105ee1191adf83d36a753ea37941a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1773619200'
# Mon, 16 Mar 2026 23:17:41 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Mon, 16 Mar 2026 23:17:45 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 23:18:07 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Mon, 16 Mar 2026 23:18:07 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Mon, 16 Mar 2026 23:18:07 GMT
VOLUME [/spiped]
# Mon, 16 Mar 2026 23:18:07 GMT
WORKDIR /spiped
# Mon, 16 Mar 2026 23:18:07 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Mon, 16 Mar 2026 23:18:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 16 Mar 2026 23:18:07 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:7d73604d2a042e7beeb809f68c76f5be3576747809bfaa49747f334227d8d250`  
		Last Modified: Mon, 16 Mar 2026 21:53:24 GMT  
		Size: 26.2 MB (26209505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:658299db6ef3056cf755c844791cbd82e4508468df390e37a8aad706f3a48f4c`  
		Last Modified: Mon, 16 Mar 2026 23:18:14 GMT  
		Size: 1.1 KB (1103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8faf32f19b630a82f84ed9470b862ab68393803b1e37f045f46258e8890f7d50`  
		Last Modified: Mon, 16 Mar 2026 23:18:14 GMT  
		Size: 828.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba29f29a0220be91155a5596cf59a8ec1e848dc1c59089563006ce592b99f829`  
		Last Modified: Mon, 16 Mar 2026 23:18:14 GMT  
		Size: 5.6 MB (5584559 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:571f3aa9916ae33f81a8eff41f15615107662751591ab2cae13c31339f2cdb35`  
		Last Modified: Mon, 16 Mar 2026 23:18:14 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0023499b415317d80739286a45ec7393c98ddc05a638d045c05812141aa28b0`  
		Last Modified: Mon, 16 Mar 2026 23:18:15 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1` - unknown; unknown

```console
$ docker pull spiped@sha256:b778f2f8e613351de55fec9efa1c2283e7262e815379cb9c01090839b522f03b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3633463 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:820126e67739682404e3e543b661db54a249ad7238843089922bd27097f59140`

```dockerfile
```

-	Layers:
	-	`sha256:34fdc3e15f493cc5e996b5a867605ede0f868b1b23e1156f69a1d24198213663`  
		Last Modified: Mon, 16 Mar 2026 23:18:14 GMT  
		Size: 3.6 MB (3618375 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7867a53cd4efb0b6f41304907e82351cc690be89532e8db042be1139471fee68`  
		Last Modified: Mon, 16 Mar 2026 23:18:14 GMT  
		Size: 15.1 KB (15088 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1` - linux; arm64 variant v8

```console
$ docker pull spiped@sha256:4ae6755ad03f743b18a351fbafa71c65c711f58faea3a81b665befd8567053b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.4 MB (36374360 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0fbe5e7be982e3e0a47d2310365b2015977222cf3f9135331a2ddafbc2a09e29`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1773619200'
# Mon, 16 Mar 2026 22:38:29 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Mon, 16 Mar 2026 22:38:32 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:38:55 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Mon, 16 Mar 2026 22:38:55 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Mon, 16 Mar 2026 22:38:55 GMT
VOLUME [/spiped]
# Mon, 16 Mar 2026 22:38:55 GMT
WORKDIR /spiped
# Mon, 16 Mar 2026 22:38:55 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Mon, 16 Mar 2026 22:38:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 16 Mar 2026 22:38:55 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:f4badedbec24858ef2dc51256f6418328e305e9c3c5a5e093581f83425618bd5`  
		Last Modified: Mon, 16 Mar 2026 21:53:04 GMT  
		Size: 30.1 MB (30138416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59eb94c76468927e4e914285fecca640b78cd857ba3998fcfc270e51a5999a76`  
		Last Modified: Mon, 16 Mar 2026 22:39:02 GMT  
		Size: 1.1 KB (1104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11b2a5c6f2a1a593d60739bde8e5edb5ede5cc1c07d169f19ef39a67402cd65b`  
		Last Modified: Mon, 16 Mar 2026 22:39:02 GMT  
		Size: 828.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bedfccd6793021acdd75a491c31f9164e9dc33b3e7429226d6093a2dd780093`  
		Last Modified: Mon, 16 Mar 2026 22:39:03 GMT  
		Size: 6.2 MB (6233579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b277914700ac4bb0336072358245beede0af746b61ba9febb726f5a24443909`  
		Last Modified: Mon, 16 Mar 2026 22:39:03 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fcc46f0d3ebea317699d8e2e6d3e2c8d2e022621162b4aeb23e6aec0d21d6f3`  
		Last Modified: Mon, 16 Mar 2026 22:39:03 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1` - unknown; unknown

```console
$ docker pull spiped@sha256:3bb60c38b60da93affbf4a161bd60f5d201524ab747841166084d1e18235b678
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3636412 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:acfdeacc136a94cefd95b5fc4a223865929593d17a4df005eb979067d4539f09`

```dockerfile
```

-	Layers:
	-	`sha256:da2db9f7e9ec3796af7d7b3c2062fb98cdf3bf4c8cbc30041368b9529682b6e4`  
		Last Modified: Mon, 16 Mar 2026 22:39:03 GMT  
		Size: 3.6 MB (3621296 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c581a66bb5f391583c1fd9137f24523cc1f7cfb6e13f4dca2a22a36d28db1f75`  
		Last Modified: Mon, 16 Mar 2026 22:39:02 GMT  
		Size: 15.1 KB (15116 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1` - linux; 386

```console
$ docker pull spiped@sha256:44d93dff5b665eb236d8d461091f645401dad4215fc6e748e75d845e5f88359a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.7 MB (37735593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b145875baf2722671a7d04cbdec8ce2e4e0044fe83f4480f7d13be40ef1b7f0d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1773619200'
# Mon, 16 Mar 2026 22:43:15 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Mon, 16 Mar 2026 22:43:17 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:43:39 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Mon, 16 Mar 2026 22:43:39 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Mon, 16 Mar 2026 22:43:39 GMT
VOLUME [/spiped]
# Mon, 16 Mar 2026 22:43:39 GMT
WORKDIR /spiped
# Mon, 16 Mar 2026 22:43:39 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Mon, 16 Mar 2026 22:43:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 16 Mar 2026 22:43:39 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:2c0c3f3238f3d4cecd93e4dee6eda788943ef955de61c3ad4ff659da1f43ba60`  
		Last Modified: Mon, 16 Mar 2026 21:53:39 GMT  
		Size: 31.3 MB (31291132 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e26822c10be4229a362fafa19cf7744d8e4afd786250bc983de1db93de19f3ff`  
		Last Modified: Mon, 16 Mar 2026 22:43:45 GMT  
		Size: 1.1 KB (1103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6acce4a1df323ade11febca20e664df3454379e4a4d62367fda308fd3377a5b7`  
		Last Modified: Mon, 16 Mar 2026 22:43:45 GMT  
		Size: 827.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ceb4b68e89c0b0dc1a9dc9754d84e4fdcc68a054100397edf14eea9bb6cc12b`  
		Last Modified: Mon, 16 Mar 2026 22:43:46 GMT  
		Size: 6.4 MB (6442097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:300ea57bc8db031eb298c0be9439b59a132b01d16a7971119ccb7c917fbb6554`  
		Last Modified: Mon, 16 Mar 2026 22:43:45 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a7afc0484bbe3e1c40b997eebf00362bc5e5e5711f5533cb6ff54e22c2413b4`  
		Last Modified: Mon, 16 Mar 2026 22:43:46 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1` - unknown; unknown

```console
$ docker pull spiped@sha256:513effd7016736f664ccfba169fc4d2d2fbac9b2d09ae5c2427af606b4fef17d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3635335 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03f65e618603d756ec27e2173381823753cc22ece11b748008e7b4745130c1da`

```dockerfile
```

-	Layers:
	-	`sha256:5f750ca150313a2349433840e5c82fdef74358685b619d6b14e5b58e76f0781a`  
		Last Modified: Mon, 16 Mar 2026 22:43:46 GMT  
		Size: 3.6 MB (3620389 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:23ece012ebd2581aea85be27bbc3fe9da829f9ee6cb39f7e97a3637110ad5770`  
		Last Modified: Mon, 16 Mar 2026 22:43:45 GMT  
		Size: 14.9 KB (14946 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1` - linux; ppc64le

```console
$ docker pull spiped@sha256:558d9e854b92393e1d96ef6e4d632b42659ff94decbb53b76989997d1e0ec224
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.4 MB (40435868 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8fb525945e5b18678cd55fe712bfb5b6997167921072dfe24c99cc7441368efc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1773619200'
# Tue, 17 Mar 2026 01:48:02 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Tue, 17 Mar 2026 01:48:07 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 01:49:05 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Tue, 17 Mar 2026 01:49:05 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 17 Mar 2026 01:49:05 GMT
VOLUME [/spiped]
# Tue, 17 Mar 2026 01:49:05 GMT
WORKDIR /spiped
# Tue, 17 Mar 2026 01:49:06 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Tue, 17 Mar 2026 01:49:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Mar 2026 01:49:06 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:f078139432e0b368e27241df524f6ef0ed0148b217d7495670dc297af77699fb`  
		Last Modified: Mon, 16 Mar 2026 21:55:56 GMT  
		Size: 33.6 MB (33592834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b23cdd3695d4f8d7ed89e6ef14a27bade53f83dc908d0d81ca0e30631851657d`  
		Last Modified: Tue, 17 Mar 2026 01:49:20 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2aeba3f4cf41d1fe339b87612255223a740f20ca43890419c57f646a0d6b4700`  
		Last Modified: Tue, 17 Mar 2026 01:49:20 GMT  
		Size: 827.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2900931ab7a20d4ba700e41e56664ad7605eb9d341f250b7e024800c787b1f57`  
		Last Modified: Tue, 17 Mar 2026 01:49:20 GMT  
		Size: 6.8 MB (6840666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd461ff0c7b461bb5a3b5a2abf96ce3dec4858db537c1939b8bdfbe1fc8d1dac`  
		Last Modified: Tue, 17 Mar 2026 01:49:20 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8147ab40850402c527ecc2d439d4ce4dab6d232336aa43c20444dc18829f1273`  
		Last Modified: Tue, 17 Mar 2026 01:49:21 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1` - unknown; unknown

```console
$ docker pull spiped@sha256:f200a47fd65a47d561c18eabdbae5cd6d9935be2507254b566d43b48e6c57456
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3637027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f8f2b490d9a358d5a7fea9f4d29b4098981a442f93c062a3b276cf4357de8c3`

```dockerfile
```

-	Layers:
	-	`sha256:887ec06e855bee10271ac461e307cde47e3b0f61f873ebe04e4b7bd6687368f2`  
		Last Modified: Tue, 17 Mar 2026 01:49:20 GMT  
		Size: 3.6 MB (3621997 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:91f36846163a85b9df751c3b92a108c1257a4e2dac2c2e2f37c380787eb44d19`  
		Last Modified: Tue, 17 Mar 2026 01:49:20 GMT  
		Size: 15.0 KB (15030 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1` - linux; riscv64

```console
$ docker pull spiped@sha256:8bb82489fc130e0ebd5f9bbd52581be946042cfd96ea517ea76d5bc3bf8ebefb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.6 MB (37637359 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3782bede9d9edafc097d7e1829603f7130a6de5afd0278b055260b72c9dc1997`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1771804800'
# Thu, 26 Feb 2026 21:27:02 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Thu, 26 Feb 2026 21:27:31 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 26 Feb 2026 21:30:35 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Thu, 26 Feb 2026 21:30:35 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Thu, 26 Feb 2026 21:30:35 GMT
VOLUME [/spiped]
# Thu, 26 Feb 2026 21:30:36 GMT
WORKDIR /spiped
# Thu, 26 Feb 2026 21:30:36 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Thu, 26 Feb 2026 21:30:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 26 Feb 2026 21:30:36 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:7d614b9ad5a6f3dd0478c6903a6d2ffddc9bc5b17650714d4c1f761161fde58d`  
		Last Modified: Tue, 24 Feb 2026 18:59:14 GMT  
		Size: 28.3 MB (28276417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afbc2b651dc4281762485417954f26f00a147e635dd4386b4dc36ec1c12057b8`  
		Last Modified: Thu, 26 Feb 2026 21:31:48 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04ad29eaeb47daebdc8fd5d52da1dcf0f8ef0dd3a9f796c0f14675426e200e89`  
		Last Modified: Thu, 26 Feb 2026 21:31:48 GMT  
		Size: 822.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b04499c1af0fd231152f64530568de3e0fe490576c3d0bcf0c9743990a7938f7`  
		Last Modified: Thu, 26 Feb 2026 21:31:49 GMT  
		Size: 9.4 MB (9358576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19d9ae5d28f72fa67e546ccb83e7e39152304c5e1d393ceb17fee76009b87c30`  
		Last Modified: Thu, 26 Feb 2026 21:31:48 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c9afcb0cccd5e3f03a3850046642ebf8a8029bf602e5e5b8bd9422d3cf7b350`  
		Last Modified: Thu, 26 Feb 2026 21:31:49 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1` - unknown; unknown

```console
$ docker pull spiped@sha256:e5cf967432204ce7118f3ebbd169698a80d6df6bc23555049960d38da754a9d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3628397 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd419f8646942dcae52af9b19c3f390a9c3f6271d67369dcf6fc2c6b69d54b9d`

```dockerfile
```

-	Layers:
	-	`sha256:f67ba2453a68b55021d7f90d26cc1c990f9286371a00137c7cad53780d0559ba`  
		Last Modified: Thu, 26 Feb 2026 21:31:49 GMT  
		Size: 3.6 MB (3613367 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cf05fe9bfbfcb881eacb026a48af7d361ee01b63efce4a7f453d9c6fa4af7fa2`  
		Last Modified: Thu, 26 Feb 2026 21:31:48 GMT  
		Size: 15.0 KB (15030 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1` - linux; s390x

```console
$ docker pull spiped@sha256:c3ea82efea9854cb0da628935b60cf04f6c53931b6f7c2d20cd31aa9d27deaf0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.0 MB (35958813 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:579c56a7419832fa8be7ed9c8c7faaf68cb1da36770f667bfdce26ab4c03d59b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1773619200'
# Mon, 16 Mar 2026 23:43:38 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Mon, 16 Mar 2026 23:43:41 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 23:44:00 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Mon, 16 Mar 2026 23:44:00 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Mon, 16 Mar 2026 23:44:00 GMT
VOLUME [/spiped]
# Mon, 16 Mar 2026 23:44:00 GMT
WORKDIR /spiped
# Mon, 16 Mar 2026 23:44:00 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Mon, 16 Mar 2026 23:44:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 16 Mar 2026 23:44:00 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:2c02a3d3f135c4bbe56488921bd86d969a76dcd5278abca1e81884d3bff0bd88`  
		Last Modified: Mon, 16 Mar 2026 21:52:55 GMT  
		Size: 29.8 MB (29835265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c81e7613d635aa581f38ab946c2047e14837502a75f3f4e08fff5f611175fa1`  
		Last Modified: Mon, 16 Mar 2026 23:44:13 GMT  
		Size: 1.1 KB (1105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e7af70f2f5d7c87a4eef797de7cdee0fc7fe1f22a5cdd1d147f73cd11cd3c66`  
		Last Modified: Mon, 16 Mar 2026 23:44:13 GMT  
		Size: 828.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fc179ed0ea05be607a3fd6ab65992063b0b8fad92eba54e1abc2f376ad37586`  
		Last Modified: Mon, 16 Mar 2026 23:44:13 GMT  
		Size: 6.1 MB (6121184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97d07658b602778f575172b4841e370cbe43b5899cb54c7748a2978f0da94aae`  
		Last Modified: Mon, 16 Mar 2026 23:44:13 GMT  
		Size: 94.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2f0b086128c318c28efb4541b0c5264857fb53e45dd2a7cfc468fdf981146fe`  
		Last Modified: Mon, 16 Mar 2026 23:44:14 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1` - unknown; unknown

```console
$ docker pull spiped@sha256:ceb5259222252c09f46d1586c4beb858ae638bfa5623656db13b549d96d21d09
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3633605 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38f77179e2c665d2a86e12bc17bfedc7f450031d205ba7c907005662463dd141`

```dockerfile
```

-	Layers:
	-	`sha256:a6c5d5579933f8a016f12bcfd02838e397274cce0d8c07d3b637a90946cef6b9`  
		Last Modified: Mon, 16 Mar 2026 23:44:13 GMT  
		Size: 3.6 MB (3618623 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:39e9ea0d638105f70bced5f876f7ce8f9adcd4138140b8d5d517b41dd0e8974b`  
		Last Modified: Mon, 16 Mar 2026 23:44:13 GMT  
		Size: 15.0 KB (14982 bytes)  
		MIME: application/vnd.in-toto+json

## `spiped:1-alpine`

```console
$ docker pull spiped@sha256:2e861202f057586ae2e6dc3a5290d61949120d861e272b5700c1e30e1ae9774c
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
$ docker pull spiped@sha256:45aa25e16b20aaf22415c03717dfbffb2460250d93ccfbf50d304296f0323560
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3921849 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c42c3ad8f87ea2a2987c07857dc357c5caa6eb7fe68f8ab758c81d2c67f6316`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:40 GMT
ADD alpine-minirootfs-3.22.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:40 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:36:46 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Wed, 28 Jan 2026 02:36:47 GMT
RUN apk add --no-cache libssl3 # buildkit
# Wed, 28 Jan 2026 02:36:57 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Wed, 28 Jan 2026 02:36:57 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Wed, 28 Jan 2026 02:36:57 GMT
VOLUME [/spiped]
# Wed, 28 Jan 2026 02:36:57 GMT
WORKDIR /spiped
# Wed, 28 Jan 2026 02:36:57 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 02:36:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 02:36:57 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:d49a2dee86fb12766dd648402d010ca105846a41bd58738454e53780d4bb8e97`  
		Last Modified: Wed, 28 Jan 2026 01:18:46 GMT  
		Size: 3.8 MB (3804875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:255f2b198269941f9011d88cebad6e20b25c8054b5ac4ebd1b07f9750a69d255`  
		Last Modified: Wed, 28 Jan 2026 02:37:03 GMT  
		Size: 949.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed562f6049bf766f9af2aeb064224279b938162b44667a74bc7ca9c31ac1d70a`  
		Last Modified: Wed, 28 Jan 2026 02:37:03 GMT  
		Size: 7.9 KB (7945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d20d0ab7b6d45d1dbeebe557e32936e50678b9985769e6bd0ff3e1ff5e433e69`  
		Last Modified: Wed, 28 Jan 2026 02:37:03 GMT  
		Size: 107.6 KB (107647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:868415b885be47751e88ed3c97ca195abec55deffeb9f4ad2846ad3d25cdec28`  
		Last Modified: Wed, 28 Jan 2026 02:37:03 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7d8f030e4a64f48108d2120539708364c71dc39133649b15a0ad263ec9bfe40`  
		Last Modified: Wed, 28 Jan 2026 02:37:04 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:14bccfab21e7b3f36806b9521edfd711ef99c418ce1a38f2c913859e95caa2fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.5 KB (96451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e0f387ff25d96b6eec2a5942d1be095ce8d2cd8945dadefd293a3706d31ea69`

```dockerfile
```

-	Layers:
	-	`sha256:3abca7ed4aae68f57768d18d39b5d6b1c58a733af4507188677241020e39e0d9`  
		Last Modified: Wed, 28 Jan 2026 02:37:03 GMT  
		Size: 82.2 KB (82192 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bf6768ac276576d5f59511c63ded4afa12e2d77d28be7bffc6d1537d58bb57bb`  
		Last Modified: Wed, 28 Jan 2026 02:37:03 GMT  
		Size: 14.3 KB (14259 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1-alpine` - linux; arm variant v6

```console
$ docker pull spiped@sha256:3840e207c5f175385b57ca037766c41623e4a780197b93760ca83297bd8e51ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3603526 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f07ce0978d45ec15bdc0a08bdc59ff908f2bd78005af85d4bbad7345be081ee2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:06 GMT
ADD alpine-minirootfs-3.22.3-armhf.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:06 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:56:33 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Wed, 28 Jan 2026 02:56:34 GMT
RUN apk add --no-cache libssl3 # buildkit
# Wed, 28 Jan 2026 02:56:44 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Wed, 28 Jan 2026 02:56:44 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Wed, 28 Jan 2026 02:56:44 GMT
VOLUME [/spiped]
# Wed, 28 Jan 2026 02:56:44 GMT
WORKDIR /spiped
# Wed, 28 Jan 2026 02:56:44 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 02:56:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 02:56:44 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:835838571e5c80c63481753299e25a9f89f366d8f4a9c1a2043b8fdf98176f17`  
		Last Modified: Wed, 28 Jan 2026 01:18:10 GMT  
		Size: 3.5 MB (3505046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5a5ad93e4f03c704fabcd2728cb1ab8244c96ef0876f3fcc9779085a8d3be96`  
		Last Modified: Wed, 28 Jan 2026 02:56:48 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:092107d3ff0fcf3229ae39acf729a354fda97b10c713e7073d550bb7c69025bc`  
		Last Modified: Wed, 28 Jan 2026 02:56:48 GMT  
		Size: 7.9 KB (7944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcb00245db6ff8769dfa116d0e6194c8908449cd54b3995e5f0044b278d0fb45`  
		Last Modified: Wed, 28 Jan 2026 02:56:48 GMT  
		Size: 89.2 KB (89154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3375ee92dad5bd59b0dde03ad45bdf7a8f7df3aaa1e2847b17cdd6734893cfb8`  
		Last Modified: Wed, 28 Jan 2026 02:56:48 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc41431154f4cccb130328f9bda92ac3cd374c3bc4ef8b29827399ebd22bc749`  
		Last Modified: Wed, 28 Jan 2026 02:56:49 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:193c4ff5e06269d1446ab3235284aa43d244fdbc13dffdc98c715540fcc455e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.1 KB (14146 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:060b8b064e4aba529d56ef354367ffae940f6b152b36f64ea427dfcd51e51f1e`

```dockerfile
```

-	Layers:
	-	`sha256:9257c6b08dae939c45fb6b5cd969064dde84328d15653df8b0ab98dae6b31d32`  
		Last Modified: Wed, 28 Jan 2026 02:56:48 GMT  
		Size: 14.1 KB (14146 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1-alpine` - linux; arm variant v7

```console
$ docker pull spiped@sha256:71592cfee4b071cad3b52c3cfdefddd8ff72e3d5e644d8859d2d8cec8397a0d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3314649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c48ddb927471eeb09c0d2e183b02bb1074d36b5caa9dbd3477ee935a8eed01f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:29 GMT
ADD alpine-minirootfs-3.22.3-armv7.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:29 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:56:24 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Wed, 28 Jan 2026 02:56:25 GMT
RUN apk add --no-cache libssl3 # buildkit
# Wed, 28 Jan 2026 02:56:34 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Wed, 28 Jan 2026 02:56:34 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Wed, 28 Jan 2026 02:56:34 GMT
VOLUME [/spiped]
# Wed, 28 Jan 2026 02:56:34 GMT
WORKDIR /spiped
# Wed, 28 Jan 2026 02:56:34 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 02:56:34 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 02:56:34 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:caca1d0e2f8affe80569328af55c755a8480801c5ee912e55aaa828c8209aa6e`  
		Last Modified: Wed, 28 Jan 2026 01:18:35 GMT  
		Size: 3.2 MB (3223629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:332ba379620ebeacb95d57ee5ff3ce395b9868fe9f8d00a5b85dd41df19b3a23`  
		Last Modified: Wed, 28 Jan 2026 02:56:39 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:471e6c87dbde5f46d8cd1e26b6a653a7d77209c851df54df0c065355b1c36749`  
		Last Modified: Wed, 28 Jan 2026 02:56:39 GMT  
		Size: 8.0 KB (7952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:917e2b19aaa32cc304579e079305131ee112e7015524177e84f33379315c24f6`  
		Last Modified: Wed, 28 Jan 2026 02:56:39 GMT  
		Size: 81.7 KB (81685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9d229583db181996be822e85b4fe259ecd55350b04637a090977de317d8cb53`  
		Last Modified: Wed, 28 Jan 2026 02:56:39 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:283dd24da1a4b40bed9d28f9196f24341abf5ee8a13f180db2b3e6daa7e85b8d`  
		Last Modified: Wed, 28 Jan 2026 02:56:40 GMT  
		Size: 336.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:b0d30665b0b25a584022937647a82e260a99dc3822f06eae03c777c08c589459
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.6 KB (96590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5de7b9137b4705f6bfaa43d68be9ab47cda877656a88568a8b98eaecf834d723`

```dockerfile
```

-	Layers:
	-	`sha256:bf20f6c9425bc14bf83c368ad820cbac85037f9cfe9e8f428105dcae79aa5f0a`  
		Last Modified: Wed, 28 Jan 2026 02:56:39 GMT  
		Size: 82.2 KB (82228 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3c326467351e8aaa1070327395a8ce06feaf36e791288cc8d0efc059293853a6`  
		Last Modified: Wed, 28 Jan 2026 02:56:39 GMT  
		Size: 14.4 KB (14362 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1-alpine` - linux; arm64 variant v8

```console
$ docker pull spiped@sha256:effcfa5e900325dc5a9f2ce725d32bb928170b9fae13c2414035f7c74db4832d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4249465 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1129da21c1ac14cfe9747c51280fa104e3e2a4a7fb499fce9d2f79394c096e45`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:55 GMT
ADD alpine-minirootfs-3.22.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:55 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:37:44 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Wed, 28 Jan 2026 02:37:45 GMT
RUN apk add --no-cache libssl3 # buildkit
# Wed, 28 Jan 2026 02:37:55 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Wed, 28 Jan 2026 02:37:55 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Wed, 28 Jan 2026 02:37:55 GMT
VOLUME [/spiped]
# Wed, 28 Jan 2026 02:37:55 GMT
WORKDIR /spiped
# Wed, 28 Jan 2026 02:37:55 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 02:37:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 02:37:55 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:d741ee1608f399e21c72d05f0f818c348c6801af33aeb83523893d09dc153957`  
		Last Modified: Wed, 28 Jan 2026 01:18:00 GMT  
		Size: 4.1 MB (4139519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a215f43d3f31692bff6dbb7a8464a9777ff146fd6817d85616dd79d628db9a4e`  
		Last Modified: Wed, 28 Jan 2026 02:38:00 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a149826e8201bd60e39e8acb8c71ee749c537b2c783a541e04af7a7b3fc6b5d`  
		Last Modified: Wed, 28 Jan 2026 02:38:00 GMT  
		Size: 8.0 KB (7951 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3816514d66f19e4e15afc0dae177ea8f1397bbaeba0189b4a33a3f265afbb21`  
		Last Modified: Wed, 28 Jan 2026 02:38:00 GMT  
		Size: 100.6 KB (100615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f073eca19d0c28ea18c16d7aa1388a52393935ac0e76036549b53fca85d50741`  
		Last Modified: Wed, 28 Jan 2026 02:38:00 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56ae442366147b99273aabaaf180c7a0347dd957817ff21ec6495a8f374fd7b5`  
		Last Modified: Wed, 28 Jan 2026 02:38:01 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:20c426c97f5ccc77dcb4c2895905f7a3e9aedaf5bf12fbf4b3ff87748f7ebc74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.6 KB (96641 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f74a0ff8267a4110c62ab6dcdcf2bf4949f9f54a7ff5e5b96a7e78b99f9770c`

```dockerfile
```

-	Layers:
	-	`sha256:ce7e8f74c44956e8b3a9213e0686a5007c77ddc5cd5210760e512537c99dcb4f`  
		Last Modified: Wed, 28 Jan 2026 02:38:00 GMT  
		Size: 82.2 KB (82248 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5744a1e9a5178b40c2e43ceccdad37fa256e17fb5a7e73342aa361c38b071ea6`  
		Last Modified: Wed, 28 Jan 2026 02:38:00 GMT  
		Size: 14.4 KB (14393 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1-alpine` - linux; 386

```console
$ docker pull spiped@sha256:d29799b7499dd97718236dec910ca0fb21a58b93b04c13b9d32bd3972850d109
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3750150 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c829adab8d4ab1c5c9eef2ab8cd6fc3b09ac7a5b2c98b60eb750eaadcf3ca449`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:53 GMT
ADD alpine-minirootfs-3.22.3-x86.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:53 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:31:22 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Wed, 28 Jan 2026 02:31:22 GMT
RUN apk add --no-cache libssl3 # buildkit
# Wed, 28 Jan 2026 02:31:32 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Wed, 28 Jan 2026 02:31:32 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Wed, 28 Jan 2026 02:31:32 GMT
VOLUME [/spiped]
# Wed, 28 Jan 2026 02:31:32 GMT
WORKDIR /spiped
# Wed, 28 Jan 2026 02:31:32 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 02:31:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 02:31:32 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:757a99eda61f22434071cfbc7a70f9526b63aeb5479a64272982017ee7cd9cfd`  
		Last Modified: Wed, 28 Jan 2026 01:18:59 GMT  
		Size: 3.6 MB (3620732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2088b329d71531fcaf8b6b6b5fb05bd132488a9b146463fda72d73f3b193da77`  
		Last Modified: Wed, 28 Jan 2026 02:31:36 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df6327ced333146d36cce9bad13d15f14d00cfba342ef14347eb76323f377623`  
		Last Modified: Wed, 28 Jan 2026 02:31:37 GMT  
		Size: 7.9 KB (7940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3f74692486d32e3c25efb4bcdbdd450b58db493d05a003140a026ba85c130a6`  
		Last Modified: Wed, 28 Jan 2026 02:31:36 GMT  
		Size: 120.1 KB (120096 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b377c56ed7e39aeec7320819a810cd8637819dc2c7f00e5f02f6008223d5ed8`  
		Last Modified: Wed, 28 Jan 2026 02:31:37 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e023ec54765d4d3764e0855b6d7cfe0e2f9966db68bd933fe3f4fe6c41a2474f`  
		Last Modified: Wed, 28 Jan 2026 02:31:38 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:49494f0bf8ea2a9ac91bc338facd2f7cede025b28b7848656878d7ce0deadf5c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.4 KB (96390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16387e224ee0b4762e3111436b2fdc3a8bfebe61d796cc65af094da1ebf76cd0`

```dockerfile
```

-	Layers:
	-	`sha256:bdc547d749394448a39cd679c285ba250424589df32f26c116cdc3bca37fedf9`  
		Last Modified: Wed, 28 Jan 2026 02:31:36 GMT  
		Size: 82.2 KB (82167 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4f968b5a19cf7dfb341a81ce64526ba67dbdecae7dbd82f7332ab1f24bf7e26a`  
		Last Modified: Wed, 28 Jan 2026 02:31:36 GMT  
		Size: 14.2 KB (14223 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1-alpine` - linux; ppc64le

```console
$ docker pull spiped@sha256:ec49e51d1b31aef6ee4c32cbd2374c5115032febd535905c0146f19ca7d1b88c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3856312 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c52e05f6841b2c0f9dcb913e52c349b3ec2747c75f53e9b3d6a41cd3c6103a9d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:35 GMT
ADD alpine-minirootfs-3.22.3-ppc64le.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:35 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 03:59:19 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Wed, 28 Jan 2026 03:59:21 GMT
RUN apk add --no-cache libssl3 # buildkit
# Wed, 28 Jan 2026 03:59:33 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Wed, 28 Jan 2026 03:59:33 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Wed, 28 Jan 2026 03:59:33 GMT
VOLUME [/spiped]
# Wed, 28 Jan 2026 03:59:33 GMT
WORKDIR /spiped
# Wed, 28 Jan 2026 03:59:34 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 03:59:34 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 03:59:34 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:d7b7d5bab08f20b53e85395b2d6e793469e3acdbe8644bd234992524588b440f`  
		Last Modified: Wed, 28 Jan 2026 01:17:44 GMT  
		Size: 3.7 MB (3734297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52389dd33bb155b2c78fa5202c8c9909e97b12049d41f7cb5369100d2a7be819`  
		Last Modified: Wed, 28 Jan 2026 03:59:48 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28fd5646a7c2ce724b02160a31080c85b3571ffddbc309ccb39fb23e5075d4aa`  
		Last Modified: Wed, 28 Jan 2026 03:59:47 GMT  
		Size: 8.0 KB (7956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d83f042b4cb936ae2f704768b0462b7f539ba799143799dc6a8ce0babc73884`  
		Last Modified: Wed, 28 Jan 2026 03:59:48 GMT  
		Size: 112.7 KB (112673 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b77f4a6884030927f7cdd451b10bba40c6cf61fd40534ca3a9cf653bb742ea8f`  
		Last Modified: Wed, 28 Jan 2026 03:59:48 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34fbfb80739dd4ce26eb065be080a75c602340f3242a297925caf40baf400db0`  
		Last Modified: Wed, 28 Jan 2026 03:59:49 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:1d08517919e2dfe608c1e408886b7ef4659cd9f15bf49a67583fe931eb307650
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.6 KB (94578 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b68d34137d518c2381ecd841ecef0a23786265f08c1952e0ed2134cc2ba9073`

```dockerfile
```

-	Layers:
	-	`sha256:b57bb2bf93c55cd637df776032387ee2beae0039a87bacf4e588dd43aaa36711`  
		Last Modified: Wed, 28 Jan 2026 03:59:48 GMT  
		Size: 80.3 KB (80275 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e4a73d72709b0315e9f657137bb6dbf7c0679131d8e10876ea8a1bb94e4201b4`  
		Last Modified: Wed, 28 Jan 2026 03:59:48 GMT  
		Size: 14.3 KB (14303 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1-alpine` - linux; riscv64

```console
$ docker pull spiped@sha256:0e7e07e5944d0951da4949f8298cdccfa6ec9395c2d0ddf983aa7f40bf7807f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3625620 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00565f6907e5ae385b224d048c255c22407d6a59d79533da4912c486d4ee1360`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 28 Jan 2026 03:49:43 GMT
ADD alpine-minirootfs-3.22.3-riscv64.tar.gz / # buildkit
# Wed, 28 Jan 2026 03:49:43 GMT
CMD ["/bin/sh"]
# Thu, 29 Jan 2026 18:56:58 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Thu, 29 Jan 2026 18:57:02 GMT
RUN apk add --no-cache libssl3 # buildkit
# Thu, 29 Jan 2026 18:58:38 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Thu, 29 Jan 2026 18:58:38 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Thu, 29 Jan 2026 18:58:38 GMT
VOLUME [/spiped]
# Thu, 29 Jan 2026 18:58:39 GMT
WORKDIR /spiped
# Thu, 29 Jan 2026 18:58:39 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Thu, 29 Jan 2026 18:58:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 29 Jan 2026 18:58:39 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:15ea87d2370d91334d14e1cb46366adb6a57bbae717f07f8c9f55735cf137f62`  
		Last Modified: Wed, 28 Jan 2026 03:50:15 GMT  
		Size: 3.5 MB (3517422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c85b2fc2b9bdc2a30eea3483d034231cba4cf794b774e9c668e43189f965204b`  
		Last Modified: Thu, 29 Jan 2026 18:58:59 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7a35d458c7098a7c5f24f347a75cf6930f742a2e14ae40067defc23e63d57b5`  
		Last Modified: Thu, 29 Jan 2026 18:58:59 GMT  
		Size: 7.9 KB (7944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fbbaf165e7e5cf59739b8e5317789f9a907da0dc26f3803ae533e05f7a2068e`  
		Last Modified: Thu, 29 Jan 2026 18:58:59 GMT  
		Size: 98.9 KB (98867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15e0973003e6d2e757a9f14bfb9ab4d4b6be0abf8bbdfa7a9b699232646e0df6`  
		Last Modified: Thu, 29 Jan 2026 18:58:59 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8509faeca8d8af4689f4b76d19f92f0deeb48d08e62ab656d5ad988fe97b48e9`  
		Last Modified: Thu, 29 Jan 2026 18:59:00 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:45c5a2bccce0c2d968718cdc5b92e2d54486ce35d6f21169c8e2975138906721
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.6 KB (94575 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3828726b576d70b513dac001f2810887cf67c235a77086291ebdeb6df7a249f`

```dockerfile
```

-	Layers:
	-	`sha256:53e8f0117ebdf17125860003417afad58a90f091d2b04b6763e9b4ce1899228b`  
		Last Modified: Thu, 29 Jan 2026 18:58:59 GMT  
		Size: 80.3 KB (80271 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0edfbeca58a13ce30fdd21ef302873aa05c28498d058231b777fe51653a06eb6`  
		Last Modified: Thu, 29 Jan 2026 18:58:59 GMT  
		Size: 14.3 KB (14304 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1-alpine` - linux; s390x

```console
$ docker pull spiped@sha256:0aeb96b9c7c968a0ad51a4c785e0c76534a115d395c587eacd587a3aad55b360
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3756697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b72691935166b1882b3040950315ed19d9cf1a3678909a868fa5c27a1a58e2b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:06 GMT
ADD alpine-minirootfs-3.22.3-s390x.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:06 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 03:05:47 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Wed, 28 Jan 2026 03:05:48 GMT
RUN apk add --no-cache libssl3 # buildkit
# Wed, 28 Jan 2026 03:05:55 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Wed, 28 Jan 2026 03:05:55 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Wed, 28 Jan 2026 03:05:55 GMT
VOLUME [/spiped]
# Wed, 28 Jan 2026 03:05:55 GMT
WORKDIR /spiped
# Wed, 28 Jan 2026 03:05:55 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 03:05:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 03:05:55 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:dab48b8d1bab09fede3f54264828e67466f10d64acc37d9412190034dbcbf61f`  
		Last Modified: Wed, 28 Jan 2026 01:17:16 GMT  
		Size: 3.7 MB (3650434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0789ee1817b07966cd80a07b05a82d8e0c9bf85f6053f4955ac4731e47448ad`  
		Last Modified: Wed, 28 Jan 2026 03:06:03 GMT  
		Size: 949.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e526c5a7e2d6f02b24c7ed3860ec8221dcd7d0c6e4112d267da6729a13890448`  
		Last Modified: Wed, 28 Jan 2026 03:06:03 GMT  
		Size: 7.9 KB (7949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f10bca7622d69f6335c554b1c8cec2a82753df66ed9cf072d635820439e1af3c`  
		Last Modified: Wed, 28 Jan 2026 03:06:03 GMT  
		Size: 96.9 KB (96933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81d81cea7ec993f5c76e72bd06b1579e878f6a4d1a4a2f11114f710747ef40d4`  
		Last Modified: Wed, 28 Jan 2026 03:06:03 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:086ab53d5ebb5741d97d120d1a1ad7797bf2fda46a7ff1f9a033efa0117cd233`  
		Last Modified: Wed, 28 Jan 2026 03:06:04 GMT  
		Size: 336.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:c32f5675d459d866b7c69b2159549861b770e81fa270485088e909f23c515b9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.5 KB (94497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a76bce779a8727519c7fb65566c2ce929337d21a3d6addd2f301cd51f95516c4`

```dockerfile
```

-	Layers:
	-	`sha256:85780af5cccece93dbeac028f8517ebc14f3298ca69ddd75bcf80809c0ea3432`  
		Last Modified: Wed, 28 Jan 2026 03:06:03 GMT  
		Size: 80.2 KB (80241 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:797300601f0f43bd14d2b3e327c7100b2a1b8356e4290096f308e710af773718`  
		Last Modified: Wed, 28 Jan 2026 03:06:03 GMT  
		Size: 14.3 KB (14256 bytes)  
		MIME: application/vnd.in-toto+json

## `spiped:1.6`

```console
$ docker pull spiped@sha256:86bfe9d75887a0c865ca400bce9556e55f0100324ab12cea4182325b4538c9d3
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
$ docker pull spiped@sha256:1dadd78b37a53143babab424620b268d0e87665451c7e0b19ee714350efeb0aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.8 MB (36825645 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6aec690f0b7647a2b707058d20c805804b9d29cdd158eb3109584ae64c2e9c96`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1773619200'
# Mon, 16 Mar 2026 22:35:50 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Mon, 16 Mar 2026 22:35:52 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:36:17 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Mon, 16 Mar 2026 22:36:17 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Mon, 16 Mar 2026 22:36:17 GMT
VOLUME [/spiped]
# Mon, 16 Mar 2026 22:36:17 GMT
WORKDIR /spiped
# Mon, 16 Mar 2026 22:36:17 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Mon, 16 Mar 2026 22:36:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 16 Mar 2026 22:36:17 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:ec781dee3f4719c2ca0dd9e73cb1d4ed834ed1a406495eb6e44b6dfaad5d1f8f`  
		Last Modified: Mon, 16 Mar 2026 21:53:19 GMT  
		Size: 29.8 MB (29775500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32ceac9107a69b7bfdee6e7660e1eff3feb8d0fd5d6f681f2a6ad1905d93ba0a`  
		Last Modified: Mon, 16 Mar 2026 22:36:24 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1aa4948bacb0a02611ec173cb9f157bd247587fd13cb63e407219ba6dd87af7d`  
		Last Modified: Mon, 16 Mar 2026 22:36:24 GMT  
		Size: 828.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50f472851b739f36f98249e60dba4ceb8a571cbd9f18c3e6b9639215d2c6dcfa`  
		Last Modified: Mon, 16 Mar 2026 22:36:24 GMT  
		Size: 7.0 MB (7047777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7dda7601460289f11e5d3db99f3c14ac9bf518a829bc22ae224a96c8c3a4d4d9`  
		Last Modified: Mon, 16 Mar 2026 22:36:24 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:597b8eb9fa679d5997894aab7d18f62d615b6cc715de0c0a98c8bddef96e43ee`  
		Last Modified: Mon, 16 Mar 2026 22:36:25 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6` - unknown; unknown

```console
$ docker pull spiped@sha256:24038ff42b84801b0e2af5de324e185ffb9b47e091947a1d6ead4da071277394
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3641241 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:204d83d1b596e75d2d7efdfccf8e0ab85c3bf694d7310417d68e3add5e86a10f`

```dockerfile
```

-	Layers:
	-	`sha256:1f60bdfcbc8114aba716d733f2c08d28946d1d47510ef32f11fe773e7efbba8c`  
		Last Modified: Mon, 16 Mar 2026 22:36:24 GMT  
		Size: 3.6 MB (3626260 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b07a02dacfe5fad817dc8acef6300290b65922a87b426e54f70d87798a0696f5`  
		Last Modified: Mon, 16 Mar 2026 22:36:24 GMT  
		Size: 15.0 KB (14981 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6` - linux; arm variant v5

```console
$ docker pull spiped@sha256:d76bab68c9ba80d6bde9b766de2f4b524b29b2e06796dea03aa1f86973b6e402
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.7 MB (33735071 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e9ce3fe44b3195308782999982dffb0e0324f65968051303e6d0ccb5e46710e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1773619200'
# Mon, 16 Mar 2026 23:15:44 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Mon, 16 Mar 2026 23:15:49 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 23:16:15 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Mon, 16 Mar 2026 23:16:15 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Mon, 16 Mar 2026 23:16:15 GMT
VOLUME [/spiped]
# Mon, 16 Mar 2026 23:16:15 GMT
WORKDIR /spiped
# Mon, 16 Mar 2026 23:16:15 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Mon, 16 Mar 2026 23:16:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 16 Mar 2026 23:16:15 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:eb1defba38d0de4655b895d4763345b3ab078983d3385db43c308a7caca13f2a`  
		Last Modified: Mon, 16 Mar 2026 21:52:26 GMT  
		Size: 27.9 MB (27943649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9cfc1da50f0fc66e4696a6b249cf2c9f19d773fda1096f22c619e19221b8de7`  
		Last Modified: Mon, 16 Mar 2026 23:16:22 GMT  
		Size: 1.1 KB (1105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a98c3d3f9d3a820c9fbfddae7bba53067abc005cb4837355fd2fe02be5159fda`  
		Last Modified: Mon, 16 Mar 2026 23:16:22 GMT  
		Size: 831.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:981177ab397ef56ea1a515604977b4812a8bccc0e0ae76b96ba1a148b66278c5`  
		Last Modified: Mon, 16 Mar 2026 23:16:22 GMT  
		Size: 5.8 MB (5789053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8116b26167b41dbbadb8f30d9738528a34e2436086fd1d12d6d83af070f87911`  
		Last Modified: Mon, 16 Mar 2026 23:16:22 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8f7d349acecae8a4190b1310446bb378d3edc921d84f55ac12cf5202b8df556`  
		Last Modified: Mon, 16 Mar 2026 23:16:23 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6` - unknown; unknown

```console
$ docker pull spiped@sha256:1ef3cb6065e7ec1c89ec491fd9bfd3dc5b3221edc45b98e1d076dc81f408837e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3634342 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6758a2f7ff038f8df9fc87c6f4130ff4358acd576e0e39211c178068863796cc`

```dockerfile
```

-	Layers:
	-	`sha256:5a7c54557652f62feaed177546a18b57a4e82674763bde13f27b1dab19e00b9d`  
		Last Modified: Mon, 16 Mar 2026 23:16:23 GMT  
		Size: 3.6 MB (3619254 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:647540c448bfbe8c1ba0711adf24d3a530725e84f4fd25c88632cf2510d9c007`  
		Last Modified: Mon, 16 Mar 2026 23:16:22 GMT  
		Size: 15.1 KB (15088 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6` - linux; arm variant v7

```console
$ docker pull spiped@sha256:723ba9f91b55f3576b2113c495e19f93cb621ee72fabcaff1531301fbcaa4b1a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.8 MB (31796429 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5cb0e019fca22ad836d890087ee6d2a180105ee1191adf83d36a753ea37941a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1773619200'
# Mon, 16 Mar 2026 23:17:41 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Mon, 16 Mar 2026 23:17:45 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 23:18:07 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Mon, 16 Mar 2026 23:18:07 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Mon, 16 Mar 2026 23:18:07 GMT
VOLUME [/spiped]
# Mon, 16 Mar 2026 23:18:07 GMT
WORKDIR /spiped
# Mon, 16 Mar 2026 23:18:07 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Mon, 16 Mar 2026 23:18:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 16 Mar 2026 23:18:07 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:7d73604d2a042e7beeb809f68c76f5be3576747809bfaa49747f334227d8d250`  
		Last Modified: Mon, 16 Mar 2026 21:53:24 GMT  
		Size: 26.2 MB (26209505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:658299db6ef3056cf755c844791cbd82e4508468df390e37a8aad706f3a48f4c`  
		Last Modified: Mon, 16 Mar 2026 23:18:14 GMT  
		Size: 1.1 KB (1103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8faf32f19b630a82f84ed9470b862ab68393803b1e37f045f46258e8890f7d50`  
		Last Modified: Mon, 16 Mar 2026 23:18:14 GMT  
		Size: 828.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba29f29a0220be91155a5596cf59a8ec1e848dc1c59089563006ce592b99f829`  
		Last Modified: Mon, 16 Mar 2026 23:18:14 GMT  
		Size: 5.6 MB (5584559 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:571f3aa9916ae33f81a8eff41f15615107662751591ab2cae13c31339f2cdb35`  
		Last Modified: Mon, 16 Mar 2026 23:18:14 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0023499b415317d80739286a45ec7393c98ddc05a638d045c05812141aa28b0`  
		Last Modified: Mon, 16 Mar 2026 23:18:15 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6` - unknown; unknown

```console
$ docker pull spiped@sha256:b778f2f8e613351de55fec9efa1c2283e7262e815379cb9c01090839b522f03b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3633463 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:820126e67739682404e3e543b661db54a249ad7238843089922bd27097f59140`

```dockerfile
```

-	Layers:
	-	`sha256:34fdc3e15f493cc5e996b5a867605ede0f868b1b23e1156f69a1d24198213663`  
		Last Modified: Mon, 16 Mar 2026 23:18:14 GMT  
		Size: 3.6 MB (3618375 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7867a53cd4efb0b6f41304907e82351cc690be89532e8db042be1139471fee68`  
		Last Modified: Mon, 16 Mar 2026 23:18:14 GMT  
		Size: 15.1 KB (15088 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6` - linux; arm64 variant v8

```console
$ docker pull spiped@sha256:4ae6755ad03f743b18a351fbafa71c65c711f58faea3a81b665befd8567053b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.4 MB (36374360 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0fbe5e7be982e3e0a47d2310365b2015977222cf3f9135331a2ddafbc2a09e29`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1773619200'
# Mon, 16 Mar 2026 22:38:29 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Mon, 16 Mar 2026 22:38:32 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:38:55 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Mon, 16 Mar 2026 22:38:55 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Mon, 16 Mar 2026 22:38:55 GMT
VOLUME [/spiped]
# Mon, 16 Mar 2026 22:38:55 GMT
WORKDIR /spiped
# Mon, 16 Mar 2026 22:38:55 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Mon, 16 Mar 2026 22:38:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 16 Mar 2026 22:38:55 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:f4badedbec24858ef2dc51256f6418328e305e9c3c5a5e093581f83425618bd5`  
		Last Modified: Mon, 16 Mar 2026 21:53:04 GMT  
		Size: 30.1 MB (30138416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59eb94c76468927e4e914285fecca640b78cd857ba3998fcfc270e51a5999a76`  
		Last Modified: Mon, 16 Mar 2026 22:39:02 GMT  
		Size: 1.1 KB (1104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11b2a5c6f2a1a593d60739bde8e5edb5ede5cc1c07d169f19ef39a67402cd65b`  
		Last Modified: Mon, 16 Mar 2026 22:39:02 GMT  
		Size: 828.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bedfccd6793021acdd75a491c31f9164e9dc33b3e7429226d6093a2dd780093`  
		Last Modified: Mon, 16 Mar 2026 22:39:03 GMT  
		Size: 6.2 MB (6233579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b277914700ac4bb0336072358245beede0af746b61ba9febb726f5a24443909`  
		Last Modified: Mon, 16 Mar 2026 22:39:03 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fcc46f0d3ebea317699d8e2e6d3e2c8d2e022621162b4aeb23e6aec0d21d6f3`  
		Last Modified: Mon, 16 Mar 2026 22:39:03 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6` - unknown; unknown

```console
$ docker pull spiped@sha256:3bb60c38b60da93affbf4a161bd60f5d201524ab747841166084d1e18235b678
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3636412 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:acfdeacc136a94cefd95b5fc4a223865929593d17a4df005eb979067d4539f09`

```dockerfile
```

-	Layers:
	-	`sha256:da2db9f7e9ec3796af7d7b3c2062fb98cdf3bf4c8cbc30041368b9529682b6e4`  
		Last Modified: Mon, 16 Mar 2026 22:39:03 GMT  
		Size: 3.6 MB (3621296 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c581a66bb5f391583c1fd9137f24523cc1f7cfb6e13f4dca2a22a36d28db1f75`  
		Last Modified: Mon, 16 Mar 2026 22:39:02 GMT  
		Size: 15.1 KB (15116 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6` - linux; 386

```console
$ docker pull spiped@sha256:44d93dff5b665eb236d8d461091f645401dad4215fc6e748e75d845e5f88359a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.7 MB (37735593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b145875baf2722671a7d04cbdec8ce2e4e0044fe83f4480f7d13be40ef1b7f0d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1773619200'
# Mon, 16 Mar 2026 22:43:15 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Mon, 16 Mar 2026 22:43:17 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:43:39 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Mon, 16 Mar 2026 22:43:39 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Mon, 16 Mar 2026 22:43:39 GMT
VOLUME [/spiped]
# Mon, 16 Mar 2026 22:43:39 GMT
WORKDIR /spiped
# Mon, 16 Mar 2026 22:43:39 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Mon, 16 Mar 2026 22:43:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 16 Mar 2026 22:43:39 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:2c0c3f3238f3d4cecd93e4dee6eda788943ef955de61c3ad4ff659da1f43ba60`  
		Last Modified: Mon, 16 Mar 2026 21:53:39 GMT  
		Size: 31.3 MB (31291132 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e26822c10be4229a362fafa19cf7744d8e4afd786250bc983de1db93de19f3ff`  
		Last Modified: Mon, 16 Mar 2026 22:43:45 GMT  
		Size: 1.1 KB (1103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6acce4a1df323ade11febca20e664df3454379e4a4d62367fda308fd3377a5b7`  
		Last Modified: Mon, 16 Mar 2026 22:43:45 GMT  
		Size: 827.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ceb4b68e89c0b0dc1a9dc9754d84e4fdcc68a054100397edf14eea9bb6cc12b`  
		Last Modified: Mon, 16 Mar 2026 22:43:46 GMT  
		Size: 6.4 MB (6442097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:300ea57bc8db031eb298c0be9439b59a132b01d16a7971119ccb7c917fbb6554`  
		Last Modified: Mon, 16 Mar 2026 22:43:45 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a7afc0484bbe3e1c40b997eebf00362bc5e5e5711f5533cb6ff54e22c2413b4`  
		Last Modified: Mon, 16 Mar 2026 22:43:46 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6` - unknown; unknown

```console
$ docker pull spiped@sha256:513effd7016736f664ccfba169fc4d2d2fbac9b2d09ae5c2427af606b4fef17d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3635335 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03f65e618603d756ec27e2173381823753cc22ece11b748008e7b4745130c1da`

```dockerfile
```

-	Layers:
	-	`sha256:5f750ca150313a2349433840e5c82fdef74358685b619d6b14e5b58e76f0781a`  
		Last Modified: Mon, 16 Mar 2026 22:43:46 GMT  
		Size: 3.6 MB (3620389 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:23ece012ebd2581aea85be27bbc3fe9da829f9ee6cb39f7e97a3637110ad5770`  
		Last Modified: Mon, 16 Mar 2026 22:43:45 GMT  
		Size: 14.9 KB (14946 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6` - linux; ppc64le

```console
$ docker pull spiped@sha256:558d9e854b92393e1d96ef6e4d632b42659ff94decbb53b76989997d1e0ec224
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.4 MB (40435868 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8fb525945e5b18678cd55fe712bfb5b6997167921072dfe24c99cc7441368efc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1773619200'
# Tue, 17 Mar 2026 01:48:02 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Tue, 17 Mar 2026 01:48:07 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 01:49:05 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Tue, 17 Mar 2026 01:49:05 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 17 Mar 2026 01:49:05 GMT
VOLUME [/spiped]
# Tue, 17 Mar 2026 01:49:05 GMT
WORKDIR /spiped
# Tue, 17 Mar 2026 01:49:06 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Tue, 17 Mar 2026 01:49:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Mar 2026 01:49:06 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:f078139432e0b368e27241df524f6ef0ed0148b217d7495670dc297af77699fb`  
		Last Modified: Mon, 16 Mar 2026 21:55:56 GMT  
		Size: 33.6 MB (33592834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b23cdd3695d4f8d7ed89e6ef14a27bade53f83dc908d0d81ca0e30631851657d`  
		Last Modified: Tue, 17 Mar 2026 01:49:20 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2aeba3f4cf41d1fe339b87612255223a740f20ca43890419c57f646a0d6b4700`  
		Last Modified: Tue, 17 Mar 2026 01:49:20 GMT  
		Size: 827.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2900931ab7a20d4ba700e41e56664ad7605eb9d341f250b7e024800c787b1f57`  
		Last Modified: Tue, 17 Mar 2026 01:49:20 GMT  
		Size: 6.8 MB (6840666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd461ff0c7b461bb5a3b5a2abf96ce3dec4858db537c1939b8bdfbe1fc8d1dac`  
		Last Modified: Tue, 17 Mar 2026 01:49:20 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8147ab40850402c527ecc2d439d4ce4dab6d232336aa43c20444dc18829f1273`  
		Last Modified: Tue, 17 Mar 2026 01:49:21 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6` - unknown; unknown

```console
$ docker pull spiped@sha256:f200a47fd65a47d561c18eabdbae5cd6d9935be2507254b566d43b48e6c57456
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3637027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f8f2b490d9a358d5a7fea9f4d29b4098981a442f93c062a3b276cf4357de8c3`

```dockerfile
```

-	Layers:
	-	`sha256:887ec06e855bee10271ac461e307cde47e3b0f61f873ebe04e4b7bd6687368f2`  
		Last Modified: Tue, 17 Mar 2026 01:49:20 GMT  
		Size: 3.6 MB (3621997 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:91f36846163a85b9df751c3b92a108c1257a4e2dac2c2e2f37c380787eb44d19`  
		Last Modified: Tue, 17 Mar 2026 01:49:20 GMT  
		Size: 15.0 KB (15030 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6` - linux; riscv64

```console
$ docker pull spiped@sha256:8bb82489fc130e0ebd5f9bbd52581be946042cfd96ea517ea76d5bc3bf8ebefb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.6 MB (37637359 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3782bede9d9edafc097d7e1829603f7130a6de5afd0278b055260b72c9dc1997`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1771804800'
# Thu, 26 Feb 2026 21:27:02 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Thu, 26 Feb 2026 21:27:31 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 26 Feb 2026 21:30:35 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Thu, 26 Feb 2026 21:30:35 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Thu, 26 Feb 2026 21:30:35 GMT
VOLUME [/spiped]
# Thu, 26 Feb 2026 21:30:36 GMT
WORKDIR /spiped
# Thu, 26 Feb 2026 21:30:36 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Thu, 26 Feb 2026 21:30:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 26 Feb 2026 21:30:36 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:7d614b9ad5a6f3dd0478c6903a6d2ffddc9bc5b17650714d4c1f761161fde58d`  
		Last Modified: Tue, 24 Feb 2026 18:59:14 GMT  
		Size: 28.3 MB (28276417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afbc2b651dc4281762485417954f26f00a147e635dd4386b4dc36ec1c12057b8`  
		Last Modified: Thu, 26 Feb 2026 21:31:48 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04ad29eaeb47daebdc8fd5d52da1dcf0f8ef0dd3a9f796c0f14675426e200e89`  
		Last Modified: Thu, 26 Feb 2026 21:31:48 GMT  
		Size: 822.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b04499c1af0fd231152f64530568de3e0fe490576c3d0bcf0c9743990a7938f7`  
		Last Modified: Thu, 26 Feb 2026 21:31:49 GMT  
		Size: 9.4 MB (9358576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19d9ae5d28f72fa67e546ccb83e7e39152304c5e1d393ceb17fee76009b87c30`  
		Last Modified: Thu, 26 Feb 2026 21:31:48 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c9afcb0cccd5e3f03a3850046642ebf8a8029bf602e5e5b8bd9422d3cf7b350`  
		Last Modified: Thu, 26 Feb 2026 21:31:49 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6` - unknown; unknown

```console
$ docker pull spiped@sha256:e5cf967432204ce7118f3ebbd169698a80d6df6bc23555049960d38da754a9d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3628397 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd419f8646942dcae52af9b19c3f390a9c3f6271d67369dcf6fc2c6b69d54b9d`

```dockerfile
```

-	Layers:
	-	`sha256:f67ba2453a68b55021d7f90d26cc1c990f9286371a00137c7cad53780d0559ba`  
		Last Modified: Thu, 26 Feb 2026 21:31:49 GMT  
		Size: 3.6 MB (3613367 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cf05fe9bfbfcb881eacb026a48af7d361ee01b63efce4a7f453d9c6fa4af7fa2`  
		Last Modified: Thu, 26 Feb 2026 21:31:48 GMT  
		Size: 15.0 KB (15030 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6` - linux; s390x

```console
$ docker pull spiped@sha256:c3ea82efea9854cb0da628935b60cf04f6c53931b6f7c2d20cd31aa9d27deaf0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.0 MB (35958813 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:579c56a7419832fa8be7ed9c8c7faaf68cb1da36770f667bfdce26ab4c03d59b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1773619200'
# Mon, 16 Mar 2026 23:43:38 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Mon, 16 Mar 2026 23:43:41 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 23:44:00 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Mon, 16 Mar 2026 23:44:00 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Mon, 16 Mar 2026 23:44:00 GMT
VOLUME [/spiped]
# Mon, 16 Mar 2026 23:44:00 GMT
WORKDIR /spiped
# Mon, 16 Mar 2026 23:44:00 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Mon, 16 Mar 2026 23:44:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 16 Mar 2026 23:44:00 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:2c02a3d3f135c4bbe56488921bd86d969a76dcd5278abca1e81884d3bff0bd88`  
		Last Modified: Mon, 16 Mar 2026 21:52:55 GMT  
		Size: 29.8 MB (29835265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c81e7613d635aa581f38ab946c2047e14837502a75f3f4e08fff5f611175fa1`  
		Last Modified: Mon, 16 Mar 2026 23:44:13 GMT  
		Size: 1.1 KB (1105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e7af70f2f5d7c87a4eef797de7cdee0fc7fe1f22a5cdd1d147f73cd11cd3c66`  
		Last Modified: Mon, 16 Mar 2026 23:44:13 GMT  
		Size: 828.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fc179ed0ea05be607a3fd6ab65992063b0b8fad92eba54e1abc2f376ad37586`  
		Last Modified: Mon, 16 Mar 2026 23:44:13 GMT  
		Size: 6.1 MB (6121184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97d07658b602778f575172b4841e370cbe43b5899cb54c7748a2978f0da94aae`  
		Last Modified: Mon, 16 Mar 2026 23:44:13 GMT  
		Size: 94.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2f0b086128c318c28efb4541b0c5264857fb53e45dd2a7cfc468fdf981146fe`  
		Last Modified: Mon, 16 Mar 2026 23:44:14 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6` - unknown; unknown

```console
$ docker pull spiped@sha256:ceb5259222252c09f46d1586c4beb858ae638bfa5623656db13b549d96d21d09
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3633605 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38f77179e2c665d2a86e12bc17bfedc7f450031d205ba7c907005662463dd141`

```dockerfile
```

-	Layers:
	-	`sha256:a6c5d5579933f8a016f12bcfd02838e397274cce0d8c07d3b637a90946cef6b9`  
		Last Modified: Mon, 16 Mar 2026 23:44:13 GMT  
		Size: 3.6 MB (3618623 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:39e9ea0d638105f70bced5f876f7ce8f9adcd4138140b8d5d517b41dd0e8974b`  
		Last Modified: Mon, 16 Mar 2026 23:44:13 GMT  
		Size: 15.0 KB (14982 bytes)  
		MIME: application/vnd.in-toto+json

## `spiped:1.6-alpine`

```console
$ docker pull spiped@sha256:2e861202f057586ae2e6dc3a5290d61949120d861e272b5700c1e30e1ae9774c
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
$ docker pull spiped@sha256:45aa25e16b20aaf22415c03717dfbffb2460250d93ccfbf50d304296f0323560
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3921849 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c42c3ad8f87ea2a2987c07857dc357c5caa6eb7fe68f8ab758c81d2c67f6316`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:40 GMT
ADD alpine-minirootfs-3.22.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:40 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:36:46 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Wed, 28 Jan 2026 02:36:47 GMT
RUN apk add --no-cache libssl3 # buildkit
# Wed, 28 Jan 2026 02:36:57 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Wed, 28 Jan 2026 02:36:57 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Wed, 28 Jan 2026 02:36:57 GMT
VOLUME [/spiped]
# Wed, 28 Jan 2026 02:36:57 GMT
WORKDIR /spiped
# Wed, 28 Jan 2026 02:36:57 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 02:36:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 02:36:57 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:d49a2dee86fb12766dd648402d010ca105846a41bd58738454e53780d4bb8e97`  
		Last Modified: Wed, 28 Jan 2026 01:18:46 GMT  
		Size: 3.8 MB (3804875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:255f2b198269941f9011d88cebad6e20b25c8054b5ac4ebd1b07f9750a69d255`  
		Last Modified: Wed, 28 Jan 2026 02:37:03 GMT  
		Size: 949.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed562f6049bf766f9af2aeb064224279b938162b44667a74bc7ca9c31ac1d70a`  
		Last Modified: Wed, 28 Jan 2026 02:37:03 GMT  
		Size: 7.9 KB (7945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d20d0ab7b6d45d1dbeebe557e32936e50678b9985769e6bd0ff3e1ff5e433e69`  
		Last Modified: Wed, 28 Jan 2026 02:37:03 GMT  
		Size: 107.6 KB (107647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:868415b885be47751e88ed3c97ca195abec55deffeb9f4ad2846ad3d25cdec28`  
		Last Modified: Wed, 28 Jan 2026 02:37:03 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7d8f030e4a64f48108d2120539708364c71dc39133649b15a0ad263ec9bfe40`  
		Last Modified: Wed, 28 Jan 2026 02:37:04 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:14bccfab21e7b3f36806b9521edfd711ef99c418ce1a38f2c913859e95caa2fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.5 KB (96451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e0f387ff25d96b6eec2a5942d1be095ce8d2cd8945dadefd293a3706d31ea69`

```dockerfile
```

-	Layers:
	-	`sha256:3abca7ed4aae68f57768d18d39b5d6b1c58a733af4507188677241020e39e0d9`  
		Last Modified: Wed, 28 Jan 2026 02:37:03 GMT  
		Size: 82.2 KB (82192 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bf6768ac276576d5f59511c63ded4afa12e2d77d28be7bffc6d1537d58bb57bb`  
		Last Modified: Wed, 28 Jan 2026 02:37:03 GMT  
		Size: 14.3 KB (14259 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6-alpine` - linux; arm variant v6

```console
$ docker pull spiped@sha256:3840e207c5f175385b57ca037766c41623e4a780197b93760ca83297bd8e51ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3603526 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f07ce0978d45ec15bdc0a08bdc59ff908f2bd78005af85d4bbad7345be081ee2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:06 GMT
ADD alpine-minirootfs-3.22.3-armhf.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:06 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:56:33 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Wed, 28 Jan 2026 02:56:34 GMT
RUN apk add --no-cache libssl3 # buildkit
# Wed, 28 Jan 2026 02:56:44 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Wed, 28 Jan 2026 02:56:44 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Wed, 28 Jan 2026 02:56:44 GMT
VOLUME [/spiped]
# Wed, 28 Jan 2026 02:56:44 GMT
WORKDIR /spiped
# Wed, 28 Jan 2026 02:56:44 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 02:56:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 02:56:44 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:835838571e5c80c63481753299e25a9f89f366d8f4a9c1a2043b8fdf98176f17`  
		Last Modified: Wed, 28 Jan 2026 01:18:10 GMT  
		Size: 3.5 MB (3505046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5a5ad93e4f03c704fabcd2728cb1ab8244c96ef0876f3fcc9779085a8d3be96`  
		Last Modified: Wed, 28 Jan 2026 02:56:48 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:092107d3ff0fcf3229ae39acf729a354fda97b10c713e7073d550bb7c69025bc`  
		Last Modified: Wed, 28 Jan 2026 02:56:48 GMT  
		Size: 7.9 KB (7944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcb00245db6ff8769dfa116d0e6194c8908449cd54b3995e5f0044b278d0fb45`  
		Last Modified: Wed, 28 Jan 2026 02:56:48 GMT  
		Size: 89.2 KB (89154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3375ee92dad5bd59b0dde03ad45bdf7a8f7df3aaa1e2847b17cdd6734893cfb8`  
		Last Modified: Wed, 28 Jan 2026 02:56:48 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc41431154f4cccb130328f9bda92ac3cd374c3bc4ef8b29827399ebd22bc749`  
		Last Modified: Wed, 28 Jan 2026 02:56:49 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:193c4ff5e06269d1446ab3235284aa43d244fdbc13dffdc98c715540fcc455e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.1 KB (14146 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:060b8b064e4aba529d56ef354367ffae940f6b152b36f64ea427dfcd51e51f1e`

```dockerfile
```

-	Layers:
	-	`sha256:9257c6b08dae939c45fb6b5cd969064dde84328d15653df8b0ab98dae6b31d32`  
		Last Modified: Wed, 28 Jan 2026 02:56:48 GMT  
		Size: 14.1 KB (14146 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6-alpine` - linux; arm variant v7

```console
$ docker pull spiped@sha256:71592cfee4b071cad3b52c3cfdefddd8ff72e3d5e644d8859d2d8cec8397a0d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3314649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c48ddb927471eeb09c0d2e183b02bb1074d36b5caa9dbd3477ee935a8eed01f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:29 GMT
ADD alpine-minirootfs-3.22.3-armv7.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:29 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:56:24 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Wed, 28 Jan 2026 02:56:25 GMT
RUN apk add --no-cache libssl3 # buildkit
# Wed, 28 Jan 2026 02:56:34 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Wed, 28 Jan 2026 02:56:34 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Wed, 28 Jan 2026 02:56:34 GMT
VOLUME [/spiped]
# Wed, 28 Jan 2026 02:56:34 GMT
WORKDIR /spiped
# Wed, 28 Jan 2026 02:56:34 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 02:56:34 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 02:56:34 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:caca1d0e2f8affe80569328af55c755a8480801c5ee912e55aaa828c8209aa6e`  
		Last Modified: Wed, 28 Jan 2026 01:18:35 GMT  
		Size: 3.2 MB (3223629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:332ba379620ebeacb95d57ee5ff3ce395b9868fe9f8d00a5b85dd41df19b3a23`  
		Last Modified: Wed, 28 Jan 2026 02:56:39 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:471e6c87dbde5f46d8cd1e26b6a653a7d77209c851df54df0c065355b1c36749`  
		Last Modified: Wed, 28 Jan 2026 02:56:39 GMT  
		Size: 8.0 KB (7952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:917e2b19aaa32cc304579e079305131ee112e7015524177e84f33379315c24f6`  
		Last Modified: Wed, 28 Jan 2026 02:56:39 GMT  
		Size: 81.7 KB (81685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9d229583db181996be822e85b4fe259ecd55350b04637a090977de317d8cb53`  
		Last Modified: Wed, 28 Jan 2026 02:56:39 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:283dd24da1a4b40bed9d28f9196f24341abf5ee8a13f180db2b3e6daa7e85b8d`  
		Last Modified: Wed, 28 Jan 2026 02:56:40 GMT  
		Size: 336.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:b0d30665b0b25a584022937647a82e260a99dc3822f06eae03c777c08c589459
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.6 KB (96590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5de7b9137b4705f6bfaa43d68be9ab47cda877656a88568a8b98eaecf834d723`

```dockerfile
```

-	Layers:
	-	`sha256:bf20f6c9425bc14bf83c368ad820cbac85037f9cfe9e8f428105dcae79aa5f0a`  
		Last Modified: Wed, 28 Jan 2026 02:56:39 GMT  
		Size: 82.2 KB (82228 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3c326467351e8aaa1070327395a8ce06feaf36e791288cc8d0efc059293853a6`  
		Last Modified: Wed, 28 Jan 2026 02:56:39 GMT  
		Size: 14.4 KB (14362 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6-alpine` - linux; arm64 variant v8

```console
$ docker pull spiped@sha256:effcfa5e900325dc5a9f2ce725d32bb928170b9fae13c2414035f7c74db4832d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4249465 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1129da21c1ac14cfe9747c51280fa104e3e2a4a7fb499fce9d2f79394c096e45`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:55 GMT
ADD alpine-minirootfs-3.22.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:55 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:37:44 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Wed, 28 Jan 2026 02:37:45 GMT
RUN apk add --no-cache libssl3 # buildkit
# Wed, 28 Jan 2026 02:37:55 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Wed, 28 Jan 2026 02:37:55 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Wed, 28 Jan 2026 02:37:55 GMT
VOLUME [/spiped]
# Wed, 28 Jan 2026 02:37:55 GMT
WORKDIR /spiped
# Wed, 28 Jan 2026 02:37:55 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 02:37:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 02:37:55 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:d741ee1608f399e21c72d05f0f818c348c6801af33aeb83523893d09dc153957`  
		Last Modified: Wed, 28 Jan 2026 01:18:00 GMT  
		Size: 4.1 MB (4139519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a215f43d3f31692bff6dbb7a8464a9777ff146fd6817d85616dd79d628db9a4e`  
		Last Modified: Wed, 28 Jan 2026 02:38:00 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a149826e8201bd60e39e8acb8c71ee749c537b2c783a541e04af7a7b3fc6b5d`  
		Last Modified: Wed, 28 Jan 2026 02:38:00 GMT  
		Size: 8.0 KB (7951 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3816514d66f19e4e15afc0dae177ea8f1397bbaeba0189b4a33a3f265afbb21`  
		Last Modified: Wed, 28 Jan 2026 02:38:00 GMT  
		Size: 100.6 KB (100615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f073eca19d0c28ea18c16d7aa1388a52393935ac0e76036549b53fca85d50741`  
		Last Modified: Wed, 28 Jan 2026 02:38:00 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56ae442366147b99273aabaaf180c7a0347dd957817ff21ec6495a8f374fd7b5`  
		Last Modified: Wed, 28 Jan 2026 02:38:01 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:20c426c97f5ccc77dcb4c2895905f7a3e9aedaf5bf12fbf4b3ff87748f7ebc74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.6 KB (96641 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f74a0ff8267a4110c62ab6dcdcf2bf4949f9f54a7ff5e5b96a7e78b99f9770c`

```dockerfile
```

-	Layers:
	-	`sha256:ce7e8f74c44956e8b3a9213e0686a5007c77ddc5cd5210760e512537c99dcb4f`  
		Last Modified: Wed, 28 Jan 2026 02:38:00 GMT  
		Size: 82.2 KB (82248 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5744a1e9a5178b40c2e43ceccdad37fa256e17fb5a7e73342aa361c38b071ea6`  
		Last Modified: Wed, 28 Jan 2026 02:38:00 GMT  
		Size: 14.4 KB (14393 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6-alpine` - linux; 386

```console
$ docker pull spiped@sha256:d29799b7499dd97718236dec910ca0fb21a58b93b04c13b9d32bd3972850d109
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3750150 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c829adab8d4ab1c5c9eef2ab8cd6fc3b09ac7a5b2c98b60eb750eaadcf3ca449`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:53 GMT
ADD alpine-minirootfs-3.22.3-x86.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:53 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:31:22 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Wed, 28 Jan 2026 02:31:22 GMT
RUN apk add --no-cache libssl3 # buildkit
# Wed, 28 Jan 2026 02:31:32 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Wed, 28 Jan 2026 02:31:32 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Wed, 28 Jan 2026 02:31:32 GMT
VOLUME [/spiped]
# Wed, 28 Jan 2026 02:31:32 GMT
WORKDIR /spiped
# Wed, 28 Jan 2026 02:31:32 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 02:31:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 02:31:32 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:757a99eda61f22434071cfbc7a70f9526b63aeb5479a64272982017ee7cd9cfd`  
		Last Modified: Wed, 28 Jan 2026 01:18:59 GMT  
		Size: 3.6 MB (3620732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2088b329d71531fcaf8b6b6b5fb05bd132488a9b146463fda72d73f3b193da77`  
		Last Modified: Wed, 28 Jan 2026 02:31:36 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df6327ced333146d36cce9bad13d15f14d00cfba342ef14347eb76323f377623`  
		Last Modified: Wed, 28 Jan 2026 02:31:37 GMT  
		Size: 7.9 KB (7940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3f74692486d32e3c25efb4bcdbdd450b58db493d05a003140a026ba85c130a6`  
		Last Modified: Wed, 28 Jan 2026 02:31:36 GMT  
		Size: 120.1 KB (120096 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b377c56ed7e39aeec7320819a810cd8637819dc2c7f00e5f02f6008223d5ed8`  
		Last Modified: Wed, 28 Jan 2026 02:31:37 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e023ec54765d4d3764e0855b6d7cfe0e2f9966db68bd933fe3f4fe6c41a2474f`  
		Last Modified: Wed, 28 Jan 2026 02:31:38 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:49494f0bf8ea2a9ac91bc338facd2f7cede025b28b7848656878d7ce0deadf5c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.4 KB (96390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16387e224ee0b4762e3111436b2fdc3a8bfebe61d796cc65af094da1ebf76cd0`

```dockerfile
```

-	Layers:
	-	`sha256:bdc547d749394448a39cd679c285ba250424589df32f26c116cdc3bca37fedf9`  
		Last Modified: Wed, 28 Jan 2026 02:31:36 GMT  
		Size: 82.2 KB (82167 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4f968b5a19cf7dfb341a81ce64526ba67dbdecae7dbd82f7332ab1f24bf7e26a`  
		Last Modified: Wed, 28 Jan 2026 02:31:36 GMT  
		Size: 14.2 KB (14223 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6-alpine` - linux; ppc64le

```console
$ docker pull spiped@sha256:ec49e51d1b31aef6ee4c32cbd2374c5115032febd535905c0146f19ca7d1b88c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3856312 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c52e05f6841b2c0f9dcb913e52c349b3ec2747c75f53e9b3d6a41cd3c6103a9d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:35 GMT
ADD alpine-minirootfs-3.22.3-ppc64le.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:35 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 03:59:19 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Wed, 28 Jan 2026 03:59:21 GMT
RUN apk add --no-cache libssl3 # buildkit
# Wed, 28 Jan 2026 03:59:33 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Wed, 28 Jan 2026 03:59:33 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Wed, 28 Jan 2026 03:59:33 GMT
VOLUME [/spiped]
# Wed, 28 Jan 2026 03:59:33 GMT
WORKDIR /spiped
# Wed, 28 Jan 2026 03:59:34 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 03:59:34 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 03:59:34 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:d7b7d5bab08f20b53e85395b2d6e793469e3acdbe8644bd234992524588b440f`  
		Last Modified: Wed, 28 Jan 2026 01:17:44 GMT  
		Size: 3.7 MB (3734297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52389dd33bb155b2c78fa5202c8c9909e97b12049d41f7cb5369100d2a7be819`  
		Last Modified: Wed, 28 Jan 2026 03:59:48 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28fd5646a7c2ce724b02160a31080c85b3571ffddbc309ccb39fb23e5075d4aa`  
		Last Modified: Wed, 28 Jan 2026 03:59:47 GMT  
		Size: 8.0 KB (7956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d83f042b4cb936ae2f704768b0462b7f539ba799143799dc6a8ce0babc73884`  
		Last Modified: Wed, 28 Jan 2026 03:59:48 GMT  
		Size: 112.7 KB (112673 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b77f4a6884030927f7cdd451b10bba40c6cf61fd40534ca3a9cf653bb742ea8f`  
		Last Modified: Wed, 28 Jan 2026 03:59:48 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34fbfb80739dd4ce26eb065be080a75c602340f3242a297925caf40baf400db0`  
		Last Modified: Wed, 28 Jan 2026 03:59:49 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:1d08517919e2dfe608c1e408886b7ef4659cd9f15bf49a67583fe931eb307650
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.6 KB (94578 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b68d34137d518c2381ecd841ecef0a23786265f08c1952e0ed2134cc2ba9073`

```dockerfile
```

-	Layers:
	-	`sha256:b57bb2bf93c55cd637df776032387ee2beae0039a87bacf4e588dd43aaa36711`  
		Last Modified: Wed, 28 Jan 2026 03:59:48 GMT  
		Size: 80.3 KB (80275 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e4a73d72709b0315e9f657137bb6dbf7c0679131d8e10876ea8a1bb94e4201b4`  
		Last Modified: Wed, 28 Jan 2026 03:59:48 GMT  
		Size: 14.3 KB (14303 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6-alpine` - linux; riscv64

```console
$ docker pull spiped@sha256:0e7e07e5944d0951da4949f8298cdccfa6ec9395c2d0ddf983aa7f40bf7807f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3625620 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00565f6907e5ae385b224d048c255c22407d6a59d79533da4912c486d4ee1360`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 28 Jan 2026 03:49:43 GMT
ADD alpine-minirootfs-3.22.3-riscv64.tar.gz / # buildkit
# Wed, 28 Jan 2026 03:49:43 GMT
CMD ["/bin/sh"]
# Thu, 29 Jan 2026 18:56:58 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Thu, 29 Jan 2026 18:57:02 GMT
RUN apk add --no-cache libssl3 # buildkit
# Thu, 29 Jan 2026 18:58:38 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Thu, 29 Jan 2026 18:58:38 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Thu, 29 Jan 2026 18:58:38 GMT
VOLUME [/spiped]
# Thu, 29 Jan 2026 18:58:39 GMT
WORKDIR /spiped
# Thu, 29 Jan 2026 18:58:39 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Thu, 29 Jan 2026 18:58:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 29 Jan 2026 18:58:39 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:15ea87d2370d91334d14e1cb46366adb6a57bbae717f07f8c9f55735cf137f62`  
		Last Modified: Wed, 28 Jan 2026 03:50:15 GMT  
		Size: 3.5 MB (3517422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c85b2fc2b9bdc2a30eea3483d034231cba4cf794b774e9c668e43189f965204b`  
		Last Modified: Thu, 29 Jan 2026 18:58:59 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7a35d458c7098a7c5f24f347a75cf6930f742a2e14ae40067defc23e63d57b5`  
		Last Modified: Thu, 29 Jan 2026 18:58:59 GMT  
		Size: 7.9 KB (7944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fbbaf165e7e5cf59739b8e5317789f9a907da0dc26f3803ae533e05f7a2068e`  
		Last Modified: Thu, 29 Jan 2026 18:58:59 GMT  
		Size: 98.9 KB (98867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15e0973003e6d2e757a9f14bfb9ab4d4b6be0abf8bbdfa7a9b699232646e0df6`  
		Last Modified: Thu, 29 Jan 2026 18:58:59 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8509faeca8d8af4689f4b76d19f92f0deeb48d08e62ab656d5ad988fe97b48e9`  
		Last Modified: Thu, 29 Jan 2026 18:59:00 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:45c5a2bccce0c2d968718cdc5b92e2d54486ce35d6f21169c8e2975138906721
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.6 KB (94575 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3828726b576d70b513dac001f2810887cf67c235a77086291ebdeb6df7a249f`

```dockerfile
```

-	Layers:
	-	`sha256:53e8f0117ebdf17125860003417afad58a90f091d2b04b6763e9b4ce1899228b`  
		Last Modified: Thu, 29 Jan 2026 18:58:59 GMT  
		Size: 80.3 KB (80271 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0edfbeca58a13ce30fdd21ef302873aa05c28498d058231b777fe51653a06eb6`  
		Last Modified: Thu, 29 Jan 2026 18:58:59 GMT  
		Size: 14.3 KB (14304 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6-alpine` - linux; s390x

```console
$ docker pull spiped@sha256:0aeb96b9c7c968a0ad51a4c785e0c76534a115d395c587eacd587a3aad55b360
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3756697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b72691935166b1882b3040950315ed19d9cf1a3678909a868fa5c27a1a58e2b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:06 GMT
ADD alpine-minirootfs-3.22.3-s390x.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:06 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 03:05:47 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Wed, 28 Jan 2026 03:05:48 GMT
RUN apk add --no-cache libssl3 # buildkit
# Wed, 28 Jan 2026 03:05:55 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Wed, 28 Jan 2026 03:05:55 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Wed, 28 Jan 2026 03:05:55 GMT
VOLUME [/spiped]
# Wed, 28 Jan 2026 03:05:55 GMT
WORKDIR /spiped
# Wed, 28 Jan 2026 03:05:55 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 03:05:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 03:05:55 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:dab48b8d1bab09fede3f54264828e67466f10d64acc37d9412190034dbcbf61f`  
		Last Modified: Wed, 28 Jan 2026 01:17:16 GMT  
		Size: 3.7 MB (3650434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0789ee1817b07966cd80a07b05a82d8e0c9bf85f6053f4955ac4731e47448ad`  
		Last Modified: Wed, 28 Jan 2026 03:06:03 GMT  
		Size: 949.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e526c5a7e2d6f02b24c7ed3860ec8221dcd7d0c6e4112d267da6729a13890448`  
		Last Modified: Wed, 28 Jan 2026 03:06:03 GMT  
		Size: 7.9 KB (7949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f10bca7622d69f6335c554b1c8cec2a82753df66ed9cf072d635820439e1af3c`  
		Last Modified: Wed, 28 Jan 2026 03:06:03 GMT  
		Size: 96.9 KB (96933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81d81cea7ec993f5c76e72bd06b1579e878f6a4d1a4a2f11114f710747ef40d4`  
		Last Modified: Wed, 28 Jan 2026 03:06:03 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:086ab53d5ebb5741d97d120d1a1ad7797bf2fda46a7ff1f9a033efa0117cd233`  
		Last Modified: Wed, 28 Jan 2026 03:06:04 GMT  
		Size: 336.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:c32f5675d459d866b7c69b2159549861b770e81fa270485088e909f23c515b9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.5 KB (94497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a76bce779a8727519c7fb65566c2ce929337d21a3d6addd2f301cd51f95516c4`

```dockerfile
```

-	Layers:
	-	`sha256:85780af5cccece93dbeac028f8517ebc14f3298ca69ddd75bcf80809c0ea3432`  
		Last Modified: Wed, 28 Jan 2026 03:06:03 GMT  
		Size: 80.2 KB (80241 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:797300601f0f43bd14d2b3e327c7100b2a1b8356e4290096f308e710af773718`  
		Last Modified: Wed, 28 Jan 2026 03:06:03 GMT  
		Size: 14.3 KB (14256 bytes)  
		MIME: application/vnd.in-toto+json

## `spiped:1.6.4`

```console
$ docker pull spiped@sha256:86bfe9d75887a0c865ca400bce9556e55f0100324ab12cea4182325b4538c9d3
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
$ docker pull spiped@sha256:1dadd78b37a53143babab424620b268d0e87665451c7e0b19ee714350efeb0aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.8 MB (36825645 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6aec690f0b7647a2b707058d20c805804b9d29cdd158eb3109584ae64c2e9c96`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1773619200'
# Mon, 16 Mar 2026 22:35:50 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Mon, 16 Mar 2026 22:35:52 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:36:17 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Mon, 16 Mar 2026 22:36:17 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Mon, 16 Mar 2026 22:36:17 GMT
VOLUME [/spiped]
# Mon, 16 Mar 2026 22:36:17 GMT
WORKDIR /spiped
# Mon, 16 Mar 2026 22:36:17 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Mon, 16 Mar 2026 22:36:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 16 Mar 2026 22:36:17 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:ec781dee3f4719c2ca0dd9e73cb1d4ed834ed1a406495eb6e44b6dfaad5d1f8f`  
		Last Modified: Mon, 16 Mar 2026 21:53:19 GMT  
		Size: 29.8 MB (29775500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32ceac9107a69b7bfdee6e7660e1eff3feb8d0fd5d6f681f2a6ad1905d93ba0a`  
		Last Modified: Mon, 16 Mar 2026 22:36:24 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1aa4948bacb0a02611ec173cb9f157bd247587fd13cb63e407219ba6dd87af7d`  
		Last Modified: Mon, 16 Mar 2026 22:36:24 GMT  
		Size: 828.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50f472851b739f36f98249e60dba4ceb8a571cbd9f18c3e6b9639215d2c6dcfa`  
		Last Modified: Mon, 16 Mar 2026 22:36:24 GMT  
		Size: 7.0 MB (7047777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7dda7601460289f11e5d3db99f3c14ac9bf518a829bc22ae224a96c8c3a4d4d9`  
		Last Modified: Mon, 16 Mar 2026 22:36:24 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:597b8eb9fa679d5997894aab7d18f62d615b6cc715de0c0a98c8bddef96e43ee`  
		Last Modified: Mon, 16 Mar 2026 22:36:25 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6.4` - unknown; unknown

```console
$ docker pull spiped@sha256:24038ff42b84801b0e2af5de324e185ffb9b47e091947a1d6ead4da071277394
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3641241 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:204d83d1b596e75d2d7efdfccf8e0ab85c3bf694d7310417d68e3add5e86a10f`

```dockerfile
```

-	Layers:
	-	`sha256:1f60bdfcbc8114aba716d733f2c08d28946d1d47510ef32f11fe773e7efbba8c`  
		Last Modified: Mon, 16 Mar 2026 22:36:24 GMT  
		Size: 3.6 MB (3626260 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b07a02dacfe5fad817dc8acef6300290b65922a87b426e54f70d87798a0696f5`  
		Last Modified: Mon, 16 Mar 2026 22:36:24 GMT  
		Size: 15.0 KB (14981 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6.4` - linux; arm variant v5

```console
$ docker pull spiped@sha256:d76bab68c9ba80d6bde9b766de2f4b524b29b2e06796dea03aa1f86973b6e402
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.7 MB (33735071 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e9ce3fe44b3195308782999982dffb0e0324f65968051303e6d0ccb5e46710e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1773619200'
# Mon, 16 Mar 2026 23:15:44 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Mon, 16 Mar 2026 23:15:49 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 23:16:15 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Mon, 16 Mar 2026 23:16:15 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Mon, 16 Mar 2026 23:16:15 GMT
VOLUME [/spiped]
# Mon, 16 Mar 2026 23:16:15 GMT
WORKDIR /spiped
# Mon, 16 Mar 2026 23:16:15 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Mon, 16 Mar 2026 23:16:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 16 Mar 2026 23:16:15 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:eb1defba38d0de4655b895d4763345b3ab078983d3385db43c308a7caca13f2a`  
		Last Modified: Mon, 16 Mar 2026 21:52:26 GMT  
		Size: 27.9 MB (27943649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9cfc1da50f0fc66e4696a6b249cf2c9f19d773fda1096f22c619e19221b8de7`  
		Last Modified: Mon, 16 Mar 2026 23:16:22 GMT  
		Size: 1.1 KB (1105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a98c3d3f9d3a820c9fbfddae7bba53067abc005cb4837355fd2fe02be5159fda`  
		Last Modified: Mon, 16 Mar 2026 23:16:22 GMT  
		Size: 831.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:981177ab397ef56ea1a515604977b4812a8bccc0e0ae76b96ba1a148b66278c5`  
		Last Modified: Mon, 16 Mar 2026 23:16:22 GMT  
		Size: 5.8 MB (5789053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8116b26167b41dbbadb8f30d9738528a34e2436086fd1d12d6d83af070f87911`  
		Last Modified: Mon, 16 Mar 2026 23:16:22 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8f7d349acecae8a4190b1310446bb378d3edc921d84f55ac12cf5202b8df556`  
		Last Modified: Mon, 16 Mar 2026 23:16:23 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6.4` - unknown; unknown

```console
$ docker pull spiped@sha256:1ef3cb6065e7ec1c89ec491fd9bfd3dc5b3221edc45b98e1d076dc81f408837e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3634342 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6758a2f7ff038f8df9fc87c6f4130ff4358acd576e0e39211c178068863796cc`

```dockerfile
```

-	Layers:
	-	`sha256:5a7c54557652f62feaed177546a18b57a4e82674763bde13f27b1dab19e00b9d`  
		Last Modified: Mon, 16 Mar 2026 23:16:23 GMT  
		Size: 3.6 MB (3619254 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:647540c448bfbe8c1ba0711adf24d3a530725e84f4fd25c88632cf2510d9c007`  
		Last Modified: Mon, 16 Mar 2026 23:16:22 GMT  
		Size: 15.1 KB (15088 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6.4` - linux; arm variant v7

```console
$ docker pull spiped@sha256:723ba9f91b55f3576b2113c495e19f93cb621ee72fabcaff1531301fbcaa4b1a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.8 MB (31796429 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5cb0e019fca22ad836d890087ee6d2a180105ee1191adf83d36a753ea37941a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1773619200'
# Mon, 16 Mar 2026 23:17:41 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Mon, 16 Mar 2026 23:17:45 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 23:18:07 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Mon, 16 Mar 2026 23:18:07 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Mon, 16 Mar 2026 23:18:07 GMT
VOLUME [/spiped]
# Mon, 16 Mar 2026 23:18:07 GMT
WORKDIR /spiped
# Mon, 16 Mar 2026 23:18:07 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Mon, 16 Mar 2026 23:18:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 16 Mar 2026 23:18:07 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:7d73604d2a042e7beeb809f68c76f5be3576747809bfaa49747f334227d8d250`  
		Last Modified: Mon, 16 Mar 2026 21:53:24 GMT  
		Size: 26.2 MB (26209505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:658299db6ef3056cf755c844791cbd82e4508468df390e37a8aad706f3a48f4c`  
		Last Modified: Mon, 16 Mar 2026 23:18:14 GMT  
		Size: 1.1 KB (1103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8faf32f19b630a82f84ed9470b862ab68393803b1e37f045f46258e8890f7d50`  
		Last Modified: Mon, 16 Mar 2026 23:18:14 GMT  
		Size: 828.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba29f29a0220be91155a5596cf59a8ec1e848dc1c59089563006ce592b99f829`  
		Last Modified: Mon, 16 Mar 2026 23:18:14 GMT  
		Size: 5.6 MB (5584559 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:571f3aa9916ae33f81a8eff41f15615107662751591ab2cae13c31339f2cdb35`  
		Last Modified: Mon, 16 Mar 2026 23:18:14 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0023499b415317d80739286a45ec7393c98ddc05a638d045c05812141aa28b0`  
		Last Modified: Mon, 16 Mar 2026 23:18:15 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6.4` - unknown; unknown

```console
$ docker pull spiped@sha256:b778f2f8e613351de55fec9efa1c2283e7262e815379cb9c01090839b522f03b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3633463 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:820126e67739682404e3e543b661db54a249ad7238843089922bd27097f59140`

```dockerfile
```

-	Layers:
	-	`sha256:34fdc3e15f493cc5e996b5a867605ede0f868b1b23e1156f69a1d24198213663`  
		Last Modified: Mon, 16 Mar 2026 23:18:14 GMT  
		Size: 3.6 MB (3618375 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7867a53cd4efb0b6f41304907e82351cc690be89532e8db042be1139471fee68`  
		Last Modified: Mon, 16 Mar 2026 23:18:14 GMT  
		Size: 15.1 KB (15088 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6.4` - linux; arm64 variant v8

```console
$ docker pull spiped@sha256:4ae6755ad03f743b18a351fbafa71c65c711f58faea3a81b665befd8567053b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.4 MB (36374360 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0fbe5e7be982e3e0a47d2310365b2015977222cf3f9135331a2ddafbc2a09e29`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1773619200'
# Mon, 16 Mar 2026 22:38:29 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Mon, 16 Mar 2026 22:38:32 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:38:55 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Mon, 16 Mar 2026 22:38:55 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Mon, 16 Mar 2026 22:38:55 GMT
VOLUME [/spiped]
# Mon, 16 Mar 2026 22:38:55 GMT
WORKDIR /spiped
# Mon, 16 Mar 2026 22:38:55 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Mon, 16 Mar 2026 22:38:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 16 Mar 2026 22:38:55 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:f4badedbec24858ef2dc51256f6418328e305e9c3c5a5e093581f83425618bd5`  
		Last Modified: Mon, 16 Mar 2026 21:53:04 GMT  
		Size: 30.1 MB (30138416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59eb94c76468927e4e914285fecca640b78cd857ba3998fcfc270e51a5999a76`  
		Last Modified: Mon, 16 Mar 2026 22:39:02 GMT  
		Size: 1.1 KB (1104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11b2a5c6f2a1a593d60739bde8e5edb5ede5cc1c07d169f19ef39a67402cd65b`  
		Last Modified: Mon, 16 Mar 2026 22:39:02 GMT  
		Size: 828.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bedfccd6793021acdd75a491c31f9164e9dc33b3e7429226d6093a2dd780093`  
		Last Modified: Mon, 16 Mar 2026 22:39:03 GMT  
		Size: 6.2 MB (6233579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b277914700ac4bb0336072358245beede0af746b61ba9febb726f5a24443909`  
		Last Modified: Mon, 16 Mar 2026 22:39:03 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fcc46f0d3ebea317699d8e2e6d3e2c8d2e022621162b4aeb23e6aec0d21d6f3`  
		Last Modified: Mon, 16 Mar 2026 22:39:03 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6.4` - unknown; unknown

```console
$ docker pull spiped@sha256:3bb60c38b60da93affbf4a161bd60f5d201524ab747841166084d1e18235b678
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3636412 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:acfdeacc136a94cefd95b5fc4a223865929593d17a4df005eb979067d4539f09`

```dockerfile
```

-	Layers:
	-	`sha256:da2db9f7e9ec3796af7d7b3c2062fb98cdf3bf4c8cbc30041368b9529682b6e4`  
		Last Modified: Mon, 16 Mar 2026 22:39:03 GMT  
		Size: 3.6 MB (3621296 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c581a66bb5f391583c1fd9137f24523cc1f7cfb6e13f4dca2a22a36d28db1f75`  
		Last Modified: Mon, 16 Mar 2026 22:39:02 GMT  
		Size: 15.1 KB (15116 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6.4` - linux; 386

```console
$ docker pull spiped@sha256:44d93dff5b665eb236d8d461091f645401dad4215fc6e748e75d845e5f88359a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.7 MB (37735593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b145875baf2722671a7d04cbdec8ce2e4e0044fe83f4480f7d13be40ef1b7f0d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1773619200'
# Mon, 16 Mar 2026 22:43:15 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Mon, 16 Mar 2026 22:43:17 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:43:39 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Mon, 16 Mar 2026 22:43:39 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Mon, 16 Mar 2026 22:43:39 GMT
VOLUME [/spiped]
# Mon, 16 Mar 2026 22:43:39 GMT
WORKDIR /spiped
# Mon, 16 Mar 2026 22:43:39 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Mon, 16 Mar 2026 22:43:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 16 Mar 2026 22:43:39 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:2c0c3f3238f3d4cecd93e4dee6eda788943ef955de61c3ad4ff659da1f43ba60`  
		Last Modified: Mon, 16 Mar 2026 21:53:39 GMT  
		Size: 31.3 MB (31291132 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e26822c10be4229a362fafa19cf7744d8e4afd786250bc983de1db93de19f3ff`  
		Last Modified: Mon, 16 Mar 2026 22:43:45 GMT  
		Size: 1.1 KB (1103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6acce4a1df323ade11febca20e664df3454379e4a4d62367fda308fd3377a5b7`  
		Last Modified: Mon, 16 Mar 2026 22:43:45 GMT  
		Size: 827.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ceb4b68e89c0b0dc1a9dc9754d84e4fdcc68a054100397edf14eea9bb6cc12b`  
		Last Modified: Mon, 16 Mar 2026 22:43:46 GMT  
		Size: 6.4 MB (6442097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:300ea57bc8db031eb298c0be9439b59a132b01d16a7971119ccb7c917fbb6554`  
		Last Modified: Mon, 16 Mar 2026 22:43:45 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a7afc0484bbe3e1c40b997eebf00362bc5e5e5711f5533cb6ff54e22c2413b4`  
		Last Modified: Mon, 16 Mar 2026 22:43:46 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6.4` - unknown; unknown

```console
$ docker pull spiped@sha256:513effd7016736f664ccfba169fc4d2d2fbac9b2d09ae5c2427af606b4fef17d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3635335 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03f65e618603d756ec27e2173381823753cc22ece11b748008e7b4745130c1da`

```dockerfile
```

-	Layers:
	-	`sha256:5f750ca150313a2349433840e5c82fdef74358685b619d6b14e5b58e76f0781a`  
		Last Modified: Mon, 16 Mar 2026 22:43:46 GMT  
		Size: 3.6 MB (3620389 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:23ece012ebd2581aea85be27bbc3fe9da829f9ee6cb39f7e97a3637110ad5770`  
		Last Modified: Mon, 16 Mar 2026 22:43:45 GMT  
		Size: 14.9 KB (14946 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6.4` - linux; ppc64le

```console
$ docker pull spiped@sha256:558d9e854b92393e1d96ef6e4d632b42659ff94decbb53b76989997d1e0ec224
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.4 MB (40435868 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8fb525945e5b18678cd55fe712bfb5b6997167921072dfe24c99cc7441368efc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1773619200'
# Tue, 17 Mar 2026 01:48:02 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Tue, 17 Mar 2026 01:48:07 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 01:49:05 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Tue, 17 Mar 2026 01:49:05 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 17 Mar 2026 01:49:05 GMT
VOLUME [/spiped]
# Tue, 17 Mar 2026 01:49:05 GMT
WORKDIR /spiped
# Tue, 17 Mar 2026 01:49:06 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Tue, 17 Mar 2026 01:49:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Mar 2026 01:49:06 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:f078139432e0b368e27241df524f6ef0ed0148b217d7495670dc297af77699fb`  
		Last Modified: Mon, 16 Mar 2026 21:55:56 GMT  
		Size: 33.6 MB (33592834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b23cdd3695d4f8d7ed89e6ef14a27bade53f83dc908d0d81ca0e30631851657d`  
		Last Modified: Tue, 17 Mar 2026 01:49:20 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2aeba3f4cf41d1fe339b87612255223a740f20ca43890419c57f646a0d6b4700`  
		Last Modified: Tue, 17 Mar 2026 01:49:20 GMT  
		Size: 827.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2900931ab7a20d4ba700e41e56664ad7605eb9d341f250b7e024800c787b1f57`  
		Last Modified: Tue, 17 Mar 2026 01:49:20 GMT  
		Size: 6.8 MB (6840666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd461ff0c7b461bb5a3b5a2abf96ce3dec4858db537c1939b8bdfbe1fc8d1dac`  
		Last Modified: Tue, 17 Mar 2026 01:49:20 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8147ab40850402c527ecc2d439d4ce4dab6d232336aa43c20444dc18829f1273`  
		Last Modified: Tue, 17 Mar 2026 01:49:21 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6.4` - unknown; unknown

```console
$ docker pull spiped@sha256:f200a47fd65a47d561c18eabdbae5cd6d9935be2507254b566d43b48e6c57456
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3637027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f8f2b490d9a358d5a7fea9f4d29b4098981a442f93c062a3b276cf4357de8c3`

```dockerfile
```

-	Layers:
	-	`sha256:887ec06e855bee10271ac461e307cde47e3b0f61f873ebe04e4b7bd6687368f2`  
		Last Modified: Tue, 17 Mar 2026 01:49:20 GMT  
		Size: 3.6 MB (3621997 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:91f36846163a85b9df751c3b92a108c1257a4e2dac2c2e2f37c380787eb44d19`  
		Last Modified: Tue, 17 Mar 2026 01:49:20 GMT  
		Size: 15.0 KB (15030 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6.4` - linux; riscv64

```console
$ docker pull spiped@sha256:8bb82489fc130e0ebd5f9bbd52581be946042cfd96ea517ea76d5bc3bf8ebefb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.6 MB (37637359 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3782bede9d9edafc097d7e1829603f7130a6de5afd0278b055260b72c9dc1997`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1771804800'
# Thu, 26 Feb 2026 21:27:02 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Thu, 26 Feb 2026 21:27:31 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 26 Feb 2026 21:30:35 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Thu, 26 Feb 2026 21:30:35 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Thu, 26 Feb 2026 21:30:35 GMT
VOLUME [/spiped]
# Thu, 26 Feb 2026 21:30:36 GMT
WORKDIR /spiped
# Thu, 26 Feb 2026 21:30:36 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Thu, 26 Feb 2026 21:30:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 26 Feb 2026 21:30:36 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:7d614b9ad5a6f3dd0478c6903a6d2ffddc9bc5b17650714d4c1f761161fde58d`  
		Last Modified: Tue, 24 Feb 2026 18:59:14 GMT  
		Size: 28.3 MB (28276417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afbc2b651dc4281762485417954f26f00a147e635dd4386b4dc36ec1c12057b8`  
		Last Modified: Thu, 26 Feb 2026 21:31:48 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04ad29eaeb47daebdc8fd5d52da1dcf0f8ef0dd3a9f796c0f14675426e200e89`  
		Last Modified: Thu, 26 Feb 2026 21:31:48 GMT  
		Size: 822.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b04499c1af0fd231152f64530568de3e0fe490576c3d0bcf0c9743990a7938f7`  
		Last Modified: Thu, 26 Feb 2026 21:31:49 GMT  
		Size: 9.4 MB (9358576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19d9ae5d28f72fa67e546ccb83e7e39152304c5e1d393ceb17fee76009b87c30`  
		Last Modified: Thu, 26 Feb 2026 21:31:48 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c9afcb0cccd5e3f03a3850046642ebf8a8029bf602e5e5b8bd9422d3cf7b350`  
		Last Modified: Thu, 26 Feb 2026 21:31:49 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6.4` - unknown; unknown

```console
$ docker pull spiped@sha256:e5cf967432204ce7118f3ebbd169698a80d6df6bc23555049960d38da754a9d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3628397 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd419f8646942dcae52af9b19c3f390a9c3f6271d67369dcf6fc2c6b69d54b9d`

```dockerfile
```

-	Layers:
	-	`sha256:f67ba2453a68b55021d7f90d26cc1c990f9286371a00137c7cad53780d0559ba`  
		Last Modified: Thu, 26 Feb 2026 21:31:49 GMT  
		Size: 3.6 MB (3613367 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cf05fe9bfbfcb881eacb026a48af7d361ee01b63efce4a7f453d9c6fa4af7fa2`  
		Last Modified: Thu, 26 Feb 2026 21:31:48 GMT  
		Size: 15.0 KB (15030 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6.4` - linux; s390x

```console
$ docker pull spiped@sha256:c3ea82efea9854cb0da628935b60cf04f6c53931b6f7c2d20cd31aa9d27deaf0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.0 MB (35958813 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:579c56a7419832fa8be7ed9c8c7faaf68cb1da36770f667bfdce26ab4c03d59b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1773619200'
# Mon, 16 Mar 2026 23:43:38 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Mon, 16 Mar 2026 23:43:41 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 23:44:00 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Mon, 16 Mar 2026 23:44:00 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Mon, 16 Mar 2026 23:44:00 GMT
VOLUME [/spiped]
# Mon, 16 Mar 2026 23:44:00 GMT
WORKDIR /spiped
# Mon, 16 Mar 2026 23:44:00 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Mon, 16 Mar 2026 23:44:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 16 Mar 2026 23:44:00 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:2c02a3d3f135c4bbe56488921bd86d969a76dcd5278abca1e81884d3bff0bd88`  
		Last Modified: Mon, 16 Mar 2026 21:52:55 GMT  
		Size: 29.8 MB (29835265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c81e7613d635aa581f38ab946c2047e14837502a75f3f4e08fff5f611175fa1`  
		Last Modified: Mon, 16 Mar 2026 23:44:13 GMT  
		Size: 1.1 KB (1105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e7af70f2f5d7c87a4eef797de7cdee0fc7fe1f22a5cdd1d147f73cd11cd3c66`  
		Last Modified: Mon, 16 Mar 2026 23:44:13 GMT  
		Size: 828.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fc179ed0ea05be607a3fd6ab65992063b0b8fad92eba54e1abc2f376ad37586`  
		Last Modified: Mon, 16 Mar 2026 23:44:13 GMT  
		Size: 6.1 MB (6121184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97d07658b602778f575172b4841e370cbe43b5899cb54c7748a2978f0da94aae`  
		Last Modified: Mon, 16 Mar 2026 23:44:13 GMT  
		Size: 94.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2f0b086128c318c28efb4541b0c5264857fb53e45dd2a7cfc468fdf981146fe`  
		Last Modified: Mon, 16 Mar 2026 23:44:14 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6.4` - unknown; unknown

```console
$ docker pull spiped@sha256:ceb5259222252c09f46d1586c4beb858ae638bfa5623656db13b549d96d21d09
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3633605 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38f77179e2c665d2a86e12bc17bfedc7f450031d205ba7c907005662463dd141`

```dockerfile
```

-	Layers:
	-	`sha256:a6c5d5579933f8a016f12bcfd02838e397274cce0d8c07d3b637a90946cef6b9`  
		Last Modified: Mon, 16 Mar 2026 23:44:13 GMT  
		Size: 3.6 MB (3618623 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:39e9ea0d638105f70bced5f876f7ce8f9adcd4138140b8d5d517b41dd0e8974b`  
		Last Modified: Mon, 16 Mar 2026 23:44:13 GMT  
		Size: 15.0 KB (14982 bytes)  
		MIME: application/vnd.in-toto+json

## `spiped:1.6.4-alpine`

```console
$ docker pull spiped@sha256:2e861202f057586ae2e6dc3a5290d61949120d861e272b5700c1e30e1ae9774c
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
$ docker pull spiped@sha256:45aa25e16b20aaf22415c03717dfbffb2460250d93ccfbf50d304296f0323560
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3921849 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c42c3ad8f87ea2a2987c07857dc357c5caa6eb7fe68f8ab758c81d2c67f6316`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:40 GMT
ADD alpine-minirootfs-3.22.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:40 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:36:46 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Wed, 28 Jan 2026 02:36:47 GMT
RUN apk add --no-cache libssl3 # buildkit
# Wed, 28 Jan 2026 02:36:57 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Wed, 28 Jan 2026 02:36:57 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Wed, 28 Jan 2026 02:36:57 GMT
VOLUME [/spiped]
# Wed, 28 Jan 2026 02:36:57 GMT
WORKDIR /spiped
# Wed, 28 Jan 2026 02:36:57 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 02:36:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 02:36:57 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:d49a2dee86fb12766dd648402d010ca105846a41bd58738454e53780d4bb8e97`  
		Last Modified: Wed, 28 Jan 2026 01:18:46 GMT  
		Size: 3.8 MB (3804875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:255f2b198269941f9011d88cebad6e20b25c8054b5ac4ebd1b07f9750a69d255`  
		Last Modified: Wed, 28 Jan 2026 02:37:03 GMT  
		Size: 949.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed562f6049bf766f9af2aeb064224279b938162b44667a74bc7ca9c31ac1d70a`  
		Last Modified: Wed, 28 Jan 2026 02:37:03 GMT  
		Size: 7.9 KB (7945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d20d0ab7b6d45d1dbeebe557e32936e50678b9985769e6bd0ff3e1ff5e433e69`  
		Last Modified: Wed, 28 Jan 2026 02:37:03 GMT  
		Size: 107.6 KB (107647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:868415b885be47751e88ed3c97ca195abec55deffeb9f4ad2846ad3d25cdec28`  
		Last Modified: Wed, 28 Jan 2026 02:37:03 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7d8f030e4a64f48108d2120539708364c71dc39133649b15a0ad263ec9bfe40`  
		Last Modified: Wed, 28 Jan 2026 02:37:04 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6.4-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:14bccfab21e7b3f36806b9521edfd711ef99c418ce1a38f2c913859e95caa2fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.5 KB (96451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e0f387ff25d96b6eec2a5942d1be095ce8d2cd8945dadefd293a3706d31ea69`

```dockerfile
```

-	Layers:
	-	`sha256:3abca7ed4aae68f57768d18d39b5d6b1c58a733af4507188677241020e39e0d9`  
		Last Modified: Wed, 28 Jan 2026 02:37:03 GMT  
		Size: 82.2 KB (82192 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bf6768ac276576d5f59511c63ded4afa12e2d77d28be7bffc6d1537d58bb57bb`  
		Last Modified: Wed, 28 Jan 2026 02:37:03 GMT  
		Size: 14.3 KB (14259 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6.4-alpine` - linux; arm variant v6

```console
$ docker pull spiped@sha256:3840e207c5f175385b57ca037766c41623e4a780197b93760ca83297bd8e51ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3603526 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f07ce0978d45ec15bdc0a08bdc59ff908f2bd78005af85d4bbad7345be081ee2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:06 GMT
ADD alpine-minirootfs-3.22.3-armhf.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:06 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:56:33 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Wed, 28 Jan 2026 02:56:34 GMT
RUN apk add --no-cache libssl3 # buildkit
# Wed, 28 Jan 2026 02:56:44 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Wed, 28 Jan 2026 02:56:44 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Wed, 28 Jan 2026 02:56:44 GMT
VOLUME [/spiped]
# Wed, 28 Jan 2026 02:56:44 GMT
WORKDIR /spiped
# Wed, 28 Jan 2026 02:56:44 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 02:56:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 02:56:44 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:835838571e5c80c63481753299e25a9f89f366d8f4a9c1a2043b8fdf98176f17`  
		Last Modified: Wed, 28 Jan 2026 01:18:10 GMT  
		Size: 3.5 MB (3505046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5a5ad93e4f03c704fabcd2728cb1ab8244c96ef0876f3fcc9779085a8d3be96`  
		Last Modified: Wed, 28 Jan 2026 02:56:48 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:092107d3ff0fcf3229ae39acf729a354fda97b10c713e7073d550bb7c69025bc`  
		Last Modified: Wed, 28 Jan 2026 02:56:48 GMT  
		Size: 7.9 KB (7944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcb00245db6ff8769dfa116d0e6194c8908449cd54b3995e5f0044b278d0fb45`  
		Last Modified: Wed, 28 Jan 2026 02:56:48 GMT  
		Size: 89.2 KB (89154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3375ee92dad5bd59b0dde03ad45bdf7a8f7df3aaa1e2847b17cdd6734893cfb8`  
		Last Modified: Wed, 28 Jan 2026 02:56:48 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc41431154f4cccb130328f9bda92ac3cd374c3bc4ef8b29827399ebd22bc749`  
		Last Modified: Wed, 28 Jan 2026 02:56:49 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6.4-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:193c4ff5e06269d1446ab3235284aa43d244fdbc13dffdc98c715540fcc455e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.1 KB (14146 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:060b8b064e4aba529d56ef354367ffae940f6b152b36f64ea427dfcd51e51f1e`

```dockerfile
```

-	Layers:
	-	`sha256:9257c6b08dae939c45fb6b5cd969064dde84328d15653df8b0ab98dae6b31d32`  
		Last Modified: Wed, 28 Jan 2026 02:56:48 GMT  
		Size: 14.1 KB (14146 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6.4-alpine` - linux; arm variant v7

```console
$ docker pull spiped@sha256:71592cfee4b071cad3b52c3cfdefddd8ff72e3d5e644d8859d2d8cec8397a0d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3314649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c48ddb927471eeb09c0d2e183b02bb1074d36b5caa9dbd3477ee935a8eed01f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:29 GMT
ADD alpine-minirootfs-3.22.3-armv7.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:29 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:56:24 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Wed, 28 Jan 2026 02:56:25 GMT
RUN apk add --no-cache libssl3 # buildkit
# Wed, 28 Jan 2026 02:56:34 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Wed, 28 Jan 2026 02:56:34 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Wed, 28 Jan 2026 02:56:34 GMT
VOLUME [/spiped]
# Wed, 28 Jan 2026 02:56:34 GMT
WORKDIR /spiped
# Wed, 28 Jan 2026 02:56:34 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 02:56:34 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 02:56:34 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:caca1d0e2f8affe80569328af55c755a8480801c5ee912e55aaa828c8209aa6e`  
		Last Modified: Wed, 28 Jan 2026 01:18:35 GMT  
		Size: 3.2 MB (3223629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:332ba379620ebeacb95d57ee5ff3ce395b9868fe9f8d00a5b85dd41df19b3a23`  
		Last Modified: Wed, 28 Jan 2026 02:56:39 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:471e6c87dbde5f46d8cd1e26b6a653a7d77209c851df54df0c065355b1c36749`  
		Last Modified: Wed, 28 Jan 2026 02:56:39 GMT  
		Size: 8.0 KB (7952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:917e2b19aaa32cc304579e079305131ee112e7015524177e84f33379315c24f6`  
		Last Modified: Wed, 28 Jan 2026 02:56:39 GMT  
		Size: 81.7 KB (81685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9d229583db181996be822e85b4fe259ecd55350b04637a090977de317d8cb53`  
		Last Modified: Wed, 28 Jan 2026 02:56:39 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:283dd24da1a4b40bed9d28f9196f24341abf5ee8a13f180db2b3e6daa7e85b8d`  
		Last Modified: Wed, 28 Jan 2026 02:56:40 GMT  
		Size: 336.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6.4-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:b0d30665b0b25a584022937647a82e260a99dc3822f06eae03c777c08c589459
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.6 KB (96590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5de7b9137b4705f6bfaa43d68be9ab47cda877656a88568a8b98eaecf834d723`

```dockerfile
```

-	Layers:
	-	`sha256:bf20f6c9425bc14bf83c368ad820cbac85037f9cfe9e8f428105dcae79aa5f0a`  
		Last Modified: Wed, 28 Jan 2026 02:56:39 GMT  
		Size: 82.2 KB (82228 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3c326467351e8aaa1070327395a8ce06feaf36e791288cc8d0efc059293853a6`  
		Last Modified: Wed, 28 Jan 2026 02:56:39 GMT  
		Size: 14.4 KB (14362 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6.4-alpine` - linux; arm64 variant v8

```console
$ docker pull spiped@sha256:effcfa5e900325dc5a9f2ce725d32bb928170b9fae13c2414035f7c74db4832d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4249465 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1129da21c1ac14cfe9747c51280fa104e3e2a4a7fb499fce9d2f79394c096e45`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:55 GMT
ADD alpine-minirootfs-3.22.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:55 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:37:44 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Wed, 28 Jan 2026 02:37:45 GMT
RUN apk add --no-cache libssl3 # buildkit
# Wed, 28 Jan 2026 02:37:55 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Wed, 28 Jan 2026 02:37:55 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Wed, 28 Jan 2026 02:37:55 GMT
VOLUME [/spiped]
# Wed, 28 Jan 2026 02:37:55 GMT
WORKDIR /spiped
# Wed, 28 Jan 2026 02:37:55 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 02:37:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 02:37:55 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:d741ee1608f399e21c72d05f0f818c348c6801af33aeb83523893d09dc153957`  
		Last Modified: Wed, 28 Jan 2026 01:18:00 GMT  
		Size: 4.1 MB (4139519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a215f43d3f31692bff6dbb7a8464a9777ff146fd6817d85616dd79d628db9a4e`  
		Last Modified: Wed, 28 Jan 2026 02:38:00 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a149826e8201bd60e39e8acb8c71ee749c537b2c783a541e04af7a7b3fc6b5d`  
		Last Modified: Wed, 28 Jan 2026 02:38:00 GMT  
		Size: 8.0 KB (7951 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3816514d66f19e4e15afc0dae177ea8f1397bbaeba0189b4a33a3f265afbb21`  
		Last Modified: Wed, 28 Jan 2026 02:38:00 GMT  
		Size: 100.6 KB (100615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f073eca19d0c28ea18c16d7aa1388a52393935ac0e76036549b53fca85d50741`  
		Last Modified: Wed, 28 Jan 2026 02:38:00 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56ae442366147b99273aabaaf180c7a0347dd957817ff21ec6495a8f374fd7b5`  
		Last Modified: Wed, 28 Jan 2026 02:38:01 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6.4-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:20c426c97f5ccc77dcb4c2895905f7a3e9aedaf5bf12fbf4b3ff87748f7ebc74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.6 KB (96641 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f74a0ff8267a4110c62ab6dcdcf2bf4949f9f54a7ff5e5b96a7e78b99f9770c`

```dockerfile
```

-	Layers:
	-	`sha256:ce7e8f74c44956e8b3a9213e0686a5007c77ddc5cd5210760e512537c99dcb4f`  
		Last Modified: Wed, 28 Jan 2026 02:38:00 GMT  
		Size: 82.2 KB (82248 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5744a1e9a5178b40c2e43ceccdad37fa256e17fb5a7e73342aa361c38b071ea6`  
		Last Modified: Wed, 28 Jan 2026 02:38:00 GMT  
		Size: 14.4 KB (14393 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6.4-alpine` - linux; 386

```console
$ docker pull spiped@sha256:d29799b7499dd97718236dec910ca0fb21a58b93b04c13b9d32bd3972850d109
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3750150 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c829adab8d4ab1c5c9eef2ab8cd6fc3b09ac7a5b2c98b60eb750eaadcf3ca449`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:53 GMT
ADD alpine-minirootfs-3.22.3-x86.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:53 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:31:22 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Wed, 28 Jan 2026 02:31:22 GMT
RUN apk add --no-cache libssl3 # buildkit
# Wed, 28 Jan 2026 02:31:32 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Wed, 28 Jan 2026 02:31:32 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Wed, 28 Jan 2026 02:31:32 GMT
VOLUME [/spiped]
# Wed, 28 Jan 2026 02:31:32 GMT
WORKDIR /spiped
# Wed, 28 Jan 2026 02:31:32 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 02:31:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 02:31:32 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:757a99eda61f22434071cfbc7a70f9526b63aeb5479a64272982017ee7cd9cfd`  
		Last Modified: Wed, 28 Jan 2026 01:18:59 GMT  
		Size: 3.6 MB (3620732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2088b329d71531fcaf8b6b6b5fb05bd132488a9b146463fda72d73f3b193da77`  
		Last Modified: Wed, 28 Jan 2026 02:31:36 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df6327ced333146d36cce9bad13d15f14d00cfba342ef14347eb76323f377623`  
		Last Modified: Wed, 28 Jan 2026 02:31:37 GMT  
		Size: 7.9 KB (7940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3f74692486d32e3c25efb4bcdbdd450b58db493d05a003140a026ba85c130a6`  
		Last Modified: Wed, 28 Jan 2026 02:31:36 GMT  
		Size: 120.1 KB (120096 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b377c56ed7e39aeec7320819a810cd8637819dc2c7f00e5f02f6008223d5ed8`  
		Last Modified: Wed, 28 Jan 2026 02:31:37 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e023ec54765d4d3764e0855b6d7cfe0e2f9966db68bd933fe3f4fe6c41a2474f`  
		Last Modified: Wed, 28 Jan 2026 02:31:38 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6.4-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:49494f0bf8ea2a9ac91bc338facd2f7cede025b28b7848656878d7ce0deadf5c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.4 KB (96390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16387e224ee0b4762e3111436b2fdc3a8bfebe61d796cc65af094da1ebf76cd0`

```dockerfile
```

-	Layers:
	-	`sha256:bdc547d749394448a39cd679c285ba250424589df32f26c116cdc3bca37fedf9`  
		Last Modified: Wed, 28 Jan 2026 02:31:36 GMT  
		Size: 82.2 KB (82167 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4f968b5a19cf7dfb341a81ce64526ba67dbdecae7dbd82f7332ab1f24bf7e26a`  
		Last Modified: Wed, 28 Jan 2026 02:31:36 GMT  
		Size: 14.2 KB (14223 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6.4-alpine` - linux; ppc64le

```console
$ docker pull spiped@sha256:ec49e51d1b31aef6ee4c32cbd2374c5115032febd535905c0146f19ca7d1b88c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3856312 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c52e05f6841b2c0f9dcb913e52c349b3ec2747c75f53e9b3d6a41cd3c6103a9d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:35 GMT
ADD alpine-minirootfs-3.22.3-ppc64le.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:35 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 03:59:19 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Wed, 28 Jan 2026 03:59:21 GMT
RUN apk add --no-cache libssl3 # buildkit
# Wed, 28 Jan 2026 03:59:33 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Wed, 28 Jan 2026 03:59:33 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Wed, 28 Jan 2026 03:59:33 GMT
VOLUME [/spiped]
# Wed, 28 Jan 2026 03:59:33 GMT
WORKDIR /spiped
# Wed, 28 Jan 2026 03:59:34 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 03:59:34 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 03:59:34 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:d7b7d5bab08f20b53e85395b2d6e793469e3acdbe8644bd234992524588b440f`  
		Last Modified: Wed, 28 Jan 2026 01:17:44 GMT  
		Size: 3.7 MB (3734297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52389dd33bb155b2c78fa5202c8c9909e97b12049d41f7cb5369100d2a7be819`  
		Last Modified: Wed, 28 Jan 2026 03:59:48 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28fd5646a7c2ce724b02160a31080c85b3571ffddbc309ccb39fb23e5075d4aa`  
		Last Modified: Wed, 28 Jan 2026 03:59:47 GMT  
		Size: 8.0 KB (7956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d83f042b4cb936ae2f704768b0462b7f539ba799143799dc6a8ce0babc73884`  
		Last Modified: Wed, 28 Jan 2026 03:59:48 GMT  
		Size: 112.7 KB (112673 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b77f4a6884030927f7cdd451b10bba40c6cf61fd40534ca3a9cf653bb742ea8f`  
		Last Modified: Wed, 28 Jan 2026 03:59:48 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34fbfb80739dd4ce26eb065be080a75c602340f3242a297925caf40baf400db0`  
		Last Modified: Wed, 28 Jan 2026 03:59:49 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6.4-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:1d08517919e2dfe608c1e408886b7ef4659cd9f15bf49a67583fe931eb307650
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.6 KB (94578 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b68d34137d518c2381ecd841ecef0a23786265f08c1952e0ed2134cc2ba9073`

```dockerfile
```

-	Layers:
	-	`sha256:b57bb2bf93c55cd637df776032387ee2beae0039a87bacf4e588dd43aaa36711`  
		Last Modified: Wed, 28 Jan 2026 03:59:48 GMT  
		Size: 80.3 KB (80275 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e4a73d72709b0315e9f657137bb6dbf7c0679131d8e10876ea8a1bb94e4201b4`  
		Last Modified: Wed, 28 Jan 2026 03:59:48 GMT  
		Size: 14.3 KB (14303 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6.4-alpine` - linux; riscv64

```console
$ docker pull spiped@sha256:0e7e07e5944d0951da4949f8298cdccfa6ec9395c2d0ddf983aa7f40bf7807f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3625620 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00565f6907e5ae385b224d048c255c22407d6a59d79533da4912c486d4ee1360`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 28 Jan 2026 03:49:43 GMT
ADD alpine-minirootfs-3.22.3-riscv64.tar.gz / # buildkit
# Wed, 28 Jan 2026 03:49:43 GMT
CMD ["/bin/sh"]
# Thu, 29 Jan 2026 18:56:58 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Thu, 29 Jan 2026 18:57:02 GMT
RUN apk add --no-cache libssl3 # buildkit
# Thu, 29 Jan 2026 18:58:38 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Thu, 29 Jan 2026 18:58:38 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Thu, 29 Jan 2026 18:58:38 GMT
VOLUME [/spiped]
# Thu, 29 Jan 2026 18:58:39 GMT
WORKDIR /spiped
# Thu, 29 Jan 2026 18:58:39 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Thu, 29 Jan 2026 18:58:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 29 Jan 2026 18:58:39 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:15ea87d2370d91334d14e1cb46366adb6a57bbae717f07f8c9f55735cf137f62`  
		Last Modified: Wed, 28 Jan 2026 03:50:15 GMT  
		Size: 3.5 MB (3517422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c85b2fc2b9bdc2a30eea3483d034231cba4cf794b774e9c668e43189f965204b`  
		Last Modified: Thu, 29 Jan 2026 18:58:59 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7a35d458c7098a7c5f24f347a75cf6930f742a2e14ae40067defc23e63d57b5`  
		Last Modified: Thu, 29 Jan 2026 18:58:59 GMT  
		Size: 7.9 KB (7944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fbbaf165e7e5cf59739b8e5317789f9a907da0dc26f3803ae533e05f7a2068e`  
		Last Modified: Thu, 29 Jan 2026 18:58:59 GMT  
		Size: 98.9 KB (98867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15e0973003e6d2e757a9f14bfb9ab4d4b6be0abf8bbdfa7a9b699232646e0df6`  
		Last Modified: Thu, 29 Jan 2026 18:58:59 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8509faeca8d8af4689f4b76d19f92f0deeb48d08e62ab656d5ad988fe97b48e9`  
		Last Modified: Thu, 29 Jan 2026 18:59:00 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6.4-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:45c5a2bccce0c2d968718cdc5b92e2d54486ce35d6f21169c8e2975138906721
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.6 KB (94575 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3828726b576d70b513dac001f2810887cf67c235a77086291ebdeb6df7a249f`

```dockerfile
```

-	Layers:
	-	`sha256:53e8f0117ebdf17125860003417afad58a90f091d2b04b6763e9b4ce1899228b`  
		Last Modified: Thu, 29 Jan 2026 18:58:59 GMT  
		Size: 80.3 KB (80271 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0edfbeca58a13ce30fdd21ef302873aa05c28498d058231b777fe51653a06eb6`  
		Last Modified: Thu, 29 Jan 2026 18:58:59 GMT  
		Size: 14.3 KB (14304 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6.4-alpine` - linux; s390x

```console
$ docker pull spiped@sha256:0aeb96b9c7c968a0ad51a4c785e0c76534a115d395c587eacd587a3aad55b360
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3756697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b72691935166b1882b3040950315ed19d9cf1a3678909a868fa5c27a1a58e2b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:06 GMT
ADD alpine-minirootfs-3.22.3-s390x.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:06 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 03:05:47 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Wed, 28 Jan 2026 03:05:48 GMT
RUN apk add --no-cache libssl3 # buildkit
# Wed, 28 Jan 2026 03:05:55 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Wed, 28 Jan 2026 03:05:55 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Wed, 28 Jan 2026 03:05:55 GMT
VOLUME [/spiped]
# Wed, 28 Jan 2026 03:05:55 GMT
WORKDIR /spiped
# Wed, 28 Jan 2026 03:05:55 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 03:05:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 03:05:55 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:dab48b8d1bab09fede3f54264828e67466f10d64acc37d9412190034dbcbf61f`  
		Last Modified: Wed, 28 Jan 2026 01:17:16 GMT  
		Size: 3.7 MB (3650434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0789ee1817b07966cd80a07b05a82d8e0c9bf85f6053f4955ac4731e47448ad`  
		Last Modified: Wed, 28 Jan 2026 03:06:03 GMT  
		Size: 949.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e526c5a7e2d6f02b24c7ed3860ec8221dcd7d0c6e4112d267da6729a13890448`  
		Last Modified: Wed, 28 Jan 2026 03:06:03 GMT  
		Size: 7.9 KB (7949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f10bca7622d69f6335c554b1c8cec2a82753df66ed9cf072d635820439e1af3c`  
		Last Modified: Wed, 28 Jan 2026 03:06:03 GMT  
		Size: 96.9 KB (96933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81d81cea7ec993f5c76e72bd06b1579e878f6a4d1a4a2f11114f710747ef40d4`  
		Last Modified: Wed, 28 Jan 2026 03:06:03 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:086ab53d5ebb5741d97d120d1a1ad7797bf2fda46a7ff1f9a033efa0117cd233`  
		Last Modified: Wed, 28 Jan 2026 03:06:04 GMT  
		Size: 336.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6.4-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:c32f5675d459d866b7c69b2159549861b770e81fa270485088e909f23c515b9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.5 KB (94497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a76bce779a8727519c7fb65566c2ce929337d21a3d6addd2f301cd51f95516c4`

```dockerfile
```

-	Layers:
	-	`sha256:85780af5cccece93dbeac028f8517ebc14f3298ca69ddd75bcf80809c0ea3432`  
		Last Modified: Wed, 28 Jan 2026 03:06:03 GMT  
		Size: 80.2 KB (80241 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:797300601f0f43bd14d2b3e327c7100b2a1b8356e4290096f308e710af773718`  
		Last Modified: Wed, 28 Jan 2026 03:06:03 GMT  
		Size: 14.3 KB (14256 bytes)  
		MIME: application/vnd.in-toto+json

## `spiped:alpine`

```console
$ docker pull spiped@sha256:2e861202f057586ae2e6dc3a5290d61949120d861e272b5700c1e30e1ae9774c
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
$ docker pull spiped@sha256:45aa25e16b20aaf22415c03717dfbffb2460250d93ccfbf50d304296f0323560
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3921849 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c42c3ad8f87ea2a2987c07857dc357c5caa6eb7fe68f8ab758c81d2c67f6316`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:40 GMT
ADD alpine-minirootfs-3.22.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:40 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:36:46 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Wed, 28 Jan 2026 02:36:47 GMT
RUN apk add --no-cache libssl3 # buildkit
# Wed, 28 Jan 2026 02:36:57 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Wed, 28 Jan 2026 02:36:57 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Wed, 28 Jan 2026 02:36:57 GMT
VOLUME [/spiped]
# Wed, 28 Jan 2026 02:36:57 GMT
WORKDIR /spiped
# Wed, 28 Jan 2026 02:36:57 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 02:36:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 02:36:57 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:d49a2dee86fb12766dd648402d010ca105846a41bd58738454e53780d4bb8e97`  
		Last Modified: Wed, 28 Jan 2026 01:18:46 GMT  
		Size: 3.8 MB (3804875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:255f2b198269941f9011d88cebad6e20b25c8054b5ac4ebd1b07f9750a69d255`  
		Last Modified: Wed, 28 Jan 2026 02:37:03 GMT  
		Size: 949.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed562f6049bf766f9af2aeb064224279b938162b44667a74bc7ca9c31ac1d70a`  
		Last Modified: Wed, 28 Jan 2026 02:37:03 GMT  
		Size: 7.9 KB (7945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d20d0ab7b6d45d1dbeebe557e32936e50678b9985769e6bd0ff3e1ff5e433e69`  
		Last Modified: Wed, 28 Jan 2026 02:37:03 GMT  
		Size: 107.6 KB (107647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:868415b885be47751e88ed3c97ca195abec55deffeb9f4ad2846ad3d25cdec28`  
		Last Modified: Wed, 28 Jan 2026 02:37:03 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7d8f030e4a64f48108d2120539708364c71dc39133649b15a0ad263ec9bfe40`  
		Last Modified: Wed, 28 Jan 2026 02:37:04 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:14bccfab21e7b3f36806b9521edfd711ef99c418ce1a38f2c913859e95caa2fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.5 KB (96451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e0f387ff25d96b6eec2a5942d1be095ce8d2cd8945dadefd293a3706d31ea69`

```dockerfile
```

-	Layers:
	-	`sha256:3abca7ed4aae68f57768d18d39b5d6b1c58a733af4507188677241020e39e0d9`  
		Last Modified: Wed, 28 Jan 2026 02:37:03 GMT  
		Size: 82.2 KB (82192 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bf6768ac276576d5f59511c63ded4afa12e2d77d28be7bffc6d1537d58bb57bb`  
		Last Modified: Wed, 28 Jan 2026 02:37:03 GMT  
		Size: 14.3 KB (14259 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:alpine` - linux; arm variant v6

```console
$ docker pull spiped@sha256:3840e207c5f175385b57ca037766c41623e4a780197b93760ca83297bd8e51ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3603526 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f07ce0978d45ec15bdc0a08bdc59ff908f2bd78005af85d4bbad7345be081ee2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:06 GMT
ADD alpine-minirootfs-3.22.3-armhf.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:06 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:56:33 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Wed, 28 Jan 2026 02:56:34 GMT
RUN apk add --no-cache libssl3 # buildkit
# Wed, 28 Jan 2026 02:56:44 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Wed, 28 Jan 2026 02:56:44 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Wed, 28 Jan 2026 02:56:44 GMT
VOLUME [/spiped]
# Wed, 28 Jan 2026 02:56:44 GMT
WORKDIR /spiped
# Wed, 28 Jan 2026 02:56:44 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 02:56:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 02:56:44 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:835838571e5c80c63481753299e25a9f89f366d8f4a9c1a2043b8fdf98176f17`  
		Last Modified: Wed, 28 Jan 2026 01:18:10 GMT  
		Size: 3.5 MB (3505046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5a5ad93e4f03c704fabcd2728cb1ab8244c96ef0876f3fcc9779085a8d3be96`  
		Last Modified: Wed, 28 Jan 2026 02:56:48 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:092107d3ff0fcf3229ae39acf729a354fda97b10c713e7073d550bb7c69025bc`  
		Last Modified: Wed, 28 Jan 2026 02:56:48 GMT  
		Size: 7.9 KB (7944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcb00245db6ff8769dfa116d0e6194c8908449cd54b3995e5f0044b278d0fb45`  
		Last Modified: Wed, 28 Jan 2026 02:56:48 GMT  
		Size: 89.2 KB (89154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3375ee92dad5bd59b0dde03ad45bdf7a8f7df3aaa1e2847b17cdd6734893cfb8`  
		Last Modified: Wed, 28 Jan 2026 02:56:48 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc41431154f4cccb130328f9bda92ac3cd374c3bc4ef8b29827399ebd22bc749`  
		Last Modified: Wed, 28 Jan 2026 02:56:49 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:193c4ff5e06269d1446ab3235284aa43d244fdbc13dffdc98c715540fcc455e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.1 KB (14146 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:060b8b064e4aba529d56ef354367ffae940f6b152b36f64ea427dfcd51e51f1e`

```dockerfile
```

-	Layers:
	-	`sha256:9257c6b08dae939c45fb6b5cd969064dde84328d15653df8b0ab98dae6b31d32`  
		Last Modified: Wed, 28 Jan 2026 02:56:48 GMT  
		Size: 14.1 KB (14146 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:alpine` - linux; arm variant v7

```console
$ docker pull spiped@sha256:71592cfee4b071cad3b52c3cfdefddd8ff72e3d5e644d8859d2d8cec8397a0d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3314649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c48ddb927471eeb09c0d2e183b02bb1074d36b5caa9dbd3477ee935a8eed01f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:29 GMT
ADD alpine-minirootfs-3.22.3-armv7.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:29 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:56:24 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Wed, 28 Jan 2026 02:56:25 GMT
RUN apk add --no-cache libssl3 # buildkit
# Wed, 28 Jan 2026 02:56:34 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Wed, 28 Jan 2026 02:56:34 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Wed, 28 Jan 2026 02:56:34 GMT
VOLUME [/spiped]
# Wed, 28 Jan 2026 02:56:34 GMT
WORKDIR /spiped
# Wed, 28 Jan 2026 02:56:34 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 02:56:34 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 02:56:34 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:caca1d0e2f8affe80569328af55c755a8480801c5ee912e55aaa828c8209aa6e`  
		Last Modified: Wed, 28 Jan 2026 01:18:35 GMT  
		Size: 3.2 MB (3223629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:332ba379620ebeacb95d57ee5ff3ce395b9868fe9f8d00a5b85dd41df19b3a23`  
		Last Modified: Wed, 28 Jan 2026 02:56:39 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:471e6c87dbde5f46d8cd1e26b6a653a7d77209c851df54df0c065355b1c36749`  
		Last Modified: Wed, 28 Jan 2026 02:56:39 GMT  
		Size: 8.0 KB (7952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:917e2b19aaa32cc304579e079305131ee112e7015524177e84f33379315c24f6`  
		Last Modified: Wed, 28 Jan 2026 02:56:39 GMT  
		Size: 81.7 KB (81685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9d229583db181996be822e85b4fe259ecd55350b04637a090977de317d8cb53`  
		Last Modified: Wed, 28 Jan 2026 02:56:39 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:283dd24da1a4b40bed9d28f9196f24341abf5ee8a13f180db2b3e6daa7e85b8d`  
		Last Modified: Wed, 28 Jan 2026 02:56:40 GMT  
		Size: 336.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:b0d30665b0b25a584022937647a82e260a99dc3822f06eae03c777c08c589459
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.6 KB (96590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5de7b9137b4705f6bfaa43d68be9ab47cda877656a88568a8b98eaecf834d723`

```dockerfile
```

-	Layers:
	-	`sha256:bf20f6c9425bc14bf83c368ad820cbac85037f9cfe9e8f428105dcae79aa5f0a`  
		Last Modified: Wed, 28 Jan 2026 02:56:39 GMT  
		Size: 82.2 KB (82228 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3c326467351e8aaa1070327395a8ce06feaf36e791288cc8d0efc059293853a6`  
		Last Modified: Wed, 28 Jan 2026 02:56:39 GMT  
		Size: 14.4 KB (14362 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:alpine` - linux; arm64 variant v8

```console
$ docker pull spiped@sha256:effcfa5e900325dc5a9f2ce725d32bb928170b9fae13c2414035f7c74db4832d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4249465 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1129da21c1ac14cfe9747c51280fa104e3e2a4a7fb499fce9d2f79394c096e45`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:55 GMT
ADD alpine-minirootfs-3.22.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:55 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:37:44 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Wed, 28 Jan 2026 02:37:45 GMT
RUN apk add --no-cache libssl3 # buildkit
# Wed, 28 Jan 2026 02:37:55 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Wed, 28 Jan 2026 02:37:55 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Wed, 28 Jan 2026 02:37:55 GMT
VOLUME [/spiped]
# Wed, 28 Jan 2026 02:37:55 GMT
WORKDIR /spiped
# Wed, 28 Jan 2026 02:37:55 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 02:37:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 02:37:55 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:d741ee1608f399e21c72d05f0f818c348c6801af33aeb83523893d09dc153957`  
		Last Modified: Wed, 28 Jan 2026 01:18:00 GMT  
		Size: 4.1 MB (4139519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a215f43d3f31692bff6dbb7a8464a9777ff146fd6817d85616dd79d628db9a4e`  
		Last Modified: Wed, 28 Jan 2026 02:38:00 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a149826e8201bd60e39e8acb8c71ee749c537b2c783a541e04af7a7b3fc6b5d`  
		Last Modified: Wed, 28 Jan 2026 02:38:00 GMT  
		Size: 8.0 KB (7951 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3816514d66f19e4e15afc0dae177ea8f1397bbaeba0189b4a33a3f265afbb21`  
		Last Modified: Wed, 28 Jan 2026 02:38:00 GMT  
		Size: 100.6 KB (100615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f073eca19d0c28ea18c16d7aa1388a52393935ac0e76036549b53fca85d50741`  
		Last Modified: Wed, 28 Jan 2026 02:38:00 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56ae442366147b99273aabaaf180c7a0347dd957817ff21ec6495a8f374fd7b5`  
		Last Modified: Wed, 28 Jan 2026 02:38:01 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:20c426c97f5ccc77dcb4c2895905f7a3e9aedaf5bf12fbf4b3ff87748f7ebc74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.6 KB (96641 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f74a0ff8267a4110c62ab6dcdcf2bf4949f9f54a7ff5e5b96a7e78b99f9770c`

```dockerfile
```

-	Layers:
	-	`sha256:ce7e8f74c44956e8b3a9213e0686a5007c77ddc5cd5210760e512537c99dcb4f`  
		Last Modified: Wed, 28 Jan 2026 02:38:00 GMT  
		Size: 82.2 KB (82248 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5744a1e9a5178b40c2e43ceccdad37fa256e17fb5a7e73342aa361c38b071ea6`  
		Last Modified: Wed, 28 Jan 2026 02:38:00 GMT  
		Size: 14.4 KB (14393 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:alpine` - linux; 386

```console
$ docker pull spiped@sha256:d29799b7499dd97718236dec910ca0fb21a58b93b04c13b9d32bd3972850d109
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3750150 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c829adab8d4ab1c5c9eef2ab8cd6fc3b09ac7a5b2c98b60eb750eaadcf3ca449`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:53 GMT
ADD alpine-minirootfs-3.22.3-x86.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:53 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:31:22 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Wed, 28 Jan 2026 02:31:22 GMT
RUN apk add --no-cache libssl3 # buildkit
# Wed, 28 Jan 2026 02:31:32 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Wed, 28 Jan 2026 02:31:32 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Wed, 28 Jan 2026 02:31:32 GMT
VOLUME [/spiped]
# Wed, 28 Jan 2026 02:31:32 GMT
WORKDIR /spiped
# Wed, 28 Jan 2026 02:31:32 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 02:31:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 02:31:32 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:757a99eda61f22434071cfbc7a70f9526b63aeb5479a64272982017ee7cd9cfd`  
		Last Modified: Wed, 28 Jan 2026 01:18:59 GMT  
		Size: 3.6 MB (3620732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2088b329d71531fcaf8b6b6b5fb05bd132488a9b146463fda72d73f3b193da77`  
		Last Modified: Wed, 28 Jan 2026 02:31:36 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df6327ced333146d36cce9bad13d15f14d00cfba342ef14347eb76323f377623`  
		Last Modified: Wed, 28 Jan 2026 02:31:37 GMT  
		Size: 7.9 KB (7940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3f74692486d32e3c25efb4bcdbdd450b58db493d05a003140a026ba85c130a6`  
		Last Modified: Wed, 28 Jan 2026 02:31:36 GMT  
		Size: 120.1 KB (120096 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b377c56ed7e39aeec7320819a810cd8637819dc2c7f00e5f02f6008223d5ed8`  
		Last Modified: Wed, 28 Jan 2026 02:31:37 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e023ec54765d4d3764e0855b6d7cfe0e2f9966db68bd933fe3f4fe6c41a2474f`  
		Last Modified: Wed, 28 Jan 2026 02:31:38 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:49494f0bf8ea2a9ac91bc338facd2f7cede025b28b7848656878d7ce0deadf5c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.4 KB (96390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16387e224ee0b4762e3111436b2fdc3a8bfebe61d796cc65af094da1ebf76cd0`

```dockerfile
```

-	Layers:
	-	`sha256:bdc547d749394448a39cd679c285ba250424589df32f26c116cdc3bca37fedf9`  
		Last Modified: Wed, 28 Jan 2026 02:31:36 GMT  
		Size: 82.2 KB (82167 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4f968b5a19cf7dfb341a81ce64526ba67dbdecae7dbd82f7332ab1f24bf7e26a`  
		Last Modified: Wed, 28 Jan 2026 02:31:36 GMT  
		Size: 14.2 KB (14223 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:alpine` - linux; ppc64le

```console
$ docker pull spiped@sha256:ec49e51d1b31aef6ee4c32cbd2374c5115032febd535905c0146f19ca7d1b88c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3856312 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c52e05f6841b2c0f9dcb913e52c349b3ec2747c75f53e9b3d6a41cd3c6103a9d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:35 GMT
ADD alpine-minirootfs-3.22.3-ppc64le.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:35 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 03:59:19 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Wed, 28 Jan 2026 03:59:21 GMT
RUN apk add --no-cache libssl3 # buildkit
# Wed, 28 Jan 2026 03:59:33 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Wed, 28 Jan 2026 03:59:33 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Wed, 28 Jan 2026 03:59:33 GMT
VOLUME [/spiped]
# Wed, 28 Jan 2026 03:59:33 GMT
WORKDIR /spiped
# Wed, 28 Jan 2026 03:59:34 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 03:59:34 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 03:59:34 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:d7b7d5bab08f20b53e85395b2d6e793469e3acdbe8644bd234992524588b440f`  
		Last Modified: Wed, 28 Jan 2026 01:17:44 GMT  
		Size: 3.7 MB (3734297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52389dd33bb155b2c78fa5202c8c9909e97b12049d41f7cb5369100d2a7be819`  
		Last Modified: Wed, 28 Jan 2026 03:59:48 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28fd5646a7c2ce724b02160a31080c85b3571ffddbc309ccb39fb23e5075d4aa`  
		Last Modified: Wed, 28 Jan 2026 03:59:47 GMT  
		Size: 8.0 KB (7956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d83f042b4cb936ae2f704768b0462b7f539ba799143799dc6a8ce0babc73884`  
		Last Modified: Wed, 28 Jan 2026 03:59:48 GMT  
		Size: 112.7 KB (112673 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b77f4a6884030927f7cdd451b10bba40c6cf61fd40534ca3a9cf653bb742ea8f`  
		Last Modified: Wed, 28 Jan 2026 03:59:48 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34fbfb80739dd4ce26eb065be080a75c602340f3242a297925caf40baf400db0`  
		Last Modified: Wed, 28 Jan 2026 03:59:49 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:1d08517919e2dfe608c1e408886b7ef4659cd9f15bf49a67583fe931eb307650
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.6 KB (94578 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b68d34137d518c2381ecd841ecef0a23786265f08c1952e0ed2134cc2ba9073`

```dockerfile
```

-	Layers:
	-	`sha256:b57bb2bf93c55cd637df776032387ee2beae0039a87bacf4e588dd43aaa36711`  
		Last Modified: Wed, 28 Jan 2026 03:59:48 GMT  
		Size: 80.3 KB (80275 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e4a73d72709b0315e9f657137bb6dbf7c0679131d8e10876ea8a1bb94e4201b4`  
		Last Modified: Wed, 28 Jan 2026 03:59:48 GMT  
		Size: 14.3 KB (14303 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:alpine` - linux; riscv64

```console
$ docker pull spiped@sha256:0e7e07e5944d0951da4949f8298cdccfa6ec9395c2d0ddf983aa7f40bf7807f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3625620 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00565f6907e5ae385b224d048c255c22407d6a59d79533da4912c486d4ee1360`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 28 Jan 2026 03:49:43 GMT
ADD alpine-minirootfs-3.22.3-riscv64.tar.gz / # buildkit
# Wed, 28 Jan 2026 03:49:43 GMT
CMD ["/bin/sh"]
# Thu, 29 Jan 2026 18:56:58 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Thu, 29 Jan 2026 18:57:02 GMT
RUN apk add --no-cache libssl3 # buildkit
# Thu, 29 Jan 2026 18:58:38 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Thu, 29 Jan 2026 18:58:38 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Thu, 29 Jan 2026 18:58:38 GMT
VOLUME [/spiped]
# Thu, 29 Jan 2026 18:58:39 GMT
WORKDIR /spiped
# Thu, 29 Jan 2026 18:58:39 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Thu, 29 Jan 2026 18:58:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 29 Jan 2026 18:58:39 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:15ea87d2370d91334d14e1cb46366adb6a57bbae717f07f8c9f55735cf137f62`  
		Last Modified: Wed, 28 Jan 2026 03:50:15 GMT  
		Size: 3.5 MB (3517422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c85b2fc2b9bdc2a30eea3483d034231cba4cf794b774e9c668e43189f965204b`  
		Last Modified: Thu, 29 Jan 2026 18:58:59 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7a35d458c7098a7c5f24f347a75cf6930f742a2e14ae40067defc23e63d57b5`  
		Last Modified: Thu, 29 Jan 2026 18:58:59 GMT  
		Size: 7.9 KB (7944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fbbaf165e7e5cf59739b8e5317789f9a907da0dc26f3803ae533e05f7a2068e`  
		Last Modified: Thu, 29 Jan 2026 18:58:59 GMT  
		Size: 98.9 KB (98867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15e0973003e6d2e757a9f14bfb9ab4d4b6be0abf8bbdfa7a9b699232646e0df6`  
		Last Modified: Thu, 29 Jan 2026 18:58:59 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8509faeca8d8af4689f4b76d19f92f0deeb48d08e62ab656d5ad988fe97b48e9`  
		Last Modified: Thu, 29 Jan 2026 18:59:00 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:45c5a2bccce0c2d968718cdc5b92e2d54486ce35d6f21169c8e2975138906721
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.6 KB (94575 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3828726b576d70b513dac001f2810887cf67c235a77086291ebdeb6df7a249f`

```dockerfile
```

-	Layers:
	-	`sha256:53e8f0117ebdf17125860003417afad58a90f091d2b04b6763e9b4ce1899228b`  
		Last Modified: Thu, 29 Jan 2026 18:58:59 GMT  
		Size: 80.3 KB (80271 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0edfbeca58a13ce30fdd21ef302873aa05c28498d058231b777fe51653a06eb6`  
		Last Modified: Thu, 29 Jan 2026 18:58:59 GMT  
		Size: 14.3 KB (14304 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:alpine` - linux; s390x

```console
$ docker pull spiped@sha256:0aeb96b9c7c968a0ad51a4c785e0c76534a115d395c587eacd587a3aad55b360
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3756697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b72691935166b1882b3040950315ed19d9cf1a3678909a868fa5c27a1a58e2b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:06 GMT
ADD alpine-minirootfs-3.22.3-s390x.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:06 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 03:05:47 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Wed, 28 Jan 2026 03:05:48 GMT
RUN apk add --no-cache libssl3 # buildkit
# Wed, 28 Jan 2026 03:05:55 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Wed, 28 Jan 2026 03:05:55 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Wed, 28 Jan 2026 03:05:55 GMT
VOLUME [/spiped]
# Wed, 28 Jan 2026 03:05:55 GMT
WORKDIR /spiped
# Wed, 28 Jan 2026 03:05:55 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 03:05:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 03:05:55 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:dab48b8d1bab09fede3f54264828e67466f10d64acc37d9412190034dbcbf61f`  
		Last Modified: Wed, 28 Jan 2026 01:17:16 GMT  
		Size: 3.7 MB (3650434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0789ee1817b07966cd80a07b05a82d8e0c9bf85f6053f4955ac4731e47448ad`  
		Last Modified: Wed, 28 Jan 2026 03:06:03 GMT  
		Size: 949.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e526c5a7e2d6f02b24c7ed3860ec8221dcd7d0c6e4112d267da6729a13890448`  
		Last Modified: Wed, 28 Jan 2026 03:06:03 GMT  
		Size: 7.9 KB (7949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f10bca7622d69f6335c554b1c8cec2a82753df66ed9cf072d635820439e1af3c`  
		Last Modified: Wed, 28 Jan 2026 03:06:03 GMT  
		Size: 96.9 KB (96933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81d81cea7ec993f5c76e72bd06b1579e878f6a4d1a4a2f11114f710747ef40d4`  
		Last Modified: Wed, 28 Jan 2026 03:06:03 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:086ab53d5ebb5741d97d120d1a1ad7797bf2fda46a7ff1f9a033efa0117cd233`  
		Last Modified: Wed, 28 Jan 2026 03:06:04 GMT  
		Size: 336.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:c32f5675d459d866b7c69b2159549861b770e81fa270485088e909f23c515b9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.5 KB (94497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a76bce779a8727519c7fb65566c2ce929337d21a3d6addd2f301cd51f95516c4`

```dockerfile
```

-	Layers:
	-	`sha256:85780af5cccece93dbeac028f8517ebc14f3298ca69ddd75bcf80809c0ea3432`  
		Last Modified: Wed, 28 Jan 2026 03:06:03 GMT  
		Size: 80.2 KB (80241 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:797300601f0f43bd14d2b3e327c7100b2a1b8356e4290096f308e710af773718`  
		Last Modified: Wed, 28 Jan 2026 03:06:03 GMT  
		Size: 14.3 KB (14256 bytes)  
		MIME: application/vnd.in-toto+json

## `spiped:latest`

```console
$ docker pull spiped@sha256:86bfe9d75887a0c865ca400bce9556e55f0100324ab12cea4182325b4538c9d3
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
$ docker pull spiped@sha256:1dadd78b37a53143babab424620b268d0e87665451c7e0b19ee714350efeb0aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.8 MB (36825645 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6aec690f0b7647a2b707058d20c805804b9d29cdd158eb3109584ae64c2e9c96`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1773619200'
# Mon, 16 Mar 2026 22:35:50 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Mon, 16 Mar 2026 22:35:52 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:36:17 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Mon, 16 Mar 2026 22:36:17 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Mon, 16 Mar 2026 22:36:17 GMT
VOLUME [/spiped]
# Mon, 16 Mar 2026 22:36:17 GMT
WORKDIR /spiped
# Mon, 16 Mar 2026 22:36:17 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Mon, 16 Mar 2026 22:36:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 16 Mar 2026 22:36:17 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:ec781dee3f4719c2ca0dd9e73cb1d4ed834ed1a406495eb6e44b6dfaad5d1f8f`  
		Last Modified: Mon, 16 Mar 2026 21:53:19 GMT  
		Size: 29.8 MB (29775500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32ceac9107a69b7bfdee6e7660e1eff3feb8d0fd5d6f681f2a6ad1905d93ba0a`  
		Last Modified: Mon, 16 Mar 2026 22:36:24 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1aa4948bacb0a02611ec173cb9f157bd247587fd13cb63e407219ba6dd87af7d`  
		Last Modified: Mon, 16 Mar 2026 22:36:24 GMT  
		Size: 828.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50f472851b739f36f98249e60dba4ceb8a571cbd9f18c3e6b9639215d2c6dcfa`  
		Last Modified: Mon, 16 Mar 2026 22:36:24 GMT  
		Size: 7.0 MB (7047777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7dda7601460289f11e5d3db99f3c14ac9bf518a829bc22ae224a96c8c3a4d4d9`  
		Last Modified: Mon, 16 Mar 2026 22:36:24 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:597b8eb9fa679d5997894aab7d18f62d615b6cc715de0c0a98c8bddef96e43ee`  
		Last Modified: Mon, 16 Mar 2026 22:36:25 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:latest` - unknown; unknown

```console
$ docker pull spiped@sha256:24038ff42b84801b0e2af5de324e185ffb9b47e091947a1d6ead4da071277394
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3641241 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:204d83d1b596e75d2d7efdfccf8e0ab85c3bf694d7310417d68e3add5e86a10f`

```dockerfile
```

-	Layers:
	-	`sha256:1f60bdfcbc8114aba716d733f2c08d28946d1d47510ef32f11fe773e7efbba8c`  
		Last Modified: Mon, 16 Mar 2026 22:36:24 GMT  
		Size: 3.6 MB (3626260 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b07a02dacfe5fad817dc8acef6300290b65922a87b426e54f70d87798a0696f5`  
		Last Modified: Mon, 16 Mar 2026 22:36:24 GMT  
		Size: 15.0 KB (14981 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:latest` - linux; arm variant v5

```console
$ docker pull spiped@sha256:d76bab68c9ba80d6bde9b766de2f4b524b29b2e06796dea03aa1f86973b6e402
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.7 MB (33735071 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e9ce3fe44b3195308782999982dffb0e0324f65968051303e6d0ccb5e46710e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1773619200'
# Mon, 16 Mar 2026 23:15:44 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Mon, 16 Mar 2026 23:15:49 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 23:16:15 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Mon, 16 Mar 2026 23:16:15 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Mon, 16 Mar 2026 23:16:15 GMT
VOLUME [/spiped]
# Mon, 16 Mar 2026 23:16:15 GMT
WORKDIR /spiped
# Mon, 16 Mar 2026 23:16:15 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Mon, 16 Mar 2026 23:16:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 16 Mar 2026 23:16:15 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:eb1defba38d0de4655b895d4763345b3ab078983d3385db43c308a7caca13f2a`  
		Last Modified: Mon, 16 Mar 2026 21:52:26 GMT  
		Size: 27.9 MB (27943649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9cfc1da50f0fc66e4696a6b249cf2c9f19d773fda1096f22c619e19221b8de7`  
		Last Modified: Mon, 16 Mar 2026 23:16:22 GMT  
		Size: 1.1 KB (1105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a98c3d3f9d3a820c9fbfddae7bba53067abc005cb4837355fd2fe02be5159fda`  
		Last Modified: Mon, 16 Mar 2026 23:16:22 GMT  
		Size: 831.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:981177ab397ef56ea1a515604977b4812a8bccc0e0ae76b96ba1a148b66278c5`  
		Last Modified: Mon, 16 Mar 2026 23:16:22 GMT  
		Size: 5.8 MB (5789053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8116b26167b41dbbadb8f30d9738528a34e2436086fd1d12d6d83af070f87911`  
		Last Modified: Mon, 16 Mar 2026 23:16:22 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8f7d349acecae8a4190b1310446bb378d3edc921d84f55ac12cf5202b8df556`  
		Last Modified: Mon, 16 Mar 2026 23:16:23 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:latest` - unknown; unknown

```console
$ docker pull spiped@sha256:1ef3cb6065e7ec1c89ec491fd9bfd3dc5b3221edc45b98e1d076dc81f408837e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3634342 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6758a2f7ff038f8df9fc87c6f4130ff4358acd576e0e39211c178068863796cc`

```dockerfile
```

-	Layers:
	-	`sha256:5a7c54557652f62feaed177546a18b57a4e82674763bde13f27b1dab19e00b9d`  
		Last Modified: Mon, 16 Mar 2026 23:16:23 GMT  
		Size: 3.6 MB (3619254 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:647540c448bfbe8c1ba0711adf24d3a530725e84f4fd25c88632cf2510d9c007`  
		Last Modified: Mon, 16 Mar 2026 23:16:22 GMT  
		Size: 15.1 KB (15088 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:latest` - linux; arm variant v7

```console
$ docker pull spiped@sha256:723ba9f91b55f3576b2113c495e19f93cb621ee72fabcaff1531301fbcaa4b1a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.8 MB (31796429 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5cb0e019fca22ad836d890087ee6d2a180105ee1191adf83d36a753ea37941a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1773619200'
# Mon, 16 Mar 2026 23:17:41 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Mon, 16 Mar 2026 23:17:45 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 23:18:07 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Mon, 16 Mar 2026 23:18:07 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Mon, 16 Mar 2026 23:18:07 GMT
VOLUME [/spiped]
# Mon, 16 Mar 2026 23:18:07 GMT
WORKDIR /spiped
# Mon, 16 Mar 2026 23:18:07 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Mon, 16 Mar 2026 23:18:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 16 Mar 2026 23:18:07 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:7d73604d2a042e7beeb809f68c76f5be3576747809bfaa49747f334227d8d250`  
		Last Modified: Mon, 16 Mar 2026 21:53:24 GMT  
		Size: 26.2 MB (26209505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:658299db6ef3056cf755c844791cbd82e4508468df390e37a8aad706f3a48f4c`  
		Last Modified: Mon, 16 Mar 2026 23:18:14 GMT  
		Size: 1.1 KB (1103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8faf32f19b630a82f84ed9470b862ab68393803b1e37f045f46258e8890f7d50`  
		Last Modified: Mon, 16 Mar 2026 23:18:14 GMT  
		Size: 828.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba29f29a0220be91155a5596cf59a8ec1e848dc1c59089563006ce592b99f829`  
		Last Modified: Mon, 16 Mar 2026 23:18:14 GMT  
		Size: 5.6 MB (5584559 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:571f3aa9916ae33f81a8eff41f15615107662751591ab2cae13c31339f2cdb35`  
		Last Modified: Mon, 16 Mar 2026 23:18:14 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0023499b415317d80739286a45ec7393c98ddc05a638d045c05812141aa28b0`  
		Last Modified: Mon, 16 Mar 2026 23:18:15 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:latest` - unknown; unknown

```console
$ docker pull spiped@sha256:b778f2f8e613351de55fec9efa1c2283e7262e815379cb9c01090839b522f03b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3633463 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:820126e67739682404e3e543b661db54a249ad7238843089922bd27097f59140`

```dockerfile
```

-	Layers:
	-	`sha256:34fdc3e15f493cc5e996b5a867605ede0f868b1b23e1156f69a1d24198213663`  
		Last Modified: Mon, 16 Mar 2026 23:18:14 GMT  
		Size: 3.6 MB (3618375 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7867a53cd4efb0b6f41304907e82351cc690be89532e8db042be1139471fee68`  
		Last Modified: Mon, 16 Mar 2026 23:18:14 GMT  
		Size: 15.1 KB (15088 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:latest` - linux; arm64 variant v8

```console
$ docker pull spiped@sha256:4ae6755ad03f743b18a351fbafa71c65c711f58faea3a81b665befd8567053b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.4 MB (36374360 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0fbe5e7be982e3e0a47d2310365b2015977222cf3f9135331a2ddafbc2a09e29`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1773619200'
# Mon, 16 Mar 2026 22:38:29 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Mon, 16 Mar 2026 22:38:32 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:38:55 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Mon, 16 Mar 2026 22:38:55 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Mon, 16 Mar 2026 22:38:55 GMT
VOLUME [/spiped]
# Mon, 16 Mar 2026 22:38:55 GMT
WORKDIR /spiped
# Mon, 16 Mar 2026 22:38:55 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Mon, 16 Mar 2026 22:38:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 16 Mar 2026 22:38:55 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:f4badedbec24858ef2dc51256f6418328e305e9c3c5a5e093581f83425618bd5`  
		Last Modified: Mon, 16 Mar 2026 21:53:04 GMT  
		Size: 30.1 MB (30138416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59eb94c76468927e4e914285fecca640b78cd857ba3998fcfc270e51a5999a76`  
		Last Modified: Mon, 16 Mar 2026 22:39:02 GMT  
		Size: 1.1 KB (1104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11b2a5c6f2a1a593d60739bde8e5edb5ede5cc1c07d169f19ef39a67402cd65b`  
		Last Modified: Mon, 16 Mar 2026 22:39:02 GMT  
		Size: 828.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bedfccd6793021acdd75a491c31f9164e9dc33b3e7429226d6093a2dd780093`  
		Last Modified: Mon, 16 Mar 2026 22:39:03 GMT  
		Size: 6.2 MB (6233579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b277914700ac4bb0336072358245beede0af746b61ba9febb726f5a24443909`  
		Last Modified: Mon, 16 Mar 2026 22:39:03 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fcc46f0d3ebea317699d8e2e6d3e2c8d2e022621162b4aeb23e6aec0d21d6f3`  
		Last Modified: Mon, 16 Mar 2026 22:39:03 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:latest` - unknown; unknown

```console
$ docker pull spiped@sha256:3bb60c38b60da93affbf4a161bd60f5d201524ab747841166084d1e18235b678
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3636412 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:acfdeacc136a94cefd95b5fc4a223865929593d17a4df005eb979067d4539f09`

```dockerfile
```

-	Layers:
	-	`sha256:da2db9f7e9ec3796af7d7b3c2062fb98cdf3bf4c8cbc30041368b9529682b6e4`  
		Last Modified: Mon, 16 Mar 2026 22:39:03 GMT  
		Size: 3.6 MB (3621296 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c581a66bb5f391583c1fd9137f24523cc1f7cfb6e13f4dca2a22a36d28db1f75`  
		Last Modified: Mon, 16 Mar 2026 22:39:02 GMT  
		Size: 15.1 KB (15116 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:latest` - linux; 386

```console
$ docker pull spiped@sha256:44d93dff5b665eb236d8d461091f645401dad4215fc6e748e75d845e5f88359a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.7 MB (37735593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b145875baf2722671a7d04cbdec8ce2e4e0044fe83f4480f7d13be40ef1b7f0d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1773619200'
# Mon, 16 Mar 2026 22:43:15 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Mon, 16 Mar 2026 22:43:17 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:43:39 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Mon, 16 Mar 2026 22:43:39 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Mon, 16 Mar 2026 22:43:39 GMT
VOLUME [/spiped]
# Mon, 16 Mar 2026 22:43:39 GMT
WORKDIR /spiped
# Mon, 16 Mar 2026 22:43:39 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Mon, 16 Mar 2026 22:43:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 16 Mar 2026 22:43:39 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:2c0c3f3238f3d4cecd93e4dee6eda788943ef955de61c3ad4ff659da1f43ba60`  
		Last Modified: Mon, 16 Mar 2026 21:53:39 GMT  
		Size: 31.3 MB (31291132 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e26822c10be4229a362fafa19cf7744d8e4afd786250bc983de1db93de19f3ff`  
		Last Modified: Mon, 16 Mar 2026 22:43:45 GMT  
		Size: 1.1 KB (1103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6acce4a1df323ade11febca20e664df3454379e4a4d62367fda308fd3377a5b7`  
		Last Modified: Mon, 16 Mar 2026 22:43:45 GMT  
		Size: 827.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ceb4b68e89c0b0dc1a9dc9754d84e4fdcc68a054100397edf14eea9bb6cc12b`  
		Last Modified: Mon, 16 Mar 2026 22:43:46 GMT  
		Size: 6.4 MB (6442097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:300ea57bc8db031eb298c0be9439b59a132b01d16a7971119ccb7c917fbb6554`  
		Last Modified: Mon, 16 Mar 2026 22:43:45 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a7afc0484bbe3e1c40b997eebf00362bc5e5e5711f5533cb6ff54e22c2413b4`  
		Last Modified: Mon, 16 Mar 2026 22:43:46 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:latest` - unknown; unknown

```console
$ docker pull spiped@sha256:513effd7016736f664ccfba169fc4d2d2fbac9b2d09ae5c2427af606b4fef17d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3635335 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03f65e618603d756ec27e2173381823753cc22ece11b748008e7b4745130c1da`

```dockerfile
```

-	Layers:
	-	`sha256:5f750ca150313a2349433840e5c82fdef74358685b619d6b14e5b58e76f0781a`  
		Last Modified: Mon, 16 Mar 2026 22:43:46 GMT  
		Size: 3.6 MB (3620389 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:23ece012ebd2581aea85be27bbc3fe9da829f9ee6cb39f7e97a3637110ad5770`  
		Last Modified: Mon, 16 Mar 2026 22:43:45 GMT  
		Size: 14.9 KB (14946 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:latest` - linux; ppc64le

```console
$ docker pull spiped@sha256:558d9e854b92393e1d96ef6e4d632b42659ff94decbb53b76989997d1e0ec224
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.4 MB (40435868 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8fb525945e5b18678cd55fe712bfb5b6997167921072dfe24c99cc7441368efc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1773619200'
# Tue, 17 Mar 2026 01:48:02 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Tue, 17 Mar 2026 01:48:07 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 01:49:05 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Tue, 17 Mar 2026 01:49:05 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 17 Mar 2026 01:49:05 GMT
VOLUME [/spiped]
# Tue, 17 Mar 2026 01:49:05 GMT
WORKDIR /spiped
# Tue, 17 Mar 2026 01:49:06 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Tue, 17 Mar 2026 01:49:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Mar 2026 01:49:06 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:f078139432e0b368e27241df524f6ef0ed0148b217d7495670dc297af77699fb`  
		Last Modified: Mon, 16 Mar 2026 21:55:56 GMT  
		Size: 33.6 MB (33592834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b23cdd3695d4f8d7ed89e6ef14a27bade53f83dc908d0d81ca0e30631851657d`  
		Last Modified: Tue, 17 Mar 2026 01:49:20 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2aeba3f4cf41d1fe339b87612255223a740f20ca43890419c57f646a0d6b4700`  
		Last Modified: Tue, 17 Mar 2026 01:49:20 GMT  
		Size: 827.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2900931ab7a20d4ba700e41e56664ad7605eb9d341f250b7e024800c787b1f57`  
		Last Modified: Tue, 17 Mar 2026 01:49:20 GMT  
		Size: 6.8 MB (6840666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd461ff0c7b461bb5a3b5a2abf96ce3dec4858db537c1939b8bdfbe1fc8d1dac`  
		Last Modified: Tue, 17 Mar 2026 01:49:20 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8147ab40850402c527ecc2d439d4ce4dab6d232336aa43c20444dc18829f1273`  
		Last Modified: Tue, 17 Mar 2026 01:49:21 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:latest` - unknown; unknown

```console
$ docker pull spiped@sha256:f200a47fd65a47d561c18eabdbae5cd6d9935be2507254b566d43b48e6c57456
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3637027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f8f2b490d9a358d5a7fea9f4d29b4098981a442f93c062a3b276cf4357de8c3`

```dockerfile
```

-	Layers:
	-	`sha256:887ec06e855bee10271ac461e307cde47e3b0f61f873ebe04e4b7bd6687368f2`  
		Last Modified: Tue, 17 Mar 2026 01:49:20 GMT  
		Size: 3.6 MB (3621997 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:91f36846163a85b9df751c3b92a108c1257a4e2dac2c2e2f37c380787eb44d19`  
		Last Modified: Tue, 17 Mar 2026 01:49:20 GMT  
		Size: 15.0 KB (15030 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:latest` - linux; riscv64

```console
$ docker pull spiped@sha256:8bb82489fc130e0ebd5f9bbd52581be946042cfd96ea517ea76d5bc3bf8ebefb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.6 MB (37637359 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3782bede9d9edafc097d7e1829603f7130a6de5afd0278b055260b72c9dc1997`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1771804800'
# Thu, 26 Feb 2026 21:27:02 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Thu, 26 Feb 2026 21:27:31 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 26 Feb 2026 21:30:35 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Thu, 26 Feb 2026 21:30:35 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Thu, 26 Feb 2026 21:30:35 GMT
VOLUME [/spiped]
# Thu, 26 Feb 2026 21:30:36 GMT
WORKDIR /spiped
# Thu, 26 Feb 2026 21:30:36 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Thu, 26 Feb 2026 21:30:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 26 Feb 2026 21:30:36 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:7d614b9ad5a6f3dd0478c6903a6d2ffddc9bc5b17650714d4c1f761161fde58d`  
		Last Modified: Tue, 24 Feb 2026 18:59:14 GMT  
		Size: 28.3 MB (28276417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afbc2b651dc4281762485417954f26f00a147e635dd4386b4dc36ec1c12057b8`  
		Last Modified: Thu, 26 Feb 2026 21:31:48 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04ad29eaeb47daebdc8fd5d52da1dcf0f8ef0dd3a9f796c0f14675426e200e89`  
		Last Modified: Thu, 26 Feb 2026 21:31:48 GMT  
		Size: 822.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b04499c1af0fd231152f64530568de3e0fe490576c3d0bcf0c9743990a7938f7`  
		Last Modified: Thu, 26 Feb 2026 21:31:49 GMT  
		Size: 9.4 MB (9358576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19d9ae5d28f72fa67e546ccb83e7e39152304c5e1d393ceb17fee76009b87c30`  
		Last Modified: Thu, 26 Feb 2026 21:31:48 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c9afcb0cccd5e3f03a3850046642ebf8a8029bf602e5e5b8bd9422d3cf7b350`  
		Last Modified: Thu, 26 Feb 2026 21:31:49 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:latest` - unknown; unknown

```console
$ docker pull spiped@sha256:e5cf967432204ce7118f3ebbd169698a80d6df6bc23555049960d38da754a9d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3628397 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd419f8646942dcae52af9b19c3f390a9c3f6271d67369dcf6fc2c6b69d54b9d`

```dockerfile
```

-	Layers:
	-	`sha256:f67ba2453a68b55021d7f90d26cc1c990f9286371a00137c7cad53780d0559ba`  
		Last Modified: Thu, 26 Feb 2026 21:31:49 GMT  
		Size: 3.6 MB (3613367 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cf05fe9bfbfcb881eacb026a48af7d361ee01b63efce4a7f453d9c6fa4af7fa2`  
		Last Modified: Thu, 26 Feb 2026 21:31:48 GMT  
		Size: 15.0 KB (15030 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:latest` - linux; s390x

```console
$ docker pull spiped@sha256:c3ea82efea9854cb0da628935b60cf04f6c53931b6f7c2d20cd31aa9d27deaf0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.0 MB (35958813 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:579c56a7419832fa8be7ed9c8c7faaf68cb1da36770f667bfdce26ab4c03d59b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1773619200'
# Mon, 16 Mar 2026 23:43:38 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Mon, 16 Mar 2026 23:43:41 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 23:44:00 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Mon, 16 Mar 2026 23:44:00 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Mon, 16 Mar 2026 23:44:00 GMT
VOLUME [/spiped]
# Mon, 16 Mar 2026 23:44:00 GMT
WORKDIR /spiped
# Mon, 16 Mar 2026 23:44:00 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Mon, 16 Mar 2026 23:44:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 16 Mar 2026 23:44:00 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:2c02a3d3f135c4bbe56488921bd86d969a76dcd5278abca1e81884d3bff0bd88`  
		Last Modified: Mon, 16 Mar 2026 21:52:55 GMT  
		Size: 29.8 MB (29835265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c81e7613d635aa581f38ab946c2047e14837502a75f3f4e08fff5f611175fa1`  
		Last Modified: Mon, 16 Mar 2026 23:44:13 GMT  
		Size: 1.1 KB (1105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e7af70f2f5d7c87a4eef797de7cdee0fc7fe1f22a5cdd1d147f73cd11cd3c66`  
		Last Modified: Mon, 16 Mar 2026 23:44:13 GMT  
		Size: 828.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fc179ed0ea05be607a3fd6ab65992063b0b8fad92eba54e1abc2f376ad37586`  
		Last Modified: Mon, 16 Mar 2026 23:44:13 GMT  
		Size: 6.1 MB (6121184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97d07658b602778f575172b4841e370cbe43b5899cb54c7748a2978f0da94aae`  
		Last Modified: Mon, 16 Mar 2026 23:44:13 GMT  
		Size: 94.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2f0b086128c318c28efb4541b0c5264857fb53e45dd2a7cfc468fdf981146fe`  
		Last Modified: Mon, 16 Mar 2026 23:44:14 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:latest` - unknown; unknown

```console
$ docker pull spiped@sha256:ceb5259222252c09f46d1586c4beb858ae638bfa5623656db13b549d96d21d09
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3633605 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38f77179e2c665d2a86e12bc17bfedc7f450031d205ba7c907005662463dd141`

```dockerfile
```

-	Layers:
	-	`sha256:a6c5d5579933f8a016f12bcfd02838e397274cce0d8c07d3b637a90946cef6b9`  
		Last Modified: Mon, 16 Mar 2026 23:44:13 GMT  
		Size: 3.6 MB (3618623 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:39e9ea0d638105f70bced5f876f7ce8f9adcd4138140b8d5d517b41dd0e8974b`  
		Last Modified: Mon, 16 Mar 2026 23:44:13 GMT  
		Size: 15.0 KB (14982 bytes)  
		MIME: application/vnd.in-toto+json
