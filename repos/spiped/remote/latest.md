## `spiped:latest`

```console
$ docker pull spiped@sha256:973e4d87d0da873d90f4034c1d77e7f888b47cd75847332e6d4ed19501df0b4c
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
$ docker pull spiped@sha256:77683e090b064dc957d75c77935a82e42c2a1fbf2232bd03984c11f4e1a3a541
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.8 MB (36824237 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2b91e64b96880f5eb6ddb6ac876f8512e03516ad8c871b8d3d4a0b04ca7e427`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 02:03:17 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Tue, 13 Jan 2026 02:03:19 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 02:03:40 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Tue, 13 Jan 2026 02:03:40 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 13 Jan 2026 02:03:40 GMT
VOLUME [/spiped]
# Tue, 13 Jan 2026 02:03:40 GMT
WORKDIR /spiped
# Tue, 13 Jan 2026 02:03:40 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Tue, 13 Jan 2026 02:03:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 13 Jan 2026 02:03:40 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:119d43eec815e5f9a47da3a7d59454581b1e204b0c34db86f171b7ceb3336533`  
		Last Modified: Tue, 13 Jan 2026 00:42:27 GMT  
		Size: 29.8 MB (29773685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f07f421fd20c1878c7dd6ac59c398f0364e0f88eab610f6e57b43bca361b5e5e`  
		Last Modified: Tue, 13 Jan 2026 02:03:48 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:058788ff9125ab88746594dc01afd97e7e996a3e4d8b3f6856fcd44171dc482c`  
		Last Modified: Tue, 13 Jan 2026 02:03:48 GMT  
		Size: 828.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18ec8d179871657e1ab7f3a16a0e30233e7d9d7c36f40940a4e82f4aa132e064`  
		Last Modified: Tue, 13 Jan 2026 02:03:49 GMT  
		Size: 7.0 MB (7048182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:301a16ed5f26fff36bf5bef8d54749c1a96204be067088a99a9d5af8ef22e777`  
		Last Modified: Tue, 13 Jan 2026 02:03:48 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05a0bc16a722dd63c79b2cc30dbad0c6b7ef6df3520ac9b1d63ec3a186a54777`  
		Last Modified: Tue, 13 Jan 2026 02:03:49 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:latest` - unknown; unknown

```console
$ docker pull spiped@sha256:c941c0105587dab559666d5f118c62d4436b75df7570b251b0a6bcf8676d244e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3641206 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8050f3279ff98be53b688006a5763a82f5c062d4c55718fa03f4321e24fb2ad6`

```dockerfile
```

-	Layers:
	-	`sha256:b955459c9cfcdb977ba5cc37f7d667ddf681c863f9638cf81a57944495c6fd2a`  
		Last Modified: Tue, 13 Jan 2026 02:03:48 GMT  
		Size: 3.6 MB (3626224 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:362389aee666db610977c4428258e498959b82449b814b6fa9e3895f290ffbda`  
		Last Modified: Tue, 13 Jan 2026 02:03:48 GMT  
		Size: 15.0 KB (14982 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:latest` - linux; arm variant v5

```console
$ docker pull spiped@sha256:f49dbd6876881040f8a97794963ab8f897e27d420d774fa7f836d0a98b197b93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.7 MB (33734522 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb94a1967baa51559b21a9fd3b60819b7c57c18416324a0e2e7bd9d619368a0c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 02:28:00 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Tue, 13 Jan 2026 02:28:05 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 02:28:31 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Tue, 13 Jan 2026 02:28:31 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 13 Jan 2026 02:28:31 GMT
VOLUME [/spiped]
# Tue, 13 Jan 2026 02:28:31 GMT
WORKDIR /spiped
# Tue, 13 Jan 2026 02:28:31 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Tue, 13 Jan 2026 02:28:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 13 Jan 2026 02:28:31 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:c113d410d30c2c035a105b56d3937958c81fbe2530f44add3bae903be6864324`  
		Last Modified: Tue, 13 Jan 2026 00:42:23 GMT  
		Size: 27.9 MB (27942724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21f58043e9c53785e6a9ee6666072775194d0f1f78ffaa364100d13c3702af68`  
		Last Modified: Tue, 13 Jan 2026 02:28:39 GMT  
		Size: 1.1 KB (1105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a93792ca404d5989c68276c7f1b92fcdcb0533835eec176619a1c17eb300ceab`  
		Last Modified: Tue, 13 Jan 2026 02:28:39 GMT  
		Size: 832.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3770096adf56bffd20a1371e4ba64990c5a432e11a9083c27ae393be70f81bdc`  
		Last Modified: Tue, 13 Jan 2026 02:28:39 GMT  
		Size: 5.8 MB (5789426 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f773528ba233ec37e7021415709fd47085703caa44200a4c5e298b4b238c7cf1`  
		Last Modified: Tue, 13 Jan 2026 02:28:39 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13a6adad206d03b1f700eae49a87374fde73e14f45ef3ef3282e8c46c9c19fef`  
		Last Modified: Tue, 13 Jan 2026 02:28:40 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:latest` - unknown; unknown

```console
$ docker pull spiped@sha256:05cf26b49e987b8fc5e5b1f95f08b4bbe2a41888c7a1dfc8d053ddbcf55dad6d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3634305 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0fb169b5bfc92299e8ebb8077f8e988ce368962802bd4f74219eb94cd779898`

```dockerfile
```

-	Layers:
	-	`sha256:66f9d6574372b68f7b40a0ebd018c7a04cf087116275d9427ab683875705cd88`  
		Last Modified: Tue, 13 Jan 2026 02:28:39 GMT  
		Size: 3.6 MB (3619218 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1c7d7693bcee2e2c3ef0d1768be5c428dc8e5cbf4bc0888c6260d2e4bc83f40c`  
		Last Modified: Tue, 13 Jan 2026 02:28:39 GMT  
		Size: 15.1 KB (15087 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:latest` - linux; arm variant v7

```console
$ docker pull spiped@sha256:e22c673bc5d3436255cf303a33da07e04e0a0c747aa84e63a034bb76f251b463
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.8 MB (31795581 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb7e0e036e754ae2a08aeef463c97a2bc97f4e49e1bce5eae5cef5f8afcaf66e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 02:50:15 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Tue, 13 Jan 2026 02:50:18 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 02:50:42 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Tue, 13 Jan 2026 02:50:42 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 13 Jan 2026 02:50:42 GMT
VOLUME [/spiped]
# Tue, 13 Jan 2026 02:50:42 GMT
WORKDIR /spiped
# Tue, 13 Jan 2026 02:50:42 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Tue, 13 Jan 2026 02:50:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 13 Jan 2026 02:50:42 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:7c33f0ee8e5c8636ae24c5685841e42e721bbb2973888f046a05ab9eb619e682`  
		Last Modified: Tue, 13 Jan 2026 00:42:23 GMT  
		Size: 26.2 MB (26208578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85bf60274842280b1741a2bd3a5c311abf4da24fba1e7fa8e7459c924f276be5`  
		Last Modified: Tue, 13 Jan 2026 02:50:49 GMT  
		Size: 1.1 KB (1105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7caeb66a3ecdffb1cc94997ddb812f431d2727bd14b1038aa86bb4b158dc26eb`  
		Last Modified: Tue, 13 Jan 2026 02:50:49 GMT  
		Size: 828.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f0638210137e96c53330207b0c48c3573e50bbd6938e200c866a54fa5670587`  
		Last Modified: Tue, 13 Jan 2026 02:50:49 GMT  
		Size: 5.6 MB (5584637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:983fac13a9a9db87c37a2e68633ff8d8ba6de6ceab1fd96703b98375464ba962`  
		Last Modified: Tue, 13 Jan 2026 02:50:49 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ff09a6ada35b7b64df92396980eee5bfc048cd96888224f08e0d2427d6f8317`  
		Last Modified: Tue, 13 Jan 2026 02:50:50 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:latest` - unknown; unknown

```console
$ docker pull spiped@sha256:bbfd28a7341737fe41be2d8148ed284a04a23659d622f5a208bf17b3e2b659bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3633427 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:343a78e82ac4ac449e4e48eec68ee3a115bfe6babd4f0981a1c9f105a55fa46d`

```dockerfile
```

-	Layers:
	-	`sha256:5107e1cd66ec5596bee8e181870b7098ccdf15d117b62b9777d05fbbd6425da2`  
		Last Modified: Tue, 13 Jan 2026 02:50:49 GMT  
		Size: 3.6 MB (3618339 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f4b5126f306174e663ab6bfbb6c1ea51dad885e1351a21591c62bfd64fdc8f9a`  
		Last Modified: Tue, 13 Jan 2026 02:50:49 GMT  
		Size: 15.1 KB (15088 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:latest` - linux; arm64 variant v8

```console
$ docker pull spiped@sha256:c5ac7642b68a7d62ff1668ee9ccd593c5b4baf9647ba82968cb32bb60af02b7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.4 MB (36369164 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c182edf494edd54de7622035fda29964a6d3aa35b2017345462c2af4f9aabe1a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 02:10:31 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Tue, 13 Jan 2026 02:10:34 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 02:10:57 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Tue, 13 Jan 2026 02:10:57 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 13 Jan 2026 02:10:57 GMT
VOLUME [/spiped]
# Tue, 13 Jan 2026 02:10:57 GMT
WORKDIR /spiped
# Tue, 13 Jan 2026 02:10:57 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Tue, 13 Jan 2026 02:10:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 13 Jan 2026 02:10:57 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:d637807aba98f742a62ad9b0146579ceb0297a3c831f56b2361664b7f5fbc75b`  
		Last Modified: Tue, 13 Jan 2026 00:42:41 GMT  
		Size: 30.1 MB (30134042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa738792cac53efb73662ac021b3ff961cda2a9fd5ff2d16099b1484559d374f`  
		Last Modified: Tue, 13 Jan 2026 02:11:06 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfdaf94089cb016262308955f88eed98d371f5d22a8e9d98ae37e620955f1c1f`  
		Last Modified: Tue, 13 Jan 2026 02:11:06 GMT  
		Size: 827.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22e93808490a2d574721dc6c2b6026a9752567e270543e4dd38429615e0cb92c`  
		Last Modified: Tue, 13 Jan 2026 02:11:06 GMT  
		Size: 6.2 MB (6232754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6528f27a2771e82620b708c90c56e8ad51d204361b4840118b22750fed8b6a6`  
		Last Modified: Tue, 13 Jan 2026 02:11:06 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f1da2564128444a92450a4a59862d9468b245d767224eb106222be1c7d01458`  
		Last Modified: Tue, 13 Jan 2026 02:11:07 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:latest` - unknown; unknown

```console
$ docker pull spiped@sha256:57811de6379e93c9312f47423935b6e3a49fb4ddc35ef68994d6963bd9d85ccd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3636376 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7182e12c82cd89e69110040b6ee3df90b56612f25f521314e032b1acefae3429`

```dockerfile
```

-	Layers:
	-	`sha256:d37e4ed01ed487dc42abdf509e4f4d19b3924c3e66fd4755f2f689d64b521b1e`  
		Last Modified: Tue, 13 Jan 2026 02:11:06 GMT  
		Size: 3.6 MB (3621260 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f2499b37440a6c3eabebfe76ec56fb252ea8747d68928be12b891bfbd85074cb`  
		Last Modified: Tue, 13 Jan 2026 02:11:06 GMT  
		Size: 15.1 KB (15116 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:latest` - linux; 386

```console
$ docker pull spiped@sha256:1cdb842fc6e02f60626019e0e57c7fafd4e7f5b2eed04880b3d713f203931940
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.7 MB (37733503 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e0460a7c0ac1bd1b00243d134ab4e9f5c3764c6fdbc34a5f65b1c8b088d94da`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 02:00:57 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Tue, 13 Jan 2026 02:01:00 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 02:01:25 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Tue, 13 Jan 2026 02:01:25 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 13 Jan 2026 02:01:25 GMT
VOLUME [/spiped]
# Tue, 13 Jan 2026 02:01:25 GMT
WORKDIR /spiped
# Tue, 13 Jan 2026 02:01:25 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Tue, 13 Jan 2026 02:01:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 13 Jan 2026 02:01:25 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:27bb6d39eda5ced7626db280c3902aacdfade5acd11a16ef9618e3185f69b102`  
		Last Modified: Tue, 13 Jan 2026 00:42:56 GMT  
		Size: 31.3 MB (31288476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60592460d62df311cafe6009f0b1e88a3b8ddc79aa3e7cf473c43931b99a17da`  
		Last Modified: Tue, 13 Jan 2026 02:01:32 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cb3b27b0d5aa2bf7825784f25f831a2345a35bdb1aa9db4ef943cf92bb484cb`  
		Last Modified: Tue, 13 Jan 2026 02:01:32 GMT  
		Size: 827.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22e0f4978baa80656995d7a0c03833b59df3a6052c5bbd5d40f6f90afd3cfe8e`  
		Last Modified: Tue, 13 Jan 2026 02:01:32 GMT  
		Size: 6.4 MB (6442660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40b59d2e996687725ce32a680e81cd4d2d6bccfb615a52e20c79e648182ae9a2`  
		Last Modified: Tue, 13 Jan 2026 02:01:32 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b392555143b5ce8e36cc2d3003e29d7337718b66d8588629ad709beb98e10921`  
		Last Modified: Tue, 13 Jan 2026 02:01:33 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:latest` - unknown; unknown

```console
$ docker pull spiped@sha256:9fa0f002c06fe84ef172b8e5d8fee2863cadf4e78b24618ec0c542c8af312545
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3635299 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa89b41ff4abd30fb1724f48a2076ce65996bd55b5e41e09808dcba89582b177`

```dockerfile
```

-	Layers:
	-	`sha256:a7e924435a489e1fb4dec36bca26ef56134a0fb5268b6f1c4efefffc0d572c17`  
		Last Modified: Tue, 13 Jan 2026 02:01:32 GMT  
		Size: 3.6 MB (3620353 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5d7d7705b4a9214730fcf189f5236c787d39f0544808b30c9f33460b09c8e441`  
		Last Modified: Tue, 13 Jan 2026 02:01:32 GMT  
		Size: 14.9 KB (14946 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:latest` - linux; ppc64le

```console
$ docker pull spiped@sha256:217a6ad63ff5068c0b74f7eae17e94c2cb71d70c272df72a0677a68fcdfa68ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.4 MB (40438466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ffd19b90beec6ea9757fde0576791284385447cc4c172cfd321d52ec2c97be76`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 03:23:23 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Tue, 13 Jan 2026 03:23:27 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 03:24:43 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Tue, 13 Jan 2026 03:24:43 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 13 Jan 2026 03:24:43 GMT
VOLUME [/spiped]
# Tue, 13 Jan 2026 03:24:44 GMT
WORKDIR /spiped
# Tue, 13 Jan 2026 03:24:44 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Tue, 13 Jan 2026 03:24:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 13 Jan 2026 03:24:44 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:9a275bb13cf8b3e9db52a41b6b4ff22ee1ffed00394f6deddd2de45044bd3bae`  
		Last Modified: Tue, 13 Jan 2026 00:57:06 GMT  
		Size: 33.6 MB (33595600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:225190aaf825e37a5b2cf27017ed41ba2d9173d83def87c73b958dd97381f2aa`  
		Last Modified: Tue, 13 Jan 2026 03:25:13 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ccd03d24216b5040cbf1d93ba92ad64768a13ea627295014d57b5e282ca6a50`  
		Last Modified: Tue, 13 Jan 2026 03:25:13 GMT  
		Size: 824.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b851c03de8c749491081d69ed679aa1ad63958039e2afa99cf05f4ae81d860a0`  
		Last Modified: Tue, 13 Jan 2026 03:25:13 GMT  
		Size: 6.8 MB (6840503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4b2e0f5f412a88905ed12af6300709e494f53f6e08d985f54520c76906b9814`  
		Last Modified: Tue, 13 Jan 2026 03:25:13 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bb5e826c86b31929ab528e7c1f2e43801991a819d31dbbde072a295ad375a77`  
		Last Modified: Tue, 13 Jan 2026 03:25:14 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:latest` - unknown; unknown

```console
$ docker pull spiped@sha256:3a4b6e540625773d2125af7752a1629a7d315ede426bba80610cbaa92e9b92af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3636991 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ae20156a9d00bc9c74b3a76385fe6e56c21765c902ac11e9b6dcb1c250958eb`

```dockerfile
```

-	Layers:
	-	`sha256:02870f0cbecfd9962d0147c091d6790429b5b3c54a6c4c2e5b8171882b41507f`  
		Last Modified: Tue, 13 Jan 2026 03:25:13 GMT  
		Size: 3.6 MB (3621961 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:feeb52a1c08c600fece2b0b16fb3afd3b91213213f8e0ecb56e72ee580c1a028`  
		Last Modified: Tue, 13 Jan 2026 03:25:13 GMT  
		Size: 15.0 KB (15030 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:latest` - linux; riscv64

```console
$ docker pull spiped@sha256:c3726522ae3244f8e5fc4fff7b8f5caaa648c5af80dd1242df5b9b0203a50b61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.6 MB (37632620 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6901900fa0f28a8994f2a5c6167065703cea25c38b46e682c7aa85ebf4c50f8a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1768176000'
# Fri, 16 Jan 2026 05:28:46 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Fri, 16 Jan 2026 05:29:13 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 16 Jan 2026 05:32:13 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Fri, 16 Jan 2026 05:32:13 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Fri, 16 Jan 2026 05:32:13 GMT
VOLUME [/spiped]
# Fri, 16 Jan 2026 05:32:13 GMT
WORKDIR /spiped
# Fri, 16 Jan 2026 05:32:13 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Fri, 16 Jan 2026 05:32:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 16 Jan 2026 05:32:13 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:8c2d1639f4f145e07ecf59940bfa96f17083c024b5c96e8082c50d6075a08b82`  
		Last Modified: Tue, 13 Jan 2026 01:07:54 GMT  
		Size: 28.3 MB (28271687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0565826c8fe4b1dacce6d9e839c402d5f7f058df52502fb3afc9c1fe362273ab`  
		Last Modified: Fri, 16 Jan 2026 05:33:25 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d54f9b8a5d71461439339ce26a0c07c07fbc5a8f883874f06636ae124d4b6406`  
		Last Modified: Fri, 16 Jan 2026 05:33:25 GMT  
		Size: 818.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5e14934a15b1e232262f936875f5c3c3faf525c75fb01a98c1e77355c8d3879`  
		Last Modified: Fri, 16 Jan 2026 05:33:27 GMT  
		Size: 9.4 MB (9358574 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcad698be725811e7e426b85f2dd52a1d1e7963a1d1977d99b6853d7b29d1d99`  
		Last Modified: Fri, 16 Jan 2026 05:33:25 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:492e62971c5bbebb5c3ac87efe8c5f00292840225c2295daf96e49886856bd0d`  
		Last Modified: Fri, 16 Jan 2026 05:33:27 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:latest` - unknown; unknown

```console
$ docker pull spiped@sha256:20c580ff798af1e2f3b4ea4d32d2a4df3f8a4d6cf589acca184232c7eb9ff72e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3628397 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e539bf6b82092c6a4f98991afff364af3c7d9c9f618a72fdbf396b9090cbdd62`

```dockerfile
```

-	Layers:
	-	`sha256:468f7c87bf94fe22429b696b878ab697ecd32432c631e71062b7bd058b3faab0`  
		Last Modified: Fri, 16 Jan 2026 05:33:26 GMT  
		Size: 3.6 MB (3613367 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d7df9a72d10446f51bf6f2ad7ea6f3b30523ac77067a2eef729971e3a94c4d9a`  
		Last Modified: Fri, 16 Jan 2026 05:33:25 GMT  
		Size: 15.0 KB (15030 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:latest` - linux; s390x

```console
$ docker pull spiped@sha256:b46215872c00e42011d21220800d0ee463b258cd8d166d49ccd469adc47dc457
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.0 MB (35957717 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df15f3626274fb67ddf6a8005b94e134403179f690da6ef23659775f72efef18`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 14:57:57 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Tue, 13 Jan 2026 14:57:59 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 14:58:15 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Tue, 13 Jan 2026 14:58:15 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 13 Jan 2026 14:58:15 GMT
VOLUME [/spiped]
# Tue, 13 Jan 2026 14:58:15 GMT
WORKDIR /spiped
# Tue, 13 Jan 2026 14:58:15 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Tue, 13 Jan 2026 14:58:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 13 Jan 2026 14:58:15 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:2b46bc94baaae0a37e5e04b1babf7e1f37c4390b83d49c3c6820188deba770e3`  
		Last Modified: Tue, 13 Jan 2026 13:10:27 GMT  
		Size: 29.8 MB (29833411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3b1093dbc4689c27e231c6dd119b898927b68bd0b8d9f3c6cf38639a1bdd0b3`  
		Last Modified: Tue, 13 Jan 2026 14:58:26 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a95729b68b03a5258c5b837956a82a3f035958eae31806944cfc3d000f57544`  
		Last Modified: Tue, 13 Jan 2026 14:58:26 GMT  
		Size: 827.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d69ee5aeb4cd94df02c0f1a0a8cd4ed392ff13e793121546a4bd8c47b2290e92`  
		Last Modified: Tue, 13 Jan 2026 14:58:26 GMT  
		Size: 6.1 MB (6121939 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b0ca9453fa28464fce732f333b89260706417874c40f190ed807d86d520a93f`  
		Last Modified: Tue, 13 Jan 2026 14:58:26 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b0ccaf36ff928c0e2cc6c1f91d607513b642e72bcc47b1caa7697f08a3f34df`  
		Last Modified: Tue, 13 Jan 2026 14:58:27 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:latest` - unknown; unknown

```console
$ docker pull spiped@sha256:0cae8eeb93ee297fe79218a995091abdc555a181b6cf923d9ce6d45fea739d38
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3633569 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d573eb0590afb15caeedd77101da3dd9ab9bc629b7b9e3fa1c8e8dee4413af36`

```dockerfile
```

-	Layers:
	-	`sha256:0c275ec6d71543ab1ba7563b52722ba79e575b6001abfd2e8e4bd6a78c25b884`  
		Last Modified: Tue, 13 Jan 2026 14:58:26 GMT  
		Size: 3.6 MB (3618587 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b1d70cd62ea5f4fe1e6b6fb7a633b99a94345536ef639f33351ce3782f983cc7`  
		Last Modified: Tue, 13 Jan 2026 14:58:26 GMT  
		Size: 15.0 KB (14982 bytes)  
		MIME: application/vnd.in-toto+json
