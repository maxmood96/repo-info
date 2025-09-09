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
$ docker pull spiped@sha256:b586e1d1671a5a4d482ce5b8df8966999d21558852b067628c0a48d8ed69ef6f
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
$ docker pull spiped@sha256:0e98723f217e68ca2774427cf116e7c7574aa09f9b9a18b5b21de176d28a4670
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.8 MB (36824172 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff0e5840319ad5219238c791c630509e8c30be1096a1b99e5592cd7030b7950f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Fri, 29 Aug 2025 17:20:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1757289600'
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
	-	`sha256:ce1261c6d567efa8e3b457673eeeb474a0a8066df6bb95ca9a6a94a31e219dd3`  
		Last Modified: Mon, 08 Sep 2025 21:12:35 GMT  
		Size: 29.8 MB (29773495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3570ca07452dc62dc94984a1c13acf3398d82c2880023c457b6cb3d263d5cda4`  
		Last Modified: Mon, 08 Sep 2025 21:42:46 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a4b482011ba954768f0d6a90985562074facde0be6173ae854bff1c14e6c756`  
		Last Modified: Mon, 08 Sep 2025 21:42:50 GMT  
		Size: 823.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6c80701e3504f6e412af3c2019a5e39a7734041a9a002b66a85bf80ad7c1181`  
		Last Modified: Mon, 08 Sep 2025 22:09:01 GMT  
		Size: 7.0 MB (7048316 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b764e75de60d7ac3c81edb39aa029be7569c5c413c5cc9ba6827dfeb471ed4f5`  
		Last Modified: Mon, 08 Sep 2025 21:43:01 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e517e7196c838fac3308c6407fedd9c1f1beb666f298cc7ec073e71b40c851d5`  
		Last Modified: Mon, 08 Sep 2025 21:43:05 GMT  
		Size: 336.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1` - unknown; unknown

```console
$ docker pull spiped@sha256:b501f289010fc927fff92c3202a83d284fdcf366995b9947313c156436f212c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3641103 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6387d422edbc7148dcfdfd6b3a5c24c748e0ea407bf8c1907759c80e07e81b57`

```dockerfile
```

-	Layers:
	-	`sha256:0f274709f88dd5dd45c593c4ed6dd585dbb78216b8ab4109fd19afe2f352d762`  
		Last Modified: Mon, 08 Sep 2025 22:04:31 GMT  
		Size: 3.6 MB (3626078 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b30c4de1e7317d116582b0e3e56ec6a4f52f04e6879e73bfee6bc10651007778`  
		Last Modified: Mon, 08 Sep 2025 22:04:32 GMT  
		Size: 15.0 KB (15025 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1` - linux; arm variant v5

```console
$ docker pull spiped@sha256:2be3786a15bc910ea972ecd811dd4a953bfceb940bff8f5bfa2daec9e488f71c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.7 MB (33733472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c506215bfe7412857fcca1d71cedc4de07c3af973f2895cf7313ee033274349`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Fri, 29 Aug 2025 17:20:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1757289600'
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
	-	`sha256:5d61fc20e756831552727f89a087e2b45b07dace604ad2cda0a2afa80ace388d`  
		Last Modified: Mon, 08 Sep 2025 21:13:29 GMT  
		Size: 27.9 MB (27941760 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2048a7797742deda4a2cad05375b6d113e9954cd71ca2b1c29b890b6ede8db56`  
		Last Modified: Mon, 08 Sep 2025 22:04:02 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0290870c9fd09735b9a1a14513ac5cbaba4f131c258757b90e0596512725687e`  
		Last Modified: Mon, 08 Sep 2025 22:04:06 GMT  
		Size: 833.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ac8541099751a00e29431eef23f987bc00549735209ce497c6b83ea34d01315`  
		Last Modified: Mon, 08 Sep 2025 22:28:18 GMT  
		Size: 5.8 MB (5789340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ae4c824bf9b61979a828809d5d5a417e33963d9824f988fbd3701381ae61e82`  
		Last Modified: Mon, 08 Sep 2025 22:04:10 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f319c861a951dddde13625b0698753da831f49126c96f1abce8385232fdb923`  
		Last Modified: Mon, 08 Sep 2025 22:04:14 GMT  
		Size: 336.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1` - unknown; unknown

```console
$ docker pull spiped@sha256:8337e80157647554c90537d86a37253c41b794f85ffa73ab90367849dac09134
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3634202 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:278446c0f2bf208b2238b94eb45c3cf122a66492598663f90f2ba83833dd3a5b`

```dockerfile
```

-	Layers:
	-	`sha256:a47de1c44f6e4184ee91c743b4ce1f377fdd734180d1e0a652c84b5fa906bfa4`  
		Last Modified: Mon, 08 Sep 2025 22:04:38 GMT  
		Size: 3.6 MB (3619072 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e94d87a927a69b6ac792670d12cb5ecae277dbb0a409b6a386ca2fdd5243dc50`  
		Last Modified: Mon, 08 Sep 2025 22:04:39 GMT  
		Size: 15.1 KB (15130 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1` - linux; arm variant v7

```console
$ docker pull spiped@sha256:55c1924462ce41de687f42e2603b9295efb3af2ea9416e2c25e3f9fdd34afb64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.8 MB (31794747 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b264184152b054bd80ca19a24fec1f4060c0f6c53fd9419139ce0187034c9cb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Fri, 29 Aug 2025 17:20:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1757289600'
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
	-	`sha256:c01338083e94735040ac705e73d3207fecb1a829de94334396239199538796bd`  
		Last Modified: Mon, 08 Sep 2025 21:13:56 GMT  
		Size: 26.2 MB (26207847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1135c42cd92801939fa6513bb162537bb967d875405841f452ae92aa019e5bfe`  
		Last Modified: Mon, 08 Sep 2025 22:16:32 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2df69bf0846187df4227a06f55de71273baee4d386ccb1f98bb6e74ad188874a`  
		Last Modified: Mon, 08 Sep 2025 22:16:38 GMT  
		Size: 827.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd1eed6b9285bafc18f4c963dbf92dff69f211d78afcc6e9f6e750147a8681f6`  
		Last Modified: Mon, 08 Sep 2025 22:49:33 GMT  
		Size: 5.6 MB (5584533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07a57a1b1c83bb1f19dbbd26fe2bceb4f92d9d7951f1f17fb60d28ca37cfbf8f`  
		Last Modified: Mon, 08 Sep 2025 22:16:41 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3755b9c4ec1e1535de44613e7ff33ce001f5799640318ceaf4187cd1dd428a0f`  
		Last Modified: Mon, 08 Sep 2025 22:16:44 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1` - unknown; unknown

```console
$ docker pull spiped@sha256:b96e349fb89eafa7400bb0137272e43e7aa3f42efcd87d166a136ad9b0e1e783
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3633324 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef3ecc4e0843e63369fdd1aea3d2a5e46f2f8f891f2a9660bd7b841c5078b335`

```dockerfile
```

-	Layers:
	-	`sha256:416818cdf08bf484514867f324a9c87f81b1fd4a826f731bd0b95c88d8c643d3`  
		Last Modified: Tue, 09 Sep 2025 01:04:25 GMT  
		Size: 3.6 MB (3618193 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bbc0b5538d2093419837cea2916b8e4b7473900ca2c1c5fcde6d183855056eaf`  
		Last Modified: Tue, 09 Sep 2025 01:04:26 GMT  
		Size: 15.1 KB (15131 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1` - linux; arm64 variant v8

```console
$ docker pull spiped@sha256:b30af9feecd6d2d3e060442d3a65f6e96ddfa1a80fed606c84c1f016a2e3ec98
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.4 MB (36370794 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4cd3ed48417c32b96cea00093023ea9133743c7d939098b1666f4dd6e5b6a44b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Fri, 29 Aug 2025 17:20:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1757289600'
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
	-	`sha256:b2feff975e6dd2ebaf182772fb9ee26274648387b061e821e0bb5026735dd094`  
		Last Modified: Mon, 08 Sep 2025 21:13:54 GMT  
		Size: 30.1 MB (30136631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf96c895c9ecb8c50b531abc85aae3b4e1618dd151bee2548e8f0f324a66d264`  
		Last Modified: Mon, 08 Sep 2025 22:08:07 GMT  
		Size: 1.1 KB (1105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d894fd8e76b8c24189989a2c4edcede7b07f861c7878d352bdfead93f052b114`  
		Last Modified: Mon, 08 Sep 2025 22:08:11 GMT  
		Size: 824.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:009c3a2ddeae00427400405aae3478f6145688b476d8e0a6332ec10033d0214a`  
		Last Modified: Mon, 08 Sep 2025 22:31:44 GMT  
		Size: 6.2 MB (6231800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:771b828e58dae600ab30ba08fd29c1f6999e6ad1e0046d8130cc9fb4dfa3230b`  
		Last Modified: Mon, 08 Sep 2025 22:08:16 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c538a87d62b081105d070718eebcabf29d31a37763736eaf01e7e57bd1aa4e2f`  
		Last Modified: Mon, 08 Sep 2025 22:08:19 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1` - unknown; unknown

```console
$ docker pull spiped@sha256:b4b6c21230283163829ba358f0011d55d69c385a2cba19fa01e97ee624229b25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3636273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec6ae267ebdb45e6c8daf2e30f3457f918cd0da29621862f41bb5f294d7e3142`

```dockerfile
```

-	Layers:
	-	`sha256:d5b5755081e9d83cc165f6f2f16af8973276b35a16325e5d6324b4fd57784cce`  
		Last Modified: Mon, 08 Sep 2025 22:04:50 GMT  
		Size: 3.6 MB (3621114 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:002e4f513e5bbf2214b3303f88fd4499f1622400a327fbe0721cf244a7d239ed`  
		Last Modified: Mon, 08 Sep 2025 22:04:51 GMT  
		Size: 15.2 KB (15159 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1` - linux; 386

```console
$ docker pull spiped@sha256:82171e0666e35ff746fbb4f2dfa2952132328bb53429717390797dbe93bfc17e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.7 MB (37734562 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f616dd7bbc1f42449fdc926a447f0d4328e9e133a475731c7460bb30db8c2b70`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Fri, 29 Aug 2025 17:20:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1757289600'
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
	-	`sha256:d6e01c57fc6d674eef68e6bfe57a080b0a70c1c25810b7d6e769151bad3645bf`  
		Last Modified: Mon, 08 Sep 2025 21:12:32 GMT  
		Size: 31.3 MB (31289784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9fbcdd1371662f71ddb2b23df80fbf351b005debab82aafc902262981ba08ab`  
		Last Modified: Mon, 08 Sep 2025 21:57:17 GMT  
		Size: 1.1 KB (1104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85701ac5b161301c0a05e4843ffa9727392f95db70819ce77c42c30226553c80`  
		Last Modified: Mon, 08 Sep 2025 21:57:19 GMT  
		Size: 827.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50bb5031c8241b37a2e696ec8db5c03b82b1bd1ee65904857cfe42b14fac04af`  
		Last Modified: Mon, 08 Sep 2025 21:57:22 GMT  
		Size: 6.4 MB (6442413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:934469e6381f737152de5a1b3f6dd1729b3784cf1f1bae109fe5d3529099a832`  
		Last Modified: Mon, 08 Sep 2025 21:57:15 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d17cd8e8171dbc807b1bedab727c5008a91341d002e8f731f019a7f1ed51f3d`  
		Last Modified: Mon, 08 Sep 2025 21:57:14 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1` - unknown; unknown

```console
$ docker pull spiped@sha256:dfafee5c17a53e878812bb4dff43ecef3eca0c87e52722ca1d7d2bfb87c6797a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3635196 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49def9b4fb17d9ed6e5081b5415496b65daf1abe47fecc43f29182d4729ceb85`

```dockerfile
```

-	Layers:
	-	`sha256:55fc616258ae4fd67f353ff39a69793c11ab295b8f55ee9a3b8a23db68bedd00`  
		Last Modified: Mon, 08 Sep 2025 22:04:56 GMT  
		Size: 3.6 MB (3620207 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8b3162a00f4793a413edfb2b0c0cac933355d8dc353782e0efb33e4bcd6a98f2`  
		Last Modified: Mon, 08 Sep 2025 22:04:57 GMT  
		Size: 15.0 KB (14989 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1` - linux; ppc64le

```console
$ docker pull spiped@sha256:dd0f2c26fba6d8f7e91efc7236bc5ae26c6c586ebafbf27ba67b05e7405c585a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.4 MB (40436895 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7da8485c8492a65bd7db4a06ef4be5e13fa36922e67991803bd5b1597ce5908d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Fri, 29 Aug 2025 17:20:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1757289600'
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
	-	`sha256:d11c44105444ef722eccd8c92c6b2fce9986e3274ba9b346e044a458c0425852`  
		Last Modified: Mon, 08 Sep 2025 22:03:02 GMT  
		Size: 33.6 MB (33594351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1ff6f5b89d4b84c15ed34cf42385122a4619cef97f26b3b00fcf1ce99826e4e`  
		Last Modified: Tue, 09 Sep 2025 02:16:11 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2147f6accb00e92c1eedf8f3e292138aa51f43b774e82dbf3d236cd25c7a6ef5`  
		Last Modified: Tue, 09 Sep 2025 02:16:12 GMT  
		Size: 827.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12b36c08f12f5edbb0ebb0705a1fcbf0751d18146517cd3eac584f7a0e0e7db3`  
		Last Modified: Tue, 09 Sep 2025 02:16:10 GMT  
		Size: 6.8 MB (6840177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69c16bd3132d22ed6e04816499858f07b1a6caecb5e593723f22e1c664fd2504`  
		Last Modified: Tue, 09 Sep 2025 02:16:13 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbcf4a0a26c7a4eb0cae2a7bc2b099ccdd386daa17a0388ccc953332ef162ba9`  
		Last Modified: Tue, 09 Sep 2025 02:16:11 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1` - unknown; unknown

```console
$ docker pull spiped@sha256:fdddf2e236221e21497abda9439774a7dfa99c89501e1f61344f91f288ac160b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3636888 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cc8e6b9798028e08951fd7894a1176bc5de4172976f59bbb7d7a99a1fb24470`

```dockerfile
```

-	Layers:
	-	`sha256:cd3e3f7f121b597b3ae88011a5350cf0229bae2285264b9e515b5f46f48a7b9f`  
		Last Modified: Tue, 09 Sep 2025 04:04:37 GMT  
		Size: 3.6 MB (3621815 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:561d39bebbd3a77be83f987074591f029589166e840124add7a2af8871dbfa2d`  
		Last Modified: Tue, 09 Sep 2025 04:04:38 GMT  
		Size: 15.1 KB (15073 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1` - linux; riscv64

```console
$ docker pull spiped@sha256:3b3676cb2123fc9a1e4c327fa70e1857a75050bf33a275e9bd1d802151bcec4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.6 MB (37631686 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:640570b0b3bda692dcea0827850a72c5b2ee0b43583c995c0eb457af9a193f55`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1754870400'
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
	-	`sha256:a37386b9234ad75f65b5aa72f3d919ff0eb3bb18978566fa959d6e357480594c`  
		Last Modified: Wed, 13 Aug 2025 04:01:43 GMT  
		Size: 28.3 MB (28271623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf45ba83e1202bc173e329dc23766a0c3b8f738706ea301cda047e1348826c8b`  
		Last Modified: Mon, 01 Sep 2025 16:51:10 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1289b217d2c4a16ddbd2b4d846971cedbfc1a799389778f50d60a1036fc024a6`  
		Last Modified: Mon, 01 Sep 2025 16:51:10 GMT  
		Size: 825.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5c4f37ceddaefd5451a85453565dcee0f13860226efd805bc8c2dc3ae8ccd14`  
		Last Modified: Mon, 01 Sep 2025 16:51:10 GMT  
		Size: 9.4 MB (9357695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee843d99237854181305ecdd766749ac1bbb3e3bcd47e8b414a85a011862653c`  
		Last Modified: Mon, 01 Sep 2025 16:51:10 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0dc22da2f4339a139638305ec66c0783e946b8f0adff62530e43d73c487e5bd`  
		Last Modified: Mon, 01 Sep 2025 16:51:10 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1` - unknown; unknown

```console
$ docker pull spiped@sha256:35e5912a111ea507f93a7e0032bc1b2e8da82b06019cc75a58da48d7eb2e91b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3627446 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6bd2db2812e5fef7854b1d160553111506105875f89f941b7f315d71501d78f`

```dockerfile
```

-	Layers:
	-	`sha256:805bcf15f820505976cb5a30bf72471359a5fca4131aba384f3584599ddb7045`  
		Last Modified: Mon, 01 Sep 2025 19:04:42 GMT  
		Size: 3.6 MB (3612373 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cbd40f85e785916c7ddb424fb3a8f9a0b9545ec9ab0a04ea5ea5dc326ba8a2b5`  
		Last Modified: Mon, 01 Sep 2025 19:04:43 GMT  
		Size: 15.1 KB (15073 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1` - linux; s390x

```console
$ docker pull spiped@sha256:f43d82c5a3d35f6ce2cddbdf9ec0205301960afbde878d2ca5a7861df01aeb4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.0 MB (35956343 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d59764c7f98b190c53b1f7bc6dd3b9098f2d767322d48956bd085d7b071c49c9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Fri, 29 Aug 2025 17:20:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1757289600'
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
	-	`sha256:8af003c0cb712f415b555d33f1c4a9cc3fad82782766d388f3426c4d807a5ab2`  
		Last Modified: Mon, 08 Sep 2025 21:53:51 GMT  
		Size: 29.8 MB (29832904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2763f4a4daec888c7d63b0e0ff81db10dadc52fb53a435fa22ae03ee5decf09a`  
		Last Modified: Tue, 09 Sep 2025 00:21:56 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5161d34bcac535a56ad8efb0d748f8b339da9725c091b74f67c1823ec2bb58d9`  
		Last Modified: Tue, 09 Sep 2025 00:21:59 GMT  
		Size: 827.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b4a51a796aa3aaf724cc5bbec39ecd4f3b9a5b8244e1af98a933025d02f4ffd`  
		Last Modified: Tue, 09 Sep 2025 01:21:28 GMT  
		Size: 6.1 MB (6121071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa8daf184e635c2a7d701efea95606a1b0e8e8a2a745d9a541e956f2b0b71a39`  
		Last Modified: Tue, 09 Sep 2025 00:22:01 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90f4edae4a9a40914726f530d046af5b5b1f4e4c4048a15ee60f70e0ab94f709`  
		Last Modified: Tue, 09 Sep 2025 00:22:05 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1` - unknown; unknown

```console
$ docker pull spiped@sha256:def719779c2d7857b30da66a7a9f95579e191353a797ea6592ccef059ba709e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3633466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d10bf28afc205e156ee5a6abfde2d897204f3852cd6ba8108423663144fb84a9`

```dockerfile
```

-	Layers:
	-	`sha256:bab5214c083436ce496b531b010d96bf6ce4fc5d41d6254cd2944891972578bb`  
		Last Modified: Tue, 09 Sep 2025 04:04:44 GMT  
		Size: 3.6 MB (3618441 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0fc2bc9ff9441d9915eae99b2766d2b72f0d4aa3b4904864a6f976f52fceadeb`  
		Last Modified: Tue, 09 Sep 2025 04:04:46 GMT  
		Size: 15.0 KB (15025 bytes)  
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
$ docker pull spiped@sha256:b586e1d1671a5a4d482ce5b8df8966999d21558852b067628c0a48d8ed69ef6f
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
$ docker pull spiped@sha256:0e98723f217e68ca2774427cf116e7c7574aa09f9b9a18b5b21de176d28a4670
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.8 MB (36824172 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff0e5840319ad5219238c791c630509e8c30be1096a1b99e5592cd7030b7950f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Fri, 29 Aug 2025 17:20:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1757289600'
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
	-	`sha256:ce1261c6d567efa8e3b457673eeeb474a0a8066df6bb95ca9a6a94a31e219dd3`  
		Last Modified: Mon, 08 Sep 2025 21:12:35 GMT  
		Size: 29.8 MB (29773495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3570ca07452dc62dc94984a1c13acf3398d82c2880023c457b6cb3d263d5cda4`  
		Last Modified: Mon, 08 Sep 2025 21:42:46 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a4b482011ba954768f0d6a90985562074facde0be6173ae854bff1c14e6c756`  
		Last Modified: Mon, 08 Sep 2025 21:42:50 GMT  
		Size: 823.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6c80701e3504f6e412af3c2019a5e39a7734041a9a002b66a85bf80ad7c1181`  
		Last Modified: Mon, 08 Sep 2025 22:09:01 GMT  
		Size: 7.0 MB (7048316 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b764e75de60d7ac3c81edb39aa029be7569c5c413c5cc9ba6827dfeb471ed4f5`  
		Last Modified: Mon, 08 Sep 2025 21:43:01 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e517e7196c838fac3308c6407fedd9c1f1beb666f298cc7ec073e71b40c851d5`  
		Last Modified: Mon, 08 Sep 2025 21:43:05 GMT  
		Size: 336.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6` - unknown; unknown

```console
$ docker pull spiped@sha256:b501f289010fc927fff92c3202a83d284fdcf366995b9947313c156436f212c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3641103 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6387d422edbc7148dcfdfd6b3a5c24c748e0ea407bf8c1907759c80e07e81b57`

```dockerfile
```

-	Layers:
	-	`sha256:0f274709f88dd5dd45c593c4ed6dd585dbb78216b8ab4109fd19afe2f352d762`  
		Last Modified: Mon, 08 Sep 2025 22:04:31 GMT  
		Size: 3.6 MB (3626078 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b30c4de1e7317d116582b0e3e56ec6a4f52f04e6879e73bfee6bc10651007778`  
		Last Modified: Mon, 08 Sep 2025 22:04:32 GMT  
		Size: 15.0 KB (15025 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6` - linux; arm variant v5

```console
$ docker pull spiped@sha256:2be3786a15bc910ea972ecd811dd4a953bfceb940bff8f5bfa2daec9e488f71c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.7 MB (33733472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c506215bfe7412857fcca1d71cedc4de07c3af973f2895cf7313ee033274349`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Fri, 29 Aug 2025 17:20:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1757289600'
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
	-	`sha256:5d61fc20e756831552727f89a087e2b45b07dace604ad2cda0a2afa80ace388d`  
		Last Modified: Mon, 08 Sep 2025 21:13:29 GMT  
		Size: 27.9 MB (27941760 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2048a7797742deda4a2cad05375b6d113e9954cd71ca2b1c29b890b6ede8db56`  
		Last Modified: Mon, 08 Sep 2025 22:04:02 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0290870c9fd09735b9a1a14513ac5cbaba4f131c258757b90e0596512725687e`  
		Last Modified: Mon, 08 Sep 2025 22:04:06 GMT  
		Size: 833.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ac8541099751a00e29431eef23f987bc00549735209ce497c6b83ea34d01315`  
		Last Modified: Mon, 08 Sep 2025 22:28:18 GMT  
		Size: 5.8 MB (5789340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ae4c824bf9b61979a828809d5d5a417e33963d9824f988fbd3701381ae61e82`  
		Last Modified: Mon, 08 Sep 2025 22:04:10 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f319c861a951dddde13625b0698753da831f49126c96f1abce8385232fdb923`  
		Last Modified: Mon, 08 Sep 2025 22:04:14 GMT  
		Size: 336.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6` - unknown; unknown

```console
$ docker pull spiped@sha256:8337e80157647554c90537d86a37253c41b794f85ffa73ab90367849dac09134
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3634202 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:278446c0f2bf208b2238b94eb45c3cf122a66492598663f90f2ba83833dd3a5b`

```dockerfile
```

-	Layers:
	-	`sha256:a47de1c44f6e4184ee91c743b4ce1f377fdd734180d1e0a652c84b5fa906bfa4`  
		Last Modified: Mon, 08 Sep 2025 22:04:38 GMT  
		Size: 3.6 MB (3619072 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e94d87a927a69b6ac792670d12cb5ecae277dbb0a409b6a386ca2fdd5243dc50`  
		Last Modified: Mon, 08 Sep 2025 22:04:39 GMT  
		Size: 15.1 KB (15130 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6` - linux; arm variant v7

```console
$ docker pull spiped@sha256:55c1924462ce41de687f42e2603b9295efb3af2ea9416e2c25e3f9fdd34afb64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.8 MB (31794747 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b264184152b054bd80ca19a24fec1f4060c0f6c53fd9419139ce0187034c9cb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Fri, 29 Aug 2025 17:20:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1757289600'
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
	-	`sha256:c01338083e94735040ac705e73d3207fecb1a829de94334396239199538796bd`  
		Last Modified: Mon, 08 Sep 2025 21:13:56 GMT  
		Size: 26.2 MB (26207847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1135c42cd92801939fa6513bb162537bb967d875405841f452ae92aa019e5bfe`  
		Last Modified: Mon, 08 Sep 2025 22:16:32 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2df69bf0846187df4227a06f55de71273baee4d386ccb1f98bb6e74ad188874a`  
		Last Modified: Mon, 08 Sep 2025 22:16:38 GMT  
		Size: 827.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd1eed6b9285bafc18f4c963dbf92dff69f211d78afcc6e9f6e750147a8681f6`  
		Last Modified: Mon, 08 Sep 2025 22:49:33 GMT  
		Size: 5.6 MB (5584533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07a57a1b1c83bb1f19dbbd26fe2bceb4f92d9d7951f1f17fb60d28ca37cfbf8f`  
		Last Modified: Mon, 08 Sep 2025 22:16:41 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3755b9c4ec1e1535de44613e7ff33ce001f5799640318ceaf4187cd1dd428a0f`  
		Last Modified: Mon, 08 Sep 2025 22:16:44 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6` - unknown; unknown

```console
$ docker pull spiped@sha256:b96e349fb89eafa7400bb0137272e43e7aa3f42efcd87d166a136ad9b0e1e783
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3633324 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef3ecc4e0843e63369fdd1aea3d2a5e46f2f8f891f2a9660bd7b841c5078b335`

```dockerfile
```

-	Layers:
	-	`sha256:416818cdf08bf484514867f324a9c87f81b1fd4a826f731bd0b95c88d8c643d3`  
		Last Modified: Tue, 09 Sep 2025 01:04:25 GMT  
		Size: 3.6 MB (3618193 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bbc0b5538d2093419837cea2916b8e4b7473900ca2c1c5fcde6d183855056eaf`  
		Last Modified: Tue, 09 Sep 2025 01:04:26 GMT  
		Size: 15.1 KB (15131 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6` - linux; arm64 variant v8

```console
$ docker pull spiped@sha256:b30af9feecd6d2d3e060442d3a65f6e96ddfa1a80fed606c84c1f016a2e3ec98
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.4 MB (36370794 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4cd3ed48417c32b96cea00093023ea9133743c7d939098b1666f4dd6e5b6a44b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Fri, 29 Aug 2025 17:20:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1757289600'
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
	-	`sha256:b2feff975e6dd2ebaf182772fb9ee26274648387b061e821e0bb5026735dd094`  
		Last Modified: Mon, 08 Sep 2025 21:13:54 GMT  
		Size: 30.1 MB (30136631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf96c895c9ecb8c50b531abc85aae3b4e1618dd151bee2548e8f0f324a66d264`  
		Last Modified: Mon, 08 Sep 2025 22:08:07 GMT  
		Size: 1.1 KB (1105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d894fd8e76b8c24189989a2c4edcede7b07f861c7878d352bdfead93f052b114`  
		Last Modified: Mon, 08 Sep 2025 22:08:11 GMT  
		Size: 824.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:009c3a2ddeae00427400405aae3478f6145688b476d8e0a6332ec10033d0214a`  
		Last Modified: Mon, 08 Sep 2025 22:31:44 GMT  
		Size: 6.2 MB (6231800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:771b828e58dae600ab30ba08fd29c1f6999e6ad1e0046d8130cc9fb4dfa3230b`  
		Last Modified: Mon, 08 Sep 2025 22:08:16 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c538a87d62b081105d070718eebcabf29d31a37763736eaf01e7e57bd1aa4e2f`  
		Last Modified: Mon, 08 Sep 2025 22:08:19 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6` - unknown; unknown

```console
$ docker pull spiped@sha256:b4b6c21230283163829ba358f0011d55d69c385a2cba19fa01e97ee624229b25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3636273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec6ae267ebdb45e6c8daf2e30f3457f918cd0da29621862f41bb5f294d7e3142`

```dockerfile
```

-	Layers:
	-	`sha256:d5b5755081e9d83cc165f6f2f16af8973276b35a16325e5d6324b4fd57784cce`  
		Last Modified: Mon, 08 Sep 2025 22:04:50 GMT  
		Size: 3.6 MB (3621114 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:002e4f513e5bbf2214b3303f88fd4499f1622400a327fbe0721cf244a7d239ed`  
		Last Modified: Mon, 08 Sep 2025 22:04:51 GMT  
		Size: 15.2 KB (15159 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6` - linux; 386

```console
$ docker pull spiped@sha256:82171e0666e35ff746fbb4f2dfa2952132328bb53429717390797dbe93bfc17e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.7 MB (37734562 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f616dd7bbc1f42449fdc926a447f0d4328e9e133a475731c7460bb30db8c2b70`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Fri, 29 Aug 2025 17:20:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1757289600'
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
	-	`sha256:d6e01c57fc6d674eef68e6bfe57a080b0a70c1c25810b7d6e769151bad3645bf`  
		Last Modified: Mon, 08 Sep 2025 21:12:32 GMT  
		Size: 31.3 MB (31289784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9fbcdd1371662f71ddb2b23df80fbf351b005debab82aafc902262981ba08ab`  
		Last Modified: Mon, 08 Sep 2025 21:57:17 GMT  
		Size: 1.1 KB (1104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85701ac5b161301c0a05e4843ffa9727392f95db70819ce77c42c30226553c80`  
		Last Modified: Mon, 08 Sep 2025 21:57:19 GMT  
		Size: 827.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50bb5031c8241b37a2e696ec8db5c03b82b1bd1ee65904857cfe42b14fac04af`  
		Last Modified: Mon, 08 Sep 2025 21:57:22 GMT  
		Size: 6.4 MB (6442413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:934469e6381f737152de5a1b3f6dd1729b3784cf1f1bae109fe5d3529099a832`  
		Last Modified: Mon, 08 Sep 2025 21:57:15 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d17cd8e8171dbc807b1bedab727c5008a91341d002e8f731f019a7f1ed51f3d`  
		Last Modified: Mon, 08 Sep 2025 21:57:14 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6` - unknown; unknown

```console
$ docker pull spiped@sha256:dfafee5c17a53e878812bb4dff43ecef3eca0c87e52722ca1d7d2bfb87c6797a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3635196 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49def9b4fb17d9ed6e5081b5415496b65daf1abe47fecc43f29182d4729ceb85`

```dockerfile
```

-	Layers:
	-	`sha256:55fc616258ae4fd67f353ff39a69793c11ab295b8f55ee9a3b8a23db68bedd00`  
		Last Modified: Mon, 08 Sep 2025 22:04:56 GMT  
		Size: 3.6 MB (3620207 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8b3162a00f4793a413edfb2b0c0cac933355d8dc353782e0efb33e4bcd6a98f2`  
		Last Modified: Mon, 08 Sep 2025 22:04:57 GMT  
		Size: 15.0 KB (14989 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6` - linux; ppc64le

```console
$ docker pull spiped@sha256:dd0f2c26fba6d8f7e91efc7236bc5ae26c6c586ebafbf27ba67b05e7405c585a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.4 MB (40436895 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7da8485c8492a65bd7db4a06ef4be5e13fa36922e67991803bd5b1597ce5908d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Fri, 29 Aug 2025 17:20:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1757289600'
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
	-	`sha256:d11c44105444ef722eccd8c92c6b2fce9986e3274ba9b346e044a458c0425852`  
		Last Modified: Mon, 08 Sep 2025 22:03:02 GMT  
		Size: 33.6 MB (33594351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1ff6f5b89d4b84c15ed34cf42385122a4619cef97f26b3b00fcf1ce99826e4e`  
		Last Modified: Tue, 09 Sep 2025 02:16:11 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2147f6accb00e92c1eedf8f3e292138aa51f43b774e82dbf3d236cd25c7a6ef5`  
		Last Modified: Tue, 09 Sep 2025 02:16:12 GMT  
		Size: 827.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12b36c08f12f5edbb0ebb0705a1fcbf0751d18146517cd3eac584f7a0e0e7db3`  
		Last Modified: Tue, 09 Sep 2025 02:16:10 GMT  
		Size: 6.8 MB (6840177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69c16bd3132d22ed6e04816499858f07b1a6caecb5e593723f22e1c664fd2504`  
		Last Modified: Tue, 09 Sep 2025 02:16:13 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbcf4a0a26c7a4eb0cae2a7bc2b099ccdd386daa17a0388ccc953332ef162ba9`  
		Last Modified: Tue, 09 Sep 2025 02:16:11 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6` - unknown; unknown

```console
$ docker pull spiped@sha256:fdddf2e236221e21497abda9439774a7dfa99c89501e1f61344f91f288ac160b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3636888 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cc8e6b9798028e08951fd7894a1176bc5de4172976f59bbb7d7a99a1fb24470`

```dockerfile
```

-	Layers:
	-	`sha256:cd3e3f7f121b597b3ae88011a5350cf0229bae2285264b9e515b5f46f48a7b9f`  
		Last Modified: Tue, 09 Sep 2025 04:04:37 GMT  
		Size: 3.6 MB (3621815 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:561d39bebbd3a77be83f987074591f029589166e840124add7a2af8871dbfa2d`  
		Last Modified: Tue, 09 Sep 2025 04:04:38 GMT  
		Size: 15.1 KB (15073 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6` - linux; riscv64

```console
$ docker pull spiped@sha256:3b3676cb2123fc9a1e4c327fa70e1857a75050bf33a275e9bd1d802151bcec4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.6 MB (37631686 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:640570b0b3bda692dcea0827850a72c5b2ee0b43583c995c0eb457af9a193f55`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1754870400'
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
	-	`sha256:a37386b9234ad75f65b5aa72f3d919ff0eb3bb18978566fa959d6e357480594c`  
		Last Modified: Wed, 13 Aug 2025 04:01:43 GMT  
		Size: 28.3 MB (28271623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf45ba83e1202bc173e329dc23766a0c3b8f738706ea301cda047e1348826c8b`  
		Last Modified: Mon, 01 Sep 2025 16:51:10 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1289b217d2c4a16ddbd2b4d846971cedbfc1a799389778f50d60a1036fc024a6`  
		Last Modified: Mon, 01 Sep 2025 16:51:10 GMT  
		Size: 825.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5c4f37ceddaefd5451a85453565dcee0f13860226efd805bc8c2dc3ae8ccd14`  
		Last Modified: Mon, 01 Sep 2025 16:51:10 GMT  
		Size: 9.4 MB (9357695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee843d99237854181305ecdd766749ac1bbb3e3bcd47e8b414a85a011862653c`  
		Last Modified: Mon, 01 Sep 2025 16:51:10 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0dc22da2f4339a139638305ec66c0783e946b8f0adff62530e43d73c487e5bd`  
		Last Modified: Mon, 01 Sep 2025 16:51:10 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6` - unknown; unknown

```console
$ docker pull spiped@sha256:35e5912a111ea507f93a7e0032bc1b2e8da82b06019cc75a58da48d7eb2e91b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3627446 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6bd2db2812e5fef7854b1d160553111506105875f89f941b7f315d71501d78f`

```dockerfile
```

-	Layers:
	-	`sha256:805bcf15f820505976cb5a30bf72471359a5fca4131aba384f3584599ddb7045`  
		Last Modified: Mon, 01 Sep 2025 19:04:42 GMT  
		Size: 3.6 MB (3612373 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cbd40f85e785916c7ddb424fb3a8f9a0b9545ec9ab0a04ea5ea5dc326ba8a2b5`  
		Last Modified: Mon, 01 Sep 2025 19:04:43 GMT  
		Size: 15.1 KB (15073 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6` - linux; s390x

```console
$ docker pull spiped@sha256:f43d82c5a3d35f6ce2cddbdf9ec0205301960afbde878d2ca5a7861df01aeb4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.0 MB (35956343 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d59764c7f98b190c53b1f7bc6dd3b9098f2d767322d48956bd085d7b071c49c9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Fri, 29 Aug 2025 17:20:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1757289600'
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
	-	`sha256:8af003c0cb712f415b555d33f1c4a9cc3fad82782766d388f3426c4d807a5ab2`  
		Last Modified: Mon, 08 Sep 2025 21:53:51 GMT  
		Size: 29.8 MB (29832904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2763f4a4daec888c7d63b0e0ff81db10dadc52fb53a435fa22ae03ee5decf09a`  
		Last Modified: Tue, 09 Sep 2025 00:21:56 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5161d34bcac535a56ad8efb0d748f8b339da9725c091b74f67c1823ec2bb58d9`  
		Last Modified: Tue, 09 Sep 2025 00:21:59 GMT  
		Size: 827.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b4a51a796aa3aaf724cc5bbec39ecd4f3b9a5b8244e1af98a933025d02f4ffd`  
		Last Modified: Tue, 09 Sep 2025 01:21:28 GMT  
		Size: 6.1 MB (6121071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa8daf184e635c2a7d701efea95606a1b0e8e8a2a745d9a541e956f2b0b71a39`  
		Last Modified: Tue, 09 Sep 2025 00:22:01 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90f4edae4a9a40914726f530d046af5b5b1f4e4c4048a15ee60f70e0ab94f709`  
		Last Modified: Tue, 09 Sep 2025 00:22:05 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6` - unknown; unknown

```console
$ docker pull spiped@sha256:def719779c2d7857b30da66a7a9f95579e191353a797ea6592ccef059ba709e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3633466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d10bf28afc205e156ee5a6abfde2d897204f3852cd6ba8108423663144fb84a9`

```dockerfile
```

-	Layers:
	-	`sha256:bab5214c083436ce496b531b010d96bf6ce4fc5d41d6254cd2944891972578bb`  
		Last Modified: Tue, 09 Sep 2025 04:04:44 GMT  
		Size: 3.6 MB (3618441 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0fc2bc9ff9441d9915eae99b2766d2b72f0d4aa3b4904864a6f976f52fceadeb`  
		Last Modified: Tue, 09 Sep 2025 04:04:46 GMT  
		Size: 15.0 KB (15025 bytes)  
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
$ docker pull spiped@sha256:b586e1d1671a5a4d482ce5b8df8966999d21558852b067628c0a48d8ed69ef6f
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
$ docker pull spiped@sha256:0e98723f217e68ca2774427cf116e7c7574aa09f9b9a18b5b21de176d28a4670
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.8 MB (36824172 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff0e5840319ad5219238c791c630509e8c30be1096a1b99e5592cd7030b7950f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Fri, 29 Aug 2025 17:20:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1757289600'
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
	-	`sha256:ce1261c6d567efa8e3b457673eeeb474a0a8066df6bb95ca9a6a94a31e219dd3`  
		Last Modified: Mon, 08 Sep 2025 21:12:35 GMT  
		Size: 29.8 MB (29773495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3570ca07452dc62dc94984a1c13acf3398d82c2880023c457b6cb3d263d5cda4`  
		Last Modified: Mon, 08 Sep 2025 21:42:46 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a4b482011ba954768f0d6a90985562074facde0be6173ae854bff1c14e6c756`  
		Last Modified: Mon, 08 Sep 2025 21:42:50 GMT  
		Size: 823.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6c80701e3504f6e412af3c2019a5e39a7734041a9a002b66a85bf80ad7c1181`  
		Last Modified: Mon, 08 Sep 2025 22:09:01 GMT  
		Size: 7.0 MB (7048316 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b764e75de60d7ac3c81edb39aa029be7569c5c413c5cc9ba6827dfeb471ed4f5`  
		Last Modified: Mon, 08 Sep 2025 21:43:01 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e517e7196c838fac3308c6407fedd9c1f1beb666f298cc7ec073e71b40c851d5`  
		Last Modified: Mon, 08 Sep 2025 21:43:05 GMT  
		Size: 336.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6.4` - unknown; unknown

```console
$ docker pull spiped@sha256:b501f289010fc927fff92c3202a83d284fdcf366995b9947313c156436f212c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3641103 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6387d422edbc7148dcfdfd6b3a5c24c748e0ea407bf8c1907759c80e07e81b57`

```dockerfile
```

-	Layers:
	-	`sha256:0f274709f88dd5dd45c593c4ed6dd585dbb78216b8ab4109fd19afe2f352d762`  
		Last Modified: Mon, 08 Sep 2025 22:04:31 GMT  
		Size: 3.6 MB (3626078 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b30c4de1e7317d116582b0e3e56ec6a4f52f04e6879e73bfee6bc10651007778`  
		Last Modified: Mon, 08 Sep 2025 22:04:32 GMT  
		Size: 15.0 KB (15025 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6.4` - linux; arm variant v5

```console
$ docker pull spiped@sha256:2be3786a15bc910ea972ecd811dd4a953bfceb940bff8f5bfa2daec9e488f71c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.7 MB (33733472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c506215bfe7412857fcca1d71cedc4de07c3af973f2895cf7313ee033274349`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Fri, 29 Aug 2025 17:20:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1757289600'
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
	-	`sha256:5d61fc20e756831552727f89a087e2b45b07dace604ad2cda0a2afa80ace388d`  
		Last Modified: Mon, 08 Sep 2025 21:13:29 GMT  
		Size: 27.9 MB (27941760 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2048a7797742deda4a2cad05375b6d113e9954cd71ca2b1c29b890b6ede8db56`  
		Last Modified: Mon, 08 Sep 2025 22:04:02 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0290870c9fd09735b9a1a14513ac5cbaba4f131c258757b90e0596512725687e`  
		Last Modified: Mon, 08 Sep 2025 22:04:06 GMT  
		Size: 833.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ac8541099751a00e29431eef23f987bc00549735209ce497c6b83ea34d01315`  
		Last Modified: Mon, 08 Sep 2025 22:28:18 GMT  
		Size: 5.8 MB (5789340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ae4c824bf9b61979a828809d5d5a417e33963d9824f988fbd3701381ae61e82`  
		Last Modified: Mon, 08 Sep 2025 22:04:10 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f319c861a951dddde13625b0698753da831f49126c96f1abce8385232fdb923`  
		Last Modified: Mon, 08 Sep 2025 22:04:14 GMT  
		Size: 336.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6.4` - unknown; unknown

```console
$ docker pull spiped@sha256:8337e80157647554c90537d86a37253c41b794f85ffa73ab90367849dac09134
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3634202 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:278446c0f2bf208b2238b94eb45c3cf122a66492598663f90f2ba83833dd3a5b`

```dockerfile
```

-	Layers:
	-	`sha256:a47de1c44f6e4184ee91c743b4ce1f377fdd734180d1e0a652c84b5fa906bfa4`  
		Last Modified: Mon, 08 Sep 2025 22:04:38 GMT  
		Size: 3.6 MB (3619072 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e94d87a927a69b6ac792670d12cb5ecae277dbb0a409b6a386ca2fdd5243dc50`  
		Last Modified: Mon, 08 Sep 2025 22:04:39 GMT  
		Size: 15.1 KB (15130 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6.4` - linux; arm variant v7

```console
$ docker pull spiped@sha256:55c1924462ce41de687f42e2603b9295efb3af2ea9416e2c25e3f9fdd34afb64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.8 MB (31794747 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b264184152b054bd80ca19a24fec1f4060c0f6c53fd9419139ce0187034c9cb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Fri, 29 Aug 2025 17:20:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1757289600'
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
	-	`sha256:c01338083e94735040ac705e73d3207fecb1a829de94334396239199538796bd`  
		Last Modified: Mon, 08 Sep 2025 21:13:56 GMT  
		Size: 26.2 MB (26207847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1135c42cd92801939fa6513bb162537bb967d875405841f452ae92aa019e5bfe`  
		Last Modified: Mon, 08 Sep 2025 22:16:32 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2df69bf0846187df4227a06f55de71273baee4d386ccb1f98bb6e74ad188874a`  
		Last Modified: Mon, 08 Sep 2025 22:16:38 GMT  
		Size: 827.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd1eed6b9285bafc18f4c963dbf92dff69f211d78afcc6e9f6e750147a8681f6`  
		Last Modified: Mon, 08 Sep 2025 22:49:33 GMT  
		Size: 5.6 MB (5584533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07a57a1b1c83bb1f19dbbd26fe2bceb4f92d9d7951f1f17fb60d28ca37cfbf8f`  
		Last Modified: Mon, 08 Sep 2025 22:16:41 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3755b9c4ec1e1535de44613e7ff33ce001f5799640318ceaf4187cd1dd428a0f`  
		Last Modified: Mon, 08 Sep 2025 22:16:44 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6.4` - unknown; unknown

```console
$ docker pull spiped@sha256:b96e349fb89eafa7400bb0137272e43e7aa3f42efcd87d166a136ad9b0e1e783
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3633324 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef3ecc4e0843e63369fdd1aea3d2a5e46f2f8f891f2a9660bd7b841c5078b335`

```dockerfile
```

-	Layers:
	-	`sha256:416818cdf08bf484514867f324a9c87f81b1fd4a826f731bd0b95c88d8c643d3`  
		Last Modified: Tue, 09 Sep 2025 01:04:25 GMT  
		Size: 3.6 MB (3618193 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bbc0b5538d2093419837cea2916b8e4b7473900ca2c1c5fcde6d183855056eaf`  
		Last Modified: Tue, 09 Sep 2025 01:04:26 GMT  
		Size: 15.1 KB (15131 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6.4` - linux; arm64 variant v8

```console
$ docker pull spiped@sha256:b30af9feecd6d2d3e060442d3a65f6e96ddfa1a80fed606c84c1f016a2e3ec98
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.4 MB (36370794 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4cd3ed48417c32b96cea00093023ea9133743c7d939098b1666f4dd6e5b6a44b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Fri, 29 Aug 2025 17:20:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1757289600'
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
	-	`sha256:b2feff975e6dd2ebaf182772fb9ee26274648387b061e821e0bb5026735dd094`  
		Last Modified: Mon, 08 Sep 2025 21:13:54 GMT  
		Size: 30.1 MB (30136631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf96c895c9ecb8c50b531abc85aae3b4e1618dd151bee2548e8f0f324a66d264`  
		Last Modified: Mon, 08 Sep 2025 22:08:07 GMT  
		Size: 1.1 KB (1105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d894fd8e76b8c24189989a2c4edcede7b07f861c7878d352bdfead93f052b114`  
		Last Modified: Mon, 08 Sep 2025 22:08:11 GMT  
		Size: 824.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:009c3a2ddeae00427400405aae3478f6145688b476d8e0a6332ec10033d0214a`  
		Last Modified: Mon, 08 Sep 2025 22:31:44 GMT  
		Size: 6.2 MB (6231800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:771b828e58dae600ab30ba08fd29c1f6999e6ad1e0046d8130cc9fb4dfa3230b`  
		Last Modified: Mon, 08 Sep 2025 22:08:16 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c538a87d62b081105d070718eebcabf29d31a37763736eaf01e7e57bd1aa4e2f`  
		Last Modified: Mon, 08 Sep 2025 22:08:19 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6.4` - unknown; unknown

```console
$ docker pull spiped@sha256:b4b6c21230283163829ba358f0011d55d69c385a2cba19fa01e97ee624229b25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3636273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec6ae267ebdb45e6c8daf2e30f3457f918cd0da29621862f41bb5f294d7e3142`

```dockerfile
```

-	Layers:
	-	`sha256:d5b5755081e9d83cc165f6f2f16af8973276b35a16325e5d6324b4fd57784cce`  
		Last Modified: Mon, 08 Sep 2025 22:04:50 GMT  
		Size: 3.6 MB (3621114 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:002e4f513e5bbf2214b3303f88fd4499f1622400a327fbe0721cf244a7d239ed`  
		Last Modified: Mon, 08 Sep 2025 22:04:51 GMT  
		Size: 15.2 KB (15159 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6.4` - linux; 386

```console
$ docker pull spiped@sha256:82171e0666e35ff746fbb4f2dfa2952132328bb53429717390797dbe93bfc17e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.7 MB (37734562 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f616dd7bbc1f42449fdc926a447f0d4328e9e133a475731c7460bb30db8c2b70`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Fri, 29 Aug 2025 17:20:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1757289600'
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
	-	`sha256:d6e01c57fc6d674eef68e6bfe57a080b0a70c1c25810b7d6e769151bad3645bf`  
		Last Modified: Mon, 08 Sep 2025 21:12:32 GMT  
		Size: 31.3 MB (31289784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9fbcdd1371662f71ddb2b23df80fbf351b005debab82aafc902262981ba08ab`  
		Last Modified: Mon, 08 Sep 2025 21:57:17 GMT  
		Size: 1.1 KB (1104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85701ac5b161301c0a05e4843ffa9727392f95db70819ce77c42c30226553c80`  
		Last Modified: Mon, 08 Sep 2025 21:57:19 GMT  
		Size: 827.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50bb5031c8241b37a2e696ec8db5c03b82b1bd1ee65904857cfe42b14fac04af`  
		Last Modified: Mon, 08 Sep 2025 21:57:22 GMT  
		Size: 6.4 MB (6442413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:934469e6381f737152de5a1b3f6dd1729b3784cf1f1bae109fe5d3529099a832`  
		Last Modified: Mon, 08 Sep 2025 21:57:15 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d17cd8e8171dbc807b1bedab727c5008a91341d002e8f731f019a7f1ed51f3d`  
		Last Modified: Mon, 08 Sep 2025 21:57:14 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6.4` - unknown; unknown

```console
$ docker pull spiped@sha256:dfafee5c17a53e878812bb4dff43ecef3eca0c87e52722ca1d7d2bfb87c6797a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3635196 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49def9b4fb17d9ed6e5081b5415496b65daf1abe47fecc43f29182d4729ceb85`

```dockerfile
```

-	Layers:
	-	`sha256:55fc616258ae4fd67f353ff39a69793c11ab295b8f55ee9a3b8a23db68bedd00`  
		Last Modified: Mon, 08 Sep 2025 22:04:56 GMT  
		Size: 3.6 MB (3620207 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8b3162a00f4793a413edfb2b0c0cac933355d8dc353782e0efb33e4bcd6a98f2`  
		Last Modified: Mon, 08 Sep 2025 22:04:57 GMT  
		Size: 15.0 KB (14989 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6.4` - linux; ppc64le

```console
$ docker pull spiped@sha256:dd0f2c26fba6d8f7e91efc7236bc5ae26c6c586ebafbf27ba67b05e7405c585a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.4 MB (40436895 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7da8485c8492a65bd7db4a06ef4be5e13fa36922e67991803bd5b1597ce5908d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Fri, 29 Aug 2025 17:20:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1757289600'
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
	-	`sha256:d11c44105444ef722eccd8c92c6b2fce9986e3274ba9b346e044a458c0425852`  
		Last Modified: Mon, 08 Sep 2025 22:03:02 GMT  
		Size: 33.6 MB (33594351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1ff6f5b89d4b84c15ed34cf42385122a4619cef97f26b3b00fcf1ce99826e4e`  
		Last Modified: Tue, 09 Sep 2025 02:16:11 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2147f6accb00e92c1eedf8f3e292138aa51f43b774e82dbf3d236cd25c7a6ef5`  
		Last Modified: Tue, 09 Sep 2025 02:16:12 GMT  
		Size: 827.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12b36c08f12f5edbb0ebb0705a1fcbf0751d18146517cd3eac584f7a0e0e7db3`  
		Last Modified: Tue, 09 Sep 2025 02:16:10 GMT  
		Size: 6.8 MB (6840177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69c16bd3132d22ed6e04816499858f07b1a6caecb5e593723f22e1c664fd2504`  
		Last Modified: Tue, 09 Sep 2025 02:16:13 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbcf4a0a26c7a4eb0cae2a7bc2b099ccdd386daa17a0388ccc953332ef162ba9`  
		Last Modified: Tue, 09 Sep 2025 02:16:11 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6.4` - unknown; unknown

```console
$ docker pull spiped@sha256:fdddf2e236221e21497abda9439774a7dfa99c89501e1f61344f91f288ac160b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3636888 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cc8e6b9798028e08951fd7894a1176bc5de4172976f59bbb7d7a99a1fb24470`

```dockerfile
```

-	Layers:
	-	`sha256:cd3e3f7f121b597b3ae88011a5350cf0229bae2285264b9e515b5f46f48a7b9f`  
		Last Modified: Tue, 09 Sep 2025 04:04:37 GMT  
		Size: 3.6 MB (3621815 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:561d39bebbd3a77be83f987074591f029589166e840124add7a2af8871dbfa2d`  
		Last Modified: Tue, 09 Sep 2025 04:04:38 GMT  
		Size: 15.1 KB (15073 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6.4` - linux; riscv64

```console
$ docker pull spiped@sha256:3b3676cb2123fc9a1e4c327fa70e1857a75050bf33a275e9bd1d802151bcec4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.6 MB (37631686 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:640570b0b3bda692dcea0827850a72c5b2ee0b43583c995c0eb457af9a193f55`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1754870400'
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
	-	`sha256:a37386b9234ad75f65b5aa72f3d919ff0eb3bb18978566fa959d6e357480594c`  
		Last Modified: Wed, 13 Aug 2025 04:01:43 GMT  
		Size: 28.3 MB (28271623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf45ba83e1202bc173e329dc23766a0c3b8f738706ea301cda047e1348826c8b`  
		Last Modified: Mon, 01 Sep 2025 16:51:10 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1289b217d2c4a16ddbd2b4d846971cedbfc1a799389778f50d60a1036fc024a6`  
		Last Modified: Mon, 01 Sep 2025 16:51:10 GMT  
		Size: 825.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5c4f37ceddaefd5451a85453565dcee0f13860226efd805bc8c2dc3ae8ccd14`  
		Last Modified: Mon, 01 Sep 2025 16:51:10 GMT  
		Size: 9.4 MB (9357695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee843d99237854181305ecdd766749ac1bbb3e3bcd47e8b414a85a011862653c`  
		Last Modified: Mon, 01 Sep 2025 16:51:10 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0dc22da2f4339a139638305ec66c0783e946b8f0adff62530e43d73c487e5bd`  
		Last Modified: Mon, 01 Sep 2025 16:51:10 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6.4` - unknown; unknown

```console
$ docker pull spiped@sha256:35e5912a111ea507f93a7e0032bc1b2e8da82b06019cc75a58da48d7eb2e91b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3627446 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6bd2db2812e5fef7854b1d160553111506105875f89f941b7f315d71501d78f`

```dockerfile
```

-	Layers:
	-	`sha256:805bcf15f820505976cb5a30bf72471359a5fca4131aba384f3584599ddb7045`  
		Last Modified: Mon, 01 Sep 2025 19:04:42 GMT  
		Size: 3.6 MB (3612373 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cbd40f85e785916c7ddb424fb3a8f9a0b9545ec9ab0a04ea5ea5dc326ba8a2b5`  
		Last Modified: Mon, 01 Sep 2025 19:04:43 GMT  
		Size: 15.1 KB (15073 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6.4` - linux; s390x

```console
$ docker pull spiped@sha256:f43d82c5a3d35f6ce2cddbdf9ec0205301960afbde878d2ca5a7861df01aeb4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.0 MB (35956343 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d59764c7f98b190c53b1f7bc6dd3b9098f2d767322d48956bd085d7b071c49c9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Fri, 29 Aug 2025 17:20:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1757289600'
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
	-	`sha256:8af003c0cb712f415b555d33f1c4a9cc3fad82782766d388f3426c4d807a5ab2`  
		Last Modified: Mon, 08 Sep 2025 21:53:51 GMT  
		Size: 29.8 MB (29832904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2763f4a4daec888c7d63b0e0ff81db10dadc52fb53a435fa22ae03ee5decf09a`  
		Last Modified: Tue, 09 Sep 2025 00:21:56 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5161d34bcac535a56ad8efb0d748f8b339da9725c091b74f67c1823ec2bb58d9`  
		Last Modified: Tue, 09 Sep 2025 00:21:59 GMT  
		Size: 827.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b4a51a796aa3aaf724cc5bbec39ecd4f3b9a5b8244e1af98a933025d02f4ffd`  
		Last Modified: Tue, 09 Sep 2025 01:21:28 GMT  
		Size: 6.1 MB (6121071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa8daf184e635c2a7d701efea95606a1b0e8e8a2a745d9a541e956f2b0b71a39`  
		Last Modified: Tue, 09 Sep 2025 00:22:01 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90f4edae4a9a40914726f530d046af5b5b1f4e4c4048a15ee60f70e0ab94f709`  
		Last Modified: Tue, 09 Sep 2025 00:22:05 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6.4` - unknown; unknown

```console
$ docker pull spiped@sha256:def719779c2d7857b30da66a7a9f95579e191353a797ea6592ccef059ba709e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3633466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d10bf28afc205e156ee5a6abfde2d897204f3852cd6ba8108423663144fb84a9`

```dockerfile
```

-	Layers:
	-	`sha256:bab5214c083436ce496b531b010d96bf6ce4fc5d41d6254cd2944891972578bb`  
		Last Modified: Tue, 09 Sep 2025 04:04:44 GMT  
		Size: 3.6 MB (3618441 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0fc2bc9ff9441d9915eae99b2766d2b72f0d4aa3b4904864a6f976f52fceadeb`  
		Last Modified: Tue, 09 Sep 2025 04:04:46 GMT  
		Size: 15.0 KB (15025 bytes)  
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
$ docker pull spiped@sha256:b586e1d1671a5a4d482ce5b8df8966999d21558852b067628c0a48d8ed69ef6f
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
$ docker pull spiped@sha256:0e98723f217e68ca2774427cf116e7c7574aa09f9b9a18b5b21de176d28a4670
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.8 MB (36824172 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff0e5840319ad5219238c791c630509e8c30be1096a1b99e5592cd7030b7950f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Fri, 29 Aug 2025 17:20:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1757289600'
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
	-	`sha256:ce1261c6d567efa8e3b457673eeeb474a0a8066df6bb95ca9a6a94a31e219dd3`  
		Last Modified: Mon, 08 Sep 2025 21:12:35 GMT  
		Size: 29.8 MB (29773495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3570ca07452dc62dc94984a1c13acf3398d82c2880023c457b6cb3d263d5cda4`  
		Last Modified: Mon, 08 Sep 2025 21:42:46 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a4b482011ba954768f0d6a90985562074facde0be6173ae854bff1c14e6c756`  
		Last Modified: Mon, 08 Sep 2025 21:42:50 GMT  
		Size: 823.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6c80701e3504f6e412af3c2019a5e39a7734041a9a002b66a85bf80ad7c1181`  
		Last Modified: Mon, 08 Sep 2025 22:09:01 GMT  
		Size: 7.0 MB (7048316 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b764e75de60d7ac3c81edb39aa029be7569c5c413c5cc9ba6827dfeb471ed4f5`  
		Last Modified: Mon, 08 Sep 2025 21:43:01 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e517e7196c838fac3308c6407fedd9c1f1beb666f298cc7ec073e71b40c851d5`  
		Last Modified: Mon, 08 Sep 2025 21:43:05 GMT  
		Size: 336.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:latest` - unknown; unknown

```console
$ docker pull spiped@sha256:b501f289010fc927fff92c3202a83d284fdcf366995b9947313c156436f212c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3641103 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6387d422edbc7148dcfdfd6b3a5c24c748e0ea407bf8c1907759c80e07e81b57`

```dockerfile
```

-	Layers:
	-	`sha256:0f274709f88dd5dd45c593c4ed6dd585dbb78216b8ab4109fd19afe2f352d762`  
		Last Modified: Mon, 08 Sep 2025 22:04:31 GMT  
		Size: 3.6 MB (3626078 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b30c4de1e7317d116582b0e3e56ec6a4f52f04e6879e73bfee6bc10651007778`  
		Last Modified: Mon, 08 Sep 2025 22:04:32 GMT  
		Size: 15.0 KB (15025 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:latest` - linux; arm variant v5

```console
$ docker pull spiped@sha256:2be3786a15bc910ea972ecd811dd4a953bfceb940bff8f5bfa2daec9e488f71c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.7 MB (33733472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c506215bfe7412857fcca1d71cedc4de07c3af973f2895cf7313ee033274349`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Fri, 29 Aug 2025 17:20:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1757289600'
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
	-	`sha256:5d61fc20e756831552727f89a087e2b45b07dace604ad2cda0a2afa80ace388d`  
		Last Modified: Mon, 08 Sep 2025 21:13:29 GMT  
		Size: 27.9 MB (27941760 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2048a7797742deda4a2cad05375b6d113e9954cd71ca2b1c29b890b6ede8db56`  
		Last Modified: Mon, 08 Sep 2025 22:04:02 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0290870c9fd09735b9a1a14513ac5cbaba4f131c258757b90e0596512725687e`  
		Last Modified: Mon, 08 Sep 2025 22:04:06 GMT  
		Size: 833.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ac8541099751a00e29431eef23f987bc00549735209ce497c6b83ea34d01315`  
		Last Modified: Mon, 08 Sep 2025 22:28:18 GMT  
		Size: 5.8 MB (5789340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ae4c824bf9b61979a828809d5d5a417e33963d9824f988fbd3701381ae61e82`  
		Last Modified: Mon, 08 Sep 2025 22:04:10 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f319c861a951dddde13625b0698753da831f49126c96f1abce8385232fdb923`  
		Last Modified: Mon, 08 Sep 2025 22:04:14 GMT  
		Size: 336.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:latest` - unknown; unknown

```console
$ docker pull spiped@sha256:8337e80157647554c90537d86a37253c41b794f85ffa73ab90367849dac09134
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3634202 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:278446c0f2bf208b2238b94eb45c3cf122a66492598663f90f2ba83833dd3a5b`

```dockerfile
```

-	Layers:
	-	`sha256:a47de1c44f6e4184ee91c743b4ce1f377fdd734180d1e0a652c84b5fa906bfa4`  
		Last Modified: Mon, 08 Sep 2025 22:04:38 GMT  
		Size: 3.6 MB (3619072 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e94d87a927a69b6ac792670d12cb5ecae277dbb0a409b6a386ca2fdd5243dc50`  
		Last Modified: Mon, 08 Sep 2025 22:04:39 GMT  
		Size: 15.1 KB (15130 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:latest` - linux; arm variant v7

```console
$ docker pull spiped@sha256:55c1924462ce41de687f42e2603b9295efb3af2ea9416e2c25e3f9fdd34afb64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.8 MB (31794747 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b264184152b054bd80ca19a24fec1f4060c0f6c53fd9419139ce0187034c9cb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Fri, 29 Aug 2025 17:20:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1757289600'
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
	-	`sha256:c01338083e94735040ac705e73d3207fecb1a829de94334396239199538796bd`  
		Last Modified: Mon, 08 Sep 2025 21:13:56 GMT  
		Size: 26.2 MB (26207847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1135c42cd92801939fa6513bb162537bb967d875405841f452ae92aa019e5bfe`  
		Last Modified: Mon, 08 Sep 2025 22:16:32 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2df69bf0846187df4227a06f55de71273baee4d386ccb1f98bb6e74ad188874a`  
		Last Modified: Mon, 08 Sep 2025 22:16:38 GMT  
		Size: 827.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd1eed6b9285bafc18f4c963dbf92dff69f211d78afcc6e9f6e750147a8681f6`  
		Last Modified: Mon, 08 Sep 2025 22:49:33 GMT  
		Size: 5.6 MB (5584533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07a57a1b1c83bb1f19dbbd26fe2bceb4f92d9d7951f1f17fb60d28ca37cfbf8f`  
		Last Modified: Mon, 08 Sep 2025 22:16:41 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3755b9c4ec1e1535de44613e7ff33ce001f5799640318ceaf4187cd1dd428a0f`  
		Last Modified: Mon, 08 Sep 2025 22:16:44 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:latest` - unknown; unknown

```console
$ docker pull spiped@sha256:b96e349fb89eafa7400bb0137272e43e7aa3f42efcd87d166a136ad9b0e1e783
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3633324 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef3ecc4e0843e63369fdd1aea3d2a5e46f2f8f891f2a9660bd7b841c5078b335`

```dockerfile
```

-	Layers:
	-	`sha256:416818cdf08bf484514867f324a9c87f81b1fd4a826f731bd0b95c88d8c643d3`  
		Last Modified: Tue, 09 Sep 2025 01:04:25 GMT  
		Size: 3.6 MB (3618193 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bbc0b5538d2093419837cea2916b8e4b7473900ca2c1c5fcde6d183855056eaf`  
		Last Modified: Tue, 09 Sep 2025 01:04:26 GMT  
		Size: 15.1 KB (15131 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:latest` - linux; arm64 variant v8

```console
$ docker pull spiped@sha256:b30af9feecd6d2d3e060442d3a65f6e96ddfa1a80fed606c84c1f016a2e3ec98
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.4 MB (36370794 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4cd3ed48417c32b96cea00093023ea9133743c7d939098b1666f4dd6e5b6a44b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Fri, 29 Aug 2025 17:20:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1757289600'
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
	-	`sha256:b2feff975e6dd2ebaf182772fb9ee26274648387b061e821e0bb5026735dd094`  
		Last Modified: Mon, 08 Sep 2025 21:13:54 GMT  
		Size: 30.1 MB (30136631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf96c895c9ecb8c50b531abc85aae3b4e1618dd151bee2548e8f0f324a66d264`  
		Last Modified: Mon, 08 Sep 2025 22:08:07 GMT  
		Size: 1.1 KB (1105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d894fd8e76b8c24189989a2c4edcede7b07f861c7878d352bdfead93f052b114`  
		Last Modified: Mon, 08 Sep 2025 22:08:11 GMT  
		Size: 824.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:009c3a2ddeae00427400405aae3478f6145688b476d8e0a6332ec10033d0214a`  
		Last Modified: Mon, 08 Sep 2025 22:31:44 GMT  
		Size: 6.2 MB (6231800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:771b828e58dae600ab30ba08fd29c1f6999e6ad1e0046d8130cc9fb4dfa3230b`  
		Last Modified: Mon, 08 Sep 2025 22:08:16 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c538a87d62b081105d070718eebcabf29d31a37763736eaf01e7e57bd1aa4e2f`  
		Last Modified: Mon, 08 Sep 2025 22:08:19 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:latest` - unknown; unknown

```console
$ docker pull spiped@sha256:b4b6c21230283163829ba358f0011d55d69c385a2cba19fa01e97ee624229b25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3636273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec6ae267ebdb45e6c8daf2e30f3457f918cd0da29621862f41bb5f294d7e3142`

```dockerfile
```

-	Layers:
	-	`sha256:d5b5755081e9d83cc165f6f2f16af8973276b35a16325e5d6324b4fd57784cce`  
		Last Modified: Mon, 08 Sep 2025 22:04:50 GMT  
		Size: 3.6 MB (3621114 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:002e4f513e5bbf2214b3303f88fd4499f1622400a327fbe0721cf244a7d239ed`  
		Last Modified: Mon, 08 Sep 2025 22:04:51 GMT  
		Size: 15.2 KB (15159 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:latest` - linux; 386

```console
$ docker pull spiped@sha256:82171e0666e35ff746fbb4f2dfa2952132328bb53429717390797dbe93bfc17e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.7 MB (37734562 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f616dd7bbc1f42449fdc926a447f0d4328e9e133a475731c7460bb30db8c2b70`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Fri, 29 Aug 2025 17:20:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1757289600'
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
	-	`sha256:d6e01c57fc6d674eef68e6bfe57a080b0a70c1c25810b7d6e769151bad3645bf`  
		Last Modified: Mon, 08 Sep 2025 21:12:32 GMT  
		Size: 31.3 MB (31289784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9fbcdd1371662f71ddb2b23df80fbf351b005debab82aafc902262981ba08ab`  
		Last Modified: Mon, 08 Sep 2025 21:57:17 GMT  
		Size: 1.1 KB (1104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85701ac5b161301c0a05e4843ffa9727392f95db70819ce77c42c30226553c80`  
		Last Modified: Mon, 08 Sep 2025 21:57:19 GMT  
		Size: 827.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50bb5031c8241b37a2e696ec8db5c03b82b1bd1ee65904857cfe42b14fac04af`  
		Last Modified: Mon, 08 Sep 2025 21:57:22 GMT  
		Size: 6.4 MB (6442413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:934469e6381f737152de5a1b3f6dd1729b3784cf1f1bae109fe5d3529099a832`  
		Last Modified: Mon, 08 Sep 2025 21:57:15 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d17cd8e8171dbc807b1bedab727c5008a91341d002e8f731f019a7f1ed51f3d`  
		Last Modified: Mon, 08 Sep 2025 21:57:14 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:latest` - unknown; unknown

```console
$ docker pull spiped@sha256:dfafee5c17a53e878812bb4dff43ecef3eca0c87e52722ca1d7d2bfb87c6797a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3635196 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49def9b4fb17d9ed6e5081b5415496b65daf1abe47fecc43f29182d4729ceb85`

```dockerfile
```

-	Layers:
	-	`sha256:55fc616258ae4fd67f353ff39a69793c11ab295b8f55ee9a3b8a23db68bedd00`  
		Last Modified: Mon, 08 Sep 2025 22:04:56 GMT  
		Size: 3.6 MB (3620207 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8b3162a00f4793a413edfb2b0c0cac933355d8dc353782e0efb33e4bcd6a98f2`  
		Last Modified: Mon, 08 Sep 2025 22:04:57 GMT  
		Size: 15.0 KB (14989 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:latest` - linux; ppc64le

```console
$ docker pull spiped@sha256:dd0f2c26fba6d8f7e91efc7236bc5ae26c6c586ebafbf27ba67b05e7405c585a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.4 MB (40436895 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7da8485c8492a65bd7db4a06ef4be5e13fa36922e67991803bd5b1597ce5908d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Fri, 29 Aug 2025 17:20:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1757289600'
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
	-	`sha256:d11c44105444ef722eccd8c92c6b2fce9986e3274ba9b346e044a458c0425852`  
		Last Modified: Mon, 08 Sep 2025 22:03:02 GMT  
		Size: 33.6 MB (33594351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1ff6f5b89d4b84c15ed34cf42385122a4619cef97f26b3b00fcf1ce99826e4e`  
		Last Modified: Tue, 09 Sep 2025 02:16:11 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2147f6accb00e92c1eedf8f3e292138aa51f43b774e82dbf3d236cd25c7a6ef5`  
		Last Modified: Tue, 09 Sep 2025 02:16:12 GMT  
		Size: 827.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12b36c08f12f5edbb0ebb0705a1fcbf0751d18146517cd3eac584f7a0e0e7db3`  
		Last Modified: Tue, 09 Sep 2025 02:16:10 GMT  
		Size: 6.8 MB (6840177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69c16bd3132d22ed6e04816499858f07b1a6caecb5e593723f22e1c664fd2504`  
		Last Modified: Tue, 09 Sep 2025 02:16:13 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbcf4a0a26c7a4eb0cae2a7bc2b099ccdd386daa17a0388ccc953332ef162ba9`  
		Last Modified: Tue, 09 Sep 2025 02:16:11 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:latest` - unknown; unknown

```console
$ docker pull spiped@sha256:fdddf2e236221e21497abda9439774a7dfa99c89501e1f61344f91f288ac160b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3636888 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cc8e6b9798028e08951fd7894a1176bc5de4172976f59bbb7d7a99a1fb24470`

```dockerfile
```

-	Layers:
	-	`sha256:cd3e3f7f121b597b3ae88011a5350cf0229bae2285264b9e515b5f46f48a7b9f`  
		Last Modified: Tue, 09 Sep 2025 04:04:37 GMT  
		Size: 3.6 MB (3621815 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:561d39bebbd3a77be83f987074591f029589166e840124add7a2af8871dbfa2d`  
		Last Modified: Tue, 09 Sep 2025 04:04:38 GMT  
		Size: 15.1 KB (15073 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:latest` - linux; riscv64

```console
$ docker pull spiped@sha256:3b3676cb2123fc9a1e4c327fa70e1857a75050bf33a275e9bd1d802151bcec4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.6 MB (37631686 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:640570b0b3bda692dcea0827850a72c5b2ee0b43583c995c0eb457af9a193f55`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1754870400'
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
	-	`sha256:a37386b9234ad75f65b5aa72f3d919ff0eb3bb18978566fa959d6e357480594c`  
		Last Modified: Wed, 13 Aug 2025 04:01:43 GMT  
		Size: 28.3 MB (28271623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf45ba83e1202bc173e329dc23766a0c3b8f738706ea301cda047e1348826c8b`  
		Last Modified: Mon, 01 Sep 2025 16:51:10 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1289b217d2c4a16ddbd2b4d846971cedbfc1a799389778f50d60a1036fc024a6`  
		Last Modified: Mon, 01 Sep 2025 16:51:10 GMT  
		Size: 825.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5c4f37ceddaefd5451a85453565dcee0f13860226efd805bc8c2dc3ae8ccd14`  
		Last Modified: Mon, 01 Sep 2025 16:51:10 GMT  
		Size: 9.4 MB (9357695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee843d99237854181305ecdd766749ac1bbb3e3bcd47e8b414a85a011862653c`  
		Last Modified: Mon, 01 Sep 2025 16:51:10 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0dc22da2f4339a139638305ec66c0783e946b8f0adff62530e43d73c487e5bd`  
		Last Modified: Mon, 01 Sep 2025 16:51:10 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:latest` - unknown; unknown

```console
$ docker pull spiped@sha256:35e5912a111ea507f93a7e0032bc1b2e8da82b06019cc75a58da48d7eb2e91b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3627446 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6bd2db2812e5fef7854b1d160553111506105875f89f941b7f315d71501d78f`

```dockerfile
```

-	Layers:
	-	`sha256:805bcf15f820505976cb5a30bf72471359a5fca4131aba384f3584599ddb7045`  
		Last Modified: Mon, 01 Sep 2025 19:04:42 GMT  
		Size: 3.6 MB (3612373 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cbd40f85e785916c7ddb424fb3a8f9a0b9545ec9ab0a04ea5ea5dc326ba8a2b5`  
		Last Modified: Mon, 01 Sep 2025 19:04:43 GMT  
		Size: 15.1 KB (15073 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:latest` - linux; s390x

```console
$ docker pull spiped@sha256:f43d82c5a3d35f6ce2cddbdf9ec0205301960afbde878d2ca5a7861df01aeb4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.0 MB (35956343 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d59764c7f98b190c53b1f7bc6dd3b9098f2d767322d48956bd085d7b071c49c9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Fri, 29 Aug 2025 17:20:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1757289600'
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
	-	`sha256:8af003c0cb712f415b555d33f1c4a9cc3fad82782766d388f3426c4d807a5ab2`  
		Last Modified: Mon, 08 Sep 2025 21:53:51 GMT  
		Size: 29.8 MB (29832904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2763f4a4daec888c7d63b0e0ff81db10dadc52fb53a435fa22ae03ee5decf09a`  
		Last Modified: Tue, 09 Sep 2025 00:21:56 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5161d34bcac535a56ad8efb0d748f8b339da9725c091b74f67c1823ec2bb58d9`  
		Last Modified: Tue, 09 Sep 2025 00:21:59 GMT  
		Size: 827.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b4a51a796aa3aaf724cc5bbec39ecd4f3b9a5b8244e1af98a933025d02f4ffd`  
		Last Modified: Tue, 09 Sep 2025 01:21:28 GMT  
		Size: 6.1 MB (6121071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa8daf184e635c2a7d701efea95606a1b0e8e8a2a745d9a541e956f2b0b71a39`  
		Last Modified: Tue, 09 Sep 2025 00:22:01 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90f4edae4a9a40914726f530d046af5b5b1f4e4c4048a15ee60f70e0ab94f709`  
		Last Modified: Tue, 09 Sep 2025 00:22:05 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:latest` - unknown; unknown

```console
$ docker pull spiped@sha256:def719779c2d7857b30da66a7a9f95579e191353a797ea6592ccef059ba709e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3633466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d10bf28afc205e156ee5a6abfde2d897204f3852cd6ba8108423663144fb84a9`

```dockerfile
```

-	Layers:
	-	`sha256:bab5214c083436ce496b531b010d96bf6ce4fc5d41d6254cd2944891972578bb`  
		Last Modified: Tue, 09 Sep 2025 04:04:44 GMT  
		Size: 3.6 MB (3618441 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0fc2bc9ff9441d9915eae99b2766d2b72f0d4aa3b4904864a6f976f52fceadeb`  
		Last Modified: Tue, 09 Sep 2025 04:04:46 GMT  
		Size: 15.0 KB (15025 bytes)  
		MIME: application/vnd.in-toto+json
