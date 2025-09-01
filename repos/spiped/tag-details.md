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
$ docker pull spiped@sha256:fa8cc1db019181c9115dd856665c7ecbfda6a245a420395ef8289ab28e82cfbf
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
$ docker pull spiped@sha256:3ef6a68bec16df3d49ac1119266e73804149779578c26208adfde5be4811db83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.8 MB (36823735 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d7fc64f06c4c58f0559d0930092fb12193ce356ed564676ef093a1f8cdc3c88`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1754870400'
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
	-	`sha256:396b1da7636e2dcd10565cb4f2f952cbb4a8a38b58d3b86a2cacb172fb70117c`  
		Last Modified: Tue, 12 Aug 2025 20:45:08 GMT  
		Size: 29.8 MB (29773285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0c4a6bf8c68ef3bb6ba597f3faca719888855ba6e3eb4fd0221f8005f88b578`  
		Last Modified: Fri, 29 Aug 2025 17:33:40 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8291215610373f818679d1441dc23d6414241c02b328a2d74c75ee6f43edb47`  
		Last Modified: Fri, 29 Aug 2025 17:33:40 GMT  
		Size: 828.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abfff1a4e7c04610b35cfa4681e2dc2aec187c18865702f204d9373f7f3937f1`  
		Last Modified: Fri, 29 Aug 2025 17:33:43 GMT  
		Size: 7.0 MB (7048080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74530c0255a2e254f8e851b46c40bbb1abcc79fe14a3a923182ea7f008eb953f`  
		Last Modified: Fri, 29 Aug 2025 17:33:40 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:447d4247cfd5b820273da6bbba318f8e21f2c9bcc28f55e93c200b6295b736af`  
		Last Modified: Fri, 29 Aug 2025 17:33:41 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1` - unknown; unknown

```console
$ docker pull spiped@sha256:fa6bf0713892c5beaaa9cc160afab5d917c5cc13ce70f6b55fbed9667e52e725
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3640255 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4352c813b000b4ffdd961f6bdb4cf2048d9001115ef073eba4864baa4351ccf`

```dockerfile
```

-	Layers:
	-	`sha256:17386d721162f1fe8cf87199caf138e7c670be8e7d3956e735eeb43813620dad`  
		Last Modified: Fri, 29 Aug 2025 19:04:40 GMT  
		Size: 3.6 MB (3625230 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1f26786168c5d5fd557db75e3200dfa805106b43e29c62eaefea65ace2df74d9`  
		Last Modified: Fri, 29 Aug 2025 19:04:41 GMT  
		Size: 15.0 KB (15025 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1` - linux; arm variant v5

```console
$ docker pull spiped@sha256:775c9a677f3eea419a2cfdab021bc73ea15a1f0eeabad8ddf5d109eaddebf987
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.7 MB (33733042 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:893a9f0c3890343e165b7a090fb3cf98522a2be3fb383bcc08279e28c97a307e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1754870400'
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
	-	`sha256:498399880872f14c562c46bd2a1ef4cfcf3c2a1453514ff0d0f6b7d89f8010dd`  
		Last Modified: Tue, 12 Aug 2025 22:02:01 GMT  
		Size: 27.9 MB (27941706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29082b3905ccb7de954a88ea955cbdf9a83dac9250d8d80de1abdeeafb051af4`  
		Last Modified: Fri, 29 Aug 2025 17:33:08 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1c8b3da67e1ae83930836f15a6bc2326925939ceb8bfde62fd3c1be32e4ff63`  
		Last Modified: Fri, 29 Aug 2025 17:33:08 GMT  
		Size: 832.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3bd6dfd17377cd518eefa5090b847afb64042f8ca7301629e498c40bd76fc18`  
		Last Modified: Fri, 29 Aug 2025 17:33:09 GMT  
		Size: 5.8 MB (5788961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4925ddd4cbbd4e0f0552eb8d7bd4dc917105d66235cd2aa023f1ced94b42dac8`  
		Last Modified: Fri, 29 Aug 2025 17:33:08 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79e22b81fbccf50276e0a0119e314ddd089195fde3023a114e1710efb08360da`  
		Last Modified: Fri, 29 Aug 2025 17:40:24 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1` - unknown; unknown

```console
$ docker pull spiped@sha256:e0dcda5aa6d420f41e885934e8d19deadc188142ed26721c7a8729f72fce03cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3633351 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc99de0b923227b61b33d206e2167d77c4a5635d6d82e71675287b766e9aa71a`

```dockerfile
```

-	Layers:
	-	`sha256:1e4d10b7dbe06386b35f345b0a4bed1e6524b04934b277901c20ef1f41a0a193`  
		Last Modified: Fri, 29 Aug 2025 19:04:46 GMT  
		Size: 3.6 MB (3618224 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8165e679713497e1a387bddb798c12153bc4d22f642cf83469cad62339033d49`  
		Last Modified: Fri, 29 Aug 2025 19:04:47 GMT  
		Size: 15.1 KB (15127 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1` - linux; arm variant v7

```console
$ docker pull spiped@sha256:f87b2e8141e5dc0e1e06c580713a5ebe8a2c260f244f7bdcdea78714f00cc3b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.8 MB (31794250 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a3b9065cf06fdf2af1c2a24ea909722d65b64439387288f2672b8efc6a1038f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1754870400'
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
	-	`sha256:d480d07cd33d2a61cb24d871a17254661d250ae887a2db15a7e99cb67383a74e`  
		Last Modified: Tue, 12 Aug 2025 20:52:10 GMT  
		Size: 26.2 MB (26207488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fecbe4210c70bc3e538dad13a5f8a4ee3ab0d106268e42dfa80a971ac77bc0d`  
		Last Modified: Fri, 29 Aug 2025 17:32:58 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34148ed6b26e88d3d7a7c3a98fbae82c52c329016d3eca423a16836a07c9dbce`  
		Last Modified: Fri, 29 Aug 2025 17:32:58 GMT  
		Size: 825.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d256a5a77b507a955cf7e3d03a7166949da3e560460b1000011e054979d70628`  
		Last Modified: Fri, 29 Aug 2025 17:33:00 GMT  
		Size: 5.6 MB (5584393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:656c2e207f2bd9664ca3591eeab603fe4ad05be7ffcd8dfc7761b6db836bed35`  
		Last Modified: Fri, 29 Aug 2025 17:32:58 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d750cbed80655934a514a4ee40e186bdc38155dd958c3ac037e0917fa5a5245`  
		Last Modified: Fri, 29 Aug 2025 17:32:58 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1` - unknown; unknown

```console
$ docker pull spiped@sha256:6ae77ff0bcf2a50f789f2f2841bbcc896e112247136781bc0da91bb058553cee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3632472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25492705ffccd901687c0f01d38b16fb5481183837785fea959754d2cb317b31`

```dockerfile
```

-	Layers:
	-	`sha256:23eee19f68a1b7930f8f02e0e2999d1a94a6d7b6625e68882288d71bc6e1b5d8`  
		Last Modified: Fri, 29 Aug 2025 19:04:51 GMT  
		Size: 3.6 MB (3617345 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c82d8e54a24d0f61dd4f978f5a9aa7fa21b8488a559050cf0499ddf07326fc95`  
		Last Modified: Fri, 29 Aug 2025 19:04:52 GMT  
		Size: 15.1 KB (15127 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1` - linux; arm64 variant v8

```console
$ docker pull spiped@sha256:bf441e6b20fe3c68abd00975a9de044d99b6902c4f105b9b4d5fcca621f4f163
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.4 MB (36369917 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6324fc3857cd905718785b4db6d60827bbbdb477417615b2bfc9c9a8d249a95`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1754870400'
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
	-	`sha256:9a6263cdeaa5d408640880103ee36920ef814974ca8e2674412ad6460e8968c9`  
		Last Modified: Tue, 12 Aug 2025 22:12:42 GMT  
		Size: 30.1 MB (30136044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cd31d256f52a45f839cb7de272b3deca6eee338a96c08b38da9076814d516b5`  
		Last Modified: Fri, 29 Aug 2025 17:33:03 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:512707d9128cd8badb8edd5168565f652d375d4cb981e3e7359c1ab67a0fdf3c`  
		Last Modified: Fri, 29 Aug 2025 17:33:03 GMT  
		Size: 828.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebab66b6a0be26be9392866319a8360a1516a1bc6ecf5efe4b2b7ab6d69a2222`  
		Last Modified: Fri, 29 Aug 2025 17:33:04 GMT  
		Size: 6.2 MB (6231503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e63be8c19281fc15dce3e70b954c2f37b48224b874afa4f684dc2ac1e534d76`  
		Last Modified: Fri, 29 Aug 2025 17:33:03 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd68a8cba102356cd65222b4bd6769d96d54d40ff9819507ebd547f873ae1675`  
		Last Modified: Fri, 29 Aug 2025 17:33:03 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1` - unknown; unknown

```console
$ docker pull spiped@sha256:4fe512ce76c7021740395ba0ce698366ca33c5df0d7ce00b59c0a3ce693568ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3635425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7a7c701338af6b5611e76e87c04e4cbe547754c92d981b9c41c20a059037dc5`

```dockerfile
```

-	Layers:
	-	`sha256:35fd43c927b6d65170b6e73cd99253106f56c0bf8fc00d210b8dea964ccf1dcd`  
		Last Modified: Fri, 29 Aug 2025 19:04:57 GMT  
		Size: 3.6 MB (3620266 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bb73fffccc386dde1f6a61868e0a17dac4f052ce75e90203b040b73bb2e1da12`  
		Last Modified: Fri, 29 Aug 2025 19:04:58 GMT  
		Size: 15.2 KB (15159 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1` - linux; 386

```console
$ docker pull spiped@sha256:e21fd11c4575ac83db30d0870ce8b1909393db426e769913e368989e42eb94ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.7 MB (37733752 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5df072e5a48747d0fb778894ace9e57e45756be4da3d4caf26b3f4e5958b1e83`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1754870400'
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
	-	`sha256:346d0c953bdbc38917a27a6f30726e5b46419d98ecaf4d2d8f201bc3b7025e57`  
		Last Modified: Tue, 12 Aug 2025 20:45:00 GMT  
		Size: 31.3 MB (31289378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f63f74a69468fc2acc1bd2a6ffd16aa7c3b461c719619504b4e208871e0a94a`  
		Last Modified: Fri, 29 Aug 2025 17:33:42 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a1520a614c988b98e1995e06613907c489562d65634c6a7e55f75cf975ac467`  
		Last Modified: Fri, 29 Aug 2025 17:33:42 GMT  
		Size: 828.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1ab6e794167d2c138d6e5986ae639a38571c7aa53eb5005fa3c0dc50621719a`  
		Last Modified: Fri, 29 Aug 2025 17:33:43 GMT  
		Size: 6.4 MB (6442003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d016b6b6bcd6d93a988faed26fd017a6f0109e6a0bd580557aabd037c2614064`  
		Last Modified: Fri, 29 Aug 2025 17:33:44 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10de62ac80528d9c9fd3232cb65ef310a09d9403cfdb7c96b5c77ba6662d707b`  
		Last Modified: Fri, 29 Aug 2025 17:33:40 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1` - unknown; unknown

```console
$ docker pull spiped@sha256:78575350c68a0455e8dba0b99c65d1f7c4de8ceea05c20ec5ad85e6a10fc1bbe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3634348 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7349d067f8d072b2300174cb9d9478cd11bf63a85a9b0ea56bd0f59064ce904`

```dockerfile
```

-	Layers:
	-	`sha256:f17ff7be52b05394f9faca48008984eb34022f2730306c4b5e4624081976cad8`  
		Last Modified: Fri, 29 Aug 2025 19:05:02 GMT  
		Size: 3.6 MB (3619359 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dd0a7e7a63f0f39246d0099e816021fb11f5aa955b1fbb2d27c3ab6e84d68e13`  
		Last Modified: Fri, 29 Aug 2025 19:05:03 GMT  
		Size: 15.0 KB (14989 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1` - linux; ppc64le

```console
$ docker pull spiped@sha256:d7e882296f82ff515c6b7e25d0fe26109721704e0290fc159c1237c1ad13bc20
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.4 MB (40436446 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d8c42f0b031d41a60ad454e14474cd9952b294e505c5fb6bfa1ec51d37b3020`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1754870400'
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
	-	`sha256:52a4daa8724e9e1632306e15fe478aa26ff0ebcb7ba924cb168e9b6738c239d5`  
		Last Modified: Wed, 13 Aug 2025 01:42:36 GMT  
		Size: 33.6 MB (33594213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc559a346c52f0f42d55a8b704817cf8a88d1b77699564e48a5b0b53030d0eeb`  
		Last Modified: Fri, 29 Aug 2025 17:34:00 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1b7971605e54829a0d8926db240a359db09df68c4a44aa1a10f39a3a3ca22fd`  
		Last Modified: Fri, 29 Aug 2025 17:34:02 GMT  
		Size: 829.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72fb014cef1414fead51e60f6f137d2813ad430172c6ed5b514d200d50958002`  
		Last Modified: Fri, 29 Aug 2025 17:34:03 GMT  
		Size: 6.8 MB (6839861 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c48e8c7818509d33221884ced67ec2035e0bda0e71821c41b9254bbe1b65c591`  
		Last Modified: Fri, 29 Aug 2025 17:34:02 GMT  
		Size: 94.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b035aa0e12be73b492a26f9066458209e72fa35a17bb5d5c3c33106051a6be46`  
		Last Modified: Fri, 29 Aug 2025 17:34:03 GMT  
		Size: 341.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1` - unknown; unknown

```console
$ docker pull spiped@sha256:b3d9482f09219f380e4497df9a4b15d28c8f3b75620e531d8b504549bdcc3599
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3636040 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8551f02e77ebbaa7e1b6613113354f909315dcd145b303c71015b92bf85172ff`

```dockerfile
```

-	Layers:
	-	`sha256:bb4fe81c44bf267a7b0a2be60b0a8f4414c39313dc7958eb14ee87ad8a40b3bb`  
		Last Modified: Fri, 29 Aug 2025 19:05:08 GMT  
		Size: 3.6 MB (3620967 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:361b1f0f6e13750899ca78a508eaa9dda9b4b0675918ee1604a65f9222852e5b`  
		Last Modified: Fri, 29 Aug 2025 19:05:09 GMT  
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
$ docker pull spiped@sha256:971a98798525dda6f9e7186f5f8f00c3a9a85971ef868e5735b240f305c01495
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.0 MB (35955636 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5dd452c0ad86184e337fb92ff500d9d975c2bf1ee1fc9f7fc16ed80c764c513f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1754870400'
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
	-	`sha256:bfe4d60a27c9392ab729f16b50a763cda36622d744066c3cf029a072133f2907`  
		Last Modified: Tue, 12 Aug 2025 20:59:52 GMT  
		Size: 29.8 MB (29833057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee1e72abadfa82b43b60b1f35da5ec06d5b929e2d36ee59ba7fac09b38158137`  
		Last Modified: Fri, 29 Aug 2025 17:34:35 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6da709972cad7ef527beb58c27162c5297d2898d6bbe37bf72a4ad0b875e8bf`  
		Last Modified: Fri, 29 Aug 2025 17:34:35 GMT  
		Size: 826.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c037b23c412da0dfcecac8846c67a23f22b94078b6d9ee11097ea1d4ffd2664`  
		Last Modified: Fri, 29 Aug 2025 17:34:37 GMT  
		Size: 6.1 MB (6120208 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c61027a0ec9d7ddedea31031c7852426e4aea9b6a68157f296eb16c027e5fd7`  
		Last Modified: Fri, 29 Aug 2025 17:34:35 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:983ddf74fd727cc9be924969a0e4160869a09753f21773195924b52e52e12c15`  
		Last Modified: Fri, 29 Aug 2025 17:34:35 GMT  
		Size: 341.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1` - unknown; unknown

```console
$ docker pull spiped@sha256:41b62f6c31ab522141ab290c3039ca5fc5f079667b5383ba00cb476f87e76126
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3632617 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f231a59432a7c83e6a6c2e773118bec44ee2a38536b02b7a5452c6c0aae17e1a`

```dockerfile
```

-	Layers:
	-	`sha256:27f2faa66bf854f32b888751318fc1bf861403f4abbbd02814273b92f265302d`  
		Last Modified: Fri, 29 Aug 2025 19:05:17 GMT  
		Size: 3.6 MB (3617593 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9ab13e11e4c038119bc34cceafc7cd53073417c92e76b936eac28da2501db8ba`  
		Last Modified: Fri, 29 Aug 2025 19:05:18 GMT  
		Size: 15.0 KB (15024 bytes)  
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
$ docker pull spiped@sha256:fa8cc1db019181c9115dd856665c7ecbfda6a245a420395ef8289ab28e82cfbf
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
$ docker pull spiped@sha256:3ef6a68bec16df3d49ac1119266e73804149779578c26208adfde5be4811db83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.8 MB (36823735 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d7fc64f06c4c58f0559d0930092fb12193ce356ed564676ef093a1f8cdc3c88`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1754870400'
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
	-	`sha256:396b1da7636e2dcd10565cb4f2f952cbb4a8a38b58d3b86a2cacb172fb70117c`  
		Last Modified: Tue, 12 Aug 2025 20:45:08 GMT  
		Size: 29.8 MB (29773285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0c4a6bf8c68ef3bb6ba597f3faca719888855ba6e3eb4fd0221f8005f88b578`  
		Last Modified: Fri, 29 Aug 2025 17:33:40 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8291215610373f818679d1441dc23d6414241c02b328a2d74c75ee6f43edb47`  
		Last Modified: Fri, 29 Aug 2025 17:33:40 GMT  
		Size: 828.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abfff1a4e7c04610b35cfa4681e2dc2aec187c18865702f204d9373f7f3937f1`  
		Last Modified: Fri, 29 Aug 2025 17:33:43 GMT  
		Size: 7.0 MB (7048080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74530c0255a2e254f8e851b46c40bbb1abcc79fe14a3a923182ea7f008eb953f`  
		Last Modified: Fri, 29 Aug 2025 17:33:40 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:447d4247cfd5b820273da6bbba318f8e21f2c9bcc28f55e93c200b6295b736af`  
		Last Modified: Fri, 29 Aug 2025 17:33:41 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6` - unknown; unknown

```console
$ docker pull spiped@sha256:fa6bf0713892c5beaaa9cc160afab5d917c5cc13ce70f6b55fbed9667e52e725
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3640255 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4352c813b000b4ffdd961f6bdb4cf2048d9001115ef073eba4864baa4351ccf`

```dockerfile
```

-	Layers:
	-	`sha256:17386d721162f1fe8cf87199caf138e7c670be8e7d3956e735eeb43813620dad`  
		Last Modified: Fri, 29 Aug 2025 19:04:40 GMT  
		Size: 3.6 MB (3625230 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1f26786168c5d5fd557db75e3200dfa805106b43e29c62eaefea65ace2df74d9`  
		Last Modified: Fri, 29 Aug 2025 19:04:41 GMT  
		Size: 15.0 KB (15025 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6` - linux; arm variant v5

```console
$ docker pull spiped@sha256:775c9a677f3eea419a2cfdab021bc73ea15a1f0eeabad8ddf5d109eaddebf987
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.7 MB (33733042 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:893a9f0c3890343e165b7a090fb3cf98522a2be3fb383bcc08279e28c97a307e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1754870400'
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
	-	`sha256:498399880872f14c562c46bd2a1ef4cfcf3c2a1453514ff0d0f6b7d89f8010dd`  
		Last Modified: Tue, 12 Aug 2025 22:02:01 GMT  
		Size: 27.9 MB (27941706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29082b3905ccb7de954a88ea955cbdf9a83dac9250d8d80de1abdeeafb051af4`  
		Last Modified: Fri, 29 Aug 2025 17:33:08 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1c8b3da67e1ae83930836f15a6bc2326925939ceb8bfde62fd3c1be32e4ff63`  
		Last Modified: Fri, 29 Aug 2025 17:33:08 GMT  
		Size: 832.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3bd6dfd17377cd518eefa5090b847afb64042f8ca7301629e498c40bd76fc18`  
		Last Modified: Fri, 29 Aug 2025 17:33:09 GMT  
		Size: 5.8 MB (5788961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4925ddd4cbbd4e0f0552eb8d7bd4dc917105d66235cd2aa023f1ced94b42dac8`  
		Last Modified: Fri, 29 Aug 2025 17:33:08 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79e22b81fbccf50276e0a0119e314ddd089195fde3023a114e1710efb08360da`  
		Last Modified: Fri, 29 Aug 2025 17:40:24 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6` - unknown; unknown

```console
$ docker pull spiped@sha256:e0dcda5aa6d420f41e885934e8d19deadc188142ed26721c7a8729f72fce03cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3633351 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc99de0b923227b61b33d206e2167d77c4a5635d6d82e71675287b766e9aa71a`

```dockerfile
```

-	Layers:
	-	`sha256:1e4d10b7dbe06386b35f345b0a4bed1e6524b04934b277901c20ef1f41a0a193`  
		Last Modified: Fri, 29 Aug 2025 19:04:46 GMT  
		Size: 3.6 MB (3618224 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8165e679713497e1a387bddb798c12153bc4d22f642cf83469cad62339033d49`  
		Last Modified: Fri, 29 Aug 2025 19:04:47 GMT  
		Size: 15.1 KB (15127 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6` - linux; arm variant v7

```console
$ docker pull spiped@sha256:f87b2e8141e5dc0e1e06c580713a5ebe8a2c260f244f7bdcdea78714f00cc3b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.8 MB (31794250 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a3b9065cf06fdf2af1c2a24ea909722d65b64439387288f2672b8efc6a1038f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1754870400'
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
	-	`sha256:d480d07cd33d2a61cb24d871a17254661d250ae887a2db15a7e99cb67383a74e`  
		Last Modified: Tue, 12 Aug 2025 20:52:10 GMT  
		Size: 26.2 MB (26207488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fecbe4210c70bc3e538dad13a5f8a4ee3ab0d106268e42dfa80a971ac77bc0d`  
		Last Modified: Fri, 29 Aug 2025 17:32:58 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34148ed6b26e88d3d7a7c3a98fbae82c52c329016d3eca423a16836a07c9dbce`  
		Last Modified: Fri, 29 Aug 2025 17:32:58 GMT  
		Size: 825.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d256a5a77b507a955cf7e3d03a7166949da3e560460b1000011e054979d70628`  
		Last Modified: Fri, 29 Aug 2025 17:33:00 GMT  
		Size: 5.6 MB (5584393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:656c2e207f2bd9664ca3591eeab603fe4ad05be7ffcd8dfc7761b6db836bed35`  
		Last Modified: Fri, 29 Aug 2025 17:32:58 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d750cbed80655934a514a4ee40e186bdc38155dd958c3ac037e0917fa5a5245`  
		Last Modified: Fri, 29 Aug 2025 17:32:58 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6` - unknown; unknown

```console
$ docker pull spiped@sha256:6ae77ff0bcf2a50f789f2f2841bbcc896e112247136781bc0da91bb058553cee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3632472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25492705ffccd901687c0f01d38b16fb5481183837785fea959754d2cb317b31`

```dockerfile
```

-	Layers:
	-	`sha256:23eee19f68a1b7930f8f02e0e2999d1a94a6d7b6625e68882288d71bc6e1b5d8`  
		Last Modified: Fri, 29 Aug 2025 19:04:51 GMT  
		Size: 3.6 MB (3617345 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c82d8e54a24d0f61dd4f978f5a9aa7fa21b8488a559050cf0499ddf07326fc95`  
		Last Modified: Fri, 29 Aug 2025 19:04:52 GMT  
		Size: 15.1 KB (15127 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6` - linux; arm64 variant v8

```console
$ docker pull spiped@sha256:bf441e6b20fe3c68abd00975a9de044d99b6902c4f105b9b4d5fcca621f4f163
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.4 MB (36369917 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6324fc3857cd905718785b4db6d60827bbbdb477417615b2bfc9c9a8d249a95`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1754870400'
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
	-	`sha256:9a6263cdeaa5d408640880103ee36920ef814974ca8e2674412ad6460e8968c9`  
		Last Modified: Tue, 12 Aug 2025 22:12:42 GMT  
		Size: 30.1 MB (30136044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cd31d256f52a45f839cb7de272b3deca6eee338a96c08b38da9076814d516b5`  
		Last Modified: Fri, 29 Aug 2025 17:33:03 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:512707d9128cd8badb8edd5168565f652d375d4cb981e3e7359c1ab67a0fdf3c`  
		Last Modified: Fri, 29 Aug 2025 17:33:03 GMT  
		Size: 828.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebab66b6a0be26be9392866319a8360a1516a1bc6ecf5efe4b2b7ab6d69a2222`  
		Last Modified: Fri, 29 Aug 2025 17:33:04 GMT  
		Size: 6.2 MB (6231503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e63be8c19281fc15dce3e70b954c2f37b48224b874afa4f684dc2ac1e534d76`  
		Last Modified: Fri, 29 Aug 2025 17:33:03 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd68a8cba102356cd65222b4bd6769d96d54d40ff9819507ebd547f873ae1675`  
		Last Modified: Fri, 29 Aug 2025 17:33:03 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6` - unknown; unknown

```console
$ docker pull spiped@sha256:4fe512ce76c7021740395ba0ce698366ca33c5df0d7ce00b59c0a3ce693568ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3635425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7a7c701338af6b5611e76e87c04e4cbe547754c92d981b9c41c20a059037dc5`

```dockerfile
```

-	Layers:
	-	`sha256:35fd43c927b6d65170b6e73cd99253106f56c0bf8fc00d210b8dea964ccf1dcd`  
		Last Modified: Fri, 29 Aug 2025 19:04:57 GMT  
		Size: 3.6 MB (3620266 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bb73fffccc386dde1f6a61868e0a17dac4f052ce75e90203b040b73bb2e1da12`  
		Last Modified: Fri, 29 Aug 2025 19:04:58 GMT  
		Size: 15.2 KB (15159 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6` - linux; 386

```console
$ docker pull spiped@sha256:e21fd11c4575ac83db30d0870ce8b1909393db426e769913e368989e42eb94ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.7 MB (37733752 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5df072e5a48747d0fb778894ace9e57e45756be4da3d4caf26b3f4e5958b1e83`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1754870400'
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
	-	`sha256:346d0c953bdbc38917a27a6f30726e5b46419d98ecaf4d2d8f201bc3b7025e57`  
		Last Modified: Tue, 12 Aug 2025 20:45:00 GMT  
		Size: 31.3 MB (31289378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f63f74a69468fc2acc1bd2a6ffd16aa7c3b461c719619504b4e208871e0a94a`  
		Last Modified: Fri, 29 Aug 2025 17:33:42 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a1520a614c988b98e1995e06613907c489562d65634c6a7e55f75cf975ac467`  
		Last Modified: Fri, 29 Aug 2025 17:33:42 GMT  
		Size: 828.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1ab6e794167d2c138d6e5986ae639a38571c7aa53eb5005fa3c0dc50621719a`  
		Last Modified: Fri, 29 Aug 2025 17:33:43 GMT  
		Size: 6.4 MB (6442003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d016b6b6bcd6d93a988faed26fd017a6f0109e6a0bd580557aabd037c2614064`  
		Last Modified: Fri, 29 Aug 2025 17:33:44 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10de62ac80528d9c9fd3232cb65ef310a09d9403cfdb7c96b5c77ba6662d707b`  
		Last Modified: Fri, 29 Aug 2025 17:33:40 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6` - unknown; unknown

```console
$ docker pull spiped@sha256:78575350c68a0455e8dba0b99c65d1f7c4de8ceea05c20ec5ad85e6a10fc1bbe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3634348 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7349d067f8d072b2300174cb9d9478cd11bf63a85a9b0ea56bd0f59064ce904`

```dockerfile
```

-	Layers:
	-	`sha256:f17ff7be52b05394f9faca48008984eb34022f2730306c4b5e4624081976cad8`  
		Last Modified: Fri, 29 Aug 2025 19:05:02 GMT  
		Size: 3.6 MB (3619359 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dd0a7e7a63f0f39246d0099e816021fb11f5aa955b1fbb2d27c3ab6e84d68e13`  
		Last Modified: Fri, 29 Aug 2025 19:05:03 GMT  
		Size: 15.0 KB (14989 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6` - linux; ppc64le

```console
$ docker pull spiped@sha256:d7e882296f82ff515c6b7e25d0fe26109721704e0290fc159c1237c1ad13bc20
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.4 MB (40436446 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d8c42f0b031d41a60ad454e14474cd9952b294e505c5fb6bfa1ec51d37b3020`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1754870400'
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
	-	`sha256:52a4daa8724e9e1632306e15fe478aa26ff0ebcb7ba924cb168e9b6738c239d5`  
		Last Modified: Wed, 13 Aug 2025 01:42:36 GMT  
		Size: 33.6 MB (33594213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc559a346c52f0f42d55a8b704817cf8a88d1b77699564e48a5b0b53030d0eeb`  
		Last Modified: Fri, 29 Aug 2025 17:34:00 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1b7971605e54829a0d8926db240a359db09df68c4a44aa1a10f39a3a3ca22fd`  
		Last Modified: Fri, 29 Aug 2025 17:34:02 GMT  
		Size: 829.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72fb014cef1414fead51e60f6f137d2813ad430172c6ed5b514d200d50958002`  
		Last Modified: Fri, 29 Aug 2025 17:34:03 GMT  
		Size: 6.8 MB (6839861 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c48e8c7818509d33221884ced67ec2035e0bda0e71821c41b9254bbe1b65c591`  
		Last Modified: Fri, 29 Aug 2025 17:34:02 GMT  
		Size: 94.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b035aa0e12be73b492a26f9066458209e72fa35a17bb5d5c3c33106051a6be46`  
		Last Modified: Fri, 29 Aug 2025 17:34:03 GMT  
		Size: 341.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6` - unknown; unknown

```console
$ docker pull spiped@sha256:b3d9482f09219f380e4497df9a4b15d28c8f3b75620e531d8b504549bdcc3599
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3636040 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8551f02e77ebbaa7e1b6613113354f909315dcd145b303c71015b92bf85172ff`

```dockerfile
```

-	Layers:
	-	`sha256:bb4fe81c44bf267a7b0a2be60b0a8f4414c39313dc7958eb14ee87ad8a40b3bb`  
		Last Modified: Fri, 29 Aug 2025 19:05:08 GMT  
		Size: 3.6 MB (3620967 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:361b1f0f6e13750899ca78a508eaa9dda9b4b0675918ee1604a65f9222852e5b`  
		Last Modified: Fri, 29 Aug 2025 19:05:09 GMT  
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
$ docker pull spiped@sha256:971a98798525dda6f9e7186f5f8f00c3a9a85971ef868e5735b240f305c01495
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.0 MB (35955636 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5dd452c0ad86184e337fb92ff500d9d975c2bf1ee1fc9f7fc16ed80c764c513f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1754870400'
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
	-	`sha256:bfe4d60a27c9392ab729f16b50a763cda36622d744066c3cf029a072133f2907`  
		Last Modified: Tue, 12 Aug 2025 20:59:52 GMT  
		Size: 29.8 MB (29833057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee1e72abadfa82b43b60b1f35da5ec06d5b929e2d36ee59ba7fac09b38158137`  
		Last Modified: Fri, 29 Aug 2025 17:34:35 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6da709972cad7ef527beb58c27162c5297d2898d6bbe37bf72a4ad0b875e8bf`  
		Last Modified: Fri, 29 Aug 2025 17:34:35 GMT  
		Size: 826.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c037b23c412da0dfcecac8846c67a23f22b94078b6d9ee11097ea1d4ffd2664`  
		Last Modified: Fri, 29 Aug 2025 17:34:37 GMT  
		Size: 6.1 MB (6120208 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c61027a0ec9d7ddedea31031c7852426e4aea9b6a68157f296eb16c027e5fd7`  
		Last Modified: Fri, 29 Aug 2025 17:34:35 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:983ddf74fd727cc9be924969a0e4160869a09753f21773195924b52e52e12c15`  
		Last Modified: Fri, 29 Aug 2025 17:34:35 GMT  
		Size: 341.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6` - unknown; unknown

```console
$ docker pull spiped@sha256:41b62f6c31ab522141ab290c3039ca5fc5f079667b5383ba00cb476f87e76126
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3632617 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f231a59432a7c83e6a6c2e773118bec44ee2a38536b02b7a5452c6c0aae17e1a`

```dockerfile
```

-	Layers:
	-	`sha256:27f2faa66bf854f32b888751318fc1bf861403f4abbbd02814273b92f265302d`  
		Last Modified: Fri, 29 Aug 2025 19:05:17 GMT  
		Size: 3.6 MB (3617593 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9ab13e11e4c038119bc34cceafc7cd53073417c92e76b936eac28da2501db8ba`  
		Last Modified: Fri, 29 Aug 2025 19:05:18 GMT  
		Size: 15.0 KB (15024 bytes)  
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
$ docker pull spiped@sha256:fa8cc1db019181c9115dd856665c7ecbfda6a245a420395ef8289ab28e82cfbf
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
$ docker pull spiped@sha256:3ef6a68bec16df3d49ac1119266e73804149779578c26208adfde5be4811db83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.8 MB (36823735 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d7fc64f06c4c58f0559d0930092fb12193ce356ed564676ef093a1f8cdc3c88`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1754870400'
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
	-	`sha256:396b1da7636e2dcd10565cb4f2f952cbb4a8a38b58d3b86a2cacb172fb70117c`  
		Last Modified: Tue, 12 Aug 2025 20:45:08 GMT  
		Size: 29.8 MB (29773285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0c4a6bf8c68ef3bb6ba597f3faca719888855ba6e3eb4fd0221f8005f88b578`  
		Last Modified: Fri, 29 Aug 2025 17:33:40 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8291215610373f818679d1441dc23d6414241c02b328a2d74c75ee6f43edb47`  
		Last Modified: Fri, 29 Aug 2025 17:33:40 GMT  
		Size: 828.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abfff1a4e7c04610b35cfa4681e2dc2aec187c18865702f204d9373f7f3937f1`  
		Last Modified: Fri, 29 Aug 2025 17:33:43 GMT  
		Size: 7.0 MB (7048080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74530c0255a2e254f8e851b46c40bbb1abcc79fe14a3a923182ea7f008eb953f`  
		Last Modified: Fri, 29 Aug 2025 17:33:40 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:447d4247cfd5b820273da6bbba318f8e21f2c9bcc28f55e93c200b6295b736af`  
		Last Modified: Fri, 29 Aug 2025 17:33:41 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6.4` - unknown; unknown

```console
$ docker pull spiped@sha256:fa6bf0713892c5beaaa9cc160afab5d917c5cc13ce70f6b55fbed9667e52e725
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3640255 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4352c813b000b4ffdd961f6bdb4cf2048d9001115ef073eba4864baa4351ccf`

```dockerfile
```

-	Layers:
	-	`sha256:17386d721162f1fe8cf87199caf138e7c670be8e7d3956e735eeb43813620dad`  
		Last Modified: Fri, 29 Aug 2025 19:04:40 GMT  
		Size: 3.6 MB (3625230 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1f26786168c5d5fd557db75e3200dfa805106b43e29c62eaefea65ace2df74d9`  
		Last Modified: Fri, 29 Aug 2025 19:04:41 GMT  
		Size: 15.0 KB (15025 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6.4` - linux; arm variant v5

```console
$ docker pull spiped@sha256:775c9a677f3eea419a2cfdab021bc73ea15a1f0eeabad8ddf5d109eaddebf987
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.7 MB (33733042 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:893a9f0c3890343e165b7a090fb3cf98522a2be3fb383bcc08279e28c97a307e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1754870400'
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
	-	`sha256:498399880872f14c562c46bd2a1ef4cfcf3c2a1453514ff0d0f6b7d89f8010dd`  
		Last Modified: Tue, 12 Aug 2025 22:02:01 GMT  
		Size: 27.9 MB (27941706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29082b3905ccb7de954a88ea955cbdf9a83dac9250d8d80de1abdeeafb051af4`  
		Last Modified: Fri, 29 Aug 2025 17:33:08 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1c8b3da67e1ae83930836f15a6bc2326925939ceb8bfde62fd3c1be32e4ff63`  
		Last Modified: Fri, 29 Aug 2025 17:33:08 GMT  
		Size: 832.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3bd6dfd17377cd518eefa5090b847afb64042f8ca7301629e498c40bd76fc18`  
		Last Modified: Fri, 29 Aug 2025 17:33:09 GMT  
		Size: 5.8 MB (5788961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4925ddd4cbbd4e0f0552eb8d7bd4dc917105d66235cd2aa023f1ced94b42dac8`  
		Last Modified: Fri, 29 Aug 2025 17:33:08 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79e22b81fbccf50276e0a0119e314ddd089195fde3023a114e1710efb08360da`  
		Last Modified: Fri, 29 Aug 2025 17:40:24 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6.4` - unknown; unknown

```console
$ docker pull spiped@sha256:e0dcda5aa6d420f41e885934e8d19deadc188142ed26721c7a8729f72fce03cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3633351 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc99de0b923227b61b33d206e2167d77c4a5635d6d82e71675287b766e9aa71a`

```dockerfile
```

-	Layers:
	-	`sha256:1e4d10b7dbe06386b35f345b0a4bed1e6524b04934b277901c20ef1f41a0a193`  
		Last Modified: Fri, 29 Aug 2025 19:04:46 GMT  
		Size: 3.6 MB (3618224 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8165e679713497e1a387bddb798c12153bc4d22f642cf83469cad62339033d49`  
		Last Modified: Fri, 29 Aug 2025 19:04:47 GMT  
		Size: 15.1 KB (15127 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6.4` - linux; arm variant v7

```console
$ docker pull spiped@sha256:f87b2e8141e5dc0e1e06c580713a5ebe8a2c260f244f7bdcdea78714f00cc3b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.8 MB (31794250 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a3b9065cf06fdf2af1c2a24ea909722d65b64439387288f2672b8efc6a1038f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1754870400'
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
	-	`sha256:d480d07cd33d2a61cb24d871a17254661d250ae887a2db15a7e99cb67383a74e`  
		Last Modified: Tue, 12 Aug 2025 20:52:10 GMT  
		Size: 26.2 MB (26207488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fecbe4210c70bc3e538dad13a5f8a4ee3ab0d106268e42dfa80a971ac77bc0d`  
		Last Modified: Fri, 29 Aug 2025 17:32:58 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34148ed6b26e88d3d7a7c3a98fbae82c52c329016d3eca423a16836a07c9dbce`  
		Last Modified: Fri, 29 Aug 2025 17:32:58 GMT  
		Size: 825.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d256a5a77b507a955cf7e3d03a7166949da3e560460b1000011e054979d70628`  
		Last Modified: Fri, 29 Aug 2025 17:33:00 GMT  
		Size: 5.6 MB (5584393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:656c2e207f2bd9664ca3591eeab603fe4ad05be7ffcd8dfc7761b6db836bed35`  
		Last Modified: Fri, 29 Aug 2025 17:32:58 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d750cbed80655934a514a4ee40e186bdc38155dd958c3ac037e0917fa5a5245`  
		Last Modified: Fri, 29 Aug 2025 17:32:58 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6.4` - unknown; unknown

```console
$ docker pull spiped@sha256:6ae77ff0bcf2a50f789f2f2841bbcc896e112247136781bc0da91bb058553cee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3632472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25492705ffccd901687c0f01d38b16fb5481183837785fea959754d2cb317b31`

```dockerfile
```

-	Layers:
	-	`sha256:23eee19f68a1b7930f8f02e0e2999d1a94a6d7b6625e68882288d71bc6e1b5d8`  
		Last Modified: Fri, 29 Aug 2025 19:04:51 GMT  
		Size: 3.6 MB (3617345 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c82d8e54a24d0f61dd4f978f5a9aa7fa21b8488a559050cf0499ddf07326fc95`  
		Last Modified: Fri, 29 Aug 2025 19:04:52 GMT  
		Size: 15.1 KB (15127 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6.4` - linux; arm64 variant v8

```console
$ docker pull spiped@sha256:bf441e6b20fe3c68abd00975a9de044d99b6902c4f105b9b4d5fcca621f4f163
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.4 MB (36369917 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6324fc3857cd905718785b4db6d60827bbbdb477417615b2bfc9c9a8d249a95`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1754870400'
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
	-	`sha256:9a6263cdeaa5d408640880103ee36920ef814974ca8e2674412ad6460e8968c9`  
		Last Modified: Tue, 12 Aug 2025 22:12:42 GMT  
		Size: 30.1 MB (30136044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cd31d256f52a45f839cb7de272b3deca6eee338a96c08b38da9076814d516b5`  
		Last Modified: Fri, 29 Aug 2025 17:33:03 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:512707d9128cd8badb8edd5168565f652d375d4cb981e3e7359c1ab67a0fdf3c`  
		Last Modified: Fri, 29 Aug 2025 17:33:03 GMT  
		Size: 828.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebab66b6a0be26be9392866319a8360a1516a1bc6ecf5efe4b2b7ab6d69a2222`  
		Last Modified: Fri, 29 Aug 2025 17:33:04 GMT  
		Size: 6.2 MB (6231503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e63be8c19281fc15dce3e70b954c2f37b48224b874afa4f684dc2ac1e534d76`  
		Last Modified: Fri, 29 Aug 2025 17:33:03 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd68a8cba102356cd65222b4bd6769d96d54d40ff9819507ebd547f873ae1675`  
		Last Modified: Fri, 29 Aug 2025 17:33:03 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6.4` - unknown; unknown

```console
$ docker pull spiped@sha256:4fe512ce76c7021740395ba0ce698366ca33c5df0d7ce00b59c0a3ce693568ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3635425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7a7c701338af6b5611e76e87c04e4cbe547754c92d981b9c41c20a059037dc5`

```dockerfile
```

-	Layers:
	-	`sha256:35fd43c927b6d65170b6e73cd99253106f56c0bf8fc00d210b8dea964ccf1dcd`  
		Last Modified: Fri, 29 Aug 2025 19:04:57 GMT  
		Size: 3.6 MB (3620266 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bb73fffccc386dde1f6a61868e0a17dac4f052ce75e90203b040b73bb2e1da12`  
		Last Modified: Fri, 29 Aug 2025 19:04:58 GMT  
		Size: 15.2 KB (15159 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6.4` - linux; 386

```console
$ docker pull spiped@sha256:e21fd11c4575ac83db30d0870ce8b1909393db426e769913e368989e42eb94ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.7 MB (37733752 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5df072e5a48747d0fb778894ace9e57e45756be4da3d4caf26b3f4e5958b1e83`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1754870400'
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
	-	`sha256:346d0c953bdbc38917a27a6f30726e5b46419d98ecaf4d2d8f201bc3b7025e57`  
		Last Modified: Tue, 12 Aug 2025 20:45:00 GMT  
		Size: 31.3 MB (31289378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f63f74a69468fc2acc1bd2a6ffd16aa7c3b461c719619504b4e208871e0a94a`  
		Last Modified: Fri, 29 Aug 2025 17:33:42 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a1520a614c988b98e1995e06613907c489562d65634c6a7e55f75cf975ac467`  
		Last Modified: Fri, 29 Aug 2025 17:33:42 GMT  
		Size: 828.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1ab6e794167d2c138d6e5986ae639a38571c7aa53eb5005fa3c0dc50621719a`  
		Last Modified: Fri, 29 Aug 2025 17:33:43 GMT  
		Size: 6.4 MB (6442003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d016b6b6bcd6d93a988faed26fd017a6f0109e6a0bd580557aabd037c2614064`  
		Last Modified: Fri, 29 Aug 2025 17:33:44 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10de62ac80528d9c9fd3232cb65ef310a09d9403cfdb7c96b5c77ba6662d707b`  
		Last Modified: Fri, 29 Aug 2025 17:33:40 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6.4` - unknown; unknown

```console
$ docker pull spiped@sha256:78575350c68a0455e8dba0b99c65d1f7c4de8ceea05c20ec5ad85e6a10fc1bbe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3634348 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7349d067f8d072b2300174cb9d9478cd11bf63a85a9b0ea56bd0f59064ce904`

```dockerfile
```

-	Layers:
	-	`sha256:f17ff7be52b05394f9faca48008984eb34022f2730306c4b5e4624081976cad8`  
		Last Modified: Fri, 29 Aug 2025 19:05:02 GMT  
		Size: 3.6 MB (3619359 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dd0a7e7a63f0f39246d0099e816021fb11f5aa955b1fbb2d27c3ab6e84d68e13`  
		Last Modified: Fri, 29 Aug 2025 19:05:03 GMT  
		Size: 15.0 KB (14989 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6.4` - linux; ppc64le

```console
$ docker pull spiped@sha256:d7e882296f82ff515c6b7e25d0fe26109721704e0290fc159c1237c1ad13bc20
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.4 MB (40436446 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d8c42f0b031d41a60ad454e14474cd9952b294e505c5fb6bfa1ec51d37b3020`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1754870400'
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
	-	`sha256:52a4daa8724e9e1632306e15fe478aa26ff0ebcb7ba924cb168e9b6738c239d5`  
		Last Modified: Wed, 13 Aug 2025 01:42:36 GMT  
		Size: 33.6 MB (33594213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc559a346c52f0f42d55a8b704817cf8a88d1b77699564e48a5b0b53030d0eeb`  
		Last Modified: Fri, 29 Aug 2025 17:34:00 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1b7971605e54829a0d8926db240a359db09df68c4a44aa1a10f39a3a3ca22fd`  
		Last Modified: Fri, 29 Aug 2025 17:34:02 GMT  
		Size: 829.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72fb014cef1414fead51e60f6f137d2813ad430172c6ed5b514d200d50958002`  
		Last Modified: Fri, 29 Aug 2025 17:34:03 GMT  
		Size: 6.8 MB (6839861 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c48e8c7818509d33221884ced67ec2035e0bda0e71821c41b9254bbe1b65c591`  
		Last Modified: Fri, 29 Aug 2025 17:34:02 GMT  
		Size: 94.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b035aa0e12be73b492a26f9066458209e72fa35a17bb5d5c3c33106051a6be46`  
		Last Modified: Fri, 29 Aug 2025 17:34:03 GMT  
		Size: 341.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6.4` - unknown; unknown

```console
$ docker pull spiped@sha256:b3d9482f09219f380e4497df9a4b15d28c8f3b75620e531d8b504549bdcc3599
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3636040 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8551f02e77ebbaa7e1b6613113354f909315dcd145b303c71015b92bf85172ff`

```dockerfile
```

-	Layers:
	-	`sha256:bb4fe81c44bf267a7b0a2be60b0a8f4414c39313dc7958eb14ee87ad8a40b3bb`  
		Last Modified: Fri, 29 Aug 2025 19:05:08 GMT  
		Size: 3.6 MB (3620967 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:361b1f0f6e13750899ca78a508eaa9dda9b4b0675918ee1604a65f9222852e5b`  
		Last Modified: Fri, 29 Aug 2025 19:05:09 GMT  
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
$ docker pull spiped@sha256:971a98798525dda6f9e7186f5f8f00c3a9a85971ef868e5735b240f305c01495
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.0 MB (35955636 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5dd452c0ad86184e337fb92ff500d9d975c2bf1ee1fc9f7fc16ed80c764c513f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1754870400'
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
	-	`sha256:bfe4d60a27c9392ab729f16b50a763cda36622d744066c3cf029a072133f2907`  
		Last Modified: Tue, 12 Aug 2025 20:59:52 GMT  
		Size: 29.8 MB (29833057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee1e72abadfa82b43b60b1f35da5ec06d5b929e2d36ee59ba7fac09b38158137`  
		Last Modified: Fri, 29 Aug 2025 17:34:35 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6da709972cad7ef527beb58c27162c5297d2898d6bbe37bf72a4ad0b875e8bf`  
		Last Modified: Fri, 29 Aug 2025 17:34:35 GMT  
		Size: 826.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c037b23c412da0dfcecac8846c67a23f22b94078b6d9ee11097ea1d4ffd2664`  
		Last Modified: Fri, 29 Aug 2025 17:34:37 GMT  
		Size: 6.1 MB (6120208 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c61027a0ec9d7ddedea31031c7852426e4aea9b6a68157f296eb16c027e5fd7`  
		Last Modified: Fri, 29 Aug 2025 17:34:35 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:983ddf74fd727cc9be924969a0e4160869a09753f21773195924b52e52e12c15`  
		Last Modified: Fri, 29 Aug 2025 17:34:35 GMT  
		Size: 341.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6.4` - unknown; unknown

```console
$ docker pull spiped@sha256:41b62f6c31ab522141ab290c3039ca5fc5f079667b5383ba00cb476f87e76126
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3632617 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f231a59432a7c83e6a6c2e773118bec44ee2a38536b02b7a5452c6c0aae17e1a`

```dockerfile
```

-	Layers:
	-	`sha256:27f2faa66bf854f32b888751318fc1bf861403f4abbbd02814273b92f265302d`  
		Last Modified: Fri, 29 Aug 2025 19:05:17 GMT  
		Size: 3.6 MB (3617593 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9ab13e11e4c038119bc34cceafc7cd53073417c92e76b936eac28da2501db8ba`  
		Last Modified: Fri, 29 Aug 2025 19:05:18 GMT  
		Size: 15.0 KB (15024 bytes)  
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
$ docker pull spiped@sha256:fa8cc1db019181c9115dd856665c7ecbfda6a245a420395ef8289ab28e82cfbf
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
$ docker pull spiped@sha256:3ef6a68bec16df3d49ac1119266e73804149779578c26208adfde5be4811db83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.8 MB (36823735 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d7fc64f06c4c58f0559d0930092fb12193ce356ed564676ef093a1f8cdc3c88`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1754870400'
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
	-	`sha256:396b1da7636e2dcd10565cb4f2f952cbb4a8a38b58d3b86a2cacb172fb70117c`  
		Last Modified: Tue, 12 Aug 2025 20:45:08 GMT  
		Size: 29.8 MB (29773285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0c4a6bf8c68ef3bb6ba597f3faca719888855ba6e3eb4fd0221f8005f88b578`  
		Last Modified: Fri, 29 Aug 2025 17:33:40 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8291215610373f818679d1441dc23d6414241c02b328a2d74c75ee6f43edb47`  
		Last Modified: Fri, 29 Aug 2025 17:33:40 GMT  
		Size: 828.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abfff1a4e7c04610b35cfa4681e2dc2aec187c18865702f204d9373f7f3937f1`  
		Last Modified: Fri, 29 Aug 2025 17:33:43 GMT  
		Size: 7.0 MB (7048080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74530c0255a2e254f8e851b46c40bbb1abcc79fe14a3a923182ea7f008eb953f`  
		Last Modified: Fri, 29 Aug 2025 17:33:40 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:447d4247cfd5b820273da6bbba318f8e21f2c9bcc28f55e93c200b6295b736af`  
		Last Modified: Fri, 29 Aug 2025 17:33:41 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:latest` - unknown; unknown

```console
$ docker pull spiped@sha256:fa6bf0713892c5beaaa9cc160afab5d917c5cc13ce70f6b55fbed9667e52e725
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3640255 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4352c813b000b4ffdd961f6bdb4cf2048d9001115ef073eba4864baa4351ccf`

```dockerfile
```

-	Layers:
	-	`sha256:17386d721162f1fe8cf87199caf138e7c670be8e7d3956e735eeb43813620dad`  
		Last Modified: Fri, 29 Aug 2025 19:04:40 GMT  
		Size: 3.6 MB (3625230 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1f26786168c5d5fd557db75e3200dfa805106b43e29c62eaefea65ace2df74d9`  
		Last Modified: Fri, 29 Aug 2025 19:04:41 GMT  
		Size: 15.0 KB (15025 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:latest` - linux; arm variant v5

```console
$ docker pull spiped@sha256:775c9a677f3eea419a2cfdab021bc73ea15a1f0eeabad8ddf5d109eaddebf987
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.7 MB (33733042 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:893a9f0c3890343e165b7a090fb3cf98522a2be3fb383bcc08279e28c97a307e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1754870400'
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
	-	`sha256:498399880872f14c562c46bd2a1ef4cfcf3c2a1453514ff0d0f6b7d89f8010dd`  
		Last Modified: Tue, 12 Aug 2025 22:02:01 GMT  
		Size: 27.9 MB (27941706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29082b3905ccb7de954a88ea955cbdf9a83dac9250d8d80de1abdeeafb051af4`  
		Last Modified: Fri, 29 Aug 2025 17:33:08 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1c8b3da67e1ae83930836f15a6bc2326925939ceb8bfde62fd3c1be32e4ff63`  
		Last Modified: Fri, 29 Aug 2025 17:33:08 GMT  
		Size: 832.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3bd6dfd17377cd518eefa5090b847afb64042f8ca7301629e498c40bd76fc18`  
		Last Modified: Fri, 29 Aug 2025 17:33:09 GMT  
		Size: 5.8 MB (5788961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4925ddd4cbbd4e0f0552eb8d7bd4dc917105d66235cd2aa023f1ced94b42dac8`  
		Last Modified: Fri, 29 Aug 2025 17:33:08 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79e22b81fbccf50276e0a0119e314ddd089195fde3023a114e1710efb08360da`  
		Last Modified: Fri, 29 Aug 2025 17:40:24 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:latest` - unknown; unknown

```console
$ docker pull spiped@sha256:e0dcda5aa6d420f41e885934e8d19deadc188142ed26721c7a8729f72fce03cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3633351 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc99de0b923227b61b33d206e2167d77c4a5635d6d82e71675287b766e9aa71a`

```dockerfile
```

-	Layers:
	-	`sha256:1e4d10b7dbe06386b35f345b0a4bed1e6524b04934b277901c20ef1f41a0a193`  
		Last Modified: Fri, 29 Aug 2025 19:04:46 GMT  
		Size: 3.6 MB (3618224 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8165e679713497e1a387bddb798c12153bc4d22f642cf83469cad62339033d49`  
		Last Modified: Fri, 29 Aug 2025 19:04:47 GMT  
		Size: 15.1 KB (15127 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:latest` - linux; arm variant v7

```console
$ docker pull spiped@sha256:f87b2e8141e5dc0e1e06c580713a5ebe8a2c260f244f7bdcdea78714f00cc3b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.8 MB (31794250 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a3b9065cf06fdf2af1c2a24ea909722d65b64439387288f2672b8efc6a1038f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1754870400'
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
	-	`sha256:d480d07cd33d2a61cb24d871a17254661d250ae887a2db15a7e99cb67383a74e`  
		Last Modified: Tue, 12 Aug 2025 20:52:10 GMT  
		Size: 26.2 MB (26207488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fecbe4210c70bc3e538dad13a5f8a4ee3ab0d106268e42dfa80a971ac77bc0d`  
		Last Modified: Fri, 29 Aug 2025 17:32:58 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34148ed6b26e88d3d7a7c3a98fbae82c52c329016d3eca423a16836a07c9dbce`  
		Last Modified: Fri, 29 Aug 2025 17:32:58 GMT  
		Size: 825.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d256a5a77b507a955cf7e3d03a7166949da3e560460b1000011e054979d70628`  
		Last Modified: Fri, 29 Aug 2025 17:33:00 GMT  
		Size: 5.6 MB (5584393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:656c2e207f2bd9664ca3591eeab603fe4ad05be7ffcd8dfc7761b6db836bed35`  
		Last Modified: Fri, 29 Aug 2025 17:32:58 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d750cbed80655934a514a4ee40e186bdc38155dd958c3ac037e0917fa5a5245`  
		Last Modified: Fri, 29 Aug 2025 17:32:58 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:latest` - unknown; unknown

```console
$ docker pull spiped@sha256:6ae77ff0bcf2a50f789f2f2841bbcc896e112247136781bc0da91bb058553cee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3632472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25492705ffccd901687c0f01d38b16fb5481183837785fea959754d2cb317b31`

```dockerfile
```

-	Layers:
	-	`sha256:23eee19f68a1b7930f8f02e0e2999d1a94a6d7b6625e68882288d71bc6e1b5d8`  
		Last Modified: Fri, 29 Aug 2025 19:04:51 GMT  
		Size: 3.6 MB (3617345 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c82d8e54a24d0f61dd4f978f5a9aa7fa21b8488a559050cf0499ddf07326fc95`  
		Last Modified: Fri, 29 Aug 2025 19:04:52 GMT  
		Size: 15.1 KB (15127 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:latest` - linux; arm64 variant v8

```console
$ docker pull spiped@sha256:bf441e6b20fe3c68abd00975a9de044d99b6902c4f105b9b4d5fcca621f4f163
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.4 MB (36369917 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6324fc3857cd905718785b4db6d60827bbbdb477417615b2bfc9c9a8d249a95`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1754870400'
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
	-	`sha256:9a6263cdeaa5d408640880103ee36920ef814974ca8e2674412ad6460e8968c9`  
		Last Modified: Tue, 12 Aug 2025 22:12:42 GMT  
		Size: 30.1 MB (30136044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cd31d256f52a45f839cb7de272b3deca6eee338a96c08b38da9076814d516b5`  
		Last Modified: Fri, 29 Aug 2025 17:33:03 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:512707d9128cd8badb8edd5168565f652d375d4cb981e3e7359c1ab67a0fdf3c`  
		Last Modified: Fri, 29 Aug 2025 17:33:03 GMT  
		Size: 828.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebab66b6a0be26be9392866319a8360a1516a1bc6ecf5efe4b2b7ab6d69a2222`  
		Last Modified: Fri, 29 Aug 2025 17:33:04 GMT  
		Size: 6.2 MB (6231503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e63be8c19281fc15dce3e70b954c2f37b48224b874afa4f684dc2ac1e534d76`  
		Last Modified: Fri, 29 Aug 2025 17:33:03 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd68a8cba102356cd65222b4bd6769d96d54d40ff9819507ebd547f873ae1675`  
		Last Modified: Fri, 29 Aug 2025 17:33:03 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:latest` - unknown; unknown

```console
$ docker pull spiped@sha256:4fe512ce76c7021740395ba0ce698366ca33c5df0d7ce00b59c0a3ce693568ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3635425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7a7c701338af6b5611e76e87c04e4cbe547754c92d981b9c41c20a059037dc5`

```dockerfile
```

-	Layers:
	-	`sha256:35fd43c927b6d65170b6e73cd99253106f56c0bf8fc00d210b8dea964ccf1dcd`  
		Last Modified: Fri, 29 Aug 2025 19:04:57 GMT  
		Size: 3.6 MB (3620266 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bb73fffccc386dde1f6a61868e0a17dac4f052ce75e90203b040b73bb2e1da12`  
		Last Modified: Fri, 29 Aug 2025 19:04:58 GMT  
		Size: 15.2 KB (15159 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:latest` - linux; 386

```console
$ docker pull spiped@sha256:e21fd11c4575ac83db30d0870ce8b1909393db426e769913e368989e42eb94ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.7 MB (37733752 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5df072e5a48747d0fb778894ace9e57e45756be4da3d4caf26b3f4e5958b1e83`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1754870400'
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
	-	`sha256:346d0c953bdbc38917a27a6f30726e5b46419d98ecaf4d2d8f201bc3b7025e57`  
		Last Modified: Tue, 12 Aug 2025 20:45:00 GMT  
		Size: 31.3 MB (31289378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f63f74a69468fc2acc1bd2a6ffd16aa7c3b461c719619504b4e208871e0a94a`  
		Last Modified: Fri, 29 Aug 2025 17:33:42 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a1520a614c988b98e1995e06613907c489562d65634c6a7e55f75cf975ac467`  
		Last Modified: Fri, 29 Aug 2025 17:33:42 GMT  
		Size: 828.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1ab6e794167d2c138d6e5986ae639a38571c7aa53eb5005fa3c0dc50621719a`  
		Last Modified: Fri, 29 Aug 2025 17:33:43 GMT  
		Size: 6.4 MB (6442003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d016b6b6bcd6d93a988faed26fd017a6f0109e6a0bd580557aabd037c2614064`  
		Last Modified: Fri, 29 Aug 2025 17:33:44 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10de62ac80528d9c9fd3232cb65ef310a09d9403cfdb7c96b5c77ba6662d707b`  
		Last Modified: Fri, 29 Aug 2025 17:33:40 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:latest` - unknown; unknown

```console
$ docker pull spiped@sha256:78575350c68a0455e8dba0b99c65d1f7c4de8ceea05c20ec5ad85e6a10fc1bbe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3634348 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7349d067f8d072b2300174cb9d9478cd11bf63a85a9b0ea56bd0f59064ce904`

```dockerfile
```

-	Layers:
	-	`sha256:f17ff7be52b05394f9faca48008984eb34022f2730306c4b5e4624081976cad8`  
		Last Modified: Fri, 29 Aug 2025 19:05:02 GMT  
		Size: 3.6 MB (3619359 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dd0a7e7a63f0f39246d0099e816021fb11f5aa955b1fbb2d27c3ab6e84d68e13`  
		Last Modified: Fri, 29 Aug 2025 19:05:03 GMT  
		Size: 15.0 KB (14989 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:latest` - linux; ppc64le

```console
$ docker pull spiped@sha256:d7e882296f82ff515c6b7e25d0fe26109721704e0290fc159c1237c1ad13bc20
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.4 MB (40436446 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d8c42f0b031d41a60ad454e14474cd9952b294e505c5fb6bfa1ec51d37b3020`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1754870400'
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
	-	`sha256:52a4daa8724e9e1632306e15fe478aa26ff0ebcb7ba924cb168e9b6738c239d5`  
		Last Modified: Wed, 13 Aug 2025 01:42:36 GMT  
		Size: 33.6 MB (33594213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc559a346c52f0f42d55a8b704817cf8a88d1b77699564e48a5b0b53030d0eeb`  
		Last Modified: Fri, 29 Aug 2025 17:34:00 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1b7971605e54829a0d8926db240a359db09df68c4a44aa1a10f39a3a3ca22fd`  
		Last Modified: Fri, 29 Aug 2025 17:34:02 GMT  
		Size: 829.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72fb014cef1414fead51e60f6f137d2813ad430172c6ed5b514d200d50958002`  
		Last Modified: Fri, 29 Aug 2025 17:34:03 GMT  
		Size: 6.8 MB (6839861 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c48e8c7818509d33221884ced67ec2035e0bda0e71821c41b9254bbe1b65c591`  
		Last Modified: Fri, 29 Aug 2025 17:34:02 GMT  
		Size: 94.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b035aa0e12be73b492a26f9066458209e72fa35a17bb5d5c3c33106051a6be46`  
		Last Modified: Fri, 29 Aug 2025 17:34:03 GMT  
		Size: 341.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:latest` - unknown; unknown

```console
$ docker pull spiped@sha256:b3d9482f09219f380e4497df9a4b15d28c8f3b75620e531d8b504549bdcc3599
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3636040 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8551f02e77ebbaa7e1b6613113354f909315dcd145b303c71015b92bf85172ff`

```dockerfile
```

-	Layers:
	-	`sha256:bb4fe81c44bf267a7b0a2be60b0a8f4414c39313dc7958eb14ee87ad8a40b3bb`  
		Last Modified: Fri, 29 Aug 2025 19:05:08 GMT  
		Size: 3.6 MB (3620967 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:361b1f0f6e13750899ca78a508eaa9dda9b4b0675918ee1604a65f9222852e5b`  
		Last Modified: Fri, 29 Aug 2025 19:05:09 GMT  
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
$ docker pull spiped@sha256:971a98798525dda6f9e7186f5f8f00c3a9a85971ef868e5735b240f305c01495
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.0 MB (35955636 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5dd452c0ad86184e337fb92ff500d9d975c2bf1ee1fc9f7fc16ed80c764c513f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1754870400'
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
	-	`sha256:bfe4d60a27c9392ab729f16b50a763cda36622d744066c3cf029a072133f2907`  
		Last Modified: Tue, 12 Aug 2025 20:59:52 GMT  
		Size: 29.8 MB (29833057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee1e72abadfa82b43b60b1f35da5ec06d5b929e2d36ee59ba7fac09b38158137`  
		Last Modified: Fri, 29 Aug 2025 17:34:35 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6da709972cad7ef527beb58c27162c5297d2898d6bbe37bf72a4ad0b875e8bf`  
		Last Modified: Fri, 29 Aug 2025 17:34:35 GMT  
		Size: 826.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c037b23c412da0dfcecac8846c67a23f22b94078b6d9ee11097ea1d4ffd2664`  
		Last Modified: Fri, 29 Aug 2025 17:34:37 GMT  
		Size: 6.1 MB (6120208 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c61027a0ec9d7ddedea31031c7852426e4aea9b6a68157f296eb16c027e5fd7`  
		Last Modified: Fri, 29 Aug 2025 17:34:35 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:983ddf74fd727cc9be924969a0e4160869a09753f21773195924b52e52e12c15`  
		Last Modified: Fri, 29 Aug 2025 17:34:35 GMT  
		Size: 341.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:latest` - unknown; unknown

```console
$ docker pull spiped@sha256:41b62f6c31ab522141ab290c3039ca5fc5f079667b5383ba00cb476f87e76126
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3632617 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f231a59432a7c83e6a6c2e773118bec44ee2a38536b02b7a5452c6c0aae17e1a`

```dockerfile
```

-	Layers:
	-	`sha256:27f2faa66bf854f32b888751318fc1bf861403f4abbbd02814273b92f265302d`  
		Last Modified: Fri, 29 Aug 2025 19:05:17 GMT  
		Size: 3.6 MB (3617593 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9ab13e11e4c038119bc34cceafc7cd53073417c92e76b936eac28da2501db8ba`  
		Last Modified: Fri, 29 Aug 2025 19:05:18 GMT  
		Size: 15.0 KB (15024 bytes)  
		MIME: application/vnd.in-toto+json
