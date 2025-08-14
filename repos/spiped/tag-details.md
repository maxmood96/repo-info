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
$ docker pull spiped@sha256:393010ed037fbb2527e124feb16b874a82ef10ffbbc5b43c9ffc6f3f9bf449b4
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
$ docker pull spiped@sha256:bf92abd8857927a58bf60b37b751b45e7849904d0c3eb39428aa9ded13973b45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.8 MB (36823886 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:131dfb2d7b78cb541b4f99eb9752b00f874f76280458f7f2ed039e38a9886acc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Sun, 10 Aug 2025 19:01:23 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1754870400'
# Sun, 10 Aug 2025 19:01:23 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Sun, 10 Aug 2025 19:01:23 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 10 Aug 2025 19:01:23 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Sun, 10 Aug 2025 19:01:23 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Sun, 10 Aug 2025 19:01:23 GMT
VOLUME [/spiped]
# Sun, 10 Aug 2025 19:01:23 GMT
WORKDIR /spiped
# Sun, 10 Aug 2025 19:01:23 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 10 Aug 2025 19:01:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 10 Aug 2025 19:01:23 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:396b1da7636e2dcd10565cb4f2f952cbb4a8a38b58d3b86a2cacb172fb70117c`  
		Last Modified: Tue, 12 Aug 2025 20:45:08 GMT  
		Size: 29.8 MB (29773285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1960f8d044ed2918a9b63f9b23e244fc01996b6272a914c37ccd6d6dfcc68e4e`  
		Last Modified: Tue, 12 Aug 2025 22:33:32 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1429568f03b0485d02eb3e469fe20cdda6eb6e31f703b79f50834c7990b35868`  
		Last Modified: Tue, 12 Aug 2025 22:33:32 GMT  
		Size: 824.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f288333198193fd5d29806df7832431ab2cf3ad06e46a49c6dffea5d74eeeb7`  
		Last Modified: Tue, 12 Aug 2025 22:33:34 GMT  
		Size: 7.0 MB (7048236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f6a4df49d11a34ceed3269d89d6506916e2574f79c63ac88c6e45ce2067bb65`  
		Last Modified: Tue, 12 Aug 2025 22:33:32 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e299a1e4998ed061307241b9eb0eaf6d3f70b3dfa7c6b13aefce13c34f3e486a`  
		Last Modified: Tue, 12 Aug 2025 22:33:32 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1` - unknown; unknown

```console
$ docker pull spiped@sha256:06b0151f64cf465a20c4b3cf24d52eb8346bdf93c27fd53c814bb089ec4cb05a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3640248 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3aa7836e633ede2d640e4ee8a7f90afb38f97ad41e553c5088dc576ec98a1380`

```dockerfile
```

-	Layers:
	-	`sha256:049c8275986690c07daaa8af602e6e2eccaad28d023f774058df9cfbefbbaffe`  
		Last Modified: Wed, 13 Aug 2025 01:04:22 GMT  
		Size: 3.6 MB (3625230 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8ac5644f2c0e54bd96ba3c75290b8842a1d59415c4f6007a1540ee957de0ba98`  
		Last Modified: Wed, 13 Aug 2025 01:04:23 GMT  
		Size: 15.0 KB (15018 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1` - linux; arm variant v5

```console
$ docker pull spiped@sha256:3a8a3157e13515af48661b3359c74ad04e1a30456f7c560ae8f68e87a20ffb9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.9 MB (32910178 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dcbb748125f0b8dcd0fb6493ed4d870453d8c8efa012f4e2222c7dc2619a103a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 02 Apr 2025 21:12:22 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1753056000'
# Wed, 02 Apr 2025 21:12:22 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Wed, 02 Apr 2025 21:12:22 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
VOLUME [/spiped]
# Wed, 02 Apr 2025 21:12:22 GMT
WORKDIR /spiped
# Wed, 02 Apr 2025 21:12:22 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Apr 2025 21:12:22 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:70a0ce20524d4016d59550a3733a4080dc793deac81fcf6a038a61c9427611d7`  
		Last Modified: Tue, 22 Jul 2025 00:20:40 GMT  
		Size: 25.8 MB (25762716 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49046a4dd717e46f1d47e8b442ea16a32ae5c918851152c07d29a1ec56228f2a`  
		Last Modified: Tue, 22 Jul 2025 05:31:57 GMT  
		Size: 1.1 KB (1104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b15015636ae2d1e604b210604ec62efba4b52378febbaf8d104fdc747967525`  
		Last Modified: Tue, 22 Jul 2025 05:31:57 GMT  
		Size: 2.0 MB (1998288 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3147db3fa731dc64539822c647b65ed645104c05a5b5829ecb7b0ef27e85143`  
		Last Modified: Tue, 22 Jul 2025 05:31:57 GMT  
		Size: 5.1 MB (5147637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a27fdd8a658afb898909a24260e3428adae409d14c86ccd2e98c5e9c0ab7edc`  
		Last Modified: Tue, 22 Jul 2025 05:31:56 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d5c5f7070397c2858394d855108e31978aa74ffa73cbdd12b7200db8de2d441`  
		Last Modified: Tue, 22 Jul 2025 05:31:57 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1` - unknown; unknown

```console
$ docker pull spiped@sha256:772cf6016b094f52670a3487eacbd9f06e92145eb1e55a55b09fea0bf6aa9fdd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3617772 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c7e48cc724fee727a6693c57c4043d98e8bfac2f9242b3effde1720a1427492`

```dockerfile
```

-	Layers:
	-	`sha256:b510654d2a8c1b8ad052747c8ddb7e16c41356134db9be35752c35115580cfb1`  
		Last Modified: Tue, 22 Jul 2025 07:04:32 GMT  
		Size: 3.6 MB (3602631 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:471889e07393b6e3410d1d09003810c74afd93089e902abc26d07e1e0f8a2fce`  
		Last Modified: Tue, 22 Jul 2025 07:04:32 GMT  
		Size: 15.1 KB (15141 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1` - linux; arm variant v7

```console
$ docker pull spiped@sha256:df4a67cfc69545276ba2fa47893371e5bae16c16c7966f816afa7d6ff25c8030
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.7 MB (30685629 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3961f78e049e031a2d9c52600e014e09161ac256b60bb21f7765b25227de7da0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 02 Apr 2025 21:12:22 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1753056000'
# Wed, 02 Apr 2025 21:12:22 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Wed, 02 Apr 2025 21:12:22 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
VOLUME [/spiped]
# Wed, 02 Apr 2025 21:12:22 GMT
WORKDIR /spiped
# Wed, 02 Apr 2025 21:12:22 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Apr 2025 21:12:22 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:3d83c6df5858d91327bc312b738290e713ab4b6d4e0586c217399744d7596864`  
		Last Modified: Tue, 22 Jul 2025 00:20:36 GMT  
		Size: 23.9 MB (23938916 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe33cfed210711d85c4fb2b78824894f0d21979f013b4c59e595b535eda34fb6`  
		Last Modified: Tue, 22 Jul 2025 08:09:39 GMT  
		Size: 1.1 KB (1104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a5b5df2c8141fd6c1a420c98bbdfedda39b519cde600d577420f7822d64674e`  
		Last Modified: Tue, 22 Jul 2025 08:09:39 GMT  
		Size: 1.9 MB (1856406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8116bf27bbfb2abe4dad1a945819daa5184885a04be75e148bd91f3bab537924`  
		Last Modified: Tue, 22 Jul 2025 08:09:40 GMT  
		Size: 4.9 MB (4888769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae19946bd511763f4472e27df6f9f101f98a95a0b8e6b788beeb92d06694c152`  
		Last Modified: Tue, 22 Jul 2025 08:09:41 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcc6b3556f96d25cb1b9f9cfdc269be4883d98a05b63099eaa06187780ea70fc`  
		Last Modified: Tue, 22 Jul 2025 08:09:43 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1` - unknown; unknown

```console
$ docker pull spiped@sha256:0128ce934f586afb91aec29487355efccdefd76ccf4cce8344526da2947139c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3616955 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8dee0971e665b140b05d6053112c4d56d1111a6c474b6746e0bc68c030ecb23c`

```dockerfile
```

-	Layers:
	-	`sha256:2776f040304a973414de30d806031dbe4bb548df652c417d069b20a435fc3dd1`  
		Last Modified: Tue, 22 Jul 2025 10:07:08 GMT  
		Size: 3.6 MB (3601814 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:40b6ffb7b5108a7c93066348dec6008dc745f5e3d55e87ed73c96c7f2fb9cb03`  
		Last Modified: Tue, 22 Jul 2025 10:07:09 GMT  
		Size: 15.1 KB (15141 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1` - linux; arm64 variant v8

```console
$ docker pull spiped@sha256:e4096ff20583a5034e9280aeddf5f1a78923d9682609c199920f22185356b4fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.4 MB (36369792 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aff0f6bbb2c3ea404a50f705696846a93449e7bd0e783ad59d028a426200d382`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Sun, 10 Aug 2025 19:01:23 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1754870400'
# Sun, 10 Aug 2025 19:01:23 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Sun, 10 Aug 2025 19:01:23 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 10 Aug 2025 19:01:23 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Sun, 10 Aug 2025 19:01:23 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Sun, 10 Aug 2025 19:01:23 GMT
VOLUME [/spiped]
# Sun, 10 Aug 2025 19:01:23 GMT
WORKDIR /spiped
# Sun, 10 Aug 2025 19:01:23 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 10 Aug 2025 19:01:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 10 Aug 2025 19:01:23 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:9a6263cdeaa5d408640880103ee36920ef814974ca8e2674412ad6460e8968c9`  
		Last Modified: Tue, 12 Aug 2025 22:12:42 GMT  
		Size: 30.1 MB (30136044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af40190d6d264f1be66cb08049b70540eba02ba7fd655fae097cbda289746d53`  
		Last Modified: Wed, 13 Aug 2025 06:22:09 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:feabee456a6c96014e115867bd4e88b799f44b94e6c0b8d1b5000ec496955205`  
		Last Modified: Wed, 13 Aug 2025 06:22:09 GMT  
		Size: 827.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:422d0a380f226f779c85ec48dd7499a08ac0a2aa93252b6aa435fffccde8d8d2`  
		Last Modified: Wed, 13 Aug 2025 06:22:09 GMT  
		Size: 6.2 MB (6231378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a173632e46f201ec2b33805fcaf1d0c7df806b23f5e46a8c69672b6b4b565a4`  
		Last Modified: Wed, 13 Aug 2025 06:22:09 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bc1586a4e693693f7a15724dc111621e8887e469dd123083d647ceb15706ddf`  
		Last Modified: Wed, 13 Aug 2025 06:22:09 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1` - unknown; unknown

```console
$ docker pull spiped@sha256:034a8753ac823cfb19cac1a8b03a8fa42e7980f7937cba5bf7cfc01f4830a477
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3635418 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7286e08e8b96923d063eaa64527cb3cd08ca82cb07acf935f38efb0878583ba6`

```dockerfile
```

-	Layers:
	-	`sha256:bd5609020456c14f8bd5616333f26562e22aaf5d64128b39a58aa6d6c701dc9d`  
		Last Modified: Wed, 13 Aug 2025 10:06:23 GMT  
		Size: 3.6 MB (3620266 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d777d280a0314438cc074454754ca46996e21b39209485922e38a27cd2f5fe8d`  
		Last Modified: Wed, 13 Aug 2025 10:06:24 GMT  
		Size: 15.2 KB (15152 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1` - linux; 386

```console
$ docker pull spiped@sha256:9fcfe0c5b84d9fea6d266d29f18e4dbf8a226baeb085ca7ece3a8de5511e9c60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.7 MB (37733468 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a583f402afb8c7247d391e1083e23f97bbdcf159a97c7d203583d02d6b43500`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Sun, 10 Aug 2025 19:01:23 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1754870400'
# Sun, 10 Aug 2025 19:01:23 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Sun, 10 Aug 2025 19:01:23 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 10 Aug 2025 19:01:23 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Sun, 10 Aug 2025 19:01:23 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Sun, 10 Aug 2025 19:01:23 GMT
VOLUME [/spiped]
# Sun, 10 Aug 2025 19:01:23 GMT
WORKDIR /spiped
# Sun, 10 Aug 2025 19:01:23 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 10 Aug 2025 19:01:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 10 Aug 2025 19:01:23 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:346d0c953bdbc38917a27a6f30726e5b46419d98ecaf4d2d8f201bc3b7025e57`  
		Last Modified: Tue, 12 Aug 2025 20:45:00 GMT  
		Size: 31.3 MB (31289378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab0a9017881d45c9f4e65c372f685c6423638a8e38d92d57f8c3c99691cd7d31`  
		Last Modified: Tue, 12 Aug 2025 22:33:32 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:153819a4650c40b66474fb6dcc7d882e133f0147b067b5fc48010ae2bc8f46ba`  
		Last Modified: Tue, 12 Aug 2025 22:33:32 GMT  
		Size: 828.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a835563de046e9d403e7281f08ebf605249457ca98db2da529bd31f3fb191c68`  
		Last Modified: Tue, 12 Aug 2025 22:33:36 GMT  
		Size: 6.4 MB (6441722 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f06a8985faf5a44d315fbfa0d9975612e26c279004f7da7f8b48a116e66604c3`  
		Last Modified: Tue, 12 Aug 2025 22:33:32 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5ed637e18c93a4756562fbc235fbdf71a83fe6c2e508f6506bb9298bbf4d874`  
		Last Modified: Tue, 12 Aug 2025 22:33:32 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1` - unknown; unknown

```console
$ docker pull spiped@sha256:a22b73545c72bcc558012c681a7f3a323f62434624d93aed8a33f101a37fbf70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3634341 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9191c005b0e377ba838af7947a2eb39c66669632dcfdc9dab86f5a558b4a189`

```dockerfile
```

-	Layers:
	-	`sha256:b719e1d1247f7a8d2b2789312ebfb048bb173eedc1d0d8d7bd03213393393f7e`  
		Last Modified: Wed, 13 Aug 2025 01:04:39 GMT  
		Size: 3.6 MB (3619359 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dbc37a5a50f0a3198bced5718863ebd1123276e390992fd98e77602896183042`  
		Last Modified: Wed, 13 Aug 2025 01:04:40 GMT  
		Size: 15.0 KB (14982 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1` - linux; ppc64le

```console
$ docker pull spiped@sha256:c10b4ed278517ae49edfa7127c75c47dd1266e14633cd7f260e5c66298f1886b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.4 MB (40436468 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8248a22dee5275cedfd61db24cf28a136e1ec17f04c8aac3cad18755c6227de`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Sun, 10 Aug 2025 19:01:23 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1754870400'
# Sun, 10 Aug 2025 19:01:23 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Sun, 10 Aug 2025 19:01:23 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 10 Aug 2025 19:01:23 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Sun, 10 Aug 2025 19:01:23 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Sun, 10 Aug 2025 19:01:23 GMT
VOLUME [/spiped]
# Sun, 10 Aug 2025 19:01:23 GMT
WORKDIR /spiped
# Sun, 10 Aug 2025 19:01:23 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 10 Aug 2025 19:01:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 10 Aug 2025 19:01:23 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:52a4daa8724e9e1632306e15fe478aa26ff0ebcb7ba924cb168e9b6738c239d5`  
		Last Modified: Wed, 13 Aug 2025 01:42:36 GMT  
		Size: 33.6 MB (33594213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b31b56e1b56780df0e15411a668eb62bef22507f7082c36cbaa48e27b80a3dd`  
		Last Modified: Wed, 13 Aug 2025 11:56:38 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f93773dbbb14e44d116aaac13df032fbde418d4886ee8818b206f44616ba18c`  
		Last Modified: Wed, 13 Aug 2025 11:56:38 GMT  
		Size: 828.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1cba8a6190732e98166036b793666dec0711e36288c95969052f741b9f4561e`  
		Last Modified: Wed, 13 Aug 2025 11:56:39 GMT  
		Size: 6.8 MB (6839886 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e7c0065407c754b3de23aec850cf5698c61bd9ecd0c15fc936bb712345929e3`  
		Last Modified: Wed, 13 Aug 2025 11:56:38 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8565dc40120eabde33b3bc8ce9bc1fe16f2eea8e28f0298720ed08f9b970ed0d`  
		Last Modified: Wed, 13 Aug 2025 11:56:39 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1` - unknown; unknown

```console
$ docker pull spiped@sha256:43109fb7e5111756d35286a2c676e3530935deee3215367350f73c7717b0e368
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3636031 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45f14ba2c606d377446bf0e308bd47d6a3d8361c6adf29643758176bbed63bdf`

```dockerfile
```

-	Layers:
	-	`sha256:93dd80ad64b6ab11f964491d9b2edeb14431ec6735a30bc18db3663130f8056f`  
		Last Modified: Wed, 13 Aug 2025 13:04:36 GMT  
		Size: 3.6 MB (3620967 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:efa85ab4fe3aac389b61e3250282df7fdb0c361d597e0dd102c965020f2cd7f0`  
		Last Modified: Wed, 13 Aug 2025 13:04:37 GMT  
		Size: 15.1 KB (15064 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1` - linux; riscv64

```console
$ docker pull spiped@sha256:b8736517f7bb59c511ea4f9ad8a7b005ade95874aac45851c1047a628ec0e53d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.6 MB (37631700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:441b458a8e084c25a772f75f188b539784eb4e7a9c4aceb0f7d4ab836ef01505`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Sun, 10 Aug 2025 19:01:23 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1754870400'
# Sun, 10 Aug 2025 19:01:23 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Sun, 10 Aug 2025 19:01:23 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 10 Aug 2025 19:01:23 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Sun, 10 Aug 2025 19:01:23 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Sun, 10 Aug 2025 19:01:23 GMT
VOLUME [/spiped]
# Sun, 10 Aug 2025 19:01:23 GMT
WORKDIR /spiped
# Sun, 10 Aug 2025 19:01:23 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 10 Aug 2025 19:01:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 10 Aug 2025 19:01:23 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:a37386b9234ad75f65b5aa72f3d919ff0eb3bb18978566fa959d6e357480594c`  
		Last Modified: Wed, 13 Aug 2025 04:01:43 GMT  
		Size: 28.3 MB (28271623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:127ab5460053be42a858239f06c9bdf9bb20e426f59634680dd0952a062febe4`  
		Last Modified: Thu, 14 Aug 2025 14:39:42 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09fbdf3ef389fcfcfcde8edb7a990d48a50bb6562d381638a40a276632d2f2cb`  
		Last Modified: Thu, 14 Aug 2025 14:39:42 GMT  
		Size: 821.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e240e5ce18b11abe9700a80ae6196ee291094f1348bd44a0b4075b3d94f921d`  
		Last Modified: Thu, 14 Aug 2025 14:39:43 GMT  
		Size: 9.4 MB (9357715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b48ce987df3197aa7fa59932f4358de18054e75c420dd112aee00373e12d27e`  
		Last Modified: Thu, 14 Aug 2025 14:39:42 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2668076a38889d3caa1e8ef93527b7bcb09e1c8efde0333842323d9d6886d52`  
		Last Modified: Thu, 14 Aug 2025 14:39:43 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1` - unknown; unknown

```console
$ docker pull spiped@sha256:35913cc3f9fbe2375dbded2db7c773c530af42658aedbb3c8c1091268ab132c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3627439 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28abdef5a89cde265387c1c474ff08401948f48a3a2ad1431ed385b67b9e7e21`

```dockerfile
```

-	Layers:
	-	`sha256:a99c608ee95dedeefc4afd8c5d5002110953819bdd4bfc69f30503d9f7b29d9b`  
		Last Modified: Thu, 14 Aug 2025 16:04:41 GMT  
		Size: 3.6 MB (3612373 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:62f5c0922fff6e0c5c082f975db2470f90964d11fe3ed095088a38dc476c6df5`  
		Last Modified: Thu, 14 Aug 2025 16:04:42 GMT  
		Size: 15.1 KB (15066 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1` - linux; s390x

```console
$ docker pull spiped@sha256:77f28ec69d006b6ee6c4039b94cd23ed250849a792bcd153225cf7caaf0622b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.0 MB (35956075 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58c75aba82b1c983aca3ad0a5a3e6e29eba90da29cbb7e000e07c4ddbbf457ef`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Sun, 10 Aug 2025 19:01:23 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1754870400'
# Sun, 10 Aug 2025 19:01:23 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Sun, 10 Aug 2025 19:01:23 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 10 Aug 2025 19:01:23 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Sun, 10 Aug 2025 19:01:23 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Sun, 10 Aug 2025 19:01:23 GMT
VOLUME [/spiped]
# Sun, 10 Aug 2025 19:01:23 GMT
WORKDIR /spiped
# Sun, 10 Aug 2025 19:01:23 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 10 Aug 2025 19:01:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 10 Aug 2025 19:01:23 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:bfe4d60a27c9392ab729f16b50a763cda36622d744066c3cf029a072133f2907`  
		Last Modified: Tue, 12 Aug 2025 20:59:52 GMT  
		Size: 29.8 MB (29833057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9c626e6797dd4ed7e04641af5c80facb561257332e487c827a1ef8e5abfd9da`  
		Last Modified: Wed, 13 Aug 2025 03:13:05 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9900aed129749b40b135a4bf95bf318aaf8af8baa7324644aa65625a3d451004`  
		Last Modified: Wed, 13 Aug 2025 03:13:06 GMT  
		Size: 830.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f181815f0f2b1a7c15bd8cac9719565f616355c0b414c8b75cebeb1e47fc8407`  
		Last Modified: Wed, 13 Aug 2025 03:13:07 GMT  
		Size: 6.1 MB (6120648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba136bfaf44029a3c3e626051e20473fa8506b40643868e01503bb9f8fa7efa7`  
		Last Modified: Wed, 13 Aug 2025 03:13:07 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d75d2357fb8504e89d6cd5f62c3ba8bb87da5071bdb36e6ea261cfedca4f775`  
		Last Modified: Wed, 13 Aug 2025 03:13:07 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1` - unknown; unknown

```console
$ docker pull spiped@sha256:857963cc998457b693ce1f587d4d49b1e5025fe31ab7b0f7716489ee3e88d128
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3632611 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:749730c63bce3f602d13204e410b4980e4a58c8837357f148bcf3b1b94536afb`

```dockerfile
```

-	Layers:
	-	`sha256:0053cd2920bef5559841359b3be4f662851ac0b991797140849707d6b1fbf038`  
		Last Modified: Wed, 13 Aug 2025 07:06:49 GMT  
		Size: 3.6 MB (3617593 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:61c3f86e4dbefc122f0101f397d596f2aaef357ec79760d163a5e5862bef6588`  
		Last Modified: Wed, 13 Aug 2025 07:06:49 GMT  
		Size: 15.0 KB (15018 bytes)  
		MIME: application/vnd.in-toto+json

## `spiped:1-alpine`

```console
$ docker pull spiped@sha256:93cdaab6e3b6d95ed76ddad7bf7f5c587c528e49ffabc2b79f6bd2aea6ab2630
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
$ docker pull spiped@sha256:fe36b545330b74e242df186f67f1842fc3f32a99ef52966ca731dc6982049707
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3916658 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36831aa20b12e50c7b388081fa2b93846f37a41dba1dad419cb49e1293706737`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
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
	-	`sha256:9824c27679d3b27c5e1cb00a73adb6f4f8d556994111c12db3c5d61a0c843df8`  
		Last Modified: Tue, 15 Jul 2025 19:00:01 GMT  
		Size: 3.8 MB (3799689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54f05db9f6c272f7847748f88394ce3bec41041589aaffb85ec57022932d41b6`  
		Last Modified: Mon, 11 Aug 2025 17:12:32 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3273c8db96783d1302ea2a8fb3345410d10a9076895cba46e68c6f063b28c3b`  
		Last Modified: Mon, 11 Aug 2025 17:02:16 GMT  
		Size: 7.9 KB (7946 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6034475a687587b7ef48917e52c9c773ca57a24867d18d0b4eba7762442608d`  
		Last Modified: Mon, 11 Aug 2025 17:02:19 GMT  
		Size: 107.6 KB (107643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28b778daf20a67a656800301303d05635c6c1b4b5aaf39563d66bcddafa96f82`  
		Last Modified: Mon, 11 Aug 2025 17:02:23 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2034aa0716ef0823cb7e0732cc466b480c6e7211047b7e791408e1b2e446969`  
		Last Modified: Mon, 11 Aug 2025 17:02:30 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:f6f21269d5900649987064943467fc128bbc3c34046bbe3f34413ca7c47a199c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.5 KB (96494 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dadc5ec1136521522c7efb5c32bb14f9ad6e983626c50c8bb0ca2df8a8baa064`

```dockerfile
```

-	Layers:
	-	`sha256:627d0194d2b11eccbaee3f5ef6edc22013a7b6093f562006c2fe85e88d07dc9e`  
		Last Modified: Mon, 11 Aug 2025 19:04:42 GMT  
		Size: 82.2 KB (82192 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7f278acc8a79ab1e0936e69a45aa893cb3e9050f2d6e52d3aa94b57021047e7e`  
		Last Modified: Mon, 11 Aug 2025 19:04:43 GMT  
		Size: 14.3 KB (14302 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1-alpine` - linux; arm variant v6

```console
$ docker pull spiped@sha256:67bf8a15d391a12bf880bede827f884530e7cb5b7197db6b4f6c256bed6f8205
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3599402 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c942d42ae3b8e3004d46bf3408c8fe7f7893f60f5c91c514931f39789491c9a3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-armhf.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
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
	-	`sha256:06bab5e847c5674d6ec26b342cc11d7a051a6a231e5db8a955d57bc9f4ab5595`  
		Last Modified: Tue, 15 Jul 2025 18:59:34 GMT  
		Size: 3.5 MB (3500910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10c249d32301274a396c4398f0f9ad3e25d11b9387b71935548f7746004176c0`  
		Last Modified: Mon, 11 Aug 2025 17:07:08 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21acf12f5fa85d243eec713f52367aa2fc9fd58ece745d522619070ee2d91cfd`  
		Last Modified: Mon, 11 Aug 2025 17:07:12 GMT  
		Size: 7.9 KB (7949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:745a95091f37f0e3319bde964913fe0326b1767141fa6ccc002a3b8960025757`  
		Last Modified: Mon, 11 Aug 2025 17:07:15 GMT  
		Size: 89.2 KB (89159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c107fdd944f86a67e108331b416f8aa5deaef19c68a63ed23a8ba9ea0d3401d4`  
		Last Modified: Mon, 11 Aug 2025 17:07:17 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f42a92f540a8b148fc88f8e31cb9818a5f6618f8a1577e639ec0e24e38f9f7e`  
		Last Modified: Mon, 11 Aug 2025 17:07:20 GMT  
		Size: 336.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:f93c76c9652d3a49aa974d58b6ae433e7cb36a7bfa83c6ac0d6cc254a7ba00c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.2 KB (14186 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9211c16e5ea9fc5d8cd82834f8cc184ea937fb23dc63d93b0f565174ccaf11e0`

```dockerfile
```

-	Layers:
	-	`sha256:bc75439704d889af0e27619c5682d57a42ab81be9ff4624f8a521f4377910696`  
		Last Modified: Mon, 11 Aug 2025 19:04:47 GMT  
		Size: 14.2 KB (14186 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1-alpine` - linux; arm variant v7

```console
$ docker pull spiped@sha256:9a4d893ec119af9bc7c0ac4cf7576f963e58abf3883a80df5a16e49b111c25aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3310043 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6ff0c9b1b65653155189d3026538aef9ad32adc4e50d92d8bd56011b77575eb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-armv7.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
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
	-	`sha256:5ee064f8764b09a64829b58705219a88e0b13243f7f403d66ac0c639640426a5`  
		Last Modified: Tue, 15 Jul 2025 19:04:18 GMT  
		Size: 3.2 MB (3219038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:379d666e2282d1ef67d78e68d7d1456eb01f968d2fb8812ac738eba6158a80e9`  
		Last Modified: Mon, 11 Aug 2025 17:12:34 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59c40f7a10d1200a7ded6eb02e6bd8fd18467fcf3ff34f0cf808a4cc55bed23e`  
		Last Modified: Mon, 11 Aug 2025 17:12:39 GMT  
		Size: 7.9 KB (7943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2b5dc976627c424732ee16c786a666f6c1bfc2753fb4eb45ba52b5363d0ddc5`  
		Last Modified: Mon, 11 Aug 2025 17:12:43 GMT  
		Size: 81.7 KB (81679 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:458721a616c9dc4cf600ca98211c375a8834644ed8ef7b186d3328ac28406eae`  
		Last Modified: Mon, 11 Aug 2025 17:12:48 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61e38052aca5003fd5a5a420dc69c7e09ad4a5c937a6fe99ce9562e631927208`  
		Last Modified: Mon, 11 Aug 2025 17:12:58 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:b59043aa1ff63fcd31688fcd9d6a738aa113abdf366d458b93611854679ca46d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.6 KB (96629 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8456c8deda36f896666ee554249c53f1f1c44c53625d46df0b57b3ec07a8f90f`

```dockerfile
```

-	Layers:
	-	`sha256:604964ef49a1e639a8695215e5270aef4e51c3880d27e449bed0300fb49b10e2`  
		Last Modified: Mon, 11 Aug 2025 19:04:50 GMT  
		Size: 82.2 KB (82228 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3b749cfa2bb22f9f9bb0749d7930ddf6645b6ec8b6ff5ce281761785e69fe917`  
		Last Modified: Mon, 11 Aug 2025 19:04:51 GMT  
		Size: 14.4 KB (14401 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1-alpine` - linux; arm64 variant v8

```console
$ docker pull spiped@sha256:0aba08b25b408090092ccc3a2bfff93dd73cd53f1732f086bd5929af3a835323
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4240704 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c275338929556163beeba8cdd1efd28825491f472e207d35476d3569d9ee0e97`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-aarch64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
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
	-	`sha256:6e174226ea690ced550e5641249a412cdbefd2d09871f3e64ab52137a54ba606`  
		Last Modified: Tue, 15 Jul 2025 18:59:50 GMT  
		Size: 4.1 MB (4130750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:401e496ab6a7fec1ab1bb8f0b8a996b06c9fb697746e47439f58ec78714d57cb`  
		Last Modified: Mon, 11 Aug 2025 17:09:42 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc10c01537e03fed07cdd599b8a98a0adcfa5c06d0ba71c752ddf65d7ef18bd7`  
		Last Modified: Mon, 11 Aug 2025 17:09:45 GMT  
		Size: 8.0 KB (7951 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adfbfacdb4fddd486ebc3cf352ee0538e6eadf8b3033b6e12abdaf15234459c1`  
		Last Modified: Mon, 11 Aug 2025 17:09:48 GMT  
		Size: 100.6 KB (100617 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a7767630476c70a6cf95063bb707ffee6b4b40278b06fcdb17fa3f7dca8427b`  
		Last Modified: Mon, 11 Aug 2025 17:09:50 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25762649a73c36acce0fd48360b8be503aee4c1602f1a59b759cb8a795ab8c6b`  
		Last Modified: Mon, 11 Aug 2025 17:09:53 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:5b477d36fe748f79631e7066c0574b5a9ca9e3e1c169c735e2a960cd0cea9d95
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.7 KB (96684 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6c2517fcfde44c5508a52e01d9e77e79db6fd3daad75c70853eb4b2b378a0ae`

```dockerfile
```

-	Layers:
	-	`sha256:1903a367ec2a9e9fbbee350246fe22b734d8bacdcfb9d34f695b231aa6f96ccd`  
		Last Modified: Mon, 11 Aug 2025 19:04:55 GMT  
		Size: 82.2 KB (82248 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6d54be9922b28101eb015c8900bf1221e9437578e72fce9654714c21b92c04d6`  
		Last Modified: Mon, 11 Aug 2025 19:04:56 GMT  
		Size: 14.4 KB (14436 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1-alpine` - linux; 386

```console
$ docker pull spiped@sha256:48537809d8133274a37ab69a836499fb8479383b5b69967228ce176ac6f1be60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3744445 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f9a0ea1f48b6cac9c7ce62d1260fd3fc9040cc58f686650da2fda4a116dfe2b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-x86.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
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
	-	`sha256:a55f2fb89da4caae0d783c0045a67446dee9bbd977fecb44db9e1231550fa888`  
		Last Modified: Tue, 15 Jul 2025 19:04:11 GMT  
		Size: 3.6 MB (3615006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3eba0b59a29857fdbd92df8627b53b15ba8b6ab4ec59021ee5712b80dfed882`  
		Last Modified: Mon, 11 Aug 2025 17:07:16 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:847779e3481b940532b586da8162b98cc75b9ca766b1f6e26d1622c3ed2d8ad1`  
		Last Modified: Mon, 11 Aug 2025 17:07:19 GMT  
		Size: 7.9 KB (7947 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84ead07d68c6f9280214b36ee65459f295af32fb5a83587a9d94ff34fbd8edf9`  
		Last Modified: Mon, 11 Aug 2025 17:07:22 GMT  
		Size: 120.1 KB (120108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbd0afa8d91fe587be8847df03da4b2cd7c73dbce722c78ea9606f83cbe408ae`  
		Last Modified: Mon, 11 Aug 2025 17:07:25 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18e699ee2bbb463e05c765e96679445315e788311982f0d542d6d6c513614f78`  
		Last Modified: Mon, 11 Aug 2025 17:07:31 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:15f0f80fe34bd14b6d564b6e741552ba495ee58c3268d7ba1e7611e8f104298a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.4 KB (96433 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9ee4d0ec8becf51535d0fdeb2611b861926d3c65de73b970a6f07164630a189`

```dockerfile
```

-	Layers:
	-	`sha256:fa8d8def96807232c5de9a2689e639f51f6662c2960d1e6a13e5390c1ef5f875`  
		Last Modified: Mon, 11 Aug 2025 19:05:00 GMT  
		Size: 82.2 KB (82167 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:017908264a6caffecdaecbe817722cb1919c11d362589f17292a9cbd2d55c204`  
		Last Modified: Mon, 11 Aug 2025 19:05:00 GMT  
		Size: 14.3 KB (14266 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1-alpine` - linux; ppc64le

```console
$ docker pull spiped@sha256:79845ce442587e8a1743c515186951ae7603efaf08e38a0a7f4ce40a4af20597
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3849108 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04c74704274ad902930376019928ebde446c1deca3459f089066274bd8f1565c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-ppc64le.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
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
	-	`sha256:b762f678859bfa5c3948b5f1b04959aa43c8aba88e2389e281413d303d62a7e3`  
		Last Modified: Tue, 15 Jul 2025 18:59:53 GMT  
		Size: 3.7 MB (3727111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2373f01bf878f477a6cf1b4d56c9227ff43127b4d845c3562616e2a46d22dbdd`  
		Last Modified: Mon, 11 Aug 2025 17:13:12 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:427ad9317b0d6357fac90f31d124d5e9b36ee534067da2df12710b89392c781e`  
		Last Modified: Mon, 11 Aug 2025 17:13:15 GMT  
		Size: 7.9 KB (7948 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2f4f5c32876f7abc20796b83c3897652d454e319406eae7a6a6ed5d74ea44e3`  
		Last Modified: Mon, 11 Aug 2025 17:13:20 GMT  
		Size: 112.7 KB (112665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a9033716c014ce457c2d72e5e75fc8fa8044e87014da9f03f2fb489b825aef8`  
		Last Modified: Mon, 11 Aug 2025 17:13:26 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb03f1a2076f357e9cab2045b9652c20950ca5d8f7421f046896219b8532d06b`  
		Last Modified: Mon, 11 Aug 2025 17:13:29 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:a6d8ce06cb0ab858ad3076a0f7a57f28f1e6ed5e17a4157b6b6a30ae37c3368a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.6 KB (94625 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b10d0bb2f5cfe8395a4519604c8ace1de04e74af97cc131cea9853a67b5fc2cc`

```dockerfile
```

-	Layers:
	-	`sha256:ff1c9c59d73d4c50497a06f04ad9a30428a99ad3de292bad5a2e9dd8d91d1160`  
		Last Modified: Mon, 11 Aug 2025 19:05:05 GMT  
		Size: 80.3 KB (80275 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e7e4e7f2cdbb149daeaca2e6e837f823a3641e8d4f0c3cf28a999579d17542cf`  
		Last Modified: Mon, 11 Aug 2025 19:05:05 GMT  
		Size: 14.3 KB (14350 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1-alpine` - linux; riscv64

```console
$ docker pull spiped@sha256:eb5294dab564ed0a45bac04aff4eb51d319f7c4fd6d0fe4eb457a283aceff474
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3620988 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83d8198608b9934495dc90c953cc87dfd83d7b1d0af22c216f3636508b77fd7b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-riscv64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
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
	-	`sha256:cbe7080b5783de104ad67ff4595bfa8ae70a597181a84621f51c5ccd084218da`  
		Last Modified: Tue, 15 Jul 2025 19:00:17 GMT  
		Size: 3.5 MB (3512801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:337ef438f7e589dc4f613c730fb4dd5a761abfd9e48d0d59495d3aff151e16ab`  
		Last Modified: Mon, 11 Aug 2025 17:12:32 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89b21db99ab142ddfd5ec4b8ef25065f37bc1aee36e94cad1db40698257cd6fc`  
		Last Modified: Mon, 11 Aug 2025 17:12:36 GMT  
		Size: 7.9 KB (7945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe3dc6909718e2eb82c7628f42d658b99dcdf7135cb7db460851920d41ad58c4`  
		Last Modified: Mon, 11 Aug 2025 17:12:40 GMT  
		Size: 98.9 KB (98856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:541a31d50d76446fd96c63516c67f098fad214976beea363002d79b73ba95d22`  
		Last Modified: Mon, 11 Aug 2025 17:12:44 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7db5851f3b8a32ba3d881649070f2380d838c65cb1f702ed418b43e640f03d7a`  
		Last Modified: Mon, 11 Aug 2025 17:12:47 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:c32a8fd37856a4dfea8b91e0c18b79f0f43571bcac39779ab262c4c4741714be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.6 KB (94618 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c1f688a2498b96358ae65a439e4a1eda2bc0b14f90b0ec530106a28eb2077c4`

```dockerfile
```

-	Layers:
	-	`sha256:a3eaafb5380cff781fc2bfb357665fc4513231c31e349b37e3e7cc95f16b052b`  
		Last Modified: Mon, 11 Aug 2025 19:05:10 GMT  
		Size: 80.3 KB (80271 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:331b28e1546911de84609c9d63a3f86e0abca6d7efd8c9fa3d618f196a1ec42d`  
		Last Modified: Mon, 11 Aug 2025 19:05:10 GMT  
		Size: 14.3 KB (14347 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1-alpine` - linux; s390x

```console
$ docker pull spiped@sha256:1c717961a5e8cc5e8fd75141c21f0a6de58a68c44608450fa683029bae71c085
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3751251 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b744d847c43ddb5879abe90a22b110885a2c0ffb39ae4f72a3753f4e839db1a2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-s390x.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
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
	-	`sha256:5d29754ce036967079405405a04a54a7d3f8ba85e0057b6bdda3d03aa59c8361`  
		Last Modified: Tue, 15 Jul 2025 19:00:06 GMT  
		Size: 3.6 MB (3644971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e1bd137b03fbd1349d3ad3112f1e21d62c9baae0012a389da756b7ca6f932c7`  
		Last Modified: Mon, 11 Aug 2025 17:07:14 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a06802588e4666537f404a0ce19ebfc4da3850fd2dbe3536a4fe24380b4bc222`  
		Last Modified: Mon, 11 Aug 2025 17:07:18 GMT  
		Size: 8.0 KB (7950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f406fcd8d03a4ee6c2fc9bee5495de93682706f0ac21a261973b02e5cda0c93`  
		Last Modified: Mon, 11 Aug 2025 17:07:23 GMT  
		Size: 96.9 KB (96945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c48cae2c2a395f0f13d3dba276c545fd622a02bc6b9325ac1f1573447c6e90f`  
		Last Modified: Mon, 11 Aug 2025 17:07:27 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46bfce62ca5613c78d3504649bafb02ff12a44fa234e3dfc1134ece19652d3d7`  
		Last Modified: Mon, 11 Aug 2025 17:07:30 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:654988790b7ed5b0441b8c38603d934b9706d4cccb2a3a9a96d8d3cc5f49c40a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.5 KB (94540 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a02880e0cbcf996ddd3d1c0bf389633fb423298a93ece41330d2f645d016566`

```dockerfile
```

-	Layers:
	-	`sha256:f77f4e4ec9383facda6fb5da7eeb5bf28f59fb80e6043ee4cb4eec3950e1422d`  
		Last Modified: Mon, 11 Aug 2025 19:05:14 GMT  
		Size: 80.2 KB (80241 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d27df7657b4c19b9a7071f58a7b58946289a2dc8ca2315c4bb0375dcfd961e1e`  
		Last Modified: Mon, 11 Aug 2025 19:05:15 GMT  
		Size: 14.3 KB (14299 bytes)  
		MIME: application/vnd.in-toto+json

## `spiped:1.6`

```console
$ docker pull spiped@sha256:393010ed037fbb2527e124feb16b874a82ef10ffbbc5b43c9ffc6f3f9bf449b4
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
$ docker pull spiped@sha256:bf92abd8857927a58bf60b37b751b45e7849904d0c3eb39428aa9ded13973b45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.8 MB (36823886 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:131dfb2d7b78cb541b4f99eb9752b00f874f76280458f7f2ed039e38a9886acc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Sun, 10 Aug 2025 19:01:23 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1754870400'
# Sun, 10 Aug 2025 19:01:23 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Sun, 10 Aug 2025 19:01:23 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 10 Aug 2025 19:01:23 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Sun, 10 Aug 2025 19:01:23 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Sun, 10 Aug 2025 19:01:23 GMT
VOLUME [/spiped]
# Sun, 10 Aug 2025 19:01:23 GMT
WORKDIR /spiped
# Sun, 10 Aug 2025 19:01:23 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 10 Aug 2025 19:01:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 10 Aug 2025 19:01:23 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:396b1da7636e2dcd10565cb4f2f952cbb4a8a38b58d3b86a2cacb172fb70117c`  
		Last Modified: Tue, 12 Aug 2025 20:45:08 GMT  
		Size: 29.8 MB (29773285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1960f8d044ed2918a9b63f9b23e244fc01996b6272a914c37ccd6d6dfcc68e4e`  
		Last Modified: Tue, 12 Aug 2025 22:33:32 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1429568f03b0485d02eb3e469fe20cdda6eb6e31f703b79f50834c7990b35868`  
		Last Modified: Tue, 12 Aug 2025 22:33:32 GMT  
		Size: 824.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f288333198193fd5d29806df7832431ab2cf3ad06e46a49c6dffea5d74eeeb7`  
		Last Modified: Tue, 12 Aug 2025 22:33:34 GMT  
		Size: 7.0 MB (7048236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f6a4df49d11a34ceed3269d89d6506916e2574f79c63ac88c6e45ce2067bb65`  
		Last Modified: Tue, 12 Aug 2025 22:33:32 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e299a1e4998ed061307241b9eb0eaf6d3f70b3dfa7c6b13aefce13c34f3e486a`  
		Last Modified: Tue, 12 Aug 2025 22:33:32 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6` - unknown; unknown

```console
$ docker pull spiped@sha256:06b0151f64cf465a20c4b3cf24d52eb8346bdf93c27fd53c814bb089ec4cb05a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3640248 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3aa7836e633ede2d640e4ee8a7f90afb38f97ad41e553c5088dc576ec98a1380`

```dockerfile
```

-	Layers:
	-	`sha256:049c8275986690c07daaa8af602e6e2eccaad28d023f774058df9cfbefbbaffe`  
		Last Modified: Wed, 13 Aug 2025 01:04:22 GMT  
		Size: 3.6 MB (3625230 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8ac5644f2c0e54bd96ba3c75290b8842a1d59415c4f6007a1540ee957de0ba98`  
		Last Modified: Wed, 13 Aug 2025 01:04:23 GMT  
		Size: 15.0 KB (15018 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6` - linux; arm variant v5

```console
$ docker pull spiped@sha256:3a8a3157e13515af48661b3359c74ad04e1a30456f7c560ae8f68e87a20ffb9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.9 MB (32910178 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dcbb748125f0b8dcd0fb6493ed4d870453d8c8efa012f4e2222c7dc2619a103a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 02 Apr 2025 21:12:22 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1753056000'
# Wed, 02 Apr 2025 21:12:22 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Wed, 02 Apr 2025 21:12:22 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
VOLUME [/spiped]
# Wed, 02 Apr 2025 21:12:22 GMT
WORKDIR /spiped
# Wed, 02 Apr 2025 21:12:22 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Apr 2025 21:12:22 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:70a0ce20524d4016d59550a3733a4080dc793deac81fcf6a038a61c9427611d7`  
		Last Modified: Tue, 22 Jul 2025 00:20:40 GMT  
		Size: 25.8 MB (25762716 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49046a4dd717e46f1d47e8b442ea16a32ae5c918851152c07d29a1ec56228f2a`  
		Last Modified: Tue, 22 Jul 2025 05:31:57 GMT  
		Size: 1.1 KB (1104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b15015636ae2d1e604b210604ec62efba4b52378febbaf8d104fdc747967525`  
		Last Modified: Tue, 22 Jul 2025 05:31:57 GMT  
		Size: 2.0 MB (1998288 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3147db3fa731dc64539822c647b65ed645104c05a5b5829ecb7b0ef27e85143`  
		Last Modified: Tue, 22 Jul 2025 05:31:57 GMT  
		Size: 5.1 MB (5147637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a27fdd8a658afb898909a24260e3428adae409d14c86ccd2e98c5e9c0ab7edc`  
		Last Modified: Tue, 22 Jul 2025 05:31:56 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d5c5f7070397c2858394d855108e31978aa74ffa73cbdd12b7200db8de2d441`  
		Last Modified: Tue, 22 Jul 2025 05:31:57 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6` - unknown; unknown

```console
$ docker pull spiped@sha256:772cf6016b094f52670a3487eacbd9f06e92145eb1e55a55b09fea0bf6aa9fdd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3617772 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c7e48cc724fee727a6693c57c4043d98e8bfac2f9242b3effde1720a1427492`

```dockerfile
```

-	Layers:
	-	`sha256:b510654d2a8c1b8ad052747c8ddb7e16c41356134db9be35752c35115580cfb1`  
		Last Modified: Tue, 22 Jul 2025 07:04:32 GMT  
		Size: 3.6 MB (3602631 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:471889e07393b6e3410d1d09003810c74afd93089e902abc26d07e1e0f8a2fce`  
		Last Modified: Tue, 22 Jul 2025 07:04:32 GMT  
		Size: 15.1 KB (15141 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6` - linux; arm variant v7

```console
$ docker pull spiped@sha256:df4a67cfc69545276ba2fa47893371e5bae16c16c7966f816afa7d6ff25c8030
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.7 MB (30685629 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3961f78e049e031a2d9c52600e014e09161ac256b60bb21f7765b25227de7da0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 02 Apr 2025 21:12:22 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1753056000'
# Wed, 02 Apr 2025 21:12:22 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Wed, 02 Apr 2025 21:12:22 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
VOLUME [/spiped]
# Wed, 02 Apr 2025 21:12:22 GMT
WORKDIR /spiped
# Wed, 02 Apr 2025 21:12:22 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Apr 2025 21:12:22 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:3d83c6df5858d91327bc312b738290e713ab4b6d4e0586c217399744d7596864`  
		Last Modified: Tue, 22 Jul 2025 00:20:36 GMT  
		Size: 23.9 MB (23938916 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe33cfed210711d85c4fb2b78824894f0d21979f013b4c59e595b535eda34fb6`  
		Last Modified: Tue, 22 Jul 2025 08:09:39 GMT  
		Size: 1.1 KB (1104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a5b5df2c8141fd6c1a420c98bbdfedda39b519cde600d577420f7822d64674e`  
		Last Modified: Tue, 22 Jul 2025 08:09:39 GMT  
		Size: 1.9 MB (1856406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8116bf27bbfb2abe4dad1a945819daa5184885a04be75e148bd91f3bab537924`  
		Last Modified: Tue, 22 Jul 2025 08:09:40 GMT  
		Size: 4.9 MB (4888769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae19946bd511763f4472e27df6f9f101f98a95a0b8e6b788beeb92d06694c152`  
		Last Modified: Tue, 22 Jul 2025 08:09:41 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcc6b3556f96d25cb1b9f9cfdc269be4883d98a05b63099eaa06187780ea70fc`  
		Last Modified: Tue, 22 Jul 2025 08:09:43 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6` - unknown; unknown

```console
$ docker pull spiped@sha256:0128ce934f586afb91aec29487355efccdefd76ccf4cce8344526da2947139c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3616955 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8dee0971e665b140b05d6053112c4d56d1111a6c474b6746e0bc68c030ecb23c`

```dockerfile
```

-	Layers:
	-	`sha256:2776f040304a973414de30d806031dbe4bb548df652c417d069b20a435fc3dd1`  
		Last Modified: Tue, 22 Jul 2025 10:07:08 GMT  
		Size: 3.6 MB (3601814 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:40b6ffb7b5108a7c93066348dec6008dc745f5e3d55e87ed73c96c7f2fb9cb03`  
		Last Modified: Tue, 22 Jul 2025 10:07:09 GMT  
		Size: 15.1 KB (15141 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6` - linux; arm64 variant v8

```console
$ docker pull spiped@sha256:e4096ff20583a5034e9280aeddf5f1a78923d9682609c199920f22185356b4fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.4 MB (36369792 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aff0f6bbb2c3ea404a50f705696846a93449e7bd0e783ad59d028a426200d382`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Sun, 10 Aug 2025 19:01:23 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1754870400'
# Sun, 10 Aug 2025 19:01:23 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Sun, 10 Aug 2025 19:01:23 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 10 Aug 2025 19:01:23 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Sun, 10 Aug 2025 19:01:23 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Sun, 10 Aug 2025 19:01:23 GMT
VOLUME [/spiped]
# Sun, 10 Aug 2025 19:01:23 GMT
WORKDIR /spiped
# Sun, 10 Aug 2025 19:01:23 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 10 Aug 2025 19:01:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 10 Aug 2025 19:01:23 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:9a6263cdeaa5d408640880103ee36920ef814974ca8e2674412ad6460e8968c9`  
		Last Modified: Tue, 12 Aug 2025 22:12:42 GMT  
		Size: 30.1 MB (30136044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af40190d6d264f1be66cb08049b70540eba02ba7fd655fae097cbda289746d53`  
		Last Modified: Wed, 13 Aug 2025 06:22:09 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:feabee456a6c96014e115867bd4e88b799f44b94e6c0b8d1b5000ec496955205`  
		Last Modified: Wed, 13 Aug 2025 06:22:09 GMT  
		Size: 827.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:422d0a380f226f779c85ec48dd7499a08ac0a2aa93252b6aa435fffccde8d8d2`  
		Last Modified: Wed, 13 Aug 2025 06:22:09 GMT  
		Size: 6.2 MB (6231378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a173632e46f201ec2b33805fcaf1d0c7df806b23f5e46a8c69672b6b4b565a4`  
		Last Modified: Wed, 13 Aug 2025 06:22:09 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bc1586a4e693693f7a15724dc111621e8887e469dd123083d647ceb15706ddf`  
		Last Modified: Wed, 13 Aug 2025 06:22:09 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6` - unknown; unknown

```console
$ docker pull spiped@sha256:034a8753ac823cfb19cac1a8b03a8fa42e7980f7937cba5bf7cfc01f4830a477
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3635418 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7286e08e8b96923d063eaa64527cb3cd08ca82cb07acf935f38efb0878583ba6`

```dockerfile
```

-	Layers:
	-	`sha256:bd5609020456c14f8bd5616333f26562e22aaf5d64128b39a58aa6d6c701dc9d`  
		Last Modified: Wed, 13 Aug 2025 10:06:23 GMT  
		Size: 3.6 MB (3620266 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d777d280a0314438cc074454754ca46996e21b39209485922e38a27cd2f5fe8d`  
		Last Modified: Wed, 13 Aug 2025 10:06:24 GMT  
		Size: 15.2 KB (15152 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6` - linux; 386

```console
$ docker pull spiped@sha256:9fcfe0c5b84d9fea6d266d29f18e4dbf8a226baeb085ca7ece3a8de5511e9c60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.7 MB (37733468 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a583f402afb8c7247d391e1083e23f97bbdcf159a97c7d203583d02d6b43500`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Sun, 10 Aug 2025 19:01:23 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1754870400'
# Sun, 10 Aug 2025 19:01:23 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Sun, 10 Aug 2025 19:01:23 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 10 Aug 2025 19:01:23 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Sun, 10 Aug 2025 19:01:23 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Sun, 10 Aug 2025 19:01:23 GMT
VOLUME [/spiped]
# Sun, 10 Aug 2025 19:01:23 GMT
WORKDIR /spiped
# Sun, 10 Aug 2025 19:01:23 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 10 Aug 2025 19:01:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 10 Aug 2025 19:01:23 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:346d0c953bdbc38917a27a6f30726e5b46419d98ecaf4d2d8f201bc3b7025e57`  
		Last Modified: Tue, 12 Aug 2025 20:45:00 GMT  
		Size: 31.3 MB (31289378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab0a9017881d45c9f4e65c372f685c6423638a8e38d92d57f8c3c99691cd7d31`  
		Last Modified: Tue, 12 Aug 2025 22:33:32 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:153819a4650c40b66474fb6dcc7d882e133f0147b067b5fc48010ae2bc8f46ba`  
		Last Modified: Tue, 12 Aug 2025 22:33:32 GMT  
		Size: 828.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a835563de046e9d403e7281f08ebf605249457ca98db2da529bd31f3fb191c68`  
		Last Modified: Tue, 12 Aug 2025 22:33:36 GMT  
		Size: 6.4 MB (6441722 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f06a8985faf5a44d315fbfa0d9975612e26c279004f7da7f8b48a116e66604c3`  
		Last Modified: Tue, 12 Aug 2025 22:33:32 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5ed637e18c93a4756562fbc235fbdf71a83fe6c2e508f6506bb9298bbf4d874`  
		Last Modified: Tue, 12 Aug 2025 22:33:32 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6` - unknown; unknown

```console
$ docker pull spiped@sha256:a22b73545c72bcc558012c681a7f3a323f62434624d93aed8a33f101a37fbf70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3634341 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9191c005b0e377ba838af7947a2eb39c66669632dcfdc9dab86f5a558b4a189`

```dockerfile
```

-	Layers:
	-	`sha256:b719e1d1247f7a8d2b2789312ebfb048bb173eedc1d0d8d7bd03213393393f7e`  
		Last Modified: Wed, 13 Aug 2025 01:04:39 GMT  
		Size: 3.6 MB (3619359 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dbc37a5a50f0a3198bced5718863ebd1123276e390992fd98e77602896183042`  
		Last Modified: Wed, 13 Aug 2025 01:04:40 GMT  
		Size: 15.0 KB (14982 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6` - linux; ppc64le

```console
$ docker pull spiped@sha256:c10b4ed278517ae49edfa7127c75c47dd1266e14633cd7f260e5c66298f1886b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.4 MB (40436468 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8248a22dee5275cedfd61db24cf28a136e1ec17f04c8aac3cad18755c6227de`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Sun, 10 Aug 2025 19:01:23 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1754870400'
# Sun, 10 Aug 2025 19:01:23 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Sun, 10 Aug 2025 19:01:23 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 10 Aug 2025 19:01:23 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Sun, 10 Aug 2025 19:01:23 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Sun, 10 Aug 2025 19:01:23 GMT
VOLUME [/spiped]
# Sun, 10 Aug 2025 19:01:23 GMT
WORKDIR /spiped
# Sun, 10 Aug 2025 19:01:23 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 10 Aug 2025 19:01:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 10 Aug 2025 19:01:23 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:52a4daa8724e9e1632306e15fe478aa26ff0ebcb7ba924cb168e9b6738c239d5`  
		Last Modified: Wed, 13 Aug 2025 01:42:36 GMT  
		Size: 33.6 MB (33594213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b31b56e1b56780df0e15411a668eb62bef22507f7082c36cbaa48e27b80a3dd`  
		Last Modified: Wed, 13 Aug 2025 11:56:38 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f93773dbbb14e44d116aaac13df032fbde418d4886ee8818b206f44616ba18c`  
		Last Modified: Wed, 13 Aug 2025 11:56:38 GMT  
		Size: 828.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1cba8a6190732e98166036b793666dec0711e36288c95969052f741b9f4561e`  
		Last Modified: Wed, 13 Aug 2025 11:56:39 GMT  
		Size: 6.8 MB (6839886 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e7c0065407c754b3de23aec850cf5698c61bd9ecd0c15fc936bb712345929e3`  
		Last Modified: Wed, 13 Aug 2025 11:56:38 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8565dc40120eabde33b3bc8ce9bc1fe16f2eea8e28f0298720ed08f9b970ed0d`  
		Last Modified: Wed, 13 Aug 2025 11:56:39 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6` - unknown; unknown

```console
$ docker pull spiped@sha256:43109fb7e5111756d35286a2c676e3530935deee3215367350f73c7717b0e368
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3636031 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45f14ba2c606d377446bf0e308bd47d6a3d8361c6adf29643758176bbed63bdf`

```dockerfile
```

-	Layers:
	-	`sha256:93dd80ad64b6ab11f964491d9b2edeb14431ec6735a30bc18db3663130f8056f`  
		Last Modified: Wed, 13 Aug 2025 13:04:36 GMT  
		Size: 3.6 MB (3620967 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:efa85ab4fe3aac389b61e3250282df7fdb0c361d597e0dd102c965020f2cd7f0`  
		Last Modified: Wed, 13 Aug 2025 13:04:37 GMT  
		Size: 15.1 KB (15064 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6` - linux; riscv64

```console
$ docker pull spiped@sha256:b8736517f7bb59c511ea4f9ad8a7b005ade95874aac45851c1047a628ec0e53d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.6 MB (37631700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:441b458a8e084c25a772f75f188b539784eb4e7a9c4aceb0f7d4ab836ef01505`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Sun, 10 Aug 2025 19:01:23 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1754870400'
# Sun, 10 Aug 2025 19:01:23 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Sun, 10 Aug 2025 19:01:23 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 10 Aug 2025 19:01:23 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Sun, 10 Aug 2025 19:01:23 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Sun, 10 Aug 2025 19:01:23 GMT
VOLUME [/spiped]
# Sun, 10 Aug 2025 19:01:23 GMT
WORKDIR /spiped
# Sun, 10 Aug 2025 19:01:23 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 10 Aug 2025 19:01:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 10 Aug 2025 19:01:23 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:a37386b9234ad75f65b5aa72f3d919ff0eb3bb18978566fa959d6e357480594c`  
		Last Modified: Wed, 13 Aug 2025 04:01:43 GMT  
		Size: 28.3 MB (28271623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:127ab5460053be42a858239f06c9bdf9bb20e426f59634680dd0952a062febe4`  
		Last Modified: Thu, 14 Aug 2025 14:39:42 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09fbdf3ef389fcfcfcde8edb7a990d48a50bb6562d381638a40a276632d2f2cb`  
		Last Modified: Thu, 14 Aug 2025 14:39:42 GMT  
		Size: 821.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e240e5ce18b11abe9700a80ae6196ee291094f1348bd44a0b4075b3d94f921d`  
		Last Modified: Thu, 14 Aug 2025 14:39:43 GMT  
		Size: 9.4 MB (9357715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b48ce987df3197aa7fa59932f4358de18054e75c420dd112aee00373e12d27e`  
		Last Modified: Thu, 14 Aug 2025 14:39:42 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2668076a38889d3caa1e8ef93527b7bcb09e1c8efde0333842323d9d6886d52`  
		Last Modified: Thu, 14 Aug 2025 14:39:43 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6` - unknown; unknown

```console
$ docker pull spiped@sha256:35913cc3f9fbe2375dbded2db7c773c530af42658aedbb3c8c1091268ab132c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3627439 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28abdef5a89cde265387c1c474ff08401948f48a3a2ad1431ed385b67b9e7e21`

```dockerfile
```

-	Layers:
	-	`sha256:a99c608ee95dedeefc4afd8c5d5002110953819bdd4bfc69f30503d9f7b29d9b`  
		Last Modified: Thu, 14 Aug 2025 16:04:41 GMT  
		Size: 3.6 MB (3612373 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:62f5c0922fff6e0c5c082f975db2470f90964d11fe3ed095088a38dc476c6df5`  
		Last Modified: Thu, 14 Aug 2025 16:04:42 GMT  
		Size: 15.1 KB (15066 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6` - linux; s390x

```console
$ docker pull spiped@sha256:77f28ec69d006b6ee6c4039b94cd23ed250849a792bcd153225cf7caaf0622b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.0 MB (35956075 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58c75aba82b1c983aca3ad0a5a3e6e29eba90da29cbb7e000e07c4ddbbf457ef`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Sun, 10 Aug 2025 19:01:23 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1754870400'
# Sun, 10 Aug 2025 19:01:23 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Sun, 10 Aug 2025 19:01:23 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 10 Aug 2025 19:01:23 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Sun, 10 Aug 2025 19:01:23 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Sun, 10 Aug 2025 19:01:23 GMT
VOLUME [/spiped]
# Sun, 10 Aug 2025 19:01:23 GMT
WORKDIR /spiped
# Sun, 10 Aug 2025 19:01:23 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 10 Aug 2025 19:01:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 10 Aug 2025 19:01:23 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:bfe4d60a27c9392ab729f16b50a763cda36622d744066c3cf029a072133f2907`  
		Last Modified: Tue, 12 Aug 2025 20:59:52 GMT  
		Size: 29.8 MB (29833057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9c626e6797dd4ed7e04641af5c80facb561257332e487c827a1ef8e5abfd9da`  
		Last Modified: Wed, 13 Aug 2025 03:13:05 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9900aed129749b40b135a4bf95bf318aaf8af8baa7324644aa65625a3d451004`  
		Last Modified: Wed, 13 Aug 2025 03:13:06 GMT  
		Size: 830.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f181815f0f2b1a7c15bd8cac9719565f616355c0b414c8b75cebeb1e47fc8407`  
		Last Modified: Wed, 13 Aug 2025 03:13:07 GMT  
		Size: 6.1 MB (6120648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba136bfaf44029a3c3e626051e20473fa8506b40643868e01503bb9f8fa7efa7`  
		Last Modified: Wed, 13 Aug 2025 03:13:07 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d75d2357fb8504e89d6cd5f62c3ba8bb87da5071bdb36e6ea261cfedca4f775`  
		Last Modified: Wed, 13 Aug 2025 03:13:07 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6` - unknown; unknown

```console
$ docker pull spiped@sha256:857963cc998457b693ce1f587d4d49b1e5025fe31ab7b0f7716489ee3e88d128
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3632611 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:749730c63bce3f602d13204e410b4980e4a58c8837357f148bcf3b1b94536afb`

```dockerfile
```

-	Layers:
	-	`sha256:0053cd2920bef5559841359b3be4f662851ac0b991797140849707d6b1fbf038`  
		Last Modified: Wed, 13 Aug 2025 07:06:49 GMT  
		Size: 3.6 MB (3617593 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:61c3f86e4dbefc122f0101f397d596f2aaef357ec79760d163a5e5862bef6588`  
		Last Modified: Wed, 13 Aug 2025 07:06:49 GMT  
		Size: 15.0 KB (15018 bytes)  
		MIME: application/vnd.in-toto+json

## `spiped:1.6-alpine`

```console
$ docker pull spiped@sha256:93cdaab6e3b6d95ed76ddad7bf7f5c587c528e49ffabc2b79f6bd2aea6ab2630
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
$ docker pull spiped@sha256:fe36b545330b74e242df186f67f1842fc3f32a99ef52966ca731dc6982049707
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3916658 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36831aa20b12e50c7b388081fa2b93846f37a41dba1dad419cb49e1293706737`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
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
	-	`sha256:9824c27679d3b27c5e1cb00a73adb6f4f8d556994111c12db3c5d61a0c843df8`  
		Last Modified: Tue, 15 Jul 2025 19:00:01 GMT  
		Size: 3.8 MB (3799689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54f05db9f6c272f7847748f88394ce3bec41041589aaffb85ec57022932d41b6`  
		Last Modified: Mon, 11 Aug 2025 17:12:32 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3273c8db96783d1302ea2a8fb3345410d10a9076895cba46e68c6f063b28c3b`  
		Last Modified: Mon, 11 Aug 2025 17:02:16 GMT  
		Size: 7.9 KB (7946 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6034475a687587b7ef48917e52c9c773ca57a24867d18d0b4eba7762442608d`  
		Last Modified: Mon, 11 Aug 2025 17:02:19 GMT  
		Size: 107.6 KB (107643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28b778daf20a67a656800301303d05635c6c1b4b5aaf39563d66bcddafa96f82`  
		Last Modified: Mon, 11 Aug 2025 17:02:23 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2034aa0716ef0823cb7e0732cc466b480c6e7211047b7e791408e1b2e446969`  
		Last Modified: Mon, 11 Aug 2025 17:02:30 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:f6f21269d5900649987064943467fc128bbc3c34046bbe3f34413ca7c47a199c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.5 KB (96494 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dadc5ec1136521522c7efb5c32bb14f9ad6e983626c50c8bb0ca2df8a8baa064`

```dockerfile
```

-	Layers:
	-	`sha256:627d0194d2b11eccbaee3f5ef6edc22013a7b6093f562006c2fe85e88d07dc9e`  
		Last Modified: Mon, 11 Aug 2025 19:04:42 GMT  
		Size: 82.2 KB (82192 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7f278acc8a79ab1e0936e69a45aa893cb3e9050f2d6e52d3aa94b57021047e7e`  
		Last Modified: Mon, 11 Aug 2025 19:04:43 GMT  
		Size: 14.3 KB (14302 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6-alpine` - linux; arm variant v6

```console
$ docker pull spiped@sha256:67bf8a15d391a12bf880bede827f884530e7cb5b7197db6b4f6c256bed6f8205
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3599402 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c942d42ae3b8e3004d46bf3408c8fe7f7893f60f5c91c514931f39789491c9a3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-armhf.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
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
	-	`sha256:06bab5e847c5674d6ec26b342cc11d7a051a6a231e5db8a955d57bc9f4ab5595`  
		Last Modified: Tue, 15 Jul 2025 18:59:34 GMT  
		Size: 3.5 MB (3500910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10c249d32301274a396c4398f0f9ad3e25d11b9387b71935548f7746004176c0`  
		Last Modified: Mon, 11 Aug 2025 17:07:08 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21acf12f5fa85d243eec713f52367aa2fc9fd58ece745d522619070ee2d91cfd`  
		Last Modified: Mon, 11 Aug 2025 17:07:12 GMT  
		Size: 7.9 KB (7949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:745a95091f37f0e3319bde964913fe0326b1767141fa6ccc002a3b8960025757`  
		Last Modified: Mon, 11 Aug 2025 17:07:15 GMT  
		Size: 89.2 KB (89159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c107fdd944f86a67e108331b416f8aa5deaef19c68a63ed23a8ba9ea0d3401d4`  
		Last Modified: Mon, 11 Aug 2025 17:07:17 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f42a92f540a8b148fc88f8e31cb9818a5f6618f8a1577e639ec0e24e38f9f7e`  
		Last Modified: Mon, 11 Aug 2025 17:07:20 GMT  
		Size: 336.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:f93c76c9652d3a49aa974d58b6ae433e7cb36a7bfa83c6ac0d6cc254a7ba00c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.2 KB (14186 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9211c16e5ea9fc5d8cd82834f8cc184ea937fb23dc63d93b0f565174ccaf11e0`

```dockerfile
```

-	Layers:
	-	`sha256:bc75439704d889af0e27619c5682d57a42ab81be9ff4624f8a521f4377910696`  
		Last Modified: Mon, 11 Aug 2025 19:04:47 GMT  
		Size: 14.2 KB (14186 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6-alpine` - linux; arm variant v7

```console
$ docker pull spiped@sha256:9a4d893ec119af9bc7c0ac4cf7576f963e58abf3883a80df5a16e49b111c25aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3310043 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6ff0c9b1b65653155189d3026538aef9ad32adc4e50d92d8bd56011b77575eb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-armv7.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
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
	-	`sha256:5ee064f8764b09a64829b58705219a88e0b13243f7f403d66ac0c639640426a5`  
		Last Modified: Tue, 15 Jul 2025 19:04:18 GMT  
		Size: 3.2 MB (3219038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:379d666e2282d1ef67d78e68d7d1456eb01f968d2fb8812ac738eba6158a80e9`  
		Last Modified: Mon, 11 Aug 2025 17:12:34 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59c40f7a10d1200a7ded6eb02e6bd8fd18467fcf3ff34f0cf808a4cc55bed23e`  
		Last Modified: Mon, 11 Aug 2025 17:12:39 GMT  
		Size: 7.9 KB (7943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2b5dc976627c424732ee16c786a666f6c1bfc2753fb4eb45ba52b5363d0ddc5`  
		Last Modified: Mon, 11 Aug 2025 17:12:43 GMT  
		Size: 81.7 KB (81679 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:458721a616c9dc4cf600ca98211c375a8834644ed8ef7b186d3328ac28406eae`  
		Last Modified: Mon, 11 Aug 2025 17:12:48 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61e38052aca5003fd5a5a420dc69c7e09ad4a5c937a6fe99ce9562e631927208`  
		Last Modified: Mon, 11 Aug 2025 17:12:58 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:b59043aa1ff63fcd31688fcd9d6a738aa113abdf366d458b93611854679ca46d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.6 KB (96629 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8456c8deda36f896666ee554249c53f1f1c44c53625d46df0b57b3ec07a8f90f`

```dockerfile
```

-	Layers:
	-	`sha256:604964ef49a1e639a8695215e5270aef4e51c3880d27e449bed0300fb49b10e2`  
		Last Modified: Mon, 11 Aug 2025 19:04:50 GMT  
		Size: 82.2 KB (82228 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3b749cfa2bb22f9f9bb0749d7930ddf6645b6ec8b6ff5ce281761785e69fe917`  
		Last Modified: Mon, 11 Aug 2025 19:04:51 GMT  
		Size: 14.4 KB (14401 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6-alpine` - linux; arm64 variant v8

```console
$ docker pull spiped@sha256:0aba08b25b408090092ccc3a2bfff93dd73cd53f1732f086bd5929af3a835323
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4240704 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c275338929556163beeba8cdd1efd28825491f472e207d35476d3569d9ee0e97`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-aarch64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
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
	-	`sha256:6e174226ea690ced550e5641249a412cdbefd2d09871f3e64ab52137a54ba606`  
		Last Modified: Tue, 15 Jul 2025 18:59:50 GMT  
		Size: 4.1 MB (4130750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:401e496ab6a7fec1ab1bb8f0b8a996b06c9fb697746e47439f58ec78714d57cb`  
		Last Modified: Mon, 11 Aug 2025 17:09:42 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc10c01537e03fed07cdd599b8a98a0adcfa5c06d0ba71c752ddf65d7ef18bd7`  
		Last Modified: Mon, 11 Aug 2025 17:09:45 GMT  
		Size: 8.0 KB (7951 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adfbfacdb4fddd486ebc3cf352ee0538e6eadf8b3033b6e12abdaf15234459c1`  
		Last Modified: Mon, 11 Aug 2025 17:09:48 GMT  
		Size: 100.6 KB (100617 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a7767630476c70a6cf95063bb707ffee6b4b40278b06fcdb17fa3f7dca8427b`  
		Last Modified: Mon, 11 Aug 2025 17:09:50 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25762649a73c36acce0fd48360b8be503aee4c1602f1a59b759cb8a795ab8c6b`  
		Last Modified: Mon, 11 Aug 2025 17:09:53 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:5b477d36fe748f79631e7066c0574b5a9ca9e3e1c169c735e2a960cd0cea9d95
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.7 KB (96684 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6c2517fcfde44c5508a52e01d9e77e79db6fd3daad75c70853eb4b2b378a0ae`

```dockerfile
```

-	Layers:
	-	`sha256:1903a367ec2a9e9fbbee350246fe22b734d8bacdcfb9d34f695b231aa6f96ccd`  
		Last Modified: Mon, 11 Aug 2025 19:04:55 GMT  
		Size: 82.2 KB (82248 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6d54be9922b28101eb015c8900bf1221e9437578e72fce9654714c21b92c04d6`  
		Last Modified: Mon, 11 Aug 2025 19:04:56 GMT  
		Size: 14.4 KB (14436 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6-alpine` - linux; 386

```console
$ docker pull spiped@sha256:48537809d8133274a37ab69a836499fb8479383b5b69967228ce176ac6f1be60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3744445 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f9a0ea1f48b6cac9c7ce62d1260fd3fc9040cc58f686650da2fda4a116dfe2b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-x86.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
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
	-	`sha256:a55f2fb89da4caae0d783c0045a67446dee9bbd977fecb44db9e1231550fa888`  
		Last Modified: Tue, 15 Jul 2025 19:04:11 GMT  
		Size: 3.6 MB (3615006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3eba0b59a29857fdbd92df8627b53b15ba8b6ab4ec59021ee5712b80dfed882`  
		Last Modified: Mon, 11 Aug 2025 17:07:16 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:847779e3481b940532b586da8162b98cc75b9ca766b1f6e26d1622c3ed2d8ad1`  
		Last Modified: Mon, 11 Aug 2025 17:07:19 GMT  
		Size: 7.9 KB (7947 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84ead07d68c6f9280214b36ee65459f295af32fb5a83587a9d94ff34fbd8edf9`  
		Last Modified: Mon, 11 Aug 2025 17:07:22 GMT  
		Size: 120.1 KB (120108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbd0afa8d91fe587be8847df03da4b2cd7c73dbce722c78ea9606f83cbe408ae`  
		Last Modified: Mon, 11 Aug 2025 17:07:25 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18e699ee2bbb463e05c765e96679445315e788311982f0d542d6d6c513614f78`  
		Last Modified: Mon, 11 Aug 2025 17:07:31 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:15f0f80fe34bd14b6d564b6e741552ba495ee58c3268d7ba1e7611e8f104298a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.4 KB (96433 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9ee4d0ec8becf51535d0fdeb2611b861926d3c65de73b970a6f07164630a189`

```dockerfile
```

-	Layers:
	-	`sha256:fa8d8def96807232c5de9a2689e639f51f6662c2960d1e6a13e5390c1ef5f875`  
		Last Modified: Mon, 11 Aug 2025 19:05:00 GMT  
		Size: 82.2 KB (82167 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:017908264a6caffecdaecbe817722cb1919c11d362589f17292a9cbd2d55c204`  
		Last Modified: Mon, 11 Aug 2025 19:05:00 GMT  
		Size: 14.3 KB (14266 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6-alpine` - linux; ppc64le

```console
$ docker pull spiped@sha256:79845ce442587e8a1743c515186951ae7603efaf08e38a0a7f4ce40a4af20597
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3849108 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04c74704274ad902930376019928ebde446c1deca3459f089066274bd8f1565c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-ppc64le.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
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
	-	`sha256:b762f678859bfa5c3948b5f1b04959aa43c8aba88e2389e281413d303d62a7e3`  
		Last Modified: Tue, 15 Jul 2025 18:59:53 GMT  
		Size: 3.7 MB (3727111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2373f01bf878f477a6cf1b4d56c9227ff43127b4d845c3562616e2a46d22dbdd`  
		Last Modified: Mon, 11 Aug 2025 17:13:12 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:427ad9317b0d6357fac90f31d124d5e9b36ee534067da2df12710b89392c781e`  
		Last Modified: Mon, 11 Aug 2025 17:13:15 GMT  
		Size: 7.9 KB (7948 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2f4f5c32876f7abc20796b83c3897652d454e319406eae7a6a6ed5d74ea44e3`  
		Last Modified: Mon, 11 Aug 2025 17:13:20 GMT  
		Size: 112.7 KB (112665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a9033716c014ce457c2d72e5e75fc8fa8044e87014da9f03f2fb489b825aef8`  
		Last Modified: Mon, 11 Aug 2025 17:13:26 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb03f1a2076f357e9cab2045b9652c20950ca5d8f7421f046896219b8532d06b`  
		Last Modified: Mon, 11 Aug 2025 17:13:29 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:a6d8ce06cb0ab858ad3076a0f7a57f28f1e6ed5e17a4157b6b6a30ae37c3368a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.6 KB (94625 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b10d0bb2f5cfe8395a4519604c8ace1de04e74af97cc131cea9853a67b5fc2cc`

```dockerfile
```

-	Layers:
	-	`sha256:ff1c9c59d73d4c50497a06f04ad9a30428a99ad3de292bad5a2e9dd8d91d1160`  
		Last Modified: Mon, 11 Aug 2025 19:05:05 GMT  
		Size: 80.3 KB (80275 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e7e4e7f2cdbb149daeaca2e6e837f823a3641e8d4f0c3cf28a999579d17542cf`  
		Last Modified: Mon, 11 Aug 2025 19:05:05 GMT  
		Size: 14.3 KB (14350 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6-alpine` - linux; riscv64

```console
$ docker pull spiped@sha256:eb5294dab564ed0a45bac04aff4eb51d319f7c4fd6d0fe4eb457a283aceff474
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3620988 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83d8198608b9934495dc90c953cc87dfd83d7b1d0af22c216f3636508b77fd7b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-riscv64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
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
	-	`sha256:cbe7080b5783de104ad67ff4595bfa8ae70a597181a84621f51c5ccd084218da`  
		Last Modified: Tue, 15 Jul 2025 19:00:17 GMT  
		Size: 3.5 MB (3512801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:337ef438f7e589dc4f613c730fb4dd5a761abfd9e48d0d59495d3aff151e16ab`  
		Last Modified: Mon, 11 Aug 2025 17:12:32 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89b21db99ab142ddfd5ec4b8ef25065f37bc1aee36e94cad1db40698257cd6fc`  
		Last Modified: Mon, 11 Aug 2025 17:12:36 GMT  
		Size: 7.9 KB (7945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe3dc6909718e2eb82c7628f42d658b99dcdf7135cb7db460851920d41ad58c4`  
		Last Modified: Mon, 11 Aug 2025 17:12:40 GMT  
		Size: 98.9 KB (98856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:541a31d50d76446fd96c63516c67f098fad214976beea363002d79b73ba95d22`  
		Last Modified: Mon, 11 Aug 2025 17:12:44 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7db5851f3b8a32ba3d881649070f2380d838c65cb1f702ed418b43e640f03d7a`  
		Last Modified: Mon, 11 Aug 2025 17:12:47 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:c32a8fd37856a4dfea8b91e0c18b79f0f43571bcac39779ab262c4c4741714be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.6 KB (94618 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c1f688a2498b96358ae65a439e4a1eda2bc0b14f90b0ec530106a28eb2077c4`

```dockerfile
```

-	Layers:
	-	`sha256:a3eaafb5380cff781fc2bfb357665fc4513231c31e349b37e3e7cc95f16b052b`  
		Last Modified: Mon, 11 Aug 2025 19:05:10 GMT  
		Size: 80.3 KB (80271 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:331b28e1546911de84609c9d63a3f86e0abca6d7efd8c9fa3d618f196a1ec42d`  
		Last Modified: Mon, 11 Aug 2025 19:05:10 GMT  
		Size: 14.3 KB (14347 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6-alpine` - linux; s390x

```console
$ docker pull spiped@sha256:1c717961a5e8cc5e8fd75141c21f0a6de58a68c44608450fa683029bae71c085
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3751251 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b744d847c43ddb5879abe90a22b110885a2c0ffb39ae4f72a3753f4e839db1a2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-s390x.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
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
	-	`sha256:5d29754ce036967079405405a04a54a7d3f8ba85e0057b6bdda3d03aa59c8361`  
		Last Modified: Tue, 15 Jul 2025 19:00:06 GMT  
		Size: 3.6 MB (3644971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e1bd137b03fbd1349d3ad3112f1e21d62c9baae0012a389da756b7ca6f932c7`  
		Last Modified: Mon, 11 Aug 2025 17:07:14 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a06802588e4666537f404a0ce19ebfc4da3850fd2dbe3536a4fe24380b4bc222`  
		Last Modified: Mon, 11 Aug 2025 17:07:18 GMT  
		Size: 8.0 KB (7950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f406fcd8d03a4ee6c2fc9bee5495de93682706f0ac21a261973b02e5cda0c93`  
		Last Modified: Mon, 11 Aug 2025 17:07:23 GMT  
		Size: 96.9 KB (96945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c48cae2c2a395f0f13d3dba276c545fd622a02bc6b9325ac1f1573447c6e90f`  
		Last Modified: Mon, 11 Aug 2025 17:07:27 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46bfce62ca5613c78d3504649bafb02ff12a44fa234e3dfc1134ece19652d3d7`  
		Last Modified: Mon, 11 Aug 2025 17:07:30 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:654988790b7ed5b0441b8c38603d934b9706d4cccb2a3a9a96d8d3cc5f49c40a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.5 KB (94540 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a02880e0cbcf996ddd3d1c0bf389633fb423298a93ece41330d2f645d016566`

```dockerfile
```

-	Layers:
	-	`sha256:f77f4e4ec9383facda6fb5da7eeb5bf28f59fb80e6043ee4cb4eec3950e1422d`  
		Last Modified: Mon, 11 Aug 2025 19:05:14 GMT  
		Size: 80.2 KB (80241 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d27df7657b4c19b9a7071f58a7b58946289a2dc8ca2315c4bb0375dcfd961e1e`  
		Last Modified: Mon, 11 Aug 2025 19:05:15 GMT  
		Size: 14.3 KB (14299 bytes)  
		MIME: application/vnd.in-toto+json

## `spiped:1.6.4`

```console
$ docker pull spiped@sha256:393010ed037fbb2527e124feb16b874a82ef10ffbbc5b43c9ffc6f3f9bf449b4
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
$ docker pull spiped@sha256:bf92abd8857927a58bf60b37b751b45e7849904d0c3eb39428aa9ded13973b45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.8 MB (36823886 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:131dfb2d7b78cb541b4f99eb9752b00f874f76280458f7f2ed039e38a9886acc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Sun, 10 Aug 2025 19:01:23 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1754870400'
# Sun, 10 Aug 2025 19:01:23 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Sun, 10 Aug 2025 19:01:23 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 10 Aug 2025 19:01:23 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Sun, 10 Aug 2025 19:01:23 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Sun, 10 Aug 2025 19:01:23 GMT
VOLUME [/spiped]
# Sun, 10 Aug 2025 19:01:23 GMT
WORKDIR /spiped
# Sun, 10 Aug 2025 19:01:23 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 10 Aug 2025 19:01:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 10 Aug 2025 19:01:23 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:396b1da7636e2dcd10565cb4f2f952cbb4a8a38b58d3b86a2cacb172fb70117c`  
		Last Modified: Tue, 12 Aug 2025 20:45:08 GMT  
		Size: 29.8 MB (29773285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1960f8d044ed2918a9b63f9b23e244fc01996b6272a914c37ccd6d6dfcc68e4e`  
		Last Modified: Tue, 12 Aug 2025 22:33:32 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1429568f03b0485d02eb3e469fe20cdda6eb6e31f703b79f50834c7990b35868`  
		Last Modified: Tue, 12 Aug 2025 22:33:32 GMT  
		Size: 824.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f288333198193fd5d29806df7832431ab2cf3ad06e46a49c6dffea5d74eeeb7`  
		Last Modified: Tue, 12 Aug 2025 22:33:34 GMT  
		Size: 7.0 MB (7048236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f6a4df49d11a34ceed3269d89d6506916e2574f79c63ac88c6e45ce2067bb65`  
		Last Modified: Tue, 12 Aug 2025 22:33:32 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e299a1e4998ed061307241b9eb0eaf6d3f70b3dfa7c6b13aefce13c34f3e486a`  
		Last Modified: Tue, 12 Aug 2025 22:33:32 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6.4` - unknown; unknown

```console
$ docker pull spiped@sha256:06b0151f64cf465a20c4b3cf24d52eb8346bdf93c27fd53c814bb089ec4cb05a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3640248 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3aa7836e633ede2d640e4ee8a7f90afb38f97ad41e553c5088dc576ec98a1380`

```dockerfile
```

-	Layers:
	-	`sha256:049c8275986690c07daaa8af602e6e2eccaad28d023f774058df9cfbefbbaffe`  
		Last Modified: Wed, 13 Aug 2025 01:04:22 GMT  
		Size: 3.6 MB (3625230 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8ac5644f2c0e54bd96ba3c75290b8842a1d59415c4f6007a1540ee957de0ba98`  
		Last Modified: Wed, 13 Aug 2025 01:04:23 GMT  
		Size: 15.0 KB (15018 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6.4` - linux; arm variant v5

```console
$ docker pull spiped@sha256:3a8a3157e13515af48661b3359c74ad04e1a30456f7c560ae8f68e87a20ffb9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.9 MB (32910178 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dcbb748125f0b8dcd0fb6493ed4d870453d8c8efa012f4e2222c7dc2619a103a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 02 Apr 2025 21:12:22 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1753056000'
# Wed, 02 Apr 2025 21:12:22 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Wed, 02 Apr 2025 21:12:22 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
VOLUME [/spiped]
# Wed, 02 Apr 2025 21:12:22 GMT
WORKDIR /spiped
# Wed, 02 Apr 2025 21:12:22 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Apr 2025 21:12:22 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:70a0ce20524d4016d59550a3733a4080dc793deac81fcf6a038a61c9427611d7`  
		Last Modified: Tue, 22 Jul 2025 00:20:40 GMT  
		Size: 25.8 MB (25762716 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49046a4dd717e46f1d47e8b442ea16a32ae5c918851152c07d29a1ec56228f2a`  
		Last Modified: Tue, 22 Jul 2025 05:31:57 GMT  
		Size: 1.1 KB (1104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b15015636ae2d1e604b210604ec62efba4b52378febbaf8d104fdc747967525`  
		Last Modified: Tue, 22 Jul 2025 05:31:57 GMT  
		Size: 2.0 MB (1998288 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3147db3fa731dc64539822c647b65ed645104c05a5b5829ecb7b0ef27e85143`  
		Last Modified: Tue, 22 Jul 2025 05:31:57 GMT  
		Size: 5.1 MB (5147637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a27fdd8a658afb898909a24260e3428adae409d14c86ccd2e98c5e9c0ab7edc`  
		Last Modified: Tue, 22 Jul 2025 05:31:56 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d5c5f7070397c2858394d855108e31978aa74ffa73cbdd12b7200db8de2d441`  
		Last Modified: Tue, 22 Jul 2025 05:31:57 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6.4` - unknown; unknown

```console
$ docker pull spiped@sha256:772cf6016b094f52670a3487eacbd9f06e92145eb1e55a55b09fea0bf6aa9fdd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3617772 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c7e48cc724fee727a6693c57c4043d98e8bfac2f9242b3effde1720a1427492`

```dockerfile
```

-	Layers:
	-	`sha256:b510654d2a8c1b8ad052747c8ddb7e16c41356134db9be35752c35115580cfb1`  
		Last Modified: Tue, 22 Jul 2025 07:04:32 GMT  
		Size: 3.6 MB (3602631 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:471889e07393b6e3410d1d09003810c74afd93089e902abc26d07e1e0f8a2fce`  
		Last Modified: Tue, 22 Jul 2025 07:04:32 GMT  
		Size: 15.1 KB (15141 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6.4` - linux; arm variant v7

```console
$ docker pull spiped@sha256:df4a67cfc69545276ba2fa47893371e5bae16c16c7966f816afa7d6ff25c8030
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.7 MB (30685629 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3961f78e049e031a2d9c52600e014e09161ac256b60bb21f7765b25227de7da0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 02 Apr 2025 21:12:22 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1753056000'
# Wed, 02 Apr 2025 21:12:22 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Wed, 02 Apr 2025 21:12:22 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
VOLUME [/spiped]
# Wed, 02 Apr 2025 21:12:22 GMT
WORKDIR /spiped
# Wed, 02 Apr 2025 21:12:22 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Apr 2025 21:12:22 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:3d83c6df5858d91327bc312b738290e713ab4b6d4e0586c217399744d7596864`  
		Last Modified: Tue, 22 Jul 2025 00:20:36 GMT  
		Size: 23.9 MB (23938916 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe33cfed210711d85c4fb2b78824894f0d21979f013b4c59e595b535eda34fb6`  
		Last Modified: Tue, 22 Jul 2025 08:09:39 GMT  
		Size: 1.1 KB (1104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a5b5df2c8141fd6c1a420c98bbdfedda39b519cde600d577420f7822d64674e`  
		Last Modified: Tue, 22 Jul 2025 08:09:39 GMT  
		Size: 1.9 MB (1856406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8116bf27bbfb2abe4dad1a945819daa5184885a04be75e148bd91f3bab537924`  
		Last Modified: Tue, 22 Jul 2025 08:09:40 GMT  
		Size: 4.9 MB (4888769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae19946bd511763f4472e27df6f9f101f98a95a0b8e6b788beeb92d06694c152`  
		Last Modified: Tue, 22 Jul 2025 08:09:41 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcc6b3556f96d25cb1b9f9cfdc269be4883d98a05b63099eaa06187780ea70fc`  
		Last Modified: Tue, 22 Jul 2025 08:09:43 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6.4` - unknown; unknown

```console
$ docker pull spiped@sha256:0128ce934f586afb91aec29487355efccdefd76ccf4cce8344526da2947139c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3616955 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8dee0971e665b140b05d6053112c4d56d1111a6c474b6746e0bc68c030ecb23c`

```dockerfile
```

-	Layers:
	-	`sha256:2776f040304a973414de30d806031dbe4bb548df652c417d069b20a435fc3dd1`  
		Last Modified: Tue, 22 Jul 2025 10:07:08 GMT  
		Size: 3.6 MB (3601814 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:40b6ffb7b5108a7c93066348dec6008dc745f5e3d55e87ed73c96c7f2fb9cb03`  
		Last Modified: Tue, 22 Jul 2025 10:07:09 GMT  
		Size: 15.1 KB (15141 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6.4` - linux; arm64 variant v8

```console
$ docker pull spiped@sha256:e4096ff20583a5034e9280aeddf5f1a78923d9682609c199920f22185356b4fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.4 MB (36369792 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aff0f6bbb2c3ea404a50f705696846a93449e7bd0e783ad59d028a426200d382`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Sun, 10 Aug 2025 19:01:23 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1754870400'
# Sun, 10 Aug 2025 19:01:23 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Sun, 10 Aug 2025 19:01:23 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 10 Aug 2025 19:01:23 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Sun, 10 Aug 2025 19:01:23 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Sun, 10 Aug 2025 19:01:23 GMT
VOLUME [/spiped]
# Sun, 10 Aug 2025 19:01:23 GMT
WORKDIR /spiped
# Sun, 10 Aug 2025 19:01:23 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 10 Aug 2025 19:01:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 10 Aug 2025 19:01:23 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:9a6263cdeaa5d408640880103ee36920ef814974ca8e2674412ad6460e8968c9`  
		Last Modified: Tue, 12 Aug 2025 22:12:42 GMT  
		Size: 30.1 MB (30136044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af40190d6d264f1be66cb08049b70540eba02ba7fd655fae097cbda289746d53`  
		Last Modified: Wed, 13 Aug 2025 06:22:09 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:feabee456a6c96014e115867bd4e88b799f44b94e6c0b8d1b5000ec496955205`  
		Last Modified: Wed, 13 Aug 2025 06:22:09 GMT  
		Size: 827.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:422d0a380f226f779c85ec48dd7499a08ac0a2aa93252b6aa435fffccde8d8d2`  
		Last Modified: Wed, 13 Aug 2025 06:22:09 GMT  
		Size: 6.2 MB (6231378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a173632e46f201ec2b33805fcaf1d0c7df806b23f5e46a8c69672b6b4b565a4`  
		Last Modified: Wed, 13 Aug 2025 06:22:09 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bc1586a4e693693f7a15724dc111621e8887e469dd123083d647ceb15706ddf`  
		Last Modified: Wed, 13 Aug 2025 06:22:09 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6.4` - unknown; unknown

```console
$ docker pull spiped@sha256:034a8753ac823cfb19cac1a8b03a8fa42e7980f7937cba5bf7cfc01f4830a477
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3635418 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7286e08e8b96923d063eaa64527cb3cd08ca82cb07acf935f38efb0878583ba6`

```dockerfile
```

-	Layers:
	-	`sha256:bd5609020456c14f8bd5616333f26562e22aaf5d64128b39a58aa6d6c701dc9d`  
		Last Modified: Wed, 13 Aug 2025 10:06:23 GMT  
		Size: 3.6 MB (3620266 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d777d280a0314438cc074454754ca46996e21b39209485922e38a27cd2f5fe8d`  
		Last Modified: Wed, 13 Aug 2025 10:06:24 GMT  
		Size: 15.2 KB (15152 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6.4` - linux; 386

```console
$ docker pull spiped@sha256:9fcfe0c5b84d9fea6d266d29f18e4dbf8a226baeb085ca7ece3a8de5511e9c60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.7 MB (37733468 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a583f402afb8c7247d391e1083e23f97bbdcf159a97c7d203583d02d6b43500`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Sun, 10 Aug 2025 19:01:23 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1754870400'
# Sun, 10 Aug 2025 19:01:23 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Sun, 10 Aug 2025 19:01:23 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 10 Aug 2025 19:01:23 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Sun, 10 Aug 2025 19:01:23 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Sun, 10 Aug 2025 19:01:23 GMT
VOLUME [/spiped]
# Sun, 10 Aug 2025 19:01:23 GMT
WORKDIR /spiped
# Sun, 10 Aug 2025 19:01:23 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 10 Aug 2025 19:01:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 10 Aug 2025 19:01:23 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:346d0c953bdbc38917a27a6f30726e5b46419d98ecaf4d2d8f201bc3b7025e57`  
		Last Modified: Tue, 12 Aug 2025 20:45:00 GMT  
		Size: 31.3 MB (31289378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab0a9017881d45c9f4e65c372f685c6423638a8e38d92d57f8c3c99691cd7d31`  
		Last Modified: Tue, 12 Aug 2025 22:33:32 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:153819a4650c40b66474fb6dcc7d882e133f0147b067b5fc48010ae2bc8f46ba`  
		Last Modified: Tue, 12 Aug 2025 22:33:32 GMT  
		Size: 828.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a835563de046e9d403e7281f08ebf605249457ca98db2da529bd31f3fb191c68`  
		Last Modified: Tue, 12 Aug 2025 22:33:36 GMT  
		Size: 6.4 MB (6441722 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f06a8985faf5a44d315fbfa0d9975612e26c279004f7da7f8b48a116e66604c3`  
		Last Modified: Tue, 12 Aug 2025 22:33:32 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5ed637e18c93a4756562fbc235fbdf71a83fe6c2e508f6506bb9298bbf4d874`  
		Last Modified: Tue, 12 Aug 2025 22:33:32 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6.4` - unknown; unknown

```console
$ docker pull spiped@sha256:a22b73545c72bcc558012c681a7f3a323f62434624d93aed8a33f101a37fbf70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3634341 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9191c005b0e377ba838af7947a2eb39c66669632dcfdc9dab86f5a558b4a189`

```dockerfile
```

-	Layers:
	-	`sha256:b719e1d1247f7a8d2b2789312ebfb048bb173eedc1d0d8d7bd03213393393f7e`  
		Last Modified: Wed, 13 Aug 2025 01:04:39 GMT  
		Size: 3.6 MB (3619359 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dbc37a5a50f0a3198bced5718863ebd1123276e390992fd98e77602896183042`  
		Last Modified: Wed, 13 Aug 2025 01:04:40 GMT  
		Size: 15.0 KB (14982 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6.4` - linux; ppc64le

```console
$ docker pull spiped@sha256:c10b4ed278517ae49edfa7127c75c47dd1266e14633cd7f260e5c66298f1886b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.4 MB (40436468 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8248a22dee5275cedfd61db24cf28a136e1ec17f04c8aac3cad18755c6227de`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Sun, 10 Aug 2025 19:01:23 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1754870400'
# Sun, 10 Aug 2025 19:01:23 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Sun, 10 Aug 2025 19:01:23 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 10 Aug 2025 19:01:23 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Sun, 10 Aug 2025 19:01:23 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Sun, 10 Aug 2025 19:01:23 GMT
VOLUME [/spiped]
# Sun, 10 Aug 2025 19:01:23 GMT
WORKDIR /spiped
# Sun, 10 Aug 2025 19:01:23 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 10 Aug 2025 19:01:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 10 Aug 2025 19:01:23 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:52a4daa8724e9e1632306e15fe478aa26ff0ebcb7ba924cb168e9b6738c239d5`  
		Last Modified: Wed, 13 Aug 2025 01:42:36 GMT  
		Size: 33.6 MB (33594213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b31b56e1b56780df0e15411a668eb62bef22507f7082c36cbaa48e27b80a3dd`  
		Last Modified: Wed, 13 Aug 2025 11:56:38 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f93773dbbb14e44d116aaac13df032fbde418d4886ee8818b206f44616ba18c`  
		Last Modified: Wed, 13 Aug 2025 11:56:38 GMT  
		Size: 828.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1cba8a6190732e98166036b793666dec0711e36288c95969052f741b9f4561e`  
		Last Modified: Wed, 13 Aug 2025 11:56:39 GMT  
		Size: 6.8 MB (6839886 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e7c0065407c754b3de23aec850cf5698c61bd9ecd0c15fc936bb712345929e3`  
		Last Modified: Wed, 13 Aug 2025 11:56:38 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8565dc40120eabde33b3bc8ce9bc1fe16f2eea8e28f0298720ed08f9b970ed0d`  
		Last Modified: Wed, 13 Aug 2025 11:56:39 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6.4` - unknown; unknown

```console
$ docker pull spiped@sha256:43109fb7e5111756d35286a2c676e3530935deee3215367350f73c7717b0e368
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3636031 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45f14ba2c606d377446bf0e308bd47d6a3d8361c6adf29643758176bbed63bdf`

```dockerfile
```

-	Layers:
	-	`sha256:93dd80ad64b6ab11f964491d9b2edeb14431ec6735a30bc18db3663130f8056f`  
		Last Modified: Wed, 13 Aug 2025 13:04:36 GMT  
		Size: 3.6 MB (3620967 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:efa85ab4fe3aac389b61e3250282df7fdb0c361d597e0dd102c965020f2cd7f0`  
		Last Modified: Wed, 13 Aug 2025 13:04:37 GMT  
		Size: 15.1 KB (15064 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6.4` - linux; riscv64

```console
$ docker pull spiped@sha256:b8736517f7bb59c511ea4f9ad8a7b005ade95874aac45851c1047a628ec0e53d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.6 MB (37631700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:441b458a8e084c25a772f75f188b539784eb4e7a9c4aceb0f7d4ab836ef01505`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Sun, 10 Aug 2025 19:01:23 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1754870400'
# Sun, 10 Aug 2025 19:01:23 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Sun, 10 Aug 2025 19:01:23 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 10 Aug 2025 19:01:23 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Sun, 10 Aug 2025 19:01:23 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Sun, 10 Aug 2025 19:01:23 GMT
VOLUME [/spiped]
# Sun, 10 Aug 2025 19:01:23 GMT
WORKDIR /spiped
# Sun, 10 Aug 2025 19:01:23 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 10 Aug 2025 19:01:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 10 Aug 2025 19:01:23 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:a37386b9234ad75f65b5aa72f3d919ff0eb3bb18978566fa959d6e357480594c`  
		Last Modified: Wed, 13 Aug 2025 04:01:43 GMT  
		Size: 28.3 MB (28271623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:127ab5460053be42a858239f06c9bdf9bb20e426f59634680dd0952a062febe4`  
		Last Modified: Thu, 14 Aug 2025 14:39:42 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09fbdf3ef389fcfcfcde8edb7a990d48a50bb6562d381638a40a276632d2f2cb`  
		Last Modified: Thu, 14 Aug 2025 14:39:42 GMT  
		Size: 821.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e240e5ce18b11abe9700a80ae6196ee291094f1348bd44a0b4075b3d94f921d`  
		Last Modified: Thu, 14 Aug 2025 14:39:43 GMT  
		Size: 9.4 MB (9357715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b48ce987df3197aa7fa59932f4358de18054e75c420dd112aee00373e12d27e`  
		Last Modified: Thu, 14 Aug 2025 14:39:42 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2668076a38889d3caa1e8ef93527b7bcb09e1c8efde0333842323d9d6886d52`  
		Last Modified: Thu, 14 Aug 2025 14:39:43 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6.4` - unknown; unknown

```console
$ docker pull spiped@sha256:35913cc3f9fbe2375dbded2db7c773c530af42658aedbb3c8c1091268ab132c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3627439 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28abdef5a89cde265387c1c474ff08401948f48a3a2ad1431ed385b67b9e7e21`

```dockerfile
```

-	Layers:
	-	`sha256:a99c608ee95dedeefc4afd8c5d5002110953819bdd4bfc69f30503d9f7b29d9b`  
		Last Modified: Thu, 14 Aug 2025 16:04:41 GMT  
		Size: 3.6 MB (3612373 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:62f5c0922fff6e0c5c082f975db2470f90964d11fe3ed095088a38dc476c6df5`  
		Last Modified: Thu, 14 Aug 2025 16:04:42 GMT  
		Size: 15.1 KB (15066 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6.4` - linux; s390x

```console
$ docker pull spiped@sha256:77f28ec69d006b6ee6c4039b94cd23ed250849a792bcd153225cf7caaf0622b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.0 MB (35956075 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58c75aba82b1c983aca3ad0a5a3e6e29eba90da29cbb7e000e07c4ddbbf457ef`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Sun, 10 Aug 2025 19:01:23 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1754870400'
# Sun, 10 Aug 2025 19:01:23 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Sun, 10 Aug 2025 19:01:23 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 10 Aug 2025 19:01:23 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Sun, 10 Aug 2025 19:01:23 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Sun, 10 Aug 2025 19:01:23 GMT
VOLUME [/spiped]
# Sun, 10 Aug 2025 19:01:23 GMT
WORKDIR /spiped
# Sun, 10 Aug 2025 19:01:23 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 10 Aug 2025 19:01:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 10 Aug 2025 19:01:23 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:bfe4d60a27c9392ab729f16b50a763cda36622d744066c3cf029a072133f2907`  
		Last Modified: Tue, 12 Aug 2025 20:59:52 GMT  
		Size: 29.8 MB (29833057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9c626e6797dd4ed7e04641af5c80facb561257332e487c827a1ef8e5abfd9da`  
		Last Modified: Wed, 13 Aug 2025 03:13:05 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9900aed129749b40b135a4bf95bf318aaf8af8baa7324644aa65625a3d451004`  
		Last Modified: Wed, 13 Aug 2025 03:13:06 GMT  
		Size: 830.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f181815f0f2b1a7c15bd8cac9719565f616355c0b414c8b75cebeb1e47fc8407`  
		Last Modified: Wed, 13 Aug 2025 03:13:07 GMT  
		Size: 6.1 MB (6120648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba136bfaf44029a3c3e626051e20473fa8506b40643868e01503bb9f8fa7efa7`  
		Last Modified: Wed, 13 Aug 2025 03:13:07 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d75d2357fb8504e89d6cd5f62c3ba8bb87da5071bdb36e6ea261cfedca4f775`  
		Last Modified: Wed, 13 Aug 2025 03:13:07 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6.4` - unknown; unknown

```console
$ docker pull spiped@sha256:857963cc998457b693ce1f587d4d49b1e5025fe31ab7b0f7716489ee3e88d128
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3632611 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:749730c63bce3f602d13204e410b4980e4a58c8837357f148bcf3b1b94536afb`

```dockerfile
```

-	Layers:
	-	`sha256:0053cd2920bef5559841359b3be4f662851ac0b991797140849707d6b1fbf038`  
		Last Modified: Wed, 13 Aug 2025 07:06:49 GMT  
		Size: 3.6 MB (3617593 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:61c3f86e4dbefc122f0101f397d596f2aaef357ec79760d163a5e5862bef6588`  
		Last Modified: Wed, 13 Aug 2025 07:06:49 GMT  
		Size: 15.0 KB (15018 bytes)  
		MIME: application/vnd.in-toto+json

## `spiped:1.6.4-alpine`

```console
$ docker pull spiped@sha256:93cdaab6e3b6d95ed76ddad7bf7f5c587c528e49ffabc2b79f6bd2aea6ab2630
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
$ docker pull spiped@sha256:fe36b545330b74e242df186f67f1842fc3f32a99ef52966ca731dc6982049707
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3916658 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36831aa20b12e50c7b388081fa2b93846f37a41dba1dad419cb49e1293706737`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
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
	-	`sha256:9824c27679d3b27c5e1cb00a73adb6f4f8d556994111c12db3c5d61a0c843df8`  
		Last Modified: Tue, 15 Jul 2025 19:00:01 GMT  
		Size: 3.8 MB (3799689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54f05db9f6c272f7847748f88394ce3bec41041589aaffb85ec57022932d41b6`  
		Last Modified: Mon, 11 Aug 2025 17:12:32 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3273c8db96783d1302ea2a8fb3345410d10a9076895cba46e68c6f063b28c3b`  
		Last Modified: Mon, 11 Aug 2025 17:02:16 GMT  
		Size: 7.9 KB (7946 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6034475a687587b7ef48917e52c9c773ca57a24867d18d0b4eba7762442608d`  
		Last Modified: Mon, 11 Aug 2025 17:02:19 GMT  
		Size: 107.6 KB (107643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28b778daf20a67a656800301303d05635c6c1b4b5aaf39563d66bcddafa96f82`  
		Last Modified: Mon, 11 Aug 2025 17:02:23 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2034aa0716ef0823cb7e0732cc466b480c6e7211047b7e791408e1b2e446969`  
		Last Modified: Mon, 11 Aug 2025 17:02:30 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6.4-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:f6f21269d5900649987064943467fc128bbc3c34046bbe3f34413ca7c47a199c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.5 KB (96494 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dadc5ec1136521522c7efb5c32bb14f9ad6e983626c50c8bb0ca2df8a8baa064`

```dockerfile
```

-	Layers:
	-	`sha256:627d0194d2b11eccbaee3f5ef6edc22013a7b6093f562006c2fe85e88d07dc9e`  
		Last Modified: Mon, 11 Aug 2025 19:04:42 GMT  
		Size: 82.2 KB (82192 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7f278acc8a79ab1e0936e69a45aa893cb3e9050f2d6e52d3aa94b57021047e7e`  
		Last Modified: Mon, 11 Aug 2025 19:04:43 GMT  
		Size: 14.3 KB (14302 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6.4-alpine` - linux; arm variant v6

```console
$ docker pull spiped@sha256:67bf8a15d391a12bf880bede827f884530e7cb5b7197db6b4f6c256bed6f8205
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3599402 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c942d42ae3b8e3004d46bf3408c8fe7f7893f60f5c91c514931f39789491c9a3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-armhf.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
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
	-	`sha256:06bab5e847c5674d6ec26b342cc11d7a051a6a231e5db8a955d57bc9f4ab5595`  
		Last Modified: Tue, 15 Jul 2025 18:59:34 GMT  
		Size: 3.5 MB (3500910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10c249d32301274a396c4398f0f9ad3e25d11b9387b71935548f7746004176c0`  
		Last Modified: Mon, 11 Aug 2025 17:07:08 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21acf12f5fa85d243eec713f52367aa2fc9fd58ece745d522619070ee2d91cfd`  
		Last Modified: Mon, 11 Aug 2025 17:07:12 GMT  
		Size: 7.9 KB (7949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:745a95091f37f0e3319bde964913fe0326b1767141fa6ccc002a3b8960025757`  
		Last Modified: Mon, 11 Aug 2025 17:07:15 GMT  
		Size: 89.2 KB (89159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c107fdd944f86a67e108331b416f8aa5deaef19c68a63ed23a8ba9ea0d3401d4`  
		Last Modified: Mon, 11 Aug 2025 17:07:17 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f42a92f540a8b148fc88f8e31cb9818a5f6618f8a1577e639ec0e24e38f9f7e`  
		Last Modified: Mon, 11 Aug 2025 17:07:20 GMT  
		Size: 336.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6.4-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:f93c76c9652d3a49aa974d58b6ae433e7cb36a7bfa83c6ac0d6cc254a7ba00c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.2 KB (14186 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9211c16e5ea9fc5d8cd82834f8cc184ea937fb23dc63d93b0f565174ccaf11e0`

```dockerfile
```

-	Layers:
	-	`sha256:bc75439704d889af0e27619c5682d57a42ab81be9ff4624f8a521f4377910696`  
		Last Modified: Mon, 11 Aug 2025 19:04:47 GMT  
		Size: 14.2 KB (14186 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6.4-alpine` - linux; arm variant v7

```console
$ docker pull spiped@sha256:9a4d893ec119af9bc7c0ac4cf7576f963e58abf3883a80df5a16e49b111c25aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3310043 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6ff0c9b1b65653155189d3026538aef9ad32adc4e50d92d8bd56011b77575eb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-armv7.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
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
	-	`sha256:5ee064f8764b09a64829b58705219a88e0b13243f7f403d66ac0c639640426a5`  
		Last Modified: Tue, 15 Jul 2025 19:04:18 GMT  
		Size: 3.2 MB (3219038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:379d666e2282d1ef67d78e68d7d1456eb01f968d2fb8812ac738eba6158a80e9`  
		Last Modified: Mon, 11 Aug 2025 17:12:34 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59c40f7a10d1200a7ded6eb02e6bd8fd18467fcf3ff34f0cf808a4cc55bed23e`  
		Last Modified: Mon, 11 Aug 2025 17:12:39 GMT  
		Size: 7.9 KB (7943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2b5dc976627c424732ee16c786a666f6c1bfc2753fb4eb45ba52b5363d0ddc5`  
		Last Modified: Mon, 11 Aug 2025 17:12:43 GMT  
		Size: 81.7 KB (81679 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:458721a616c9dc4cf600ca98211c375a8834644ed8ef7b186d3328ac28406eae`  
		Last Modified: Mon, 11 Aug 2025 17:12:48 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61e38052aca5003fd5a5a420dc69c7e09ad4a5c937a6fe99ce9562e631927208`  
		Last Modified: Mon, 11 Aug 2025 17:12:58 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6.4-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:b59043aa1ff63fcd31688fcd9d6a738aa113abdf366d458b93611854679ca46d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.6 KB (96629 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8456c8deda36f896666ee554249c53f1f1c44c53625d46df0b57b3ec07a8f90f`

```dockerfile
```

-	Layers:
	-	`sha256:604964ef49a1e639a8695215e5270aef4e51c3880d27e449bed0300fb49b10e2`  
		Last Modified: Mon, 11 Aug 2025 19:04:50 GMT  
		Size: 82.2 KB (82228 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3b749cfa2bb22f9f9bb0749d7930ddf6645b6ec8b6ff5ce281761785e69fe917`  
		Last Modified: Mon, 11 Aug 2025 19:04:51 GMT  
		Size: 14.4 KB (14401 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6.4-alpine` - linux; arm64 variant v8

```console
$ docker pull spiped@sha256:0aba08b25b408090092ccc3a2bfff93dd73cd53f1732f086bd5929af3a835323
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4240704 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c275338929556163beeba8cdd1efd28825491f472e207d35476d3569d9ee0e97`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-aarch64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
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
	-	`sha256:6e174226ea690ced550e5641249a412cdbefd2d09871f3e64ab52137a54ba606`  
		Last Modified: Tue, 15 Jul 2025 18:59:50 GMT  
		Size: 4.1 MB (4130750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:401e496ab6a7fec1ab1bb8f0b8a996b06c9fb697746e47439f58ec78714d57cb`  
		Last Modified: Mon, 11 Aug 2025 17:09:42 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc10c01537e03fed07cdd599b8a98a0adcfa5c06d0ba71c752ddf65d7ef18bd7`  
		Last Modified: Mon, 11 Aug 2025 17:09:45 GMT  
		Size: 8.0 KB (7951 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adfbfacdb4fddd486ebc3cf352ee0538e6eadf8b3033b6e12abdaf15234459c1`  
		Last Modified: Mon, 11 Aug 2025 17:09:48 GMT  
		Size: 100.6 KB (100617 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a7767630476c70a6cf95063bb707ffee6b4b40278b06fcdb17fa3f7dca8427b`  
		Last Modified: Mon, 11 Aug 2025 17:09:50 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25762649a73c36acce0fd48360b8be503aee4c1602f1a59b759cb8a795ab8c6b`  
		Last Modified: Mon, 11 Aug 2025 17:09:53 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6.4-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:5b477d36fe748f79631e7066c0574b5a9ca9e3e1c169c735e2a960cd0cea9d95
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.7 KB (96684 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6c2517fcfde44c5508a52e01d9e77e79db6fd3daad75c70853eb4b2b378a0ae`

```dockerfile
```

-	Layers:
	-	`sha256:1903a367ec2a9e9fbbee350246fe22b734d8bacdcfb9d34f695b231aa6f96ccd`  
		Last Modified: Mon, 11 Aug 2025 19:04:55 GMT  
		Size: 82.2 KB (82248 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6d54be9922b28101eb015c8900bf1221e9437578e72fce9654714c21b92c04d6`  
		Last Modified: Mon, 11 Aug 2025 19:04:56 GMT  
		Size: 14.4 KB (14436 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6.4-alpine` - linux; 386

```console
$ docker pull spiped@sha256:48537809d8133274a37ab69a836499fb8479383b5b69967228ce176ac6f1be60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3744445 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f9a0ea1f48b6cac9c7ce62d1260fd3fc9040cc58f686650da2fda4a116dfe2b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-x86.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
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
	-	`sha256:a55f2fb89da4caae0d783c0045a67446dee9bbd977fecb44db9e1231550fa888`  
		Last Modified: Tue, 15 Jul 2025 19:04:11 GMT  
		Size: 3.6 MB (3615006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3eba0b59a29857fdbd92df8627b53b15ba8b6ab4ec59021ee5712b80dfed882`  
		Last Modified: Mon, 11 Aug 2025 17:07:16 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:847779e3481b940532b586da8162b98cc75b9ca766b1f6e26d1622c3ed2d8ad1`  
		Last Modified: Mon, 11 Aug 2025 17:07:19 GMT  
		Size: 7.9 KB (7947 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84ead07d68c6f9280214b36ee65459f295af32fb5a83587a9d94ff34fbd8edf9`  
		Last Modified: Mon, 11 Aug 2025 17:07:22 GMT  
		Size: 120.1 KB (120108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbd0afa8d91fe587be8847df03da4b2cd7c73dbce722c78ea9606f83cbe408ae`  
		Last Modified: Mon, 11 Aug 2025 17:07:25 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18e699ee2bbb463e05c765e96679445315e788311982f0d542d6d6c513614f78`  
		Last Modified: Mon, 11 Aug 2025 17:07:31 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6.4-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:15f0f80fe34bd14b6d564b6e741552ba495ee58c3268d7ba1e7611e8f104298a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.4 KB (96433 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9ee4d0ec8becf51535d0fdeb2611b861926d3c65de73b970a6f07164630a189`

```dockerfile
```

-	Layers:
	-	`sha256:fa8d8def96807232c5de9a2689e639f51f6662c2960d1e6a13e5390c1ef5f875`  
		Last Modified: Mon, 11 Aug 2025 19:05:00 GMT  
		Size: 82.2 KB (82167 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:017908264a6caffecdaecbe817722cb1919c11d362589f17292a9cbd2d55c204`  
		Last Modified: Mon, 11 Aug 2025 19:05:00 GMT  
		Size: 14.3 KB (14266 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6.4-alpine` - linux; ppc64le

```console
$ docker pull spiped@sha256:79845ce442587e8a1743c515186951ae7603efaf08e38a0a7f4ce40a4af20597
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3849108 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04c74704274ad902930376019928ebde446c1deca3459f089066274bd8f1565c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-ppc64le.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
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
	-	`sha256:b762f678859bfa5c3948b5f1b04959aa43c8aba88e2389e281413d303d62a7e3`  
		Last Modified: Tue, 15 Jul 2025 18:59:53 GMT  
		Size: 3.7 MB (3727111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2373f01bf878f477a6cf1b4d56c9227ff43127b4d845c3562616e2a46d22dbdd`  
		Last Modified: Mon, 11 Aug 2025 17:13:12 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:427ad9317b0d6357fac90f31d124d5e9b36ee534067da2df12710b89392c781e`  
		Last Modified: Mon, 11 Aug 2025 17:13:15 GMT  
		Size: 7.9 KB (7948 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2f4f5c32876f7abc20796b83c3897652d454e319406eae7a6a6ed5d74ea44e3`  
		Last Modified: Mon, 11 Aug 2025 17:13:20 GMT  
		Size: 112.7 KB (112665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a9033716c014ce457c2d72e5e75fc8fa8044e87014da9f03f2fb489b825aef8`  
		Last Modified: Mon, 11 Aug 2025 17:13:26 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb03f1a2076f357e9cab2045b9652c20950ca5d8f7421f046896219b8532d06b`  
		Last Modified: Mon, 11 Aug 2025 17:13:29 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6.4-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:a6d8ce06cb0ab858ad3076a0f7a57f28f1e6ed5e17a4157b6b6a30ae37c3368a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.6 KB (94625 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b10d0bb2f5cfe8395a4519604c8ace1de04e74af97cc131cea9853a67b5fc2cc`

```dockerfile
```

-	Layers:
	-	`sha256:ff1c9c59d73d4c50497a06f04ad9a30428a99ad3de292bad5a2e9dd8d91d1160`  
		Last Modified: Mon, 11 Aug 2025 19:05:05 GMT  
		Size: 80.3 KB (80275 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e7e4e7f2cdbb149daeaca2e6e837f823a3641e8d4f0c3cf28a999579d17542cf`  
		Last Modified: Mon, 11 Aug 2025 19:05:05 GMT  
		Size: 14.3 KB (14350 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6.4-alpine` - linux; riscv64

```console
$ docker pull spiped@sha256:eb5294dab564ed0a45bac04aff4eb51d319f7c4fd6d0fe4eb457a283aceff474
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3620988 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83d8198608b9934495dc90c953cc87dfd83d7b1d0af22c216f3636508b77fd7b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-riscv64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
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
	-	`sha256:cbe7080b5783de104ad67ff4595bfa8ae70a597181a84621f51c5ccd084218da`  
		Last Modified: Tue, 15 Jul 2025 19:00:17 GMT  
		Size: 3.5 MB (3512801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:337ef438f7e589dc4f613c730fb4dd5a761abfd9e48d0d59495d3aff151e16ab`  
		Last Modified: Mon, 11 Aug 2025 17:12:32 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89b21db99ab142ddfd5ec4b8ef25065f37bc1aee36e94cad1db40698257cd6fc`  
		Last Modified: Mon, 11 Aug 2025 17:12:36 GMT  
		Size: 7.9 KB (7945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe3dc6909718e2eb82c7628f42d658b99dcdf7135cb7db460851920d41ad58c4`  
		Last Modified: Mon, 11 Aug 2025 17:12:40 GMT  
		Size: 98.9 KB (98856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:541a31d50d76446fd96c63516c67f098fad214976beea363002d79b73ba95d22`  
		Last Modified: Mon, 11 Aug 2025 17:12:44 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7db5851f3b8a32ba3d881649070f2380d838c65cb1f702ed418b43e640f03d7a`  
		Last Modified: Mon, 11 Aug 2025 17:12:47 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6.4-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:c32a8fd37856a4dfea8b91e0c18b79f0f43571bcac39779ab262c4c4741714be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.6 KB (94618 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c1f688a2498b96358ae65a439e4a1eda2bc0b14f90b0ec530106a28eb2077c4`

```dockerfile
```

-	Layers:
	-	`sha256:a3eaafb5380cff781fc2bfb357665fc4513231c31e349b37e3e7cc95f16b052b`  
		Last Modified: Mon, 11 Aug 2025 19:05:10 GMT  
		Size: 80.3 KB (80271 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:331b28e1546911de84609c9d63a3f86e0abca6d7efd8c9fa3d618f196a1ec42d`  
		Last Modified: Mon, 11 Aug 2025 19:05:10 GMT  
		Size: 14.3 KB (14347 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6.4-alpine` - linux; s390x

```console
$ docker pull spiped@sha256:1c717961a5e8cc5e8fd75141c21f0a6de58a68c44608450fa683029bae71c085
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3751251 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b744d847c43ddb5879abe90a22b110885a2c0ffb39ae4f72a3753f4e839db1a2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-s390x.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
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
	-	`sha256:5d29754ce036967079405405a04a54a7d3f8ba85e0057b6bdda3d03aa59c8361`  
		Last Modified: Tue, 15 Jul 2025 19:00:06 GMT  
		Size: 3.6 MB (3644971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e1bd137b03fbd1349d3ad3112f1e21d62c9baae0012a389da756b7ca6f932c7`  
		Last Modified: Mon, 11 Aug 2025 17:07:14 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a06802588e4666537f404a0ce19ebfc4da3850fd2dbe3536a4fe24380b4bc222`  
		Last Modified: Mon, 11 Aug 2025 17:07:18 GMT  
		Size: 8.0 KB (7950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f406fcd8d03a4ee6c2fc9bee5495de93682706f0ac21a261973b02e5cda0c93`  
		Last Modified: Mon, 11 Aug 2025 17:07:23 GMT  
		Size: 96.9 KB (96945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c48cae2c2a395f0f13d3dba276c545fd622a02bc6b9325ac1f1573447c6e90f`  
		Last Modified: Mon, 11 Aug 2025 17:07:27 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46bfce62ca5613c78d3504649bafb02ff12a44fa234e3dfc1134ece19652d3d7`  
		Last Modified: Mon, 11 Aug 2025 17:07:30 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6.4-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:654988790b7ed5b0441b8c38603d934b9706d4cccb2a3a9a96d8d3cc5f49c40a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.5 KB (94540 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a02880e0cbcf996ddd3d1c0bf389633fb423298a93ece41330d2f645d016566`

```dockerfile
```

-	Layers:
	-	`sha256:f77f4e4ec9383facda6fb5da7eeb5bf28f59fb80e6043ee4cb4eec3950e1422d`  
		Last Modified: Mon, 11 Aug 2025 19:05:14 GMT  
		Size: 80.2 KB (80241 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d27df7657b4c19b9a7071f58a7b58946289a2dc8ca2315c4bb0375dcfd961e1e`  
		Last Modified: Mon, 11 Aug 2025 19:05:15 GMT  
		Size: 14.3 KB (14299 bytes)  
		MIME: application/vnd.in-toto+json

## `spiped:alpine`

```console
$ docker pull spiped@sha256:93cdaab6e3b6d95ed76ddad7bf7f5c587c528e49ffabc2b79f6bd2aea6ab2630
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
$ docker pull spiped@sha256:fe36b545330b74e242df186f67f1842fc3f32a99ef52966ca731dc6982049707
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3916658 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36831aa20b12e50c7b388081fa2b93846f37a41dba1dad419cb49e1293706737`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
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
	-	`sha256:9824c27679d3b27c5e1cb00a73adb6f4f8d556994111c12db3c5d61a0c843df8`  
		Last Modified: Tue, 15 Jul 2025 19:00:01 GMT  
		Size: 3.8 MB (3799689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54f05db9f6c272f7847748f88394ce3bec41041589aaffb85ec57022932d41b6`  
		Last Modified: Mon, 11 Aug 2025 17:12:32 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3273c8db96783d1302ea2a8fb3345410d10a9076895cba46e68c6f063b28c3b`  
		Last Modified: Mon, 11 Aug 2025 17:02:16 GMT  
		Size: 7.9 KB (7946 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6034475a687587b7ef48917e52c9c773ca57a24867d18d0b4eba7762442608d`  
		Last Modified: Mon, 11 Aug 2025 17:02:19 GMT  
		Size: 107.6 KB (107643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28b778daf20a67a656800301303d05635c6c1b4b5aaf39563d66bcddafa96f82`  
		Last Modified: Mon, 11 Aug 2025 17:02:23 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2034aa0716ef0823cb7e0732cc466b480c6e7211047b7e791408e1b2e446969`  
		Last Modified: Mon, 11 Aug 2025 17:02:30 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:f6f21269d5900649987064943467fc128bbc3c34046bbe3f34413ca7c47a199c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.5 KB (96494 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dadc5ec1136521522c7efb5c32bb14f9ad6e983626c50c8bb0ca2df8a8baa064`

```dockerfile
```

-	Layers:
	-	`sha256:627d0194d2b11eccbaee3f5ef6edc22013a7b6093f562006c2fe85e88d07dc9e`  
		Last Modified: Mon, 11 Aug 2025 19:04:42 GMT  
		Size: 82.2 KB (82192 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7f278acc8a79ab1e0936e69a45aa893cb3e9050f2d6e52d3aa94b57021047e7e`  
		Last Modified: Mon, 11 Aug 2025 19:04:43 GMT  
		Size: 14.3 KB (14302 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:alpine` - linux; arm variant v6

```console
$ docker pull spiped@sha256:67bf8a15d391a12bf880bede827f884530e7cb5b7197db6b4f6c256bed6f8205
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3599402 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c942d42ae3b8e3004d46bf3408c8fe7f7893f60f5c91c514931f39789491c9a3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-armhf.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
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
	-	`sha256:06bab5e847c5674d6ec26b342cc11d7a051a6a231e5db8a955d57bc9f4ab5595`  
		Last Modified: Tue, 15 Jul 2025 18:59:34 GMT  
		Size: 3.5 MB (3500910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10c249d32301274a396c4398f0f9ad3e25d11b9387b71935548f7746004176c0`  
		Last Modified: Mon, 11 Aug 2025 17:07:08 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21acf12f5fa85d243eec713f52367aa2fc9fd58ece745d522619070ee2d91cfd`  
		Last Modified: Mon, 11 Aug 2025 17:07:12 GMT  
		Size: 7.9 KB (7949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:745a95091f37f0e3319bde964913fe0326b1767141fa6ccc002a3b8960025757`  
		Last Modified: Mon, 11 Aug 2025 17:07:15 GMT  
		Size: 89.2 KB (89159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c107fdd944f86a67e108331b416f8aa5deaef19c68a63ed23a8ba9ea0d3401d4`  
		Last Modified: Mon, 11 Aug 2025 17:07:17 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f42a92f540a8b148fc88f8e31cb9818a5f6618f8a1577e639ec0e24e38f9f7e`  
		Last Modified: Mon, 11 Aug 2025 17:07:20 GMT  
		Size: 336.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:f93c76c9652d3a49aa974d58b6ae433e7cb36a7bfa83c6ac0d6cc254a7ba00c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.2 KB (14186 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9211c16e5ea9fc5d8cd82834f8cc184ea937fb23dc63d93b0f565174ccaf11e0`

```dockerfile
```

-	Layers:
	-	`sha256:bc75439704d889af0e27619c5682d57a42ab81be9ff4624f8a521f4377910696`  
		Last Modified: Mon, 11 Aug 2025 19:04:47 GMT  
		Size: 14.2 KB (14186 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:alpine` - linux; arm variant v7

```console
$ docker pull spiped@sha256:9a4d893ec119af9bc7c0ac4cf7576f963e58abf3883a80df5a16e49b111c25aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3310043 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6ff0c9b1b65653155189d3026538aef9ad32adc4e50d92d8bd56011b77575eb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-armv7.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
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
	-	`sha256:5ee064f8764b09a64829b58705219a88e0b13243f7f403d66ac0c639640426a5`  
		Last Modified: Tue, 15 Jul 2025 19:04:18 GMT  
		Size: 3.2 MB (3219038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:379d666e2282d1ef67d78e68d7d1456eb01f968d2fb8812ac738eba6158a80e9`  
		Last Modified: Mon, 11 Aug 2025 17:12:34 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59c40f7a10d1200a7ded6eb02e6bd8fd18467fcf3ff34f0cf808a4cc55bed23e`  
		Last Modified: Mon, 11 Aug 2025 17:12:39 GMT  
		Size: 7.9 KB (7943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2b5dc976627c424732ee16c786a666f6c1bfc2753fb4eb45ba52b5363d0ddc5`  
		Last Modified: Mon, 11 Aug 2025 17:12:43 GMT  
		Size: 81.7 KB (81679 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:458721a616c9dc4cf600ca98211c375a8834644ed8ef7b186d3328ac28406eae`  
		Last Modified: Mon, 11 Aug 2025 17:12:48 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61e38052aca5003fd5a5a420dc69c7e09ad4a5c937a6fe99ce9562e631927208`  
		Last Modified: Mon, 11 Aug 2025 17:12:58 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:b59043aa1ff63fcd31688fcd9d6a738aa113abdf366d458b93611854679ca46d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.6 KB (96629 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8456c8deda36f896666ee554249c53f1f1c44c53625d46df0b57b3ec07a8f90f`

```dockerfile
```

-	Layers:
	-	`sha256:604964ef49a1e639a8695215e5270aef4e51c3880d27e449bed0300fb49b10e2`  
		Last Modified: Mon, 11 Aug 2025 19:04:50 GMT  
		Size: 82.2 KB (82228 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3b749cfa2bb22f9f9bb0749d7930ddf6645b6ec8b6ff5ce281761785e69fe917`  
		Last Modified: Mon, 11 Aug 2025 19:04:51 GMT  
		Size: 14.4 KB (14401 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:alpine` - linux; arm64 variant v8

```console
$ docker pull spiped@sha256:0aba08b25b408090092ccc3a2bfff93dd73cd53f1732f086bd5929af3a835323
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4240704 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c275338929556163beeba8cdd1efd28825491f472e207d35476d3569d9ee0e97`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-aarch64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
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
	-	`sha256:6e174226ea690ced550e5641249a412cdbefd2d09871f3e64ab52137a54ba606`  
		Last Modified: Tue, 15 Jul 2025 18:59:50 GMT  
		Size: 4.1 MB (4130750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:401e496ab6a7fec1ab1bb8f0b8a996b06c9fb697746e47439f58ec78714d57cb`  
		Last Modified: Mon, 11 Aug 2025 17:09:42 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc10c01537e03fed07cdd599b8a98a0adcfa5c06d0ba71c752ddf65d7ef18bd7`  
		Last Modified: Mon, 11 Aug 2025 17:09:45 GMT  
		Size: 8.0 KB (7951 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adfbfacdb4fddd486ebc3cf352ee0538e6eadf8b3033b6e12abdaf15234459c1`  
		Last Modified: Mon, 11 Aug 2025 17:09:48 GMT  
		Size: 100.6 KB (100617 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a7767630476c70a6cf95063bb707ffee6b4b40278b06fcdb17fa3f7dca8427b`  
		Last Modified: Mon, 11 Aug 2025 17:09:50 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25762649a73c36acce0fd48360b8be503aee4c1602f1a59b759cb8a795ab8c6b`  
		Last Modified: Mon, 11 Aug 2025 17:09:53 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:5b477d36fe748f79631e7066c0574b5a9ca9e3e1c169c735e2a960cd0cea9d95
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.7 KB (96684 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6c2517fcfde44c5508a52e01d9e77e79db6fd3daad75c70853eb4b2b378a0ae`

```dockerfile
```

-	Layers:
	-	`sha256:1903a367ec2a9e9fbbee350246fe22b734d8bacdcfb9d34f695b231aa6f96ccd`  
		Last Modified: Mon, 11 Aug 2025 19:04:55 GMT  
		Size: 82.2 KB (82248 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6d54be9922b28101eb015c8900bf1221e9437578e72fce9654714c21b92c04d6`  
		Last Modified: Mon, 11 Aug 2025 19:04:56 GMT  
		Size: 14.4 KB (14436 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:alpine` - linux; 386

```console
$ docker pull spiped@sha256:48537809d8133274a37ab69a836499fb8479383b5b69967228ce176ac6f1be60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3744445 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f9a0ea1f48b6cac9c7ce62d1260fd3fc9040cc58f686650da2fda4a116dfe2b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-x86.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
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
	-	`sha256:a55f2fb89da4caae0d783c0045a67446dee9bbd977fecb44db9e1231550fa888`  
		Last Modified: Tue, 15 Jul 2025 19:04:11 GMT  
		Size: 3.6 MB (3615006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3eba0b59a29857fdbd92df8627b53b15ba8b6ab4ec59021ee5712b80dfed882`  
		Last Modified: Mon, 11 Aug 2025 17:07:16 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:847779e3481b940532b586da8162b98cc75b9ca766b1f6e26d1622c3ed2d8ad1`  
		Last Modified: Mon, 11 Aug 2025 17:07:19 GMT  
		Size: 7.9 KB (7947 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84ead07d68c6f9280214b36ee65459f295af32fb5a83587a9d94ff34fbd8edf9`  
		Last Modified: Mon, 11 Aug 2025 17:07:22 GMT  
		Size: 120.1 KB (120108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbd0afa8d91fe587be8847df03da4b2cd7c73dbce722c78ea9606f83cbe408ae`  
		Last Modified: Mon, 11 Aug 2025 17:07:25 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18e699ee2bbb463e05c765e96679445315e788311982f0d542d6d6c513614f78`  
		Last Modified: Mon, 11 Aug 2025 17:07:31 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:15f0f80fe34bd14b6d564b6e741552ba495ee58c3268d7ba1e7611e8f104298a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.4 KB (96433 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9ee4d0ec8becf51535d0fdeb2611b861926d3c65de73b970a6f07164630a189`

```dockerfile
```

-	Layers:
	-	`sha256:fa8d8def96807232c5de9a2689e639f51f6662c2960d1e6a13e5390c1ef5f875`  
		Last Modified: Mon, 11 Aug 2025 19:05:00 GMT  
		Size: 82.2 KB (82167 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:017908264a6caffecdaecbe817722cb1919c11d362589f17292a9cbd2d55c204`  
		Last Modified: Mon, 11 Aug 2025 19:05:00 GMT  
		Size: 14.3 KB (14266 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:alpine` - linux; ppc64le

```console
$ docker pull spiped@sha256:79845ce442587e8a1743c515186951ae7603efaf08e38a0a7f4ce40a4af20597
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3849108 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04c74704274ad902930376019928ebde446c1deca3459f089066274bd8f1565c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-ppc64le.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
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
	-	`sha256:b762f678859bfa5c3948b5f1b04959aa43c8aba88e2389e281413d303d62a7e3`  
		Last Modified: Tue, 15 Jul 2025 18:59:53 GMT  
		Size: 3.7 MB (3727111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2373f01bf878f477a6cf1b4d56c9227ff43127b4d845c3562616e2a46d22dbdd`  
		Last Modified: Mon, 11 Aug 2025 17:13:12 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:427ad9317b0d6357fac90f31d124d5e9b36ee534067da2df12710b89392c781e`  
		Last Modified: Mon, 11 Aug 2025 17:13:15 GMT  
		Size: 7.9 KB (7948 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2f4f5c32876f7abc20796b83c3897652d454e319406eae7a6a6ed5d74ea44e3`  
		Last Modified: Mon, 11 Aug 2025 17:13:20 GMT  
		Size: 112.7 KB (112665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a9033716c014ce457c2d72e5e75fc8fa8044e87014da9f03f2fb489b825aef8`  
		Last Modified: Mon, 11 Aug 2025 17:13:26 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb03f1a2076f357e9cab2045b9652c20950ca5d8f7421f046896219b8532d06b`  
		Last Modified: Mon, 11 Aug 2025 17:13:29 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:a6d8ce06cb0ab858ad3076a0f7a57f28f1e6ed5e17a4157b6b6a30ae37c3368a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.6 KB (94625 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b10d0bb2f5cfe8395a4519604c8ace1de04e74af97cc131cea9853a67b5fc2cc`

```dockerfile
```

-	Layers:
	-	`sha256:ff1c9c59d73d4c50497a06f04ad9a30428a99ad3de292bad5a2e9dd8d91d1160`  
		Last Modified: Mon, 11 Aug 2025 19:05:05 GMT  
		Size: 80.3 KB (80275 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e7e4e7f2cdbb149daeaca2e6e837f823a3641e8d4f0c3cf28a999579d17542cf`  
		Last Modified: Mon, 11 Aug 2025 19:05:05 GMT  
		Size: 14.3 KB (14350 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:alpine` - linux; riscv64

```console
$ docker pull spiped@sha256:eb5294dab564ed0a45bac04aff4eb51d319f7c4fd6d0fe4eb457a283aceff474
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3620988 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83d8198608b9934495dc90c953cc87dfd83d7b1d0af22c216f3636508b77fd7b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-riscv64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
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
	-	`sha256:cbe7080b5783de104ad67ff4595bfa8ae70a597181a84621f51c5ccd084218da`  
		Last Modified: Tue, 15 Jul 2025 19:00:17 GMT  
		Size: 3.5 MB (3512801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:337ef438f7e589dc4f613c730fb4dd5a761abfd9e48d0d59495d3aff151e16ab`  
		Last Modified: Mon, 11 Aug 2025 17:12:32 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89b21db99ab142ddfd5ec4b8ef25065f37bc1aee36e94cad1db40698257cd6fc`  
		Last Modified: Mon, 11 Aug 2025 17:12:36 GMT  
		Size: 7.9 KB (7945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe3dc6909718e2eb82c7628f42d658b99dcdf7135cb7db460851920d41ad58c4`  
		Last Modified: Mon, 11 Aug 2025 17:12:40 GMT  
		Size: 98.9 KB (98856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:541a31d50d76446fd96c63516c67f098fad214976beea363002d79b73ba95d22`  
		Last Modified: Mon, 11 Aug 2025 17:12:44 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7db5851f3b8a32ba3d881649070f2380d838c65cb1f702ed418b43e640f03d7a`  
		Last Modified: Mon, 11 Aug 2025 17:12:47 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:c32a8fd37856a4dfea8b91e0c18b79f0f43571bcac39779ab262c4c4741714be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.6 KB (94618 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c1f688a2498b96358ae65a439e4a1eda2bc0b14f90b0ec530106a28eb2077c4`

```dockerfile
```

-	Layers:
	-	`sha256:a3eaafb5380cff781fc2bfb357665fc4513231c31e349b37e3e7cc95f16b052b`  
		Last Modified: Mon, 11 Aug 2025 19:05:10 GMT  
		Size: 80.3 KB (80271 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:331b28e1546911de84609c9d63a3f86e0abca6d7efd8c9fa3d618f196a1ec42d`  
		Last Modified: Mon, 11 Aug 2025 19:05:10 GMT  
		Size: 14.3 KB (14347 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:alpine` - linux; s390x

```console
$ docker pull spiped@sha256:1c717961a5e8cc5e8fd75141c21f0a6de58a68c44608450fa683029bae71c085
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3751251 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b744d847c43ddb5879abe90a22b110885a2c0ffb39ae4f72a3753f4e839db1a2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-s390x.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
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
	-	`sha256:5d29754ce036967079405405a04a54a7d3f8ba85e0057b6bdda3d03aa59c8361`  
		Last Modified: Tue, 15 Jul 2025 19:00:06 GMT  
		Size: 3.6 MB (3644971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e1bd137b03fbd1349d3ad3112f1e21d62c9baae0012a389da756b7ca6f932c7`  
		Last Modified: Mon, 11 Aug 2025 17:07:14 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a06802588e4666537f404a0ce19ebfc4da3850fd2dbe3536a4fe24380b4bc222`  
		Last Modified: Mon, 11 Aug 2025 17:07:18 GMT  
		Size: 8.0 KB (7950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f406fcd8d03a4ee6c2fc9bee5495de93682706f0ac21a261973b02e5cda0c93`  
		Last Modified: Mon, 11 Aug 2025 17:07:23 GMT  
		Size: 96.9 KB (96945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c48cae2c2a395f0f13d3dba276c545fd622a02bc6b9325ac1f1573447c6e90f`  
		Last Modified: Mon, 11 Aug 2025 17:07:27 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46bfce62ca5613c78d3504649bafb02ff12a44fa234e3dfc1134ece19652d3d7`  
		Last Modified: Mon, 11 Aug 2025 17:07:30 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:654988790b7ed5b0441b8c38603d934b9706d4cccb2a3a9a96d8d3cc5f49c40a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.5 KB (94540 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a02880e0cbcf996ddd3d1c0bf389633fb423298a93ece41330d2f645d016566`

```dockerfile
```

-	Layers:
	-	`sha256:f77f4e4ec9383facda6fb5da7eeb5bf28f59fb80e6043ee4cb4eec3950e1422d`  
		Last Modified: Mon, 11 Aug 2025 19:05:14 GMT  
		Size: 80.2 KB (80241 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d27df7657b4c19b9a7071f58a7b58946289a2dc8ca2315c4bb0375dcfd961e1e`  
		Last Modified: Mon, 11 Aug 2025 19:05:15 GMT  
		Size: 14.3 KB (14299 bytes)  
		MIME: application/vnd.in-toto+json

## `spiped:latest`

```console
$ docker pull spiped@sha256:393010ed037fbb2527e124feb16b874a82ef10ffbbc5b43c9ffc6f3f9bf449b4
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
$ docker pull spiped@sha256:bf92abd8857927a58bf60b37b751b45e7849904d0c3eb39428aa9ded13973b45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.8 MB (36823886 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:131dfb2d7b78cb541b4f99eb9752b00f874f76280458f7f2ed039e38a9886acc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Sun, 10 Aug 2025 19:01:23 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1754870400'
# Sun, 10 Aug 2025 19:01:23 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Sun, 10 Aug 2025 19:01:23 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 10 Aug 2025 19:01:23 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Sun, 10 Aug 2025 19:01:23 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Sun, 10 Aug 2025 19:01:23 GMT
VOLUME [/spiped]
# Sun, 10 Aug 2025 19:01:23 GMT
WORKDIR /spiped
# Sun, 10 Aug 2025 19:01:23 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 10 Aug 2025 19:01:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 10 Aug 2025 19:01:23 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:396b1da7636e2dcd10565cb4f2f952cbb4a8a38b58d3b86a2cacb172fb70117c`  
		Last Modified: Tue, 12 Aug 2025 20:45:08 GMT  
		Size: 29.8 MB (29773285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1960f8d044ed2918a9b63f9b23e244fc01996b6272a914c37ccd6d6dfcc68e4e`  
		Last Modified: Tue, 12 Aug 2025 22:33:32 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1429568f03b0485d02eb3e469fe20cdda6eb6e31f703b79f50834c7990b35868`  
		Last Modified: Tue, 12 Aug 2025 22:33:32 GMT  
		Size: 824.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f288333198193fd5d29806df7832431ab2cf3ad06e46a49c6dffea5d74eeeb7`  
		Last Modified: Tue, 12 Aug 2025 22:33:34 GMT  
		Size: 7.0 MB (7048236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f6a4df49d11a34ceed3269d89d6506916e2574f79c63ac88c6e45ce2067bb65`  
		Last Modified: Tue, 12 Aug 2025 22:33:32 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e299a1e4998ed061307241b9eb0eaf6d3f70b3dfa7c6b13aefce13c34f3e486a`  
		Last Modified: Tue, 12 Aug 2025 22:33:32 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:latest` - unknown; unknown

```console
$ docker pull spiped@sha256:06b0151f64cf465a20c4b3cf24d52eb8346bdf93c27fd53c814bb089ec4cb05a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3640248 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3aa7836e633ede2d640e4ee8a7f90afb38f97ad41e553c5088dc576ec98a1380`

```dockerfile
```

-	Layers:
	-	`sha256:049c8275986690c07daaa8af602e6e2eccaad28d023f774058df9cfbefbbaffe`  
		Last Modified: Wed, 13 Aug 2025 01:04:22 GMT  
		Size: 3.6 MB (3625230 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8ac5644f2c0e54bd96ba3c75290b8842a1d59415c4f6007a1540ee957de0ba98`  
		Last Modified: Wed, 13 Aug 2025 01:04:23 GMT  
		Size: 15.0 KB (15018 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:latest` - linux; arm variant v5

```console
$ docker pull spiped@sha256:3a8a3157e13515af48661b3359c74ad04e1a30456f7c560ae8f68e87a20ffb9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.9 MB (32910178 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dcbb748125f0b8dcd0fb6493ed4d870453d8c8efa012f4e2222c7dc2619a103a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 02 Apr 2025 21:12:22 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1753056000'
# Wed, 02 Apr 2025 21:12:22 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Wed, 02 Apr 2025 21:12:22 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
VOLUME [/spiped]
# Wed, 02 Apr 2025 21:12:22 GMT
WORKDIR /spiped
# Wed, 02 Apr 2025 21:12:22 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Apr 2025 21:12:22 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:70a0ce20524d4016d59550a3733a4080dc793deac81fcf6a038a61c9427611d7`  
		Last Modified: Tue, 22 Jul 2025 00:20:40 GMT  
		Size: 25.8 MB (25762716 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49046a4dd717e46f1d47e8b442ea16a32ae5c918851152c07d29a1ec56228f2a`  
		Last Modified: Tue, 22 Jul 2025 05:31:57 GMT  
		Size: 1.1 KB (1104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b15015636ae2d1e604b210604ec62efba4b52378febbaf8d104fdc747967525`  
		Last Modified: Tue, 22 Jul 2025 05:31:57 GMT  
		Size: 2.0 MB (1998288 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3147db3fa731dc64539822c647b65ed645104c05a5b5829ecb7b0ef27e85143`  
		Last Modified: Tue, 22 Jul 2025 05:31:57 GMT  
		Size: 5.1 MB (5147637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a27fdd8a658afb898909a24260e3428adae409d14c86ccd2e98c5e9c0ab7edc`  
		Last Modified: Tue, 22 Jul 2025 05:31:56 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d5c5f7070397c2858394d855108e31978aa74ffa73cbdd12b7200db8de2d441`  
		Last Modified: Tue, 22 Jul 2025 05:31:57 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:latest` - unknown; unknown

```console
$ docker pull spiped@sha256:772cf6016b094f52670a3487eacbd9f06e92145eb1e55a55b09fea0bf6aa9fdd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3617772 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c7e48cc724fee727a6693c57c4043d98e8bfac2f9242b3effde1720a1427492`

```dockerfile
```

-	Layers:
	-	`sha256:b510654d2a8c1b8ad052747c8ddb7e16c41356134db9be35752c35115580cfb1`  
		Last Modified: Tue, 22 Jul 2025 07:04:32 GMT  
		Size: 3.6 MB (3602631 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:471889e07393b6e3410d1d09003810c74afd93089e902abc26d07e1e0f8a2fce`  
		Last Modified: Tue, 22 Jul 2025 07:04:32 GMT  
		Size: 15.1 KB (15141 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:latest` - linux; arm variant v7

```console
$ docker pull spiped@sha256:df4a67cfc69545276ba2fa47893371e5bae16c16c7966f816afa7d6ff25c8030
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.7 MB (30685629 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3961f78e049e031a2d9c52600e014e09161ac256b60bb21f7765b25227de7da0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 02 Apr 2025 21:12:22 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1753056000'
# Wed, 02 Apr 2025 21:12:22 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Wed, 02 Apr 2025 21:12:22 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
VOLUME [/spiped]
# Wed, 02 Apr 2025 21:12:22 GMT
WORKDIR /spiped
# Wed, 02 Apr 2025 21:12:22 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Apr 2025 21:12:22 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:3d83c6df5858d91327bc312b738290e713ab4b6d4e0586c217399744d7596864`  
		Last Modified: Tue, 22 Jul 2025 00:20:36 GMT  
		Size: 23.9 MB (23938916 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe33cfed210711d85c4fb2b78824894f0d21979f013b4c59e595b535eda34fb6`  
		Last Modified: Tue, 22 Jul 2025 08:09:39 GMT  
		Size: 1.1 KB (1104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a5b5df2c8141fd6c1a420c98bbdfedda39b519cde600d577420f7822d64674e`  
		Last Modified: Tue, 22 Jul 2025 08:09:39 GMT  
		Size: 1.9 MB (1856406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8116bf27bbfb2abe4dad1a945819daa5184885a04be75e148bd91f3bab537924`  
		Last Modified: Tue, 22 Jul 2025 08:09:40 GMT  
		Size: 4.9 MB (4888769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae19946bd511763f4472e27df6f9f101f98a95a0b8e6b788beeb92d06694c152`  
		Last Modified: Tue, 22 Jul 2025 08:09:41 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcc6b3556f96d25cb1b9f9cfdc269be4883d98a05b63099eaa06187780ea70fc`  
		Last Modified: Tue, 22 Jul 2025 08:09:43 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:latest` - unknown; unknown

```console
$ docker pull spiped@sha256:0128ce934f586afb91aec29487355efccdefd76ccf4cce8344526da2947139c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3616955 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8dee0971e665b140b05d6053112c4d56d1111a6c474b6746e0bc68c030ecb23c`

```dockerfile
```

-	Layers:
	-	`sha256:2776f040304a973414de30d806031dbe4bb548df652c417d069b20a435fc3dd1`  
		Last Modified: Tue, 22 Jul 2025 10:07:08 GMT  
		Size: 3.6 MB (3601814 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:40b6ffb7b5108a7c93066348dec6008dc745f5e3d55e87ed73c96c7f2fb9cb03`  
		Last Modified: Tue, 22 Jul 2025 10:07:09 GMT  
		Size: 15.1 KB (15141 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:latest` - linux; arm64 variant v8

```console
$ docker pull spiped@sha256:e4096ff20583a5034e9280aeddf5f1a78923d9682609c199920f22185356b4fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.4 MB (36369792 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aff0f6bbb2c3ea404a50f705696846a93449e7bd0e783ad59d028a426200d382`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Sun, 10 Aug 2025 19:01:23 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1754870400'
# Sun, 10 Aug 2025 19:01:23 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Sun, 10 Aug 2025 19:01:23 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 10 Aug 2025 19:01:23 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Sun, 10 Aug 2025 19:01:23 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Sun, 10 Aug 2025 19:01:23 GMT
VOLUME [/spiped]
# Sun, 10 Aug 2025 19:01:23 GMT
WORKDIR /spiped
# Sun, 10 Aug 2025 19:01:23 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 10 Aug 2025 19:01:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 10 Aug 2025 19:01:23 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:9a6263cdeaa5d408640880103ee36920ef814974ca8e2674412ad6460e8968c9`  
		Last Modified: Tue, 12 Aug 2025 22:12:42 GMT  
		Size: 30.1 MB (30136044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af40190d6d264f1be66cb08049b70540eba02ba7fd655fae097cbda289746d53`  
		Last Modified: Wed, 13 Aug 2025 06:22:09 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:feabee456a6c96014e115867bd4e88b799f44b94e6c0b8d1b5000ec496955205`  
		Last Modified: Wed, 13 Aug 2025 06:22:09 GMT  
		Size: 827.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:422d0a380f226f779c85ec48dd7499a08ac0a2aa93252b6aa435fffccde8d8d2`  
		Last Modified: Wed, 13 Aug 2025 06:22:09 GMT  
		Size: 6.2 MB (6231378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a173632e46f201ec2b33805fcaf1d0c7df806b23f5e46a8c69672b6b4b565a4`  
		Last Modified: Wed, 13 Aug 2025 06:22:09 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bc1586a4e693693f7a15724dc111621e8887e469dd123083d647ceb15706ddf`  
		Last Modified: Wed, 13 Aug 2025 06:22:09 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:latest` - unknown; unknown

```console
$ docker pull spiped@sha256:034a8753ac823cfb19cac1a8b03a8fa42e7980f7937cba5bf7cfc01f4830a477
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3635418 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7286e08e8b96923d063eaa64527cb3cd08ca82cb07acf935f38efb0878583ba6`

```dockerfile
```

-	Layers:
	-	`sha256:bd5609020456c14f8bd5616333f26562e22aaf5d64128b39a58aa6d6c701dc9d`  
		Last Modified: Wed, 13 Aug 2025 10:06:23 GMT  
		Size: 3.6 MB (3620266 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d777d280a0314438cc074454754ca46996e21b39209485922e38a27cd2f5fe8d`  
		Last Modified: Wed, 13 Aug 2025 10:06:24 GMT  
		Size: 15.2 KB (15152 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:latest` - linux; 386

```console
$ docker pull spiped@sha256:9fcfe0c5b84d9fea6d266d29f18e4dbf8a226baeb085ca7ece3a8de5511e9c60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.7 MB (37733468 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a583f402afb8c7247d391e1083e23f97bbdcf159a97c7d203583d02d6b43500`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Sun, 10 Aug 2025 19:01:23 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1754870400'
# Sun, 10 Aug 2025 19:01:23 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Sun, 10 Aug 2025 19:01:23 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 10 Aug 2025 19:01:23 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Sun, 10 Aug 2025 19:01:23 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Sun, 10 Aug 2025 19:01:23 GMT
VOLUME [/spiped]
# Sun, 10 Aug 2025 19:01:23 GMT
WORKDIR /spiped
# Sun, 10 Aug 2025 19:01:23 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 10 Aug 2025 19:01:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 10 Aug 2025 19:01:23 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:346d0c953bdbc38917a27a6f30726e5b46419d98ecaf4d2d8f201bc3b7025e57`  
		Last Modified: Tue, 12 Aug 2025 20:45:00 GMT  
		Size: 31.3 MB (31289378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab0a9017881d45c9f4e65c372f685c6423638a8e38d92d57f8c3c99691cd7d31`  
		Last Modified: Tue, 12 Aug 2025 22:33:32 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:153819a4650c40b66474fb6dcc7d882e133f0147b067b5fc48010ae2bc8f46ba`  
		Last Modified: Tue, 12 Aug 2025 22:33:32 GMT  
		Size: 828.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a835563de046e9d403e7281f08ebf605249457ca98db2da529bd31f3fb191c68`  
		Last Modified: Tue, 12 Aug 2025 22:33:36 GMT  
		Size: 6.4 MB (6441722 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f06a8985faf5a44d315fbfa0d9975612e26c279004f7da7f8b48a116e66604c3`  
		Last Modified: Tue, 12 Aug 2025 22:33:32 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5ed637e18c93a4756562fbc235fbdf71a83fe6c2e508f6506bb9298bbf4d874`  
		Last Modified: Tue, 12 Aug 2025 22:33:32 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:latest` - unknown; unknown

```console
$ docker pull spiped@sha256:a22b73545c72bcc558012c681a7f3a323f62434624d93aed8a33f101a37fbf70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3634341 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9191c005b0e377ba838af7947a2eb39c66669632dcfdc9dab86f5a558b4a189`

```dockerfile
```

-	Layers:
	-	`sha256:b719e1d1247f7a8d2b2789312ebfb048bb173eedc1d0d8d7bd03213393393f7e`  
		Last Modified: Wed, 13 Aug 2025 01:04:39 GMT  
		Size: 3.6 MB (3619359 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dbc37a5a50f0a3198bced5718863ebd1123276e390992fd98e77602896183042`  
		Last Modified: Wed, 13 Aug 2025 01:04:40 GMT  
		Size: 15.0 KB (14982 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:latest` - linux; ppc64le

```console
$ docker pull spiped@sha256:c10b4ed278517ae49edfa7127c75c47dd1266e14633cd7f260e5c66298f1886b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.4 MB (40436468 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8248a22dee5275cedfd61db24cf28a136e1ec17f04c8aac3cad18755c6227de`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Sun, 10 Aug 2025 19:01:23 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1754870400'
# Sun, 10 Aug 2025 19:01:23 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Sun, 10 Aug 2025 19:01:23 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 10 Aug 2025 19:01:23 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Sun, 10 Aug 2025 19:01:23 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Sun, 10 Aug 2025 19:01:23 GMT
VOLUME [/spiped]
# Sun, 10 Aug 2025 19:01:23 GMT
WORKDIR /spiped
# Sun, 10 Aug 2025 19:01:23 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 10 Aug 2025 19:01:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 10 Aug 2025 19:01:23 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:52a4daa8724e9e1632306e15fe478aa26ff0ebcb7ba924cb168e9b6738c239d5`  
		Last Modified: Wed, 13 Aug 2025 01:42:36 GMT  
		Size: 33.6 MB (33594213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b31b56e1b56780df0e15411a668eb62bef22507f7082c36cbaa48e27b80a3dd`  
		Last Modified: Wed, 13 Aug 2025 11:56:38 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f93773dbbb14e44d116aaac13df032fbde418d4886ee8818b206f44616ba18c`  
		Last Modified: Wed, 13 Aug 2025 11:56:38 GMT  
		Size: 828.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1cba8a6190732e98166036b793666dec0711e36288c95969052f741b9f4561e`  
		Last Modified: Wed, 13 Aug 2025 11:56:39 GMT  
		Size: 6.8 MB (6839886 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e7c0065407c754b3de23aec850cf5698c61bd9ecd0c15fc936bb712345929e3`  
		Last Modified: Wed, 13 Aug 2025 11:56:38 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8565dc40120eabde33b3bc8ce9bc1fe16f2eea8e28f0298720ed08f9b970ed0d`  
		Last Modified: Wed, 13 Aug 2025 11:56:39 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:latest` - unknown; unknown

```console
$ docker pull spiped@sha256:43109fb7e5111756d35286a2c676e3530935deee3215367350f73c7717b0e368
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3636031 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45f14ba2c606d377446bf0e308bd47d6a3d8361c6adf29643758176bbed63bdf`

```dockerfile
```

-	Layers:
	-	`sha256:93dd80ad64b6ab11f964491d9b2edeb14431ec6735a30bc18db3663130f8056f`  
		Last Modified: Wed, 13 Aug 2025 13:04:36 GMT  
		Size: 3.6 MB (3620967 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:efa85ab4fe3aac389b61e3250282df7fdb0c361d597e0dd102c965020f2cd7f0`  
		Last Modified: Wed, 13 Aug 2025 13:04:37 GMT  
		Size: 15.1 KB (15064 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:latest` - linux; riscv64

```console
$ docker pull spiped@sha256:b8736517f7bb59c511ea4f9ad8a7b005ade95874aac45851c1047a628ec0e53d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.6 MB (37631700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:441b458a8e084c25a772f75f188b539784eb4e7a9c4aceb0f7d4ab836ef01505`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Sun, 10 Aug 2025 19:01:23 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1754870400'
# Sun, 10 Aug 2025 19:01:23 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Sun, 10 Aug 2025 19:01:23 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 10 Aug 2025 19:01:23 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Sun, 10 Aug 2025 19:01:23 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Sun, 10 Aug 2025 19:01:23 GMT
VOLUME [/spiped]
# Sun, 10 Aug 2025 19:01:23 GMT
WORKDIR /spiped
# Sun, 10 Aug 2025 19:01:23 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 10 Aug 2025 19:01:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 10 Aug 2025 19:01:23 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:a37386b9234ad75f65b5aa72f3d919ff0eb3bb18978566fa959d6e357480594c`  
		Last Modified: Wed, 13 Aug 2025 04:01:43 GMT  
		Size: 28.3 MB (28271623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:127ab5460053be42a858239f06c9bdf9bb20e426f59634680dd0952a062febe4`  
		Last Modified: Thu, 14 Aug 2025 14:39:42 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09fbdf3ef389fcfcfcde8edb7a990d48a50bb6562d381638a40a276632d2f2cb`  
		Last Modified: Thu, 14 Aug 2025 14:39:42 GMT  
		Size: 821.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e240e5ce18b11abe9700a80ae6196ee291094f1348bd44a0b4075b3d94f921d`  
		Last Modified: Thu, 14 Aug 2025 14:39:43 GMT  
		Size: 9.4 MB (9357715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b48ce987df3197aa7fa59932f4358de18054e75c420dd112aee00373e12d27e`  
		Last Modified: Thu, 14 Aug 2025 14:39:42 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2668076a38889d3caa1e8ef93527b7bcb09e1c8efde0333842323d9d6886d52`  
		Last Modified: Thu, 14 Aug 2025 14:39:43 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:latest` - unknown; unknown

```console
$ docker pull spiped@sha256:35913cc3f9fbe2375dbded2db7c773c530af42658aedbb3c8c1091268ab132c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3627439 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28abdef5a89cde265387c1c474ff08401948f48a3a2ad1431ed385b67b9e7e21`

```dockerfile
```

-	Layers:
	-	`sha256:a99c608ee95dedeefc4afd8c5d5002110953819bdd4bfc69f30503d9f7b29d9b`  
		Last Modified: Thu, 14 Aug 2025 16:04:41 GMT  
		Size: 3.6 MB (3612373 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:62f5c0922fff6e0c5c082f975db2470f90964d11fe3ed095088a38dc476c6df5`  
		Last Modified: Thu, 14 Aug 2025 16:04:42 GMT  
		Size: 15.1 KB (15066 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:latest` - linux; s390x

```console
$ docker pull spiped@sha256:77f28ec69d006b6ee6c4039b94cd23ed250849a792bcd153225cf7caaf0622b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.0 MB (35956075 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58c75aba82b1c983aca3ad0a5a3e6e29eba90da29cbb7e000e07c4ddbbf457ef`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Sun, 10 Aug 2025 19:01:23 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1754870400'
# Sun, 10 Aug 2025 19:01:23 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Sun, 10 Aug 2025 19:01:23 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 10 Aug 2025 19:01:23 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Sun, 10 Aug 2025 19:01:23 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Sun, 10 Aug 2025 19:01:23 GMT
VOLUME [/spiped]
# Sun, 10 Aug 2025 19:01:23 GMT
WORKDIR /spiped
# Sun, 10 Aug 2025 19:01:23 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 10 Aug 2025 19:01:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 10 Aug 2025 19:01:23 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:bfe4d60a27c9392ab729f16b50a763cda36622d744066c3cf029a072133f2907`  
		Last Modified: Tue, 12 Aug 2025 20:59:52 GMT  
		Size: 29.8 MB (29833057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9c626e6797dd4ed7e04641af5c80facb561257332e487c827a1ef8e5abfd9da`  
		Last Modified: Wed, 13 Aug 2025 03:13:05 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9900aed129749b40b135a4bf95bf318aaf8af8baa7324644aa65625a3d451004`  
		Last Modified: Wed, 13 Aug 2025 03:13:06 GMT  
		Size: 830.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f181815f0f2b1a7c15bd8cac9719565f616355c0b414c8b75cebeb1e47fc8407`  
		Last Modified: Wed, 13 Aug 2025 03:13:07 GMT  
		Size: 6.1 MB (6120648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba136bfaf44029a3c3e626051e20473fa8506b40643868e01503bb9f8fa7efa7`  
		Last Modified: Wed, 13 Aug 2025 03:13:07 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d75d2357fb8504e89d6cd5f62c3ba8bb87da5071bdb36e6ea261cfedca4f775`  
		Last Modified: Wed, 13 Aug 2025 03:13:07 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:latest` - unknown; unknown

```console
$ docker pull spiped@sha256:857963cc998457b693ce1f587d4d49b1e5025fe31ab7b0f7716489ee3e88d128
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3632611 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:749730c63bce3f602d13204e410b4980e4a58c8837357f148bcf3b1b94536afb`

```dockerfile
```

-	Layers:
	-	`sha256:0053cd2920bef5559841359b3be4f662851ac0b991797140849707d6b1fbf038`  
		Last Modified: Wed, 13 Aug 2025 07:06:49 GMT  
		Size: 3.6 MB (3617593 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:61c3f86e4dbefc122f0101f397d596f2aaef357ec79760d163a5e5862bef6588`  
		Last Modified: Wed, 13 Aug 2025 07:06:49 GMT  
		Size: 15.0 KB (15018 bytes)  
		MIME: application/vnd.in-toto+json
