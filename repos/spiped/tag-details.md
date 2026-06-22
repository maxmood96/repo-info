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
$ docker pull spiped@sha256:de4b34c7a3ad65daa04d28d7e12287d7241887e56b69c69bb8935fefbd9c0062
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
$ docker pull spiped@sha256:06f6d191d00c3c7f99f9ca6bc35961abde2cefdf0c4c3ef829ee12c8e723b1a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.8 MB (36835681 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b886f796060d79ea57dfed8e6573334428e6ba942e2416c5e9d4991e4358f4d6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 00:36:40 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Thu, 11 Jun 2026 00:36:43 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:37:07 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Thu, 11 Jun 2026 00:37:07 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Thu, 11 Jun 2026 00:37:07 GMT
VOLUME [/spiped]
# Thu, 11 Jun 2026 00:37:07 GMT
WORKDIR /spiped
# Thu, 11 Jun 2026 00:37:07 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Thu, 11 Jun 2026 00:37:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 11 Jun 2026 00:37:07 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:72c03230f1363a3fb61d2f98504cf168bad3fe22f511ad2005dc021515d7ce97`  
		Last Modified: Wed, 10 Jun 2026 23:40:25 GMT  
		Size: 29.8 MB (29785415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:527ecde60bfe50017124e67b8415956fd4fb6c9d88a886f3050cf3759f4f98dd`  
		Last Modified: Thu, 11 Jun 2026 00:37:15 GMT  
		Size: 1.1 KB (1104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ccfb06129b754706d994d24161d30c750e9d947232c5d51a4213ea845f178c5`  
		Last Modified: Thu, 11 Jun 2026 00:37:15 GMT  
		Size: 827.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef3d898f83d1faa117388bd37c5a2c913e57742474e0f610d32e0e1c83e5c8ef`  
		Last Modified: Thu, 11 Jun 2026 00:37:15 GMT  
		Size: 7.0 MB (7047900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1436ff66f580ac7020fa765af6cbc9cd8c91911721a10dfa2305b6404b18cea`  
		Last Modified: Thu, 11 Jun 2026 00:37:15 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2d6ed45d70891121ffe50995b4a569aa6dbda4c3a37a3fa16927fe16da829f7`  
		Last Modified: Thu, 11 Jun 2026 00:37:16 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1` - unknown; unknown

```console
$ docker pull spiped@sha256:d5cecdf47fa2040ff01111fdbbb75c19d537a969a776bc1c8778d421c2364a04
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3641284 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:082365ba064127a901f5498578d29ee8a542bbc7adc94e40bf4cf9e2a84a407f`

```dockerfile
```

-	Layers:
	-	`sha256:8a7bb242a706f30d64bcc8002692cee4179a16af8322cf72d23b0a8c78123a57`  
		Last Modified: Thu, 11 Jun 2026 00:37:15 GMT  
		Size: 3.6 MB (3626302 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:789d0bf94bddbb877fd99e66c1f0e2fa4901e5821fb450c040ff83bf254aeb75`  
		Last Modified: Thu, 11 Jun 2026 00:37:15 GMT  
		Size: 15.0 KB (14982 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1` - linux; arm variant v5

```console
$ docker pull spiped@sha256:3a77fd17bf87542b39acd5c371cb4509f911aba18087b5841340cdae79eb07e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.8 MB (33750953 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9f871c59019572295a1c6f16175304e8c052d7ae1bde8550e6316bd337fc36b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 01:20:06 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Thu, 11 Jun 2026 01:20:11 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 01:20:37 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Thu, 11 Jun 2026 01:20:37 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Thu, 11 Jun 2026 01:20:37 GMT
VOLUME [/spiped]
# Thu, 11 Jun 2026 01:20:37 GMT
WORKDIR /spiped
# Thu, 11 Jun 2026 01:20:38 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Thu, 11 Jun 2026 01:20:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 11 Jun 2026 01:20:38 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:ed883f3fd95b7edef302d7ca9520eefdae280af081509bd7e9e5b5ff8f4cda7c`  
		Last Modified: Wed, 10 Jun 2026 23:41:17 GMT  
		Size: 28.0 MB (27959200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e751f68dcb09ba1579bee55a24286186b59e393de92bac08ff724b4981d5d170`  
		Last Modified: Thu, 11 Jun 2026 01:20:44 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d89df5ca97fe521123a4a7aae01c94c4479bf368a9d8c696eee17064fc312bc1`  
		Last Modified: Thu, 11 Jun 2026 01:20:45 GMT  
		Size: 831.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91d2c4ac84d26c20df4907085b90aeb331861a219b69716c57682ae2cb946eb8`  
		Last Modified: Thu, 11 Jun 2026 01:20:45 GMT  
		Size: 5.8 MB (5789383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2073b26a67b2b25b8dae9d6d7a2028b43f95697825a4cb34a083684f542d8fe`  
		Last Modified: Thu, 11 Jun 2026 01:20:45 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1e64de9d592c6c09b59082de73dbb84f8e63a26763394e8083e1dd58f66d693`  
		Last Modified: Thu, 11 Jun 2026 01:20:46 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1` - unknown; unknown

```console
$ docker pull spiped@sha256:e786ed555ddf93e97965e805339e0e57e642ee1b6992efb0a38706feed7d6111
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3634384 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:678d30be6a2af3135f4751e15d6b35b82e2cd1dbc9a6858fa252aa22ea5487f6`

```dockerfile
```

-	Layers:
	-	`sha256:f416dd4fb0aef1763e3288e5f7435905aa2cacf86c5d53d1ff62343b3aee11b4`  
		Last Modified: Thu, 11 Jun 2026 01:20:45 GMT  
		Size: 3.6 MB (3619296 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6a02acc670c38ba874d76cb8784856b12a90aa7e49311ee73beff9aa2761b4c8`  
		Last Modified: Thu, 11 Jun 2026 01:20:45 GMT  
		Size: 15.1 KB (15088 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1` - linux; arm variant v7

```console
$ docker pull spiped@sha256:079fbf73e349c36cc2b4d55e664f1d5a60b482fa43a1021f0ea8cb3e38b490fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.8 MB (31798135 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:959018a10d28c5d1dde8c33184f543a1293c46376550688e906dbae7ddf55228`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 01:21:52 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Thu, 11 Jun 2026 01:21:55 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 01:22:18 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Thu, 11 Jun 2026 01:22:18 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Thu, 11 Jun 2026 01:22:18 GMT
VOLUME [/spiped]
# Thu, 11 Jun 2026 01:22:18 GMT
WORKDIR /spiped
# Thu, 11 Jun 2026 01:22:18 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Thu, 11 Jun 2026 01:22:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 11 Jun 2026 01:22:18 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:4bd6ddea06d5009ee47ddb0f254a2569aff0230c005869ebd416b20295d945c0`  
		Last Modified: Wed, 10 Jun 2026 23:42:34 GMT  
		Size: 26.2 MB (26211004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51bb869011c6d164e974fe820179933094dcc281df7a55480fc4077277232c77`  
		Last Modified: Thu, 11 Jun 2026 01:22:25 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:422e823bc0c6498856622e79affa11c1598652143bfa7f350dc04a8bae10a58a`  
		Last Modified: Thu, 11 Jun 2026 01:22:25 GMT  
		Size: 827.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fadeadb89fb7f698439cd322f47ba897a03fd1551ffe3fcf76d75f5383cd472`  
		Last Modified: Thu, 11 Jun 2026 01:22:25 GMT  
		Size: 5.6 MB (5584763 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3817b48e6549ab977fe0f1bbbb517045c499e8b6a3c28271dc05398321fe485d`  
		Last Modified: Thu, 11 Jun 2026 01:22:25 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a52c3658e003288d1598c728ef7ab0c5167ce43d1e20bf855db1dde18f30b339`  
		Last Modified: Thu, 11 Jun 2026 01:22:27 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1` - unknown; unknown

```console
$ docker pull spiped@sha256:4660d6bee86fba733a44735e9cea0b5dfa13410ac081e02edbed22229736f4ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3633504 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f7dd6ebfec69dc7720608ae6a9b0c5af682ff982f3ce0440ed4f3bf904f4c5f`

```dockerfile
```

-	Layers:
	-	`sha256:d25034d6fee06e5ff09bdc9004cbe4b4a4e9d9ed95b0624f5000cb9e580a086e`  
		Last Modified: Thu, 11 Jun 2026 01:22:25 GMT  
		Size: 3.6 MB (3618417 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:deb1d9d6f39ee38fed21b5f4de28c58d8058b0810a5cd7893d92d295084642d1`  
		Last Modified: Thu, 11 Jun 2026 01:22:25 GMT  
		Size: 15.1 KB (15087 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1` - linux; arm64 variant v8

```console
$ docker pull spiped@sha256:b666025eb8bf9bd288d28306188f384cf5e1cf793252a3092ed8467ea174a7c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.4 MB (36384823 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2b7f7df51ecb422ed1c09aa176c982afa86a96f6e553daf85ffd468ca5f3846`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 00:38:14 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Thu, 11 Jun 2026 00:38:16 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:38:39 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Thu, 11 Jun 2026 00:38:39 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Thu, 11 Jun 2026 00:38:39 GMT
VOLUME [/spiped]
# Thu, 11 Jun 2026 00:38:39 GMT
WORKDIR /spiped
# Thu, 11 Jun 2026 00:38:39 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Thu, 11 Jun 2026 00:38:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 11 Jun 2026 00:38:39 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:a25cd16f2d8653f652f8292b34b21bfbabdc85d6b39861a24b85f0896df1a95e`  
		Last Modified: Wed, 10 Jun 2026 23:40:16 GMT  
		Size: 30.1 MB (30148530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af99214715c4dd89b01b22d803c733a8cdeff8b516b64dcbc4039e3bb73edf81`  
		Last Modified: Thu, 11 Jun 2026 00:38:46 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cb7f2ca44a46746d13284bd66cb8d509327101aa851a60e2f4562b4c0b43fe4`  
		Last Modified: Thu, 11 Jun 2026 00:38:46 GMT  
		Size: 828.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fc568496a63b54431809869a1a353a056bd0286efc252ed16943213148d8e78`  
		Last Modified: Thu, 11 Jun 2026 00:38:46 GMT  
		Size: 6.2 MB (6233926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62455682699c33f1af511f11805177432eb0df675093f3a55be46e8069d099ad`  
		Last Modified: Thu, 11 Jun 2026 00:38:46 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1337cf4ae97e82beefcd0736801f263b58faa5acea8bbd02b6fb1610b3c08a69`  
		Last Modified: Thu, 11 Jun 2026 00:38:47 GMT  
		Size: 336.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1` - unknown; unknown

```console
$ docker pull spiped@sha256:28fd7f18765bc97e01aed948eb208846037e2fdc5be5b01c7b60a1dab0ecc29d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3636446 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:caaed5bb2a83f15f132837c8042bc95288ce03bd799f9d4a49b960975af17bea`

```dockerfile
```

-	Layers:
	-	`sha256:f4119ebc6f5a2232c489599390a07000eb50a2325250846032e65737506b59fb`  
		Last Modified: Thu, 11 Jun 2026 00:38:46 GMT  
		Size: 3.6 MB (3621330 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ff1ae5a7dd30d786394e331ae8fd4a26444a7fab07e0f0f35bd0d9f9e8aa11f4`  
		Last Modified: Thu, 11 Jun 2026 00:38:46 GMT  
		Size: 15.1 KB (15116 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1` - linux; 386

```console
$ docker pull spiped@sha256:02f4ba23c22e1271ac47e549272f9bb9b73d515c584ef6657b10b34089186119
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.7 MB (37746372 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c77be7a202c7361655d5298662fbd58b4ac13a280d8eea6d0e5696277b5d6dc2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 00:44:31 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Thu, 11 Jun 2026 00:44:34 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:45:03 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Thu, 11 Jun 2026 00:45:03 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Thu, 11 Jun 2026 00:45:03 GMT
VOLUME [/spiped]
# Thu, 11 Jun 2026 00:45:03 GMT
WORKDIR /spiped
# Thu, 11 Jun 2026 00:45:03 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Thu, 11 Jun 2026 00:45:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 11 Jun 2026 00:45:03 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:720f951a68f4f9ab464e52b53cf88cfb86bc876b3f00956d000420777ab93c0c`  
		Last Modified: Wed, 10 Jun 2026 23:40:30 GMT  
		Size: 31.3 MB (31301194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96b36e957fa28b38d49b885ce8ff4366a6bfcb98bf38aa1dd3dd51c9b7cd333c`  
		Last Modified: Thu, 11 Jun 2026 00:45:10 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3aae632d05299c9dee2bec97ea596046cf5c7c15eff6529e97937627b28994fa`  
		Last Modified: Thu, 11 Jun 2026 00:45:10 GMT  
		Size: 828.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd7f7718fe56cea19c8269279c48994d7ae792b5209abc4faef63781a55560f4`  
		Last Modified: Thu, 11 Jun 2026 00:45:11 GMT  
		Size: 6.4 MB (6442811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96e529f830d838d84290e5326067c74dc889693a3954cd9a7dbd43c0b583c23f`  
		Last Modified: Thu, 11 Jun 2026 00:45:10 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fe774eab45468f5459c9ea3e437c826c9c3d130cbc49f077eef0338b91a9edd`  
		Last Modified: Thu, 11 Jun 2026 00:45:12 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1` - unknown; unknown

```console
$ docker pull spiped@sha256:43aeb04090782a915b6e9289e6133f1f0327b7465670b94e07f481b847c4025b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3635377 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd02b428a54369d078699f646a6c58bb59205a7d8e90fd308ef1b652598d64f9`

```dockerfile
```

-	Layers:
	-	`sha256:20700448f422d0e1e5f84b34dcae83618e79e0454a188609c16921611a98ff5a`  
		Last Modified: Thu, 11 Jun 2026 00:45:10 GMT  
		Size: 3.6 MB (3620431 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b8c3c92718b75b733828274ef1f0c3ac60a2665e98431b090587ac61fa798684`  
		Last Modified: Thu, 11 Jun 2026 00:45:10 GMT  
		Size: 14.9 KB (14946 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1` - linux; ppc64le

```console
$ docker pull spiped@sha256:77a28ff7796938b2e628dcb8466cba0a9b9e9209373514b53eb9500a4eb54179
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.4 MB (40449493 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5c663351cf736af7041bf6dab200f7240abda1f91a38cc9154e15ecc605051b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 04:42:39 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Thu, 11 Jun 2026 04:42:43 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 04:43:31 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Thu, 11 Jun 2026 04:43:31 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Thu, 11 Jun 2026 04:43:31 GMT
VOLUME [/spiped]
# Thu, 11 Jun 2026 04:43:31 GMT
WORKDIR /spiped
# Thu, 11 Jun 2026 04:43:31 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Thu, 11 Jun 2026 04:43:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 11 Jun 2026 04:43:31 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:9d6b2e320e2b74843186d830e8202c50ebfaeccf823d239e3e3e349a8a508d80`  
		Last Modified: Thu, 11 Jun 2026 00:24:42 GMT  
		Size: 33.6 MB (33606340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae397a9bd78994d17d78508ffe6c90b95321c279f11d71546a6690cf7b3bfa56`  
		Last Modified: Thu, 11 Jun 2026 04:43:44 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:527c0346e0be1cff6e959785d2ead56a024d388a5f5b49668bb10ef02df87e5b`  
		Last Modified: Thu, 11 Jun 2026 04:43:44 GMT  
		Size: 825.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfb798ab52e9baacaca51304c7ae7bd07e22ffa204c22fa1ee3f600faa9d384c`  
		Last Modified: Thu, 11 Jun 2026 04:43:45 GMT  
		Size: 6.8 MB (6840786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9e2eda05f5b8c55e69e0f5f7b8411ef18adfa257a0964e74893e13aa8460231`  
		Last Modified: Thu, 11 Jun 2026 04:43:44 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89c91b4a125ec65053187500a3042ba5cf4b3d3c3757a5130a5b6a469502146e`  
		Last Modified: Thu, 11 Jun 2026 04:43:45 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1` - unknown; unknown

```console
$ docker pull spiped@sha256:cde6ed1dd2ca8f029ced3770c7fd29bfed2a5e054b7f88c1c2828ea61ae0d53a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3637067 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f348c1d24e29a4dd183acde8c7db1a7186ed71bf6cc2b0deb230af07b7e3608`

```dockerfile
```

-	Layers:
	-	`sha256:9028cc214c0ddc113b07afbc6b1c7d125225085781875688e233501b5e4f6973`  
		Last Modified: Thu, 11 Jun 2026 04:43:45 GMT  
		Size: 3.6 MB (3622039 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:23b0df7ce9f0c385bfc283502819fb193952bc81b97402aae117279766c4435f`  
		Last Modified: Thu, 11 Jun 2026 04:43:44 GMT  
		Size: 15.0 KB (15028 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1` - linux; riscv64

```console
$ docker pull spiped@sha256:d1196bf05f6d34c1b33d0f44d558a64dacbac606da8ede3854f0f56b7da88dd7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.6 MB (37640838 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:257f964733ff5e0fb249561928b63d968d0ea7e0f22a1650497b8f634a78b7b1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1781049600'
# Sat, 13 Jun 2026 02:38:34 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Sat, 13 Jun 2026 02:39:05 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 13 Jun 2026 02:42:10 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Sat, 13 Jun 2026 02:42:10 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Sat, 13 Jun 2026 02:42:10 GMT
VOLUME [/spiped]
# Sat, 13 Jun 2026 02:42:10 GMT
WORKDIR /spiped
# Sat, 13 Jun 2026 02:42:10 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sat, 13 Jun 2026 02:42:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 13 Jun 2026 02:42:10 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:0b510fe8545cab831b696965b5a825649c5c945581e912d31a08a0b30ff940c0`  
		Last Modified: Thu, 11 Jun 2026 03:01:06 GMT  
		Size: 28.3 MB (28282305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f639c6130c8aca0f837b171cb0a0d45c790c5d7bf9518eff2b8ff95b48f104c`  
		Last Modified: Sat, 13 Jun 2026 02:43:23 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07e14a8d467e3dc32c3ec2a585b788255e6272eeaa9763d004943122f7248c27`  
		Last Modified: Sat, 13 Jun 2026 02:43:23 GMT  
		Size: 822.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d41b9627a0c3fc9b82eb3a3347a368ac72d11d19f3ff135e81910be58f7ced5`  
		Last Modified: Sat, 13 Jun 2026 02:43:24 GMT  
		Size: 9.4 MB (9356169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4946ccd28be72a02f3c71907db8b182219a80ff46301e8a09fdd946d52683dd8`  
		Last Modified: Sat, 13 Jun 2026 02:43:23 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f74e027caa4d5bd042803e1c5847e795634af08a895bf7099c444bcdf51c4cc`  
		Last Modified: Sat, 13 Jun 2026 02:43:24 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1` - unknown; unknown

```console
$ docker pull spiped@sha256:bd59a45c25ec7d4b80d63933dffd3bd86372d97041734ebbf62964d8a991e093
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3628474 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0ed4a489648532fba6cde1d7e88a809bdb98383c98aee19aaba7a5a947fbd77`

```dockerfile
```

-	Layers:
	-	`sha256:d44a97abcbeafd6a6ec2dd69c997db68246839a5985937d49f3c1d5fbc99a495`  
		Last Modified: Sat, 13 Jun 2026 02:43:24 GMT  
		Size: 3.6 MB (3613445 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:de64e5286a1b72fafa9b68c701bf6ba016f164bdfaf60538499d95770fbf3f6a`  
		Last Modified: Sat, 13 Jun 2026 02:43:23 GMT  
		Size: 15.0 KB (15029 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1` - linux; s390x

```console
$ docker pull spiped@sha256:bd22ee71a9e9236e2ca69180ad51c06cf6d8e35afbd4add081b0d2f764edc08e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.0 MB (35975833 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1ad1052f1364f10f7a17a6666de217cbde8ab8c0e0ac3499018c5cd72b4ee17`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 01:43:42 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Thu, 11 Jun 2026 01:43:44 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 01:44:01 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Thu, 11 Jun 2026 01:44:01 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Thu, 11 Jun 2026 01:44:01 GMT
VOLUME [/spiped]
# Thu, 11 Jun 2026 01:44:01 GMT
WORKDIR /spiped
# Thu, 11 Jun 2026 01:44:01 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Thu, 11 Jun 2026 01:44:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 11 Jun 2026 01:44:01 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:760dcf74fdfe93300ce15b5b23adf9aa4af45b6ba9d69925863198f64881a537`  
		Last Modified: Wed, 10 Jun 2026 23:42:35 GMT  
		Size: 29.9 MB (29851354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbee78aca287a132f4560c3c136874e9fd2eb76d548257a9d3a3df8c901bcc4f`  
		Last Modified: Thu, 11 Jun 2026 01:44:13 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:592a34f021f7dfd15ace5226ae509b1158c586b704884d60433770343a082992`  
		Last Modified: Thu, 11 Jun 2026 01:44:13 GMT  
		Size: 828.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb3568250ea65438eb60733aee26c97620a46d0a35f1724cad1b6cdf7fbcc023`  
		Last Modified: Thu, 11 Jun 2026 01:44:13 GMT  
		Size: 6.1 MB (6122111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b205eccacc5cb65c52b6fa4618ba96b957fd2f8a2f5423e2653cc1b280d2f23`  
		Last Modified: Thu, 11 Jun 2026 01:44:13 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02c73a6752a874142787522de11c367cd55d46e4661d6e3216d3509660bc3091`  
		Last Modified: Thu, 11 Jun 2026 01:44:14 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1` - unknown; unknown

```console
$ docker pull spiped@sha256:b9ccb006c7597035afc395814bcd5e176f1c6747e8cdcbb2e2e99a609798685c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3633647 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0955f426902eecb0ba4cee729a5abb10364e89f0579f841377a2401fdd89f43`

```dockerfile
```

-	Layers:
	-	`sha256:bc258d4741b882519b7d7392f726369c450df7d38b8a5f5b761096da236e6d1a`  
		Last Modified: Thu, 11 Jun 2026 01:44:13 GMT  
		Size: 3.6 MB (3618665 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9e8ebd7ccddfecb937db9fd26d8850a9b8222af37b614601c7b7e2d424a147fa`  
		Last Modified: Thu, 11 Jun 2026 01:44:13 GMT  
		Size: 15.0 KB (14982 bytes)  
		MIME: application/vnd.in-toto+json

## `spiped:1-alpine`

```console
$ docker pull spiped@sha256:d321da057edcf67209e6a50fce596020211d058f66861249f42c546d7d818fe4
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
$ docker pull spiped@sha256:ddacdd500302ed8e0b56cfbe5eba1b03890a3a11103e2e79f118f78819546c96
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3904546 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0e50065de302c7f6a370e6ce4b691cc04feab696fd0ca4c59d5c21b96d09a5f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Mon, 22 Jun 2026 19:20:21 GMT
ADD alpine-minirootfs-3.22.5-x86_64.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:20:21 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 19:52:57 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Mon, 22 Jun 2026 19:52:58 GMT
RUN apk add --no-cache libssl3 # buildkit
# Mon, 22 Jun 2026 19:53:07 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Mon, 22 Jun 2026 19:53:07 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Mon, 22 Jun 2026 19:53:07 GMT
VOLUME [/spiped]
# Mon, 22 Jun 2026 19:53:07 GMT
WORKDIR /spiped
# Mon, 22 Jun 2026 19:53:07 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Mon, 22 Jun 2026 19:53:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 22 Jun 2026 19:53:07 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:f7ee36c9aa34bbb665f975c76e5c0d1607f0674b94c84cfb0061f87006ea5d10`  
		Last Modified: Mon, 22 Jun 2026 09:11:44 GMT  
		Size: 3.8 MB (3787595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e11e0fcbf833efd71ccdc39dad69485c2ab9e33be6a7075e11f23dfc938ee0b`  
		Last Modified: Mon, 22 Jun 2026 19:53:11 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d3df5ddcf63216635d6ac9800edfcdf71dbf67c7328ec84d1b3ab49da64adf0`  
		Last Modified: Mon, 22 Jun 2026 19:53:11 GMT  
		Size: 7.9 KB (7939 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68bf1a439bfe49642cefb4e5461e95befb5f5a9b5cced180eaf651935a1246f9`  
		Last Modified: Mon, 22 Jun 2026 19:53:11 GMT  
		Size: 107.6 KB (107630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f2716e286de0031c590e0551ee0bcfbe0740fde1029874d538fecad89dadaca`  
		Last Modified: Mon, 22 Jun 2026 19:53:12 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe62eb4d32c49f1f3ab36f4fa4341f61fe5f3eccfbb08576ec70be11772704af`  
		Last Modified: Mon, 22 Jun 2026 19:53:13 GMT  
		Size: 336.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:9cd92d324e4bfd0a2ea1f55c9daaf43dd5a3704affe05d59359da761a3ea9a57
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.5 KB (96455 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d70e5224458648b69c985eed8348a59c952ae7671493ce0b9764ad70c0812c47`

```dockerfile
```

-	Layers:
	-	`sha256:b0302e3cc8209d3dfd914c793e581ee84da322d428e5b5ccf19df7d08480f8f7`  
		Last Modified: Mon, 22 Jun 2026 19:53:12 GMT  
		Size: 82.2 KB (82197 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dd339b140e490f5380bd78b29356f7f2ac4429526ab1280b93588123237521bf`  
		Last Modified: Mon, 22 Jun 2026 19:53:11 GMT  
		Size: 14.3 KB (14258 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1-alpine` - linux; arm variant v6

```console
$ docker pull spiped@sha256:797576782eff7b771cd16a7c70d7d3aa681429bfc3a96e3d9caf80de53e1d13c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3593263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f8d26831f4f0d4c40c83254a01dab731517f05ccd3e8233eba9e650a658977b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Mon, 22 Jun 2026 19:19:53 GMT
ADD alpine-minirootfs-3.22.5-armhf.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:19:53 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 19:53:51 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Mon, 22 Jun 2026 19:53:52 GMT
RUN apk add --no-cache libssl3 # buildkit
# Mon, 22 Jun 2026 19:54:02 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Mon, 22 Jun 2026 19:54:02 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Mon, 22 Jun 2026 19:54:02 GMT
VOLUME [/spiped]
# Mon, 22 Jun 2026 19:54:02 GMT
WORKDIR /spiped
# Mon, 22 Jun 2026 19:54:02 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Mon, 22 Jun 2026 19:54:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 22 Jun 2026 19:54:02 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:8efcda622ba07f4da6b9309a34f4650a7a052a1d29a2fc346284c2c1b0899202`  
		Last Modified: Mon, 22 Jun 2026 19:19:58 GMT  
		Size: 3.5 MB (3494800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3032dd20d72fa4a27591cfc40f8eec5d055f3f37cc9eb06329f5cf0e83e19248`  
		Last Modified: Mon, 22 Jun 2026 19:54:06 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58b413eab28f41a1f71ea4831c00e243457d2f484d8b30471a585c9b791580a4`  
		Last Modified: Mon, 22 Jun 2026 19:54:06 GMT  
		Size: 7.9 KB (7935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21ddd27b334e342120f96e4a55937070fef9371ea62ef8a2ee2675febdbac2b8`  
		Last Modified: Mon, 22 Jun 2026 19:54:06 GMT  
		Size: 89.1 KB (89146 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35522b2f0660a559efa25d5c51d7550bf5f21e1df140bd02686304e0d54a6686`  
		Last Modified: Mon, 22 Jun 2026 19:54:06 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70feae8af381e1a5e4dd52b1857289c5766c1fff41f5d377dbde68b6ac8eb2d5`  
		Last Modified: Mon, 22 Jun 2026 19:54:07 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:ab1ba7ca7bcdc700ff165912b9b972504e3ae861646327b59b12551cc63bfff8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.1 KB (14147 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ae2dc57358030a5ccab2ec7826df8c7578005f688b14a6f0440f1e345896ea1`

```dockerfile
```

-	Layers:
	-	`sha256:653d549a72bdd578904772adf12dac81809cf8fb791235e047142cc62a095fe5`  
		Last Modified: Mon, 22 Jun 2026 19:54:06 GMT  
		Size: 14.1 KB (14147 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1-alpine` - linux; arm variant v7

```console
$ docker pull spiped@sha256:0a4bc8b8eb635c2de45437d249d8467c9a1d4bfa67588b7c2b7c356a09950769
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3300611 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9bdc9d57160696d38e8f96024ccba6e14e8a961af83fec3bc71547d3c2ac3477`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Mon, 22 Jun 2026 19:20:47 GMT
ADD alpine-minirootfs-3.22.5-armv7.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:20:47 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 20:07:29 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Mon, 22 Jun 2026 20:07:30 GMT
RUN apk add --no-cache libssl3 # buildkit
# Mon, 22 Jun 2026 20:07:39 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Mon, 22 Jun 2026 20:07:39 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Mon, 22 Jun 2026 20:07:39 GMT
VOLUME [/spiped]
# Mon, 22 Jun 2026 20:07:40 GMT
WORKDIR /spiped
# Mon, 22 Jun 2026 20:07:40 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Mon, 22 Jun 2026 20:07:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 22 Jun 2026 20:07:40 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:276ca41f8e7974c0de50f2551aabece03d11f231f68ab5c6c5051410e0d8c2e7`  
		Last Modified: Mon, 22 Jun 2026 12:03:28 GMT  
		Size: 3.2 MB (3209612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5d412bd01e6b05daa916f63dc49f85e1bc0e28908a915ab5433ee4f773b6d99`  
		Last Modified: Mon, 22 Jun 2026 20:07:45 GMT  
		Size: 948.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f4ca329ff828ab9881adaf1200feef78590b5cf682e928e28811a80fc9ca00c`  
		Last Modified: Mon, 22 Jun 2026 20:07:45 GMT  
		Size: 7.9 KB (7942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68bdfa617d32bd950a899f3c37fc1051103abe4c515575fd0c7a470311e7b1ce`  
		Last Modified: Mon, 22 Jun 2026 20:07:45 GMT  
		Size: 81.7 KB (81676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fb812de9569e6ea964dc192f484efa8f8b40f959ca1aa1cd28efb07d516b3b9`  
		Last Modified: Mon, 22 Jun 2026 20:07:45 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2f94d3b42c6fde945cb292d2ce19b88b4443336f40fd734cfd412ab84954e46`  
		Last Modified: Mon, 22 Jun 2026 20:07:46 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:a5f2de2594b64ce8777794fecdc26dffd6889de81c77f5c600f9de67ac2808f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.6 KB (96595 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6bfc8e0afd039f2387a8475a01f7c55cbb7d95c208d3d65e460898634384300`

```dockerfile
```

-	Layers:
	-	`sha256:c1b261c11b2c6ba30671daf53c170874acef4bb4b844d659bf83d547ab4c5775`  
		Last Modified: Mon, 22 Jun 2026 20:07:45 GMT  
		Size: 82.2 KB (82233 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2429075ab54969202e940d2018a2e0c6eed6ef226d06edb7ace72b19cc19023a`  
		Last Modified: Mon, 22 Jun 2026 20:07:44 GMT  
		Size: 14.4 KB (14362 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1-alpine` - linux; arm64 variant v8

```console
$ docker pull spiped@sha256:4756e80b073870da1063f3705ae4982190aab4ed9e17ddc85106f245d2ed7949
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4230427 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82eb3d5165ba6084a012344ffcdb5bf8cb8999837174113d002240db059e9432`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Mon, 22 Jun 2026 19:20:11 GMT
ADD alpine-minirootfs-3.22.5-aarch64.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:20:11 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 19:54:08 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Mon, 22 Jun 2026 19:54:09 GMT
RUN apk add --no-cache libssl3 # buildkit
# Mon, 22 Jun 2026 19:54:19 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Mon, 22 Jun 2026 19:54:19 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Mon, 22 Jun 2026 19:54:19 GMT
VOLUME [/spiped]
# Mon, 22 Jun 2026 19:54:19 GMT
WORKDIR /spiped
# Mon, 22 Jun 2026 19:54:19 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Mon, 22 Jun 2026 19:54:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 22 Jun 2026 19:54:19 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:738128faa30f570583b0e57efd831e0e6a2a9aacf1be88c8f4c1ef8a5b7033cc`  
		Last Modified: Mon, 22 Jun 2026 09:11:35 GMT  
		Size: 4.1 MB (4120486 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f19dec4b471d7fccd4a70ac0b2f8e3fe4c7aad315844c4b6ea4cc1f27a9e75b`  
		Last Modified: Mon, 22 Jun 2026 19:54:24 GMT  
		Size: 949.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9e119200034afb1c7ec26c08862296c1ebb06ad0e089656c82a87b0cc2ce3d5`  
		Last Modified: Mon, 22 Jun 2026 19:54:24 GMT  
		Size: 7.9 KB (7949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79ed72e155ad35b783a3b2fd26113062c65385d060c1107fd7be78775b11f5df`  
		Last Modified: Mon, 22 Jun 2026 19:54:24 GMT  
		Size: 100.6 KB (100613 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:012dc19e314abeb9a680712049f471d7b225578b746a84c90ddf45f42863b3f3`  
		Last Modified: Mon, 22 Jun 2026 19:54:24 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e2921724d5472f855da9782445382b4df2dbc3fea41b0771456c4bd179c3ac9`  
		Last Modified: Mon, 22 Jun 2026 19:54:25 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:309e398654c9ffb57cf24a14fea4bf0c2931193c153dd095abeba42196ed37a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.6 KB (96646 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9077526648e3aefcc0edbf377ed5794fd580e0064ae615bf7362ce85c3273ad3`

```dockerfile
```

-	Layers:
	-	`sha256:e905129a42e7e89130d80f327d3c87b9cdafa58974899da48f451b550c597127`  
		Last Modified: Mon, 22 Jun 2026 19:54:24 GMT  
		Size: 82.3 KB (82253 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f134d75f49539af75c4f9aa3c0a55672a33a54cf8bf103699ca234354693077c`  
		Last Modified: Mon, 22 Jun 2026 19:54:24 GMT  
		Size: 14.4 KB (14393 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1-alpine` - linux; 386

```console
$ docker pull spiped@sha256:6f3becd5ab17860d0d79cdad5a8314f9f41ade80934bec3e845f2be0549f7399
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3735070 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7c2c4aea7b344dfb6e18f2e0fca5adbbeb691624d97cccfc1e5787f7112f1c1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Mon, 22 Jun 2026 19:20:21 GMT
ADD alpine-minirootfs-3.22.5-x86.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:20:21 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 19:52:33 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Mon, 22 Jun 2026 19:52:34 GMT
RUN apk add --no-cache libssl3 # buildkit
# Mon, 22 Jun 2026 19:52:45 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Mon, 22 Jun 2026 19:52:45 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Mon, 22 Jun 2026 19:52:45 GMT
VOLUME [/spiped]
# Mon, 22 Jun 2026 19:52:45 GMT
WORKDIR /spiped
# Mon, 22 Jun 2026 19:52:45 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Mon, 22 Jun 2026 19:52:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 22 Jun 2026 19:52:45 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:a4b74ab0c43260cc6600b37d5a1ed742d904bba03625caa74b18e45744cde3d1`  
		Last Modified: Mon, 22 Jun 2026 12:03:14 GMT  
		Size: 3.6 MB (3605660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:370212c6233698cf3a2cededd4bd44f00eac7c5e03af3c80a0a1d46c8a4ffdf3`  
		Last Modified: Mon, 22 Jun 2026 19:52:49 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9589ee7d567bbc2c8b0bdd8091e2600f7493e43c86c9291e8e0c5cb80c56fd63`  
		Last Modified: Mon, 22 Jun 2026 19:52:49 GMT  
		Size: 7.9 KB (7935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40a2e946a568955b4fc26e807e13538dfc53fdf5c40195b033d6738d5eb47988`  
		Last Modified: Mon, 22 Jun 2026 19:52:49 GMT  
		Size: 120.1 KB (120096 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5c4c53f53316aa33359a13371beb39c12857d53615d08c755157fbd69bb338d`  
		Last Modified: Mon, 22 Jun 2026 19:52:49 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca3585934873b3572c65ed05b1212ac1144f16b9ef8468d66230cedacf8c04ab`  
		Last Modified: Mon, 22 Jun 2026 19:52:51 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:069fb82d31cd63808dd6a7d5c56b36a98d126a4f8d452cff42e101a369d62c21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.4 KB (96395 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a99309a2ee767f77be492110796b79f8f183f4a91c5e150ce93856bfc9eb541a`

```dockerfile
```

-	Layers:
	-	`sha256:f85f07db752d4a828f227d726b92f676379255ba60f6efa8fb1a91b8cb20e575`  
		Last Modified: Mon, 22 Jun 2026 19:52:49 GMT  
		Size: 82.2 KB (82172 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6ee94877067613386073525f14205ddff5c1f158f239bc7509f064e7c73ecc48`  
		Last Modified: Mon, 22 Jun 2026 19:52:49 GMT  
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
$ docker pull spiped@sha256:de4b34c7a3ad65daa04d28d7e12287d7241887e56b69c69bb8935fefbd9c0062
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
$ docker pull spiped@sha256:06f6d191d00c3c7f99f9ca6bc35961abde2cefdf0c4c3ef829ee12c8e723b1a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.8 MB (36835681 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b886f796060d79ea57dfed8e6573334428e6ba942e2416c5e9d4991e4358f4d6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 00:36:40 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Thu, 11 Jun 2026 00:36:43 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:37:07 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Thu, 11 Jun 2026 00:37:07 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Thu, 11 Jun 2026 00:37:07 GMT
VOLUME [/spiped]
# Thu, 11 Jun 2026 00:37:07 GMT
WORKDIR /spiped
# Thu, 11 Jun 2026 00:37:07 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Thu, 11 Jun 2026 00:37:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 11 Jun 2026 00:37:07 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:72c03230f1363a3fb61d2f98504cf168bad3fe22f511ad2005dc021515d7ce97`  
		Last Modified: Wed, 10 Jun 2026 23:40:25 GMT  
		Size: 29.8 MB (29785415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:527ecde60bfe50017124e67b8415956fd4fb6c9d88a886f3050cf3759f4f98dd`  
		Last Modified: Thu, 11 Jun 2026 00:37:15 GMT  
		Size: 1.1 KB (1104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ccfb06129b754706d994d24161d30c750e9d947232c5d51a4213ea845f178c5`  
		Last Modified: Thu, 11 Jun 2026 00:37:15 GMT  
		Size: 827.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef3d898f83d1faa117388bd37c5a2c913e57742474e0f610d32e0e1c83e5c8ef`  
		Last Modified: Thu, 11 Jun 2026 00:37:15 GMT  
		Size: 7.0 MB (7047900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1436ff66f580ac7020fa765af6cbc9cd8c91911721a10dfa2305b6404b18cea`  
		Last Modified: Thu, 11 Jun 2026 00:37:15 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2d6ed45d70891121ffe50995b4a569aa6dbda4c3a37a3fa16927fe16da829f7`  
		Last Modified: Thu, 11 Jun 2026 00:37:16 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6` - unknown; unknown

```console
$ docker pull spiped@sha256:d5cecdf47fa2040ff01111fdbbb75c19d537a969a776bc1c8778d421c2364a04
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3641284 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:082365ba064127a901f5498578d29ee8a542bbc7adc94e40bf4cf9e2a84a407f`

```dockerfile
```

-	Layers:
	-	`sha256:8a7bb242a706f30d64bcc8002692cee4179a16af8322cf72d23b0a8c78123a57`  
		Last Modified: Thu, 11 Jun 2026 00:37:15 GMT  
		Size: 3.6 MB (3626302 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:789d0bf94bddbb877fd99e66c1f0e2fa4901e5821fb450c040ff83bf254aeb75`  
		Last Modified: Thu, 11 Jun 2026 00:37:15 GMT  
		Size: 15.0 KB (14982 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6` - linux; arm variant v5

```console
$ docker pull spiped@sha256:3a77fd17bf87542b39acd5c371cb4509f911aba18087b5841340cdae79eb07e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.8 MB (33750953 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9f871c59019572295a1c6f16175304e8c052d7ae1bde8550e6316bd337fc36b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 01:20:06 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Thu, 11 Jun 2026 01:20:11 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 01:20:37 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Thu, 11 Jun 2026 01:20:37 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Thu, 11 Jun 2026 01:20:37 GMT
VOLUME [/spiped]
# Thu, 11 Jun 2026 01:20:37 GMT
WORKDIR /spiped
# Thu, 11 Jun 2026 01:20:38 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Thu, 11 Jun 2026 01:20:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 11 Jun 2026 01:20:38 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:ed883f3fd95b7edef302d7ca9520eefdae280af081509bd7e9e5b5ff8f4cda7c`  
		Last Modified: Wed, 10 Jun 2026 23:41:17 GMT  
		Size: 28.0 MB (27959200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e751f68dcb09ba1579bee55a24286186b59e393de92bac08ff724b4981d5d170`  
		Last Modified: Thu, 11 Jun 2026 01:20:44 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d89df5ca97fe521123a4a7aae01c94c4479bf368a9d8c696eee17064fc312bc1`  
		Last Modified: Thu, 11 Jun 2026 01:20:45 GMT  
		Size: 831.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91d2c4ac84d26c20df4907085b90aeb331861a219b69716c57682ae2cb946eb8`  
		Last Modified: Thu, 11 Jun 2026 01:20:45 GMT  
		Size: 5.8 MB (5789383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2073b26a67b2b25b8dae9d6d7a2028b43f95697825a4cb34a083684f542d8fe`  
		Last Modified: Thu, 11 Jun 2026 01:20:45 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1e64de9d592c6c09b59082de73dbb84f8e63a26763394e8083e1dd58f66d693`  
		Last Modified: Thu, 11 Jun 2026 01:20:46 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6` - unknown; unknown

```console
$ docker pull spiped@sha256:e786ed555ddf93e97965e805339e0e57e642ee1b6992efb0a38706feed7d6111
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3634384 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:678d30be6a2af3135f4751e15d6b35b82e2cd1dbc9a6858fa252aa22ea5487f6`

```dockerfile
```

-	Layers:
	-	`sha256:f416dd4fb0aef1763e3288e5f7435905aa2cacf86c5d53d1ff62343b3aee11b4`  
		Last Modified: Thu, 11 Jun 2026 01:20:45 GMT  
		Size: 3.6 MB (3619296 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6a02acc670c38ba874d76cb8784856b12a90aa7e49311ee73beff9aa2761b4c8`  
		Last Modified: Thu, 11 Jun 2026 01:20:45 GMT  
		Size: 15.1 KB (15088 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6` - linux; arm variant v7

```console
$ docker pull spiped@sha256:079fbf73e349c36cc2b4d55e664f1d5a60b482fa43a1021f0ea8cb3e38b490fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.8 MB (31798135 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:959018a10d28c5d1dde8c33184f543a1293c46376550688e906dbae7ddf55228`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 01:21:52 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Thu, 11 Jun 2026 01:21:55 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 01:22:18 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Thu, 11 Jun 2026 01:22:18 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Thu, 11 Jun 2026 01:22:18 GMT
VOLUME [/spiped]
# Thu, 11 Jun 2026 01:22:18 GMT
WORKDIR /spiped
# Thu, 11 Jun 2026 01:22:18 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Thu, 11 Jun 2026 01:22:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 11 Jun 2026 01:22:18 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:4bd6ddea06d5009ee47ddb0f254a2569aff0230c005869ebd416b20295d945c0`  
		Last Modified: Wed, 10 Jun 2026 23:42:34 GMT  
		Size: 26.2 MB (26211004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51bb869011c6d164e974fe820179933094dcc281df7a55480fc4077277232c77`  
		Last Modified: Thu, 11 Jun 2026 01:22:25 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:422e823bc0c6498856622e79affa11c1598652143bfa7f350dc04a8bae10a58a`  
		Last Modified: Thu, 11 Jun 2026 01:22:25 GMT  
		Size: 827.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fadeadb89fb7f698439cd322f47ba897a03fd1551ffe3fcf76d75f5383cd472`  
		Last Modified: Thu, 11 Jun 2026 01:22:25 GMT  
		Size: 5.6 MB (5584763 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3817b48e6549ab977fe0f1bbbb517045c499e8b6a3c28271dc05398321fe485d`  
		Last Modified: Thu, 11 Jun 2026 01:22:25 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a52c3658e003288d1598c728ef7ab0c5167ce43d1e20bf855db1dde18f30b339`  
		Last Modified: Thu, 11 Jun 2026 01:22:27 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6` - unknown; unknown

```console
$ docker pull spiped@sha256:4660d6bee86fba733a44735e9cea0b5dfa13410ac081e02edbed22229736f4ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3633504 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f7dd6ebfec69dc7720608ae6a9b0c5af682ff982f3ce0440ed4f3bf904f4c5f`

```dockerfile
```

-	Layers:
	-	`sha256:d25034d6fee06e5ff09bdc9004cbe4b4a4e9d9ed95b0624f5000cb9e580a086e`  
		Last Modified: Thu, 11 Jun 2026 01:22:25 GMT  
		Size: 3.6 MB (3618417 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:deb1d9d6f39ee38fed21b5f4de28c58d8058b0810a5cd7893d92d295084642d1`  
		Last Modified: Thu, 11 Jun 2026 01:22:25 GMT  
		Size: 15.1 KB (15087 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6` - linux; arm64 variant v8

```console
$ docker pull spiped@sha256:b666025eb8bf9bd288d28306188f384cf5e1cf793252a3092ed8467ea174a7c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.4 MB (36384823 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2b7f7df51ecb422ed1c09aa176c982afa86a96f6e553daf85ffd468ca5f3846`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 00:38:14 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Thu, 11 Jun 2026 00:38:16 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:38:39 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Thu, 11 Jun 2026 00:38:39 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Thu, 11 Jun 2026 00:38:39 GMT
VOLUME [/spiped]
# Thu, 11 Jun 2026 00:38:39 GMT
WORKDIR /spiped
# Thu, 11 Jun 2026 00:38:39 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Thu, 11 Jun 2026 00:38:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 11 Jun 2026 00:38:39 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:a25cd16f2d8653f652f8292b34b21bfbabdc85d6b39861a24b85f0896df1a95e`  
		Last Modified: Wed, 10 Jun 2026 23:40:16 GMT  
		Size: 30.1 MB (30148530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af99214715c4dd89b01b22d803c733a8cdeff8b516b64dcbc4039e3bb73edf81`  
		Last Modified: Thu, 11 Jun 2026 00:38:46 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cb7f2ca44a46746d13284bd66cb8d509327101aa851a60e2f4562b4c0b43fe4`  
		Last Modified: Thu, 11 Jun 2026 00:38:46 GMT  
		Size: 828.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fc568496a63b54431809869a1a353a056bd0286efc252ed16943213148d8e78`  
		Last Modified: Thu, 11 Jun 2026 00:38:46 GMT  
		Size: 6.2 MB (6233926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62455682699c33f1af511f11805177432eb0df675093f3a55be46e8069d099ad`  
		Last Modified: Thu, 11 Jun 2026 00:38:46 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1337cf4ae97e82beefcd0736801f263b58faa5acea8bbd02b6fb1610b3c08a69`  
		Last Modified: Thu, 11 Jun 2026 00:38:47 GMT  
		Size: 336.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6` - unknown; unknown

```console
$ docker pull spiped@sha256:28fd7f18765bc97e01aed948eb208846037e2fdc5be5b01c7b60a1dab0ecc29d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3636446 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:caaed5bb2a83f15f132837c8042bc95288ce03bd799f9d4a49b960975af17bea`

```dockerfile
```

-	Layers:
	-	`sha256:f4119ebc6f5a2232c489599390a07000eb50a2325250846032e65737506b59fb`  
		Last Modified: Thu, 11 Jun 2026 00:38:46 GMT  
		Size: 3.6 MB (3621330 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ff1ae5a7dd30d786394e331ae8fd4a26444a7fab07e0f0f35bd0d9f9e8aa11f4`  
		Last Modified: Thu, 11 Jun 2026 00:38:46 GMT  
		Size: 15.1 KB (15116 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6` - linux; 386

```console
$ docker pull spiped@sha256:02f4ba23c22e1271ac47e549272f9bb9b73d515c584ef6657b10b34089186119
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.7 MB (37746372 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c77be7a202c7361655d5298662fbd58b4ac13a280d8eea6d0e5696277b5d6dc2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 00:44:31 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Thu, 11 Jun 2026 00:44:34 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:45:03 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Thu, 11 Jun 2026 00:45:03 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Thu, 11 Jun 2026 00:45:03 GMT
VOLUME [/spiped]
# Thu, 11 Jun 2026 00:45:03 GMT
WORKDIR /spiped
# Thu, 11 Jun 2026 00:45:03 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Thu, 11 Jun 2026 00:45:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 11 Jun 2026 00:45:03 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:720f951a68f4f9ab464e52b53cf88cfb86bc876b3f00956d000420777ab93c0c`  
		Last Modified: Wed, 10 Jun 2026 23:40:30 GMT  
		Size: 31.3 MB (31301194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96b36e957fa28b38d49b885ce8ff4366a6bfcb98bf38aa1dd3dd51c9b7cd333c`  
		Last Modified: Thu, 11 Jun 2026 00:45:10 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3aae632d05299c9dee2bec97ea596046cf5c7c15eff6529e97937627b28994fa`  
		Last Modified: Thu, 11 Jun 2026 00:45:10 GMT  
		Size: 828.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd7f7718fe56cea19c8269279c48994d7ae792b5209abc4faef63781a55560f4`  
		Last Modified: Thu, 11 Jun 2026 00:45:11 GMT  
		Size: 6.4 MB (6442811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96e529f830d838d84290e5326067c74dc889693a3954cd9a7dbd43c0b583c23f`  
		Last Modified: Thu, 11 Jun 2026 00:45:10 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fe774eab45468f5459c9ea3e437c826c9c3d130cbc49f077eef0338b91a9edd`  
		Last Modified: Thu, 11 Jun 2026 00:45:12 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6` - unknown; unknown

```console
$ docker pull spiped@sha256:43aeb04090782a915b6e9289e6133f1f0327b7465670b94e07f481b847c4025b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3635377 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd02b428a54369d078699f646a6c58bb59205a7d8e90fd308ef1b652598d64f9`

```dockerfile
```

-	Layers:
	-	`sha256:20700448f422d0e1e5f84b34dcae83618e79e0454a188609c16921611a98ff5a`  
		Last Modified: Thu, 11 Jun 2026 00:45:10 GMT  
		Size: 3.6 MB (3620431 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b8c3c92718b75b733828274ef1f0c3ac60a2665e98431b090587ac61fa798684`  
		Last Modified: Thu, 11 Jun 2026 00:45:10 GMT  
		Size: 14.9 KB (14946 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6` - linux; ppc64le

```console
$ docker pull spiped@sha256:77a28ff7796938b2e628dcb8466cba0a9b9e9209373514b53eb9500a4eb54179
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.4 MB (40449493 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5c663351cf736af7041bf6dab200f7240abda1f91a38cc9154e15ecc605051b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 04:42:39 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Thu, 11 Jun 2026 04:42:43 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 04:43:31 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Thu, 11 Jun 2026 04:43:31 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Thu, 11 Jun 2026 04:43:31 GMT
VOLUME [/spiped]
# Thu, 11 Jun 2026 04:43:31 GMT
WORKDIR /spiped
# Thu, 11 Jun 2026 04:43:31 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Thu, 11 Jun 2026 04:43:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 11 Jun 2026 04:43:31 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:9d6b2e320e2b74843186d830e8202c50ebfaeccf823d239e3e3e349a8a508d80`  
		Last Modified: Thu, 11 Jun 2026 00:24:42 GMT  
		Size: 33.6 MB (33606340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae397a9bd78994d17d78508ffe6c90b95321c279f11d71546a6690cf7b3bfa56`  
		Last Modified: Thu, 11 Jun 2026 04:43:44 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:527c0346e0be1cff6e959785d2ead56a024d388a5f5b49668bb10ef02df87e5b`  
		Last Modified: Thu, 11 Jun 2026 04:43:44 GMT  
		Size: 825.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfb798ab52e9baacaca51304c7ae7bd07e22ffa204c22fa1ee3f600faa9d384c`  
		Last Modified: Thu, 11 Jun 2026 04:43:45 GMT  
		Size: 6.8 MB (6840786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9e2eda05f5b8c55e69e0f5f7b8411ef18adfa257a0964e74893e13aa8460231`  
		Last Modified: Thu, 11 Jun 2026 04:43:44 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89c91b4a125ec65053187500a3042ba5cf4b3d3c3757a5130a5b6a469502146e`  
		Last Modified: Thu, 11 Jun 2026 04:43:45 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6` - unknown; unknown

```console
$ docker pull spiped@sha256:cde6ed1dd2ca8f029ced3770c7fd29bfed2a5e054b7f88c1c2828ea61ae0d53a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3637067 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f348c1d24e29a4dd183acde8c7db1a7186ed71bf6cc2b0deb230af07b7e3608`

```dockerfile
```

-	Layers:
	-	`sha256:9028cc214c0ddc113b07afbc6b1c7d125225085781875688e233501b5e4f6973`  
		Last Modified: Thu, 11 Jun 2026 04:43:45 GMT  
		Size: 3.6 MB (3622039 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:23b0df7ce9f0c385bfc283502819fb193952bc81b97402aae117279766c4435f`  
		Last Modified: Thu, 11 Jun 2026 04:43:44 GMT  
		Size: 15.0 KB (15028 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6` - linux; riscv64

```console
$ docker pull spiped@sha256:d1196bf05f6d34c1b33d0f44d558a64dacbac606da8ede3854f0f56b7da88dd7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.6 MB (37640838 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:257f964733ff5e0fb249561928b63d968d0ea7e0f22a1650497b8f634a78b7b1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1781049600'
# Sat, 13 Jun 2026 02:38:34 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Sat, 13 Jun 2026 02:39:05 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 13 Jun 2026 02:42:10 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Sat, 13 Jun 2026 02:42:10 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Sat, 13 Jun 2026 02:42:10 GMT
VOLUME [/spiped]
# Sat, 13 Jun 2026 02:42:10 GMT
WORKDIR /spiped
# Sat, 13 Jun 2026 02:42:10 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sat, 13 Jun 2026 02:42:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 13 Jun 2026 02:42:10 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:0b510fe8545cab831b696965b5a825649c5c945581e912d31a08a0b30ff940c0`  
		Last Modified: Thu, 11 Jun 2026 03:01:06 GMT  
		Size: 28.3 MB (28282305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f639c6130c8aca0f837b171cb0a0d45c790c5d7bf9518eff2b8ff95b48f104c`  
		Last Modified: Sat, 13 Jun 2026 02:43:23 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07e14a8d467e3dc32c3ec2a585b788255e6272eeaa9763d004943122f7248c27`  
		Last Modified: Sat, 13 Jun 2026 02:43:23 GMT  
		Size: 822.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d41b9627a0c3fc9b82eb3a3347a368ac72d11d19f3ff135e81910be58f7ced5`  
		Last Modified: Sat, 13 Jun 2026 02:43:24 GMT  
		Size: 9.4 MB (9356169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4946ccd28be72a02f3c71907db8b182219a80ff46301e8a09fdd946d52683dd8`  
		Last Modified: Sat, 13 Jun 2026 02:43:23 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f74e027caa4d5bd042803e1c5847e795634af08a895bf7099c444bcdf51c4cc`  
		Last Modified: Sat, 13 Jun 2026 02:43:24 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6` - unknown; unknown

```console
$ docker pull spiped@sha256:bd59a45c25ec7d4b80d63933dffd3bd86372d97041734ebbf62964d8a991e093
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3628474 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0ed4a489648532fba6cde1d7e88a809bdb98383c98aee19aaba7a5a947fbd77`

```dockerfile
```

-	Layers:
	-	`sha256:d44a97abcbeafd6a6ec2dd69c997db68246839a5985937d49f3c1d5fbc99a495`  
		Last Modified: Sat, 13 Jun 2026 02:43:24 GMT  
		Size: 3.6 MB (3613445 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:de64e5286a1b72fafa9b68c701bf6ba016f164bdfaf60538499d95770fbf3f6a`  
		Last Modified: Sat, 13 Jun 2026 02:43:23 GMT  
		Size: 15.0 KB (15029 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6` - linux; s390x

```console
$ docker pull spiped@sha256:bd22ee71a9e9236e2ca69180ad51c06cf6d8e35afbd4add081b0d2f764edc08e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.0 MB (35975833 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1ad1052f1364f10f7a17a6666de217cbde8ab8c0e0ac3499018c5cd72b4ee17`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 01:43:42 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Thu, 11 Jun 2026 01:43:44 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 01:44:01 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Thu, 11 Jun 2026 01:44:01 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Thu, 11 Jun 2026 01:44:01 GMT
VOLUME [/spiped]
# Thu, 11 Jun 2026 01:44:01 GMT
WORKDIR /spiped
# Thu, 11 Jun 2026 01:44:01 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Thu, 11 Jun 2026 01:44:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 11 Jun 2026 01:44:01 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:760dcf74fdfe93300ce15b5b23adf9aa4af45b6ba9d69925863198f64881a537`  
		Last Modified: Wed, 10 Jun 2026 23:42:35 GMT  
		Size: 29.9 MB (29851354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbee78aca287a132f4560c3c136874e9fd2eb76d548257a9d3a3df8c901bcc4f`  
		Last Modified: Thu, 11 Jun 2026 01:44:13 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:592a34f021f7dfd15ace5226ae509b1158c586b704884d60433770343a082992`  
		Last Modified: Thu, 11 Jun 2026 01:44:13 GMT  
		Size: 828.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb3568250ea65438eb60733aee26c97620a46d0a35f1724cad1b6cdf7fbcc023`  
		Last Modified: Thu, 11 Jun 2026 01:44:13 GMT  
		Size: 6.1 MB (6122111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b205eccacc5cb65c52b6fa4618ba96b957fd2f8a2f5423e2653cc1b280d2f23`  
		Last Modified: Thu, 11 Jun 2026 01:44:13 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02c73a6752a874142787522de11c367cd55d46e4661d6e3216d3509660bc3091`  
		Last Modified: Thu, 11 Jun 2026 01:44:14 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6` - unknown; unknown

```console
$ docker pull spiped@sha256:b9ccb006c7597035afc395814bcd5e176f1c6747e8cdcbb2e2e99a609798685c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3633647 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0955f426902eecb0ba4cee729a5abb10364e89f0579f841377a2401fdd89f43`

```dockerfile
```

-	Layers:
	-	`sha256:bc258d4741b882519b7d7392f726369c450df7d38b8a5f5b761096da236e6d1a`  
		Last Modified: Thu, 11 Jun 2026 01:44:13 GMT  
		Size: 3.6 MB (3618665 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9e8ebd7ccddfecb937db9fd26d8850a9b8222af37b614601c7b7e2d424a147fa`  
		Last Modified: Thu, 11 Jun 2026 01:44:13 GMT  
		Size: 15.0 KB (14982 bytes)  
		MIME: application/vnd.in-toto+json

## `spiped:1.6-alpine`

```console
$ docker pull spiped@sha256:d321da057edcf67209e6a50fce596020211d058f66861249f42c546d7d818fe4
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
$ docker pull spiped@sha256:ddacdd500302ed8e0b56cfbe5eba1b03890a3a11103e2e79f118f78819546c96
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3904546 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0e50065de302c7f6a370e6ce4b691cc04feab696fd0ca4c59d5c21b96d09a5f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Mon, 22 Jun 2026 19:20:21 GMT
ADD alpine-minirootfs-3.22.5-x86_64.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:20:21 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 19:52:57 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Mon, 22 Jun 2026 19:52:58 GMT
RUN apk add --no-cache libssl3 # buildkit
# Mon, 22 Jun 2026 19:53:07 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Mon, 22 Jun 2026 19:53:07 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Mon, 22 Jun 2026 19:53:07 GMT
VOLUME [/spiped]
# Mon, 22 Jun 2026 19:53:07 GMT
WORKDIR /spiped
# Mon, 22 Jun 2026 19:53:07 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Mon, 22 Jun 2026 19:53:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 22 Jun 2026 19:53:07 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:f7ee36c9aa34bbb665f975c76e5c0d1607f0674b94c84cfb0061f87006ea5d10`  
		Last Modified: Mon, 22 Jun 2026 09:11:44 GMT  
		Size: 3.8 MB (3787595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e11e0fcbf833efd71ccdc39dad69485c2ab9e33be6a7075e11f23dfc938ee0b`  
		Last Modified: Mon, 22 Jun 2026 19:53:11 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d3df5ddcf63216635d6ac9800edfcdf71dbf67c7328ec84d1b3ab49da64adf0`  
		Last Modified: Mon, 22 Jun 2026 19:53:11 GMT  
		Size: 7.9 KB (7939 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68bf1a439bfe49642cefb4e5461e95befb5f5a9b5cced180eaf651935a1246f9`  
		Last Modified: Mon, 22 Jun 2026 19:53:11 GMT  
		Size: 107.6 KB (107630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f2716e286de0031c590e0551ee0bcfbe0740fde1029874d538fecad89dadaca`  
		Last Modified: Mon, 22 Jun 2026 19:53:12 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe62eb4d32c49f1f3ab36f4fa4341f61fe5f3eccfbb08576ec70be11772704af`  
		Last Modified: Mon, 22 Jun 2026 19:53:13 GMT  
		Size: 336.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:9cd92d324e4bfd0a2ea1f55c9daaf43dd5a3704affe05d59359da761a3ea9a57
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.5 KB (96455 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d70e5224458648b69c985eed8348a59c952ae7671493ce0b9764ad70c0812c47`

```dockerfile
```

-	Layers:
	-	`sha256:b0302e3cc8209d3dfd914c793e581ee84da322d428e5b5ccf19df7d08480f8f7`  
		Last Modified: Mon, 22 Jun 2026 19:53:12 GMT  
		Size: 82.2 KB (82197 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dd339b140e490f5380bd78b29356f7f2ac4429526ab1280b93588123237521bf`  
		Last Modified: Mon, 22 Jun 2026 19:53:11 GMT  
		Size: 14.3 KB (14258 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6-alpine` - linux; arm variant v6

```console
$ docker pull spiped@sha256:797576782eff7b771cd16a7c70d7d3aa681429bfc3a96e3d9caf80de53e1d13c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3593263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f8d26831f4f0d4c40c83254a01dab731517f05ccd3e8233eba9e650a658977b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Mon, 22 Jun 2026 19:19:53 GMT
ADD alpine-minirootfs-3.22.5-armhf.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:19:53 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 19:53:51 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Mon, 22 Jun 2026 19:53:52 GMT
RUN apk add --no-cache libssl3 # buildkit
# Mon, 22 Jun 2026 19:54:02 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Mon, 22 Jun 2026 19:54:02 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Mon, 22 Jun 2026 19:54:02 GMT
VOLUME [/spiped]
# Mon, 22 Jun 2026 19:54:02 GMT
WORKDIR /spiped
# Mon, 22 Jun 2026 19:54:02 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Mon, 22 Jun 2026 19:54:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 22 Jun 2026 19:54:02 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:8efcda622ba07f4da6b9309a34f4650a7a052a1d29a2fc346284c2c1b0899202`  
		Last Modified: Mon, 22 Jun 2026 19:19:58 GMT  
		Size: 3.5 MB (3494800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3032dd20d72fa4a27591cfc40f8eec5d055f3f37cc9eb06329f5cf0e83e19248`  
		Last Modified: Mon, 22 Jun 2026 19:54:06 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58b413eab28f41a1f71ea4831c00e243457d2f484d8b30471a585c9b791580a4`  
		Last Modified: Mon, 22 Jun 2026 19:54:06 GMT  
		Size: 7.9 KB (7935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21ddd27b334e342120f96e4a55937070fef9371ea62ef8a2ee2675febdbac2b8`  
		Last Modified: Mon, 22 Jun 2026 19:54:06 GMT  
		Size: 89.1 KB (89146 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35522b2f0660a559efa25d5c51d7550bf5f21e1df140bd02686304e0d54a6686`  
		Last Modified: Mon, 22 Jun 2026 19:54:06 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70feae8af381e1a5e4dd52b1857289c5766c1fff41f5d377dbde68b6ac8eb2d5`  
		Last Modified: Mon, 22 Jun 2026 19:54:07 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:ab1ba7ca7bcdc700ff165912b9b972504e3ae861646327b59b12551cc63bfff8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.1 KB (14147 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ae2dc57358030a5ccab2ec7826df8c7578005f688b14a6f0440f1e345896ea1`

```dockerfile
```

-	Layers:
	-	`sha256:653d549a72bdd578904772adf12dac81809cf8fb791235e047142cc62a095fe5`  
		Last Modified: Mon, 22 Jun 2026 19:54:06 GMT  
		Size: 14.1 KB (14147 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6-alpine` - linux; arm variant v7

```console
$ docker pull spiped@sha256:0a4bc8b8eb635c2de45437d249d8467c9a1d4bfa67588b7c2b7c356a09950769
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3300611 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9bdc9d57160696d38e8f96024ccba6e14e8a961af83fec3bc71547d3c2ac3477`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Mon, 22 Jun 2026 19:20:47 GMT
ADD alpine-minirootfs-3.22.5-armv7.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:20:47 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 20:07:29 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Mon, 22 Jun 2026 20:07:30 GMT
RUN apk add --no-cache libssl3 # buildkit
# Mon, 22 Jun 2026 20:07:39 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Mon, 22 Jun 2026 20:07:39 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Mon, 22 Jun 2026 20:07:39 GMT
VOLUME [/spiped]
# Mon, 22 Jun 2026 20:07:40 GMT
WORKDIR /spiped
# Mon, 22 Jun 2026 20:07:40 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Mon, 22 Jun 2026 20:07:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 22 Jun 2026 20:07:40 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:276ca41f8e7974c0de50f2551aabece03d11f231f68ab5c6c5051410e0d8c2e7`  
		Last Modified: Mon, 22 Jun 2026 12:03:28 GMT  
		Size: 3.2 MB (3209612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5d412bd01e6b05daa916f63dc49f85e1bc0e28908a915ab5433ee4f773b6d99`  
		Last Modified: Mon, 22 Jun 2026 20:07:45 GMT  
		Size: 948.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f4ca329ff828ab9881adaf1200feef78590b5cf682e928e28811a80fc9ca00c`  
		Last Modified: Mon, 22 Jun 2026 20:07:45 GMT  
		Size: 7.9 KB (7942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68bdfa617d32bd950a899f3c37fc1051103abe4c515575fd0c7a470311e7b1ce`  
		Last Modified: Mon, 22 Jun 2026 20:07:45 GMT  
		Size: 81.7 KB (81676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fb812de9569e6ea964dc192f484efa8f8b40f959ca1aa1cd28efb07d516b3b9`  
		Last Modified: Mon, 22 Jun 2026 20:07:45 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2f94d3b42c6fde945cb292d2ce19b88b4443336f40fd734cfd412ab84954e46`  
		Last Modified: Mon, 22 Jun 2026 20:07:46 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:a5f2de2594b64ce8777794fecdc26dffd6889de81c77f5c600f9de67ac2808f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.6 KB (96595 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6bfc8e0afd039f2387a8475a01f7c55cbb7d95c208d3d65e460898634384300`

```dockerfile
```

-	Layers:
	-	`sha256:c1b261c11b2c6ba30671daf53c170874acef4bb4b844d659bf83d547ab4c5775`  
		Last Modified: Mon, 22 Jun 2026 20:07:45 GMT  
		Size: 82.2 KB (82233 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2429075ab54969202e940d2018a2e0c6eed6ef226d06edb7ace72b19cc19023a`  
		Last Modified: Mon, 22 Jun 2026 20:07:44 GMT  
		Size: 14.4 KB (14362 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6-alpine` - linux; arm64 variant v8

```console
$ docker pull spiped@sha256:4756e80b073870da1063f3705ae4982190aab4ed9e17ddc85106f245d2ed7949
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4230427 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82eb3d5165ba6084a012344ffcdb5bf8cb8999837174113d002240db059e9432`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Mon, 22 Jun 2026 19:20:11 GMT
ADD alpine-minirootfs-3.22.5-aarch64.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:20:11 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 19:54:08 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Mon, 22 Jun 2026 19:54:09 GMT
RUN apk add --no-cache libssl3 # buildkit
# Mon, 22 Jun 2026 19:54:19 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Mon, 22 Jun 2026 19:54:19 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Mon, 22 Jun 2026 19:54:19 GMT
VOLUME [/spiped]
# Mon, 22 Jun 2026 19:54:19 GMT
WORKDIR /spiped
# Mon, 22 Jun 2026 19:54:19 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Mon, 22 Jun 2026 19:54:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 22 Jun 2026 19:54:19 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:738128faa30f570583b0e57efd831e0e6a2a9aacf1be88c8f4c1ef8a5b7033cc`  
		Last Modified: Mon, 22 Jun 2026 09:11:35 GMT  
		Size: 4.1 MB (4120486 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f19dec4b471d7fccd4a70ac0b2f8e3fe4c7aad315844c4b6ea4cc1f27a9e75b`  
		Last Modified: Mon, 22 Jun 2026 19:54:24 GMT  
		Size: 949.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9e119200034afb1c7ec26c08862296c1ebb06ad0e089656c82a87b0cc2ce3d5`  
		Last Modified: Mon, 22 Jun 2026 19:54:24 GMT  
		Size: 7.9 KB (7949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79ed72e155ad35b783a3b2fd26113062c65385d060c1107fd7be78775b11f5df`  
		Last Modified: Mon, 22 Jun 2026 19:54:24 GMT  
		Size: 100.6 KB (100613 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:012dc19e314abeb9a680712049f471d7b225578b746a84c90ddf45f42863b3f3`  
		Last Modified: Mon, 22 Jun 2026 19:54:24 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e2921724d5472f855da9782445382b4df2dbc3fea41b0771456c4bd179c3ac9`  
		Last Modified: Mon, 22 Jun 2026 19:54:25 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:309e398654c9ffb57cf24a14fea4bf0c2931193c153dd095abeba42196ed37a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.6 KB (96646 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9077526648e3aefcc0edbf377ed5794fd580e0064ae615bf7362ce85c3273ad3`

```dockerfile
```

-	Layers:
	-	`sha256:e905129a42e7e89130d80f327d3c87b9cdafa58974899da48f451b550c597127`  
		Last Modified: Mon, 22 Jun 2026 19:54:24 GMT  
		Size: 82.3 KB (82253 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f134d75f49539af75c4f9aa3c0a55672a33a54cf8bf103699ca234354693077c`  
		Last Modified: Mon, 22 Jun 2026 19:54:24 GMT  
		Size: 14.4 KB (14393 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6-alpine` - linux; 386

```console
$ docker pull spiped@sha256:6f3becd5ab17860d0d79cdad5a8314f9f41ade80934bec3e845f2be0549f7399
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3735070 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7c2c4aea7b344dfb6e18f2e0fca5adbbeb691624d97cccfc1e5787f7112f1c1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Mon, 22 Jun 2026 19:20:21 GMT
ADD alpine-minirootfs-3.22.5-x86.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:20:21 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 19:52:33 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Mon, 22 Jun 2026 19:52:34 GMT
RUN apk add --no-cache libssl3 # buildkit
# Mon, 22 Jun 2026 19:52:45 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Mon, 22 Jun 2026 19:52:45 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Mon, 22 Jun 2026 19:52:45 GMT
VOLUME [/spiped]
# Mon, 22 Jun 2026 19:52:45 GMT
WORKDIR /spiped
# Mon, 22 Jun 2026 19:52:45 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Mon, 22 Jun 2026 19:52:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 22 Jun 2026 19:52:45 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:a4b74ab0c43260cc6600b37d5a1ed742d904bba03625caa74b18e45744cde3d1`  
		Last Modified: Mon, 22 Jun 2026 12:03:14 GMT  
		Size: 3.6 MB (3605660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:370212c6233698cf3a2cededd4bd44f00eac7c5e03af3c80a0a1d46c8a4ffdf3`  
		Last Modified: Mon, 22 Jun 2026 19:52:49 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9589ee7d567bbc2c8b0bdd8091e2600f7493e43c86c9291e8e0c5cb80c56fd63`  
		Last Modified: Mon, 22 Jun 2026 19:52:49 GMT  
		Size: 7.9 KB (7935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40a2e946a568955b4fc26e807e13538dfc53fdf5c40195b033d6738d5eb47988`  
		Last Modified: Mon, 22 Jun 2026 19:52:49 GMT  
		Size: 120.1 KB (120096 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5c4c53f53316aa33359a13371beb39c12857d53615d08c755157fbd69bb338d`  
		Last Modified: Mon, 22 Jun 2026 19:52:49 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca3585934873b3572c65ed05b1212ac1144f16b9ef8468d66230cedacf8c04ab`  
		Last Modified: Mon, 22 Jun 2026 19:52:51 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:069fb82d31cd63808dd6a7d5c56b36a98d126a4f8d452cff42e101a369d62c21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.4 KB (96395 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a99309a2ee767f77be492110796b79f8f183f4a91c5e150ce93856bfc9eb541a`

```dockerfile
```

-	Layers:
	-	`sha256:f85f07db752d4a828f227d726b92f676379255ba60f6efa8fb1a91b8cb20e575`  
		Last Modified: Mon, 22 Jun 2026 19:52:49 GMT  
		Size: 82.2 KB (82172 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6ee94877067613386073525f14205ddff5c1f158f239bc7509f064e7c73ecc48`  
		Last Modified: Mon, 22 Jun 2026 19:52:49 GMT  
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
$ docker pull spiped@sha256:de4b34c7a3ad65daa04d28d7e12287d7241887e56b69c69bb8935fefbd9c0062
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
$ docker pull spiped@sha256:06f6d191d00c3c7f99f9ca6bc35961abde2cefdf0c4c3ef829ee12c8e723b1a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.8 MB (36835681 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b886f796060d79ea57dfed8e6573334428e6ba942e2416c5e9d4991e4358f4d6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 00:36:40 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Thu, 11 Jun 2026 00:36:43 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:37:07 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Thu, 11 Jun 2026 00:37:07 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Thu, 11 Jun 2026 00:37:07 GMT
VOLUME [/spiped]
# Thu, 11 Jun 2026 00:37:07 GMT
WORKDIR /spiped
# Thu, 11 Jun 2026 00:37:07 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Thu, 11 Jun 2026 00:37:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 11 Jun 2026 00:37:07 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:72c03230f1363a3fb61d2f98504cf168bad3fe22f511ad2005dc021515d7ce97`  
		Last Modified: Wed, 10 Jun 2026 23:40:25 GMT  
		Size: 29.8 MB (29785415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:527ecde60bfe50017124e67b8415956fd4fb6c9d88a886f3050cf3759f4f98dd`  
		Last Modified: Thu, 11 Jun 2026 00:37:15 GMT  
		Size: 1.1 KB (1104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ccfb06129b754706d994d24161d30c750e9d947232c5d51a4213ea845f178c5`  
		Last Modified: Thu, 11 Jun 2026 00:37:15 GMT  
		Size: 827.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef3d898f83d1faa117388bd37c5a2c913e57742474e0f610d32e0e1c83e5c8ef`  
		Last Modified: Thu, 11 Jun 2026 00:37:15 GMT  
		Size: 7.0 MB (7047900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1436ff66f580ac7020fa765af6cbc9cd8c91911721a10dfa2305b6404b18cea`  
		Last Modified: Thu, 11 Jun 2026 00:37:15 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2d6ed45d70891121ffe50995b4a569aa6dbda4c3a37a3fa16927fe16da829f7`  
		Last Modified: Thu, 11 Jun 2026 00:37:16 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6.4` - unknown; unknown

```console
$ docker pull spiped@sha256:d5cecdf47fa2040ff01111fdbbb75c19d537a969a776bc1c8778d421c2364a04
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3641284 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:082365ba064127a901f5498578d29ee8a542bbc7adc94e40bf4cf9e2a84a407f`

```dockerfile
```

-	Layers:
	-	`sha256:8a7bb242a706f30d64bcc8002692cee4179a16af8322cf72d23b0a8c78123a57`  
		Last Modified: Thu, 11 Jun 2026 00:37:15 GMT  
		Size: 3.6 MB (3626302 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:789d0bf94bddbb877fd99e66c1f0e2fa4901e5821fb450c040ff83bf254aeb75`  
		Last Modified: Thu, 11 Jun 2026 00:37:15 GMT  
		Size: 15.0 KB (14982 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6.4` - linux; arm variant v5

```console
$ docker pull spiped@sha256:3a77fd17bf87542b39acd5c371cb4509f911aba18087b5841340cdae79eb07e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.8 MB (33750953 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9f871c59019572295a1c6f16175304e8c052d7ae1bde8550e6316bd337fc36b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 01:20:06 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Thu, 11 Jun 2026 01:20:11 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 01:20:37 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Thu, 11 Jun 2026 01:20:37 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Thu, 11 Jun 2026 01:20:37 GMT
VOLUME [/spiped]
# Thu, 11 Jun 2026 01:20:37 GMT
WORKDIR /spiped
# Thu, 11 Jun 2026 01:20:38 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Thu, 11 Jun 2026 01:20:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 11 Jun 2026 01:20:38 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:ed883f3fd95b7edef302d7ca9520eefdae280af081509bd7e9e5b5ff8f4cda7c`  
		Last Modified: Wed, 10 Jun 2026 23:41:17 GMT  
		Size: 28.0 MB (27959200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e751f68dcb09ba1579bee55a24286186b59e393de92bac08ff724b4981d5d170`  
		Last Modified: Thu, 11 Jun 2026 01:20:44 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d89df5ca97fe521123a4a7aae01c94c4479bf368a9d8c696eee17064fc312bc1`  
		Last Modified: Thu, 11 Jun 2026 01:20:45 GMT  
		Size: 831.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91d2c4ac84d26c20df4907085b90aeb331861a219b69716c57682ae2cb946eb8`  
		Last Modified: Thu, 11 Jun 2026 01:20:45 GMT  
		Size: 5.8 MB (5789383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2073b26a67b2b25b8dae9d6d7a2028b43f95697825a4cb34a083684f542d8fe`  
		Last Modified: Thu, 11 Jun 2026 01:20:45 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1e64de9d592c6c09b59082de73dbb84f8e63a26763394e8083e1dd58f66d693`  
		Last Modified: Thu, 11 Jun 2026 01:20:46 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6.4` - unknown; unknown

```console
$ docker pull spiped@sha256:e786ed555ddf93e97965e805339e0e57e642ee1b6992efb0a38706feed7d6111
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3634384 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:678d30be6a2af3135f4751e15d6b35b82e2cd1dbc9a6858fa252aa22ea5487f6`

```dockerfile
```

-	Layers:
	-	`sha256:f416dd4fb0aef1763e3288e5f7435905aa2cacf86c5d53d1ff62343b3aee11b4`  
		Last Modified: Thu, 11 Jun 2026 01:20:45 GMT  
		Size: 3.6 MB (3619296 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6a02acc670c38ba874d76cb8784856b12a90aa7e49311ee73beff9aa2761b4c8`  
		Last Modified: Thu, 11 Jun 2026 01:20:45 GMT  
		Size: 15.1 KB (15088 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6.4` - linux; arm variant v7

```console
$ docker pull spiped@sha256:079fbf73e349c36cc2b4d55e664f1d5a60b482fa43a1021f0ea8cb3e38b490fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.8 MB (31798135 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:959018a10d28c5d1dde8c33184f543a1293c46376550688e906dbae7ddf55228`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 01:21:52 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Thu, 11 Jun 2026 01:21:55 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 01:22:18 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Thu, 11 Jun 2026 01:22:18 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Thu, 11 Jun 2026 01:22:18 GMT
VOLUME [/spiped]
# Thu, 11 Jun 2026 01:22:18 GMT
WORKDIR /spiped
# Thu, 11 Jun 2026 01:22:18 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Thu, 11 Jun 2026 01:22:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 11 Jun 2026 01:22:18 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:4bd6ddea06d5009ee47ddb0f254a2569aff0230c005869ebd416b20295d945c0`  
		Last Modified: Wed, 10 Jun 2026 23:42:34 GMT  
		Size: 26.2 MB (26211004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51bb869011c6d164e974fe820179933094dcc281df7a55480fc4077277232c77`  
		Last Modified: Thu, 11 Jun 2026 01:22:25 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:422e823bc0c6498856622e79affa11c1598652143bfa7f350dc04a8bae10a58a`  
		Last Modified: Thu, 11 Jun 2026 01:22:25 GMT  
		Size: 827.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fadeadb89fb7f698439cd322f47ba897a03fd1551ffe3fcf76d75f5383cd472`  
		Last Modified: Thu, 11 Jun 2026 01:22:25 GMT  
		Size: 5.6 MB (5584763 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3817b48e6549ab977fe0f1bbbb517045c499e8b6a3c28271dc05398321fe485d`  
		Last Modified: Thu, 11 Jun 2026 01:22:25 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a52c3658e003288d1598c728ef7ab0c5167ce43d1e20bf855db1dde18f30b339`  
		Last Modified: Thu, 11 Jun 2026 01:22:27 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6.4` - unknown; unknown

```console
$ docker pull spiped@sha256:4660d6bee86fba733a44735e9cea0b5dfa13410ac081e02edbed22229736f4ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3633504 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f7dd6ebfec69dc7720608ae6a9b0c5af682ff982f3ce0440ed4f3bf904f4c5f`

```dockerfile
```

-	Layers:
	-	`sha256:d25034d6fee06e5ff09bdc9004cbe4b4a4e9d9ed95b0624f5000cb9e580a086e`  
		Last Modified: Thu, 11 Jun 2026 01:22:25 GMT  
		Size: 3.6 MB (3618417 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:deb1d9d6f39ee38fed21b5f4de28c58d8058b0810a5cd7893d92d295084642d1`  
		Last Modified: Thu, 11 Jun 2026 01:22:25 GMT  
		Size: 15.1 KB (15087 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6.4` - linux; arm64 variant v8

```console
$ docker pull spiped@sha256:b666025eb8bf9bd288d28306188f384cf5e1cf793252a3092ed8467ea174a7c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.4 MB (36384823 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2b7f7df51ecb422ed1c09aa176c982afa86a96f6e553daf85ffd468ca5f3846`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 00:38:14 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Thu, 11 Jun 2026 00:38:16 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:38:39 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Thu, 11 Jun 2026 00:38:39 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Thu, 11 Jun 2026 00:38:39 GMT
VOLUME [/spiped]
# Thu, 11 Jun 2026 00:38:39 GMT
WORKDIR /spiped
# Thu, 11 Jun 2026 00:38:39 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Thu, 11 Jun 2026 00:38:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 11 Jun 2026 00:38:39 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:a25cd16f2d8653f652f8292b34b21bfbabdc85d6b39861a24b85f0896df1a95e`  
		Last Modified: Wed, 10 Jun 2026 23:40:16 GMT  
		Size: 30.1 MB (30148530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af99214715c4dd89b01b22d803c733a8cdeff8b516b64dcbc4039e3bb73edf81`  
		Last Modified: Thu, 11 Jun 2026 00:38:46 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cb7f2ca44a46746d13284bd66cb8d509327101aa851a60e2f4562b4c0b43fe4`  
		Last Modified: Thu, 11 Jun 2026 00:38:46 GMT  
		Size: 828.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fc568496a63b54431809869a1a353a056bd0286efc252ed16943213148d8e78`  
		Last Modified: Thu, 11 Jun 2026 00:38:46 GMT  
		Size: 6.2 MB (6233926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62455682699c33f1af511f11805177432eb0df675093f3a55be46e8069d099ad`  
		Last Modified: Thu, 11 Jun 2026 00:38:46 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1337cf4ae97e82beefcd0736801f263b58faa5acea8bbd02b6fb1610b3c08a69`  
		Last Modified: Thu, 11 Jun 2026 00:38:47 GMT  
		Size: 336.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6.4` - unknown; unknown

```console
$ docker pull spiped@sha256:28fd7f18765bc97e01aed948eb208846037e2fdc5be5b01c7b60a1dab0ecc29d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3636446 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:caaed5bb2a83f15f132837c8042bc95288ce03bd799f9d4a49b960975af17bea`

```dockerfile
```

-	Layers:
	-	`sha256:f4119ebc6f5a2232c489599390a07000eb50a2325250846032e65737506b59fb`  
		Last Modified: Thu, 11 Jun 2026 00:38:46 GMT  
		Size: 3.6 MB (3621330 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ff1ae5a7dd30d786394e331ae8fd4a26444a7fab07e0f0f35bd0d9f9e8aa11f4`  
		Last Modified: Thu, 11 Jun 2026 00:38:46 GMT  
		Size: 15.1 KB (15116 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6.4` - linux; 386

```console
$ docker pull spiped@sha256:02f4ba23c22e1271ac47e549272f9bb9b73d515c584ef6657b10b34089186119
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.7 MB (37746372 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c77be7a202c7361655d5298662fbd58b4ac13a280d8eea6d0e5696277b5d6dc2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 00:44:31 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Thu, 11 Jun 2026 00:44:34 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:45:03 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Thu, 11 Jun 2026 00:45:03 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Thu, 11 Jun 2026 00:45:03 GMT
VOLUME [/spiped]
# Thu, 11 Jun 2026 00:45:03 GMT
WORKDIR /spiped
# Thu, 11 Jun 2026 00:45:03 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Thu, 11 Jun 2026 00:45:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 11 Jun 2026 00:45:03 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:720f951a68f4f9ab464e52b53cf88cfb86bc876b3f00956d000420777ab93c0c`  
		Last Modified: Wed, 10 Jun 2026 23:40:30 GMT  
		Size: 31.3 MB (31301194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96b36e957fa28b38d49b885ce8ff4366a6bfcb98bf38aa1dd3dd51c9b7cd333c`  
		Last Modified: Thu, 11 Jun 2026 00:45:10 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3aae632d05299c9dee2bec97ea596046cf5c7c15eff6529e97937627b28994fa`  
		Last Modified: Thu, 11 Jun 2026 00:45:10 GMT  
		Size: 828.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd7f7718fe56cea19c8269279c48994d7ae792b5209abc4faef63781a55560f4`  
		Last Modified: Thu, 11 Jun 2026 00:45:11 GMT  
		Size: 6.4 MB (6442811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96e529f830d838d84290e5326067c74dc889693a3954cd9a7dbd43c0b583c23f`  
		Last Modified: Thu, 11 Jun 2026 00:45:10 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fe774eab45468f5459c9ea3e437c826c9c3d130cbc49f077eef0338b91a9edd`  
		Last Modified: Thu, 11 Jun 2026 00:45:12 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6.4` - unknown; unknown

```console
$ docker pull spiped@sha256:43aeb04090782a915b6e9289e6133f1f0327b7465670b94e07f481b847c4025b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3635377 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd02b428a54369d078699f646a6c58bb59205a7d8e90fd308ef1b652598d64f9`

```dockerfile
```

-	Layers:
	-	`sha256:20700448f422d0e1e5f84b34dcae83618e79e0454a188609c16921611a98ff5a`  
		Last Modified: Thu, 11 Jun 2026 00:45:10 GMT  
		Size: 3.6 MB (3620431 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b8c3c92718b75b733828274ef1f0c3ac60a2665e98431b090587ac61fa798684`  
		Last Modified: Thu, 11 Jun 2026 00:45:10 GMT  
		Size: 14.9 KB (14946 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6.4` - linux; ppc64le

```console
$ docker pull spiped@sha256:77a28ff7796938b2e628dcb8466cba0a9b9e9209373514b53eb9500a4eb54179
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.4 MB (40449493 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5c663351cf736af7041bf6dab200f7240abda1f91a38cc9154e15ecc605051b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 04:42:39 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Thu, 11 Jun 2026 04:42:43 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 04:43:31 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Thu, 11 Jun 2026 04:43:31 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Thu, 11 Jun 2026 04:43:31 GMT
VOLUME [/spiped]
# Thu, 11 Jun 2026 04:43:31 GMT
WORKDIR /spiped
# Thu, 11 Jun 2026 04:43:31 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Thu, 11 Jun 2026 04:43:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 11 Jun 2026 04:43:31 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:9d6b2e320e2b74843186d830e8202c50ebfaeccf823d239e3e3e349a8a508d80`  
		Last Modified: Thu, 11 Jun 2026 00:24:42 GMT  
		Size: 33.6 MB (33606340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae397a9bd78994d17d78508ffe6c90b95321c279f11d71546a6690cf7b3bfa56`  
		Last Modified: Thu, 11 Jun 2026 04:43:44 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:527c0346e0be1cff6e959785d2ead56a024d388a5f5b49668bb10ef02df87e5b`  
		Last Modified: Thu, 11 Jun 2026 04:43:44 GMT  
		Size: 825.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfb798ab52e9baacaca51304c7ae7bd07e22ffa204c22fa1ee3f600faa9d384c`  
		Last Modified: Thu, 11 Jun 2026 04:43:45 GMT  
		Size: 6.8 MB (6840786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9e2eda05f5b8c55e69e0f5f7b8411ef18adfa257a0964e74893e13aa8460231`  
		Last Modified: Thu, 11 Jun 2026 04:43:44 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89c91b4a125ec65053187500a3042ba5cf4b3d3c3757a5130a5b6a469502146e`  
		Last Modified: Thu, 11 Jun 2026 04:43:45 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6.4` - unknown; unknown

```console
$ docker pull spiped@sha256:cde6ed1dd2ca8f029ced3770c7fd29bfed2a5e054b7f88c1c2828ea61ae0d53a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3637067 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f348c1d24e29a4dd183acde8c7db1a7186ed71bf6cc2b0deb230af07b7e3608`

```dockerfile
```

-	Layers:
	-	`sha256:9028cc214c0ddc113b07afbc6b1c7d125225085781875688e233501b5e4f6973`  
		Last Modified: Thu, 11 Jun 2026 04:43:45 GMT  
		Size: 3.6 MB (3622039 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:23b0df7ce9f0c385bfc283502819fb193952bc81b97402aae117279766c4435f`  
		Last Modified: Thu, 11 Jun 2026 04:43:44 GMT  
		Size: 15.0 KB (15028 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6.4` - linux; riscv64

```console
$ docker pull spiped@sha256:d1196bf05f6d34c1b33d0f44d558a64dacbac606da8ede3854f0f56b7da88dd7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.6 MB (37640838 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:257f964733ff5e0fb249561928b63d968d0ea7e0f22a1650497b8f634a78b7b1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1781049600'
# Sat, 13 Jun 2026 02:38:34 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Sat, 13 Jun 2026 02:39:05 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 13 Jun 2026 02:42:10 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Sat, 13 Jun 2026 02:42:10 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Sat, 13 Jun 2026 02:42:10 GMT
VOLUME [/spiped]
# Sat, 13 Jun 2026 02:42:10 GMT
WORKDIR /spiped
# Sat, 13 Jun 2026 02:42:10 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sat, 13 Jun 2026 02:42:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 13 Jun 2026 02:42:10 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:0b510fe8545cab831b696965b5a825649c5c945581e912d31a08a0b30ff940c0`  
		Last Modified: Thu, 11 Jun 2026 03:01:06 GMT  
		Size: 28.3 MB (28282305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f639c6130c8aca0f837b171cb0a0d45c790c5d7bf9518eff2b8ff95b48f104c`  
		Last Modified: Sat, 13 Jun 2026 02:43:23 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07e14a8d467e3dc32c3ec2a585b788255e6272eeaa9763d004943122f7248c27`  
		Last Modified: Sat, 13 Jun 2026 02:43:23 GMT  
		Size: 822.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d41b9627a0c3fc9b82eb3a3347a368ac72d11d19f3ff135e81910be58f7ced5`  
		Last Modified: Sat, 13 Jun 2026 02:43:24 GMT  
		Size: 9.4 MB (9356169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4946ccd28be72a02f3c71907db8b182219a80ff46301e8a09fdd946d52683dd8`  
		Last Modified: Sat, 13 Jun 2026 02:43:23 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f74e027caa4d5bd042803e1c5847e795634af08a895bf7099c444bcdf51c4cc`  
		Last Modified: Sat, 13 Jun 2026 02:43:24 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6.4` - unknown; unknown

```console
$ docker pull spiped@sha256:bd59a45c25ec7d4b80d63933dffd3bd86372d97041734ebbf62964d8a991e093
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3628474 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0ed4a489648532fba6cde1d7e88a809bdb98383c98aee19aaba7a5a947fbd77`

```dockerfile
```

-	Layers:
	-	`sha256:d44a97abcbeafd6a6ec2dd69c997db68246839a5985937d49f3c1d5fbc99a495`  
		Last Modified: Sat, 13 Jun 2026 02:43:24 GMT  
		Size: 3.6 MB (3613445 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:de64e5286a1b72fafa9b68c701bf6ba016f164bdfaf60538499d95770fbf3f6a`  
		Last Modified: Sat, 13 Jun 2026 02:43:23 GMT  
		Size: 15.0 KB (15029 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6.4` - linux; s390x

```console
$ docker pull spiped@sha256:bd22ee71a9e9236e2ca69180ad51c06cf6d8e35afbd4add081b0d2f764edc08e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.0 MB (35975833 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1ad1052f1364f10f7a17a6666de217cbde8ab8c0e0ac3499018c5cd72b4ee17`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 01:43:42 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Thu, 11 Jun 2026 01:43:44 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 01:44:01 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Thu, 11 Jun 2026 01:44:01 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Thu, 11 Jun 2026 01:44:01 GMT
VOLUME [/spiped]
# Thu, 11 Jun 2026 01:44:01 GMT
WORKDIR /spiped
# Thu, 11 Jun 2026 01:44:01 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Thu, 11 Jun 2026 01:44:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 11 Jun 2026 01:44:01 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:760dcf74fdfe93300ce15b5b23adf9aa4af45b6ba9d69925863198f64881a537`  
		Last Modified: Wed, 10 Jun 2026 23:42:35 GMT  
		Size: 29.9 MB (29851354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbee78aca287a132f4560c3c136874e9fd2eb76d548257a9d3a3df8c901bcc4f`  
		Last Modified: Thu, 11 Jun 2026 01:44:13 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:592a34f021f7dfd15ace5226ae509b1158c586b704884d60433770343a082992`  
		Last Modified: Thu, 11 Jun 2026 01:44:13 GMT  
		Size: 828.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb3568250ea65438eb60733aee26c97620a46d0a35f1724cad1b6cdf7fbcc023`  
		Last Modified: Thu, 11 Jun 2026 01:44:13 GMT  
		Size: 6.1 MB (6122111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b205eccacc5cb65c52b6fa4618ba96b957fd2f8a2f5423e2653cc1b280d2f23`  
		Last Modified: Thu, 11 Jun 2026 01:44:13 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02c73a6752a874142787522de11c367cd55d46e4661d6e3216d3509660bc3091`  
		Last Modified: Thu, 11 Jun 2026 01:44:14 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6.4` - unknown; unknown

```console
$ docker pull spiped@sha256:b9ccb006c7597035afc395814bcd5e176f1c6747e8cdcbb2e2e99a609798685c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3633647 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0955f426902eecb0ba4cee729a5abb10364e89f0579f841377a2401fdd89f43`

```dockerfile
```

-	Layers:
	-	`sha256:bc258d4741b882519b7d7392f726369c450df7d38b8a5f5b761096da236e6d1a`  
		Last Modified: Thu, 11 Jun 2026 01:44:13 GMT  
		Size: 3.6 MB (3618665 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9e8ebd7ccddfecb937db9fd26d8850a9b8222af37b614601c7b7e2d424a147fa`  
		Last Modified: Thu, 11 Jun 2026 01:44:13 GMT  
		Size: 15.0 KB (14982 bytes)  
		MIME: application/vnd.in-toto+json

## `spiped:1.6.4-alpine`

```console
$ docker pull spiped@sha256:d321da057edcf67209e6a50fce596020211d058f66861249f42c546d7d818fe4
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
$ docker pull spiped@sha256:ddacdd500302ed8e0b56cfbe5eba1b03890a3a11103e2e79f118f78819546c96
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3904546 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0e50065de302c7f6a370e6ce4b691cc04feab696fd0ca4c59d5c21b96d09a5f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Mon, 22 Jun 2026 19:20:21 GMT
ADD alpine-minirootfs-3.22.5-x86_64.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:20:21 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 19:52:57 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Mon, 22 Jun 2026 19:52:58 GMT
RUN apk add --no-cache libssl3 # buildkit
# Mon, 22 Jun 2026 19:53:07 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Mon, 22 Jun 2026 19:53:07 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Mon, 22 Jun 2026 19:53:07 GMT
VOLUME [/spiped]
# Mon, 22 Jun 2026 19:53:07 GMT
WORKDIR /spiped
# Mon, 22 Jun 2026 19:53:07 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Mon, 22 Jun 2026 19:53:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 22 Jun 2026 19:53:07 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:f7ee36c9aa34bbb665f975c76e5c0d1607f0674b94c84cfb0061f87006ea5d10`  
		Last Modified: Mon, 22 Jun 2026 09:11:44 GMT  
		Size: 3.8 MB (3787595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e11e0fcbf833efd71ccdc39dad69485c2ab9e33be6a7075e11f23dfc938ee0b`  
		Last Modified: Mon, 22 Jun 2026 19:53:11 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d3df5ddcf63216635d6ac9800edfcdf71dbf67c7328ec84d1b3ab49da64adf0`  
		Last Modified: Mon, 22 Jun 2026 19:53:11 GMT  
		Size: 7.9 KB (7939 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68bf1a439bfe49642cefb4e5461e95befb5f5a9b5cced180eaf651935a1246f9`  
		Last Modified: Mon, 22 Jun 2026 19:53:11 GMT  
		Size: 107.6 KB (107630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f2716e286de0031c590e0551ee0bcfbe0740fde1029874d538fecad89dadaca`  
		Last Modified: Mon, 22 Jun 2026 19:53:12 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe62eb4d32c49f1f3ab36f4fa4341f61fe5f3eccfbb08576ec70be11772704af`  
		Last Modified: Mon, 22 Jun 2026 19:53:13 GMT  
		Size: 336.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6.4-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:9cd92d324e4bfd0a2ea1f55c9daaf43dd5a3704affe05d59359da761a3ea9a57
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.5 KB (96455 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d70e5224458648b69c985eed8348a59c952ae7671493ce0b9764ad70c0812c47`

```dockerfile
```

-	Layers:
	-	`sha256:b0302e3cc8209d3dfd914c793e581ee84da322d428e5b5ccf19df7d08480f8f7`  
		Last Modified: Mon, 22 Jun 2026 19:53:12 GMT  
		Size: 82.2 KB (82197 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dd339b140e490f5380bd78b29356f7f2ac4429526ab1280b93588123237521bf`  
		Last Modified: Mon, 22 Jun 2026 19:53:11 GMT  
		Size: 14.3 KB (14258 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6.4-alpine` - linux; arm variant v6

```console
$ docker pull spiped@sha256:797576782eff7b771cd16a7c70d7d3aa681429bfc3a96e3d9caf80de53e1d13c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3593263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f8d26831f4f0d4c40c83254a01dab731517f05ccd3e8233eba9e650a658977b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Mon, 22 Jun 2026 19:19:53 GMT
ADD alpine-minirootfs-3.22.5-armhf.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:19:53 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 19:53:51 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Mon, 22 Jun 2026 19:53:52 GMT
RUN apk add --no-cache libssl3 # buildkit
# Mon, 22 Jun 2026 19:54:02 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Mon, 22 Jun 2026 19:54:02 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Mon, 22 Jun 2026 19:54:02 GMT
VOLUME [/spiped]
# Mon, 22 Jun 2026 19:54:02 GMT
WORKDIR /spiped
# Mon, 22 Jun 2026 19:54:02 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Mon, 22 Jun 2026 19:54:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 22 Jun 2026 19:54:02 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:8efcda622ba07f4da6b9309a34f4650a7a052a1d29a2fc346284c2c1b0899202`  
		Last Modified: Mon, 22 Jun 2026 19:19:58 GMT  
		Size: 3.5 MB (3494800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3032dd20d72fa4a27591cfc40f8eec5d055f3f37cc9eb06329f5cf0e83e19248`  
		Last Modified: Mon, 22 Jun 2026 19:54:06 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58b413eab28f41a1f71ea4831c00e243457d2f484d8b30471a585c9b791580a4`  
		Last Modified: Mon, 22 Jun 2026 19:54:06 GMT  
		Size: 7.9 KB (7935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21ddd27b334e342120f96e4a55937070fef9371ea62ef8a2ee2675febdbac2b8`  
		Last Modified: Mon, 22 Jun 2026 19:54:06 GMT  
		Size: 89.1 KB (89146 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35522b2f0660a559efa25d5c51d7550bf5f21e1df140bd02686304e0d54a6686`  
		Last Modified: Mon, 22 Jun 2026 19:54:06 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70feae8af381e1a5e4dd52b1857289c5766c1fff41f5d377dbde68b6ac8eb2d5`  
		Last Modified: Mon, 22 Jun 2026 19:54:07 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6.4-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:ab1ba7ca7bcdc700ff165912b9b972504e3ae861646327b59b12551cc63bfff8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.1 KB (14147 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ae2dc57358030a5ccab2ec7826df8c7578005f688b14a6f0440f1e345896ea1`

```dockerfile
```

-	Layers:
	-	`sha256:653d549a72bdd578904772adf12dac81809cf8fb791235e047142cc62a095fe5`  
		Last Modified: Mon, 22 Jun 2026 19:54:06 GMT  
		Size: 14.1 KB (14147 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6.4-alpine` - linux; arm variant v7

```console
$ docker pull spiped@sha256:0a4bc8b8eb635c2de45437d249d8467c9a1d4bfa67588b7c2b7c356a09950769
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3300611 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9bdc9d57160696d38e8f96024ccba6e14e8a961af83fec3bc71547d3c2ac3477`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Mon, 22 Jun 2026 19:20:47 GMT
ADD alpine-minirootfs-3.22.5-armv7.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:20:47 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 20:07:29 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Mon, 22 Jun 2026 20:07:30 GMT
RUN apk add --no-cache libssl3 # buildkit
# Mon, 22 Jun 2026 20:07:39 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Mon, 22 Jun 2026 20:07:39 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Mon, 22 Jun 2026 20:07:39 GMT
VOLUME [/spiped]
# Mon, 22 Jun 2026 20:07:40 GMT
WORKDIR /spiped
# Mon, 22 Jun 2026 20:07:40 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Mon, 22 Jun 2026 20:07:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 22 Jun 2026 20:07:40 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:276ca41f8e7974c0de50f2551aabece03d11f231f68ab5c6c5051410e0d8c2e7`  
		Last Modified: Mon, 22 Jun 2026 12:03:28 GMT  
		Size: 3.2 MB (3209612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5d412bd01e6b05daa916f63dc49f85e1bc0e28908a915ab5433ee4f773b6d99`  
		Last Modified: Mon, 22 Jun 2026 20:07:45 GMT  
		Size: 948.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f4ca329ff828ab9881adaf1200feef78590b5cf682e928e28811a80fc9ca00c`  
		Last Modified: Mon, 22 Jun 2026 20:07:45 GMT  
		Size: 7.9 KB (7942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68bdfa617d32bd950a899f3c37fc1051103abe4c515575fd0c7a470311e7b1ce`  
		Last Modified: Mon, 22 Jun 2026 20:07:45 GMT  
		Size: 81.7 KB (81676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fb812de9569e6ea964dc192f484efa8f8b40f959ca1aa1cd28efb07d516b3b9`  
		Last Modified: Mon, 22 Jun 2026 20:07:45 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2f94d3b42c6fde945cb292d2ce19b88b4443336f40fd734cfd412ab84954e46`  
		Last Modified: Mon, 22 Jun 2026 20:07:46 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6.4-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:a5f2de2594b64ce8777794fecdc26dffd6889de81c77f5c600f9de67ac2808f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.6 KB (96595 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6bfc8e0afd039f2387a8475a01f7c55cbb7d95c208d3d65e460898634384300`

```dockerfile
```

-	Layers:
	-	`sha256:c1b261c11b2c6ba30671daf53c170874acef4bb4b844d659bf83d547ab4c5775`  
		Last Modified: Mon, 22 Jun 2026 20:07:45 GMT  
		Size: 82.2 KB (82233 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2429075ab54969202e940d2018a2e0c6eed6ef226d06edb7ace72b19cc19023a`  
		Last Modified: Mon, 22 Jun 2026 20:07:44 GMT  
		Size: 14.4 KB (14362 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6.4-alpine` - linux; arm64 variant v8

```console
$ docker pull spiped@sha256:4756e80b073870da1063f3705ae4982190aab4ed9e17ddc85106f245d2ed7949
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4230427 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82eb3d5165ba6084a012344ffcdb5bf8cb8999837174113d002240db059e9432`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Mon, 22 Jun 2026 19:20:11 GMT
ADD alpine-minirootfs-3.22.5-aarch64.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:20:11 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 19:54:08 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Mon, 22 Jun 2026 19:54:09 GMT
RUN apk add --no-cache libssl3 # buildkit
# Mon, 22 Jun 2026 19:54:19 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Mon, 22 Jun 2026 19:54:19 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Mon, 22 Jun 2026 19:54:19 GMT
VOLUME [/spiped]
# Mon, 22 Jun 2026 19:54:19 GMT
WORKDIR /spiped
# Mon, 22 Jun 2026 19:54:19 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Mon, 22 Jun 2026 19:54:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 22 Jun 2026 19:54:19 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:738128faa30f570583b0e57efd831e0e6a2a9aacf1be88c8f4c1ef8a5b7033cc`  
		Last Modified: Mon, 22 Jun 2026 09:11:35 GMT  
		Size: 4.1 MB (4120486 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f19dec4b471d7fccd4a70ac0b2f8e3fe4c7aad315844c4b6ea4cc1f27a9e75b`  
		Last Modified: Mon, 22 Jun 2026 19:54:24 GMT  
		Size: 949.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9e119200034afb1c7ec26c08862296c1ebb06ad0e089656c82a87b0cc2ce3d5`  
		Last Modified: Mon, 22 Jun 2026 19:54:24 GMT  
		Size: 7.9 KB (7949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79ed72e155ad35b783a3b2fd26113062c65385d060c1107fd7be78775b11f5df`  
		Last Modified: Mon, 22 Jun 2026 19:54:24 GMT  
		Size: 100.6 KB (100613 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:012dc19e314abeb9a680712049f471d7b225578b746a84c90ddf45f42863b3f3`  
		Last Modified: Mon, 22 Jun 2026 19:54:24 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e2921724d5472f855da9782445382b4df2dbc3fea41b0771456c4bd179c3ac9`  
		Last Modified: Mon, 22 Jun 2026 19:54:25 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6.4-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:309e398654c9ffb57cf24a14fea4bf0c2931193c153dd095abeba42196ed37a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.6 KB (96646 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9077526648e3aefcc0edbf377ed5794fd580e0064ae615bf7362ce85c3273ad3`

```dockerfile
```

-	Layers:
	-	`sha256:e905129a42e7e89130d80f327d3c87b9cdafa58974899da48f451b550c597127`  
		Last Modified: Mon, 22 Jun 2026 19:54:24 GMT  
		Size: 82.3 KB (82253 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f134d75f49539af75c4f9aa3c0a55672a33a54cf8bf103699ca234354693077c`  
		Last Modified: Mon, 22 Jun 2026 19:54:24 GMT  
		Size: 14.4 KB (14393 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6.4-alpine` - linux; 386

```console
$ docker pull spiped@sha256:6f3becd5ab17860d0d79cdad5a8314f9f41ade80934bec3e845f2be0549f7399
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3735070 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7c2c4aea7b344dfb6e18f2e0fca5adbbeb691624d97cccfc1e5787f7112f1c1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Mon, 22 Jun 2026 19:20:21 GMT
ADD alpine-minirootfs-3.22.5-x86.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:20:21 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 19:52:33 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Mon, 22 Jun 2026 19:52:34 GMT
RUN apk add --no-cache libssl3 # buildkit
# Mon, 22 Jun 2026 19:52:45 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Mon, 22 Jun 2026 19:52:45 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Mon, 22 Jun 2026 19:52:45 GMT
VOLUME [/spiped]
# Mon, 22 Jun 2026 19:52:45 GMT
WORKDIR /spiped
# Mon, 22 Jun 2026 19:52:45 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Mon, 22 Jun 2026 19:52:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 22 Jun 2026 19:52:45 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:a4b74ab0c43260cc6600b37d5a1ed742d904bba03625caa74b18e45744cde3d1`  
		Last Modified: Mon, 22 Jun 2026 12:03:14 GMT  
		Size: 3.6 MB (3605660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:370212c6233698cf3a2cededd4bd44f00eac7c5e03af3c80a0a1d46c8a4ffdf3`  
		Last Modified: Mon, 22 Jun 2026 19:52:49 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9589ee7d567bbc2c8b0bdd8091e2600f7493e43c86c9291e8e0c5cb80c56fd63`  
		Last Modified: Mon, 22 Jun 2026 19:52:49 GMT  
		Size: 7.9 KB (7935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40a2e946a568955b4fc26e807e13538dfc53fdf5c40195b033d6738d5eb47988`  
		Last Modified: Mon, 22 Jun 2026 19:52:49 GMT  
		Size: 120.1 KB (120096 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5c4c53f53316aa33359a13371beb39c12857d53615d08c755157fbd69bb338d`  
		Last Modified: Mon, 22 Jun 2026 19:52:49 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca3585934873b3572c65ed05b1212ac1144f16b9ef8468d66230cedacf8c04ab`  
		Last Modified: Mon, 22 Jun 2026 19:52:51 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6.4-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:069fb82d31cd63808dd6a7d5c56b36a98d126a4f8d452cff42e101a369d62c21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.4 KB (96395 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a99309a2ee767f77be492110796b79f8f183f4a91c5e150ce93856bfc9eb541a`

```dockerfile
```

-	Layers:
	-	`sha256:f85f07db752d4a828f227d726b92f676379255ba60f6efa8fb1a91b8cb20e575`  
		Last Modified: Mon, 22 Jun 2026 19:52:49 GMT  
		Size: 82.2 KB (82172 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6ee94877067613386073525f14205ddff5c1f158f239bc7509f064e7c73ecc48`  
		Last Modified: Mon, 22 Jun 2026 19:52:49 GMT  
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
$ docker pull spiped@sha256:d321da057edcf67209e6a50fce596020211d058f66861249f42c546d7d818fe4
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
$ docker pull spiped@sha256:ddacdd500302ed8e0b56cfbe5eba1b03890a3a11103e2e79f118f78819546c96
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3904546 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0e50065de302c7f6a370e6ce4b691cc04feab696fd0ca4c59d5c21b96d09a5f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Mon, 22 Jun 2026 19:20:21 GMT
ADD alpine-minirootfs-3.22.5-x86_64.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:20:21 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 19:52:57 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Mon, 22 Jun 2026 19:52:58 GMT
RUN apk add --no-cache libssl3 # buildkit
# Mon, 22 Jun 2026 19:53:07 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Mon, 22 Jun 2026 19:53:07 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Mon, 22 Jun 2026 19:53:07 GMT
VOLUME [/spiped]
# Mon, 22 Jun 2026 19:53:07 GMT
WORKDIR /spiped
# Mon, 22 Jun 2026 19:53:07 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Mon, 22 Jun 2026 19:53:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 22 Jun 2026 19:53:07 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:f7ee36c9aa34bbb665f975c76e5c0d1607f0674b94c84cfb0061f87006ea5d10`  
		Last Modified: Mon, 22 Jun 2026 09:11:44 GMT  
		Size: 3.8 MB (3787595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e11e0fcbf833efd71ccdc39dad69485c2ab9e33be6a7075e11f23dfc938ee0b`  
		Last Modified: Mon, 22 Jun 2026 19:53:11 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d3df5ddcf63216635d6ac9800edfcdf71dbf67c7328ec84d1b3ab49da64adf0`  
		Last Modified: Mon, 22 Jun 2026 19:53:11 GMT  
		Size: 7.9 KB (7939 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68bf1a439bfe49642cefb4e5461e95befb5f5a9b5cced180eaf651935a1246f9`  
		Last Modified: Mon, 22 Jun 2026 19:53:11 GMT  
		Size: 107.6 KB (107630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f2716e286de0031c590e0551ee0bcfbe0740fde1029874d538fecad89dadaca`  
		Last Modified: Mon, 22 Jun 2026 19:53:12 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe62eb4d32c49f1f3ab36f4fa4341f61fe5f3eccfbb08576ec70be11772704af`  
		Last Modified: Mon, 22 Jun 2026 19:53:13 GMT  
		Size: 336.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:9cd92d324e4bfd0a2ea1f55c9daaf43dd5a3704affe05d59359da761a3ea9a57
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.5 KB (96455 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d70e5224458648b69c985eed8348a59c952ae7671493ce0b9764ad70c0812c47`

```dockerfile
```

-	Layers:
	-	`sha256:b0302e3cc8209d3dfd914c793e581ee84da322d428e5b5ccf19df7d08480f8f7`  
		Last Modified: Mon, 22 Jun 2026 19:53:12 GMT  
		Size: 82.2 KB (82197 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dd339b140e490f5380bd78b29356f7f2ac4429526ab1280b93588123237521bf`  
		Last Modified: Mon, 22 Jun 2026 19:53:11 GMT  
		Size: 14.3 KB (14258 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:alpine` - linux; arm variant v6

```console
$ docker pull spiped@sha256:797576782eff7b771cd16a7c70d7d3aa681429bfc3a96e3d9caf80de53e1d13c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3593263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f8d26831f4f0d4c40c83254a01dab731517f05ccd3e8233eba9e650a658977b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Mon, 22 Jun 2026 19:19:53 GMT
ADD alpine-minirootfs-3.22.5-armhf.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:19:53 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 19:53:51 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Mon, 22 Jun 2026 19:53:52 GMT
RUN apk add --no-cache libssl3 # buildkit
# Mon, 22 Jun 2026 19:54:02 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Mon, 22 Jun 2026 19:54:02 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Mon, 22 Jun 2026 19:54:02 GMT
VOLUME [/spiped]
# Mon, 22 Jun 2026 19:54:02 GMT
WORKDIR /spiped
# Mon, 22 Jun 2026 19:54:02 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Mon, 22 Jun 2026 19:54:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 22 Jun 2026 19:54:02 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:8efcda622ba07f4da6b9309a34f4650a7a052a1d29a2fc346284c2c1b0899202`  
		Last Modified: Mon, 22 Jun 2026 19:19:58 GMT  
		Size: 3.5 MB (3494800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3032dd20d72fa4a27591cfc40f8eec5d055f3f37cc9eb06329f5cf0e83e19248`  
		Last Modified: Mon, 22 Jun 2026 19:54:06 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58b413eab28f41a1f71ea4831c00e243457d2f484d8b30471a585c9b791580a4`  
		Last Modified: Mon, 22 Jun 2026 19:54:06 GMT  
		Size: 7.9 KB (7935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21ddd27b334e342120f96e4a55937070fef9371ea62ef8a2ee2675febdbac2b8`  
		Last Modified: Mon, 22 Jun 2026 19:54:06 GMT  
		Size: 89.1 KB (89146 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35522b2f0660a559efa25d5c51d7550bf5f21e1df140bd02686304e0d54a6686`  
		Last Modified: Mon, 22 Jun 2026 19:54:06 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70feae8af381e1a5e4dd52b1857289c5766c1fff41f5d377dbde68b6ac8eb2d5`  
		Last Modified: Mon, 22 Jun 2026 19:54:07 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:ab1ba7ca7bcdc700ff165912b9b972504e3ae861646327b59b12551cc63bfff8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.1 KB (14147 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ae2dc57358030a5ccab2ec7826df8c7578005f688b14a6f0440f1e345896ea1`

```dockerfile
```

-	Layers:
	-	`sha256:653d549a72bdd578904772adf12dac81809cf8fb791235e047142cc62a095fe5`  
		Last Modified: Mon, 22 Jun 2026 19:54:06 GMT  
		Size: 14.1 KB (14147 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:alpine` - linux; arm variant v7

```console
$ docker pull spiped@sha256:0a4bc8b8eb635c2de45437d249d8467c9a1d4bfa67588b7c2b7c356a09950769
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3300611 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9bdc9d57160696d38e8f96024ccba6e14e8a961af83fec3bc71547d3c2ac3477`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Mon, 22 Jun 2026 19:20:47 GMT
ADD alpine-minirootfs-3.22.5-armv7.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:20:47 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 20:07:29 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Mon, 22 Jun 2026 20:07:30 GMT
RUN apk add --no-cache libssl3 # buildkit
# Mon, 22 Jun 2026 20:07:39 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Mon, 22 Jun 2026 20:07:39 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Mon, 22 Jun 2026 20:07:39 GMT
VOLUME [/spiped]
# Mon, 22 Jun 2026 20:07:40 GMT
WORKDIR /spiped
# Mon, 22 Jun 2026 20:07:40 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Mon, 22 Jun 2026 20:07:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 22 Jun 2026 20:07:40 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:276ca41f8e7974c0de50f2551aabece03d11f231f68ab5c6c5051410e0d8c2e7`  
		Last Modified: Mon, 22 Jun 2026 12:03:28 GMT  
		Size: 3.2 MB (3209612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5d412bd01e6b05daa916f63dc49f85e1bc0e28908a915ab5433ee4f773b6d99`  
		Last Modified: Mon, 22 Jun 2026 20:07:45 GMT  
		Size: 948.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f4ca329ff828ab9881adaf1200feef78590b5cf682e928e28811a80fc9ca00c`  
		Last Modified: Mon, 22 Jun 2026 20:07:45 GMT  
		Size: 7.9 KB (7942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68bdfa617d32bd950a899f3c37fc1051103abe4c515575fd0c7a470311e7b1ce`  
		Last Modified: Mon, 22 Jun 2026 20:07:45 GMT  
		Size: 81.7 KB (81676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fb812de9569e6ea964dc192f484efa8f8b40f959ca1aa1cd28efb07d516b3b9`  
		Last Modified: Mon, 22 Jun 2026 20:07:45 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2f94d3b42c6fde945cb292d2ce19b88b4443336f40fd734cfd412ab84954e46`  
		Last Modified: Mon, 22 Jun 2026 20:07:46 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:a5f2de2594b64ce8777794fecdc26dffd6889de81c77f5c600f9de67ac2808f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.6 KB (96595 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6bfc8e0afd039f2387a8475a01f7c55cbb7d95c208d3d65e460898634384300`

```dockerfile
```

-	Layers:
	-	`sha256:c1b261c11b2c6ba30671daf53c170874acef4bb4b844d659bf83d547ab4c5775`  
		Last Modified: Mon, 22 Jun 2026 20:07:45 GMT  
		Size: 82.2 KB (82233 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2429075ab54969202e940d2018a2e0c6eed6ef226d06edb7ace72b19cc19023a`  
		Last Modified: Mon, 22 Jun 2026 20:07:44 GMT  
		Size: 14.4 KB (14362 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:alpine` - linux; arm64 variant v8

```console
$ docker pull spiped@sha256:4756e80b073870da1063f3705ae4982190aab4ed9e17ddc85106f245d2ed7949
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4230427 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82eb3d5165ba6084a012344ffcdb5bf8cb8999837174113d002240db059e9432`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Mon, 22 Jun 2026 19:20:11 GMT
ADD alpine-minirootfs-3.22.5-aarch64.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:20:11 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 19:54:08 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Mon, 22 Jun 2026 19:54:09 GMT
RUN apk add --no-cache libssl3 # buildkit
# Mon, 22 Jun 2026 19:54:19 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Mon, 22 Jun 2026 19:54:19 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Mon, 22 Jun 2026 19:54:19 GMT
VOLUME [/spiped]
# Mon, 22 Jun 2026 19:54:19 GMT
WORKDIR /spiped
# Mon, 22 Jun 2026 19:54:19 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Mon, 22 Jun 2026 19:54:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 22 Jun 2026 19:54:19 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:738128faa30f570583b0e57efd831e0e6a2a9aacf1be88c8f4c1ef8a5b7033cc`  
		Last Modified: Mon, 22 Jun 2026 09:11:35 GMT  
		Size: 4.1 MB (4120486 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f19dec4b471d7fccd4a70ac0b2f8e3fe4c7aad315844c4b6ea4cc1f27a9e75b`  
		Last Modified: Mon, 22 Jun 2026 19:54:24 GMT  
		Size: 949.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9e119200034afb1c7ec26c08862296c1ebb06ad0e089656c82a87b0cc2ce3d5`  
		Last Modified: Mon, 22 Jun 2026 19:54:24 GMT  
		Size: 7.9 KB (7949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79ed72e155ad35b783a3b2fd26113062c65385d060c1107fd7be78775b11f5df`  
		Last Modified: Mon, 22 Jun 2026 19:54:24 GMT  
		Size: 100.6 KB (100613 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:012dc19e314abeb9a680712049f471d7b225578b746a84c90ddf45f42863b3f3`  
		Last Modified: Mon, 22 Jun 2026 19:54:24 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e2921724d5472f855da9782445382b4df2dbc3fea41b0771456c4bd179c3ac9`  
		Last Modified: Mon, 22 Jun 2026 19:54:25 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:309e398654c9ffb57cf24a14fea4bf0c2931193c153dd095abeba42196ed37a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.6 KB (96646 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9077526648e3aefcc0edbf377ed5794fd580e0064ae615bf7362ce85c3273ad3`

```dockerfile
```

-	Layers:
	-	`sha256:e905129a42e7e89130d80f327d3c87b9cdafa58974899da48f451b550c597127`  
		Last Modified: Mon, 22 Jun 2026 19:54:24 GMT  
		Size: 82.3 KB (82253 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f134d75f49539af75c4f9aa3c0a55672a33a54cf8bf103699ca234354693077c`  
		Last Modified: Mon, 22 Jun 2026 19:54:24 GMT  
		Size: 14.4 KB (14393 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:alpine` - linux; 386

```console
$ docker pull spiped@sha256:6f3becd5ab17860d0d79cdad5a8314f9f41ade80934bec3e845f2be0549f7399
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3735070 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7c2c4aea7b344dfb6e18f2e0fca5adbbeb691624d97cccfc1e5787f7112f1c1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Mon, 22 Jun 2026 19:20:21 GMT
ADD alpine-minirootfs-3.22.5-x86.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:20:21 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 19:52:33 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Mon, 22 Jun 2026 19:52:34 GMT
RUN apk add --no-cache libssl3 # buildkit
# Mon, 22 Jun 2026 19:52:45 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Mon, 22 Jun 2026 19:52:45 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Mon, 22 Jun 2026 19:52:45 GMT
VOLUME [/spiped]
# Mon, 22 Jun 2026 19:52:45 GMT
WORKDIR /spiped
# Mon, 22 Jun 2026 19:52:45 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Mon, 22 Jun 2026 19:52:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 22 Jun 2026 19:52:45 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:a4b74ab0c43260cc6600b37d5a1ed742d904bba03625caa74b18e45744cde3d1`  
		Last Modified: Mon, 22 Jun 2026 12:03:14 GMT  
		Size: 3.6 MB (3605660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:370212c6233698cf3a2cededd4bd44f00eac7c5e03af3c80a0a1d46c8a4ffdf3`  
		Last Modified: Mon, 22 Jun 2026 19:52:49 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9589ee7d567bbc2c8b0bdd8091e2600f7493e43c86c9291e8e0c5cb80c56fd63`  
		Last Modified: Mon, 22 Jun 2026 19:52:49 GMT  
		Size: 7.9 KB (7935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40a2e946a568955b4fc26e807e13538dfc53fdf5c40195b033d6738d5eb47988`  
		Last Modified: Mon, 22 Jun 2026 19:52:49 GMT  
		Size: 120.1 KB (120096 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5c4c53f53316aa33359a13371beb39c12857d53615d08c755157fbd69bb338d`  
		Last Modified: Mon, 22 Jun 2026 19:52:49 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca3585934873b3572c65ed05b1212ac1144f16b9ef8468d66230cedacf8c04ab`  
		Last Modified: Mon, 22 Jun 2026 19:52:51 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:069fb82d31cd63808dd6a7d5c56b36a98d126a4f8d452cff42e101a369d62c21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.4 KB (96395 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a99309a2ee767f77be492110796b79f8f183f4a91c5e150ce93856bfc9eb541a`

```dockerfile
```

-	Layers:
	-	`sha256:f85f07db752d4a828f227d726b92f676379255ba60f6efa8fb1a91b8cb20e575`  
		Last Modified: Mon, 22 Jun 2026 19:52:49 GMT  
		Size: 82.2 KB (82172 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6ee94877067613386073525f14205ddff5c1f158f239bc7509f064e7c73ecc48`  
		Last Modified: Mon, 22 Jun 2026 19:52:49 GMT  
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
$ docker pull spiped@sha256:de4b34c7a3ad65daa04d28d7e12287d7241887e56b69c69bb8935fefbd9c0062
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
$ docker pull spiped@sha256:06f6d191d00c3c7f99f9ca6bc35961abde2cefdf0c4c3ef829ee12c8e723b1a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.8 MB (36835681 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b886f796060d79ea57dfed8e6573334428e6ba942e2416c5e9d4991e4358f4d6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 00:36:40 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Thu, 11 Jun 2026 00:36:43 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:37:07 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Thu, 11 Jun 2026 00:37:07 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Thu, 11 Jun 2026 00:37:07 GMT
VOLUME [/spiped]
# Thu, 11 Jun 2026 00:37:07 GMT
WORKDIR /spiped
# Thu, 11 Jun 2026 00:37:07 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Thu, 11 Jun 2026 00:37:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 11 Jun 2026 00:37:07 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:72c03230f1363a3fb61d2f98504cf168bad3fe22f511ad2005dc021515d7ce97`  
		Last Modified: Wed, 10 Jun 2026 23:40:25 GMT  
		Size: 29.8 MB (29785415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:527ecde60bfe50017124e67b8415956fd4fb6c9d88a886f3050cf3759f4f98dd`  
		Last Modified: Thu, 11 Jun 2026 00:37:15 GMT  
		Size: 1.1 KB (1104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ccfb06129b754706d994d24161d30c750e9d947232c5d51a4213ea845f178c5`  
		Last Modified: Thu, 11 Jun 2026 00:37:15 GMT  
		Size: 827.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef3d898f83d1faa117388bd37c5a2c913e57742474e0f610d32e0e1c83e5c8ef`  
		Last Modified: Thu, 11 Jun 2026 00:37:15 GMT  
		Size: 7.0 MB (7047900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1436ff66f580ac7020fa765af6cbc9cd8c91911721a10dfa2305b6404b18cea`  
		Last Modified: Thu, 11 Jun 2026 00:37:15 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2d6ed45d70891121ffe50995b4a569aa6dbda4c3a37a3fa16927fe16da829f7`  
		Last Modified: Thu, 11 Jun 2026 00:37:16 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:latest` - unknown; unknown

```console
$ docker pull spiped@sha256:d5cecdf47fa2040ff01111fdbbb75c19d537a969a776bc1c8778d421c2364a04
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3641284 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:082365ba064127a901f5498578d29ee8a542bbc7adc94e40bf4cf9e2a84a407f`

```dockerfile
```

-	Layers:
	-	`sha256:8a7bb242a706f30d64bcc8002692cee4179a16af8322cf72d23b0a8c78123a57`  
		Last Modified: Thu, 11 Jun 2026 00:37:15 GMT  
		Size: 3.6 MB (3626302 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:789d0bf94bddbb877fd99e66c1f0e2fa4901e5821fb450c040ff83bf254aeb75`  
		Last Modified: Thu, 11 Jun 2026 00:37:15 GMT  
		Size: 15.0 KB (14982 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:latest` - linux; arm variant v5

```console
$ docker pull spiped@sha256:3a77fd17bf87542b39acd5c371cb4509f911aba18087b5841340cdae79eb07e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.8 MB (33750953 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9f871c59019572295a1c6f16175304e8c052d7ae1bde8550e6316bd337fc36b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 01:20:06 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Thu, 11 Jun 2026 01:20:11 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 01:20:37 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Thu, 11 Jun 2026 01:20:37 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Thu, 11 Jun 2026 01:20:37 GMT
VOLUME [/spiped]
# Thu, 11 Jun 2026 01:20:37 GMT
WORKDIR /spiped
# Thu, 11 Jun 2026 01:20:38 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Thu, 11 Jun 2026 01:20:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 11 Jun 2026 01:20:38 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:ed883f3fd95b7edef302d7ca9520eefdae280af081509bd7e9e5b5ff8f4cda7c`  
		Last Modified: Wed, 10 Jun 2026 23:41:17 GMT  
		Size: 28.0 MB (27959200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e751f68dcb09ba1579bee55a24286186b59e393de92bac08ff724b4981d5d170`  
		Last Modified: Thu, 11 Jun 2026 01:20:44 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d89df5ca97fe521123a4a7aae01c94c4479bf368a9d8c696eee17064fc312bc1`  
		Last Modified: Thu, 11 Jun 2026 01:20:45 GMT  
		Size: 831.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91d2c4ac84d26c20df4907085b90aeb331861a219b69716c57682ae2cb946eb8`  
		Last Modified: Thu, 11 Jun 2026 01:20:45 GMT  
		Size: 5.8 MB (5789383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2073b26a67b2b25b8dae9d6d7a2028b43f95697825a4cb34a083684f542d8fe`  
		Last Modified: Thu, 11 Jun 2026 01:20:45 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1e64de9d592c6c09b59082de73dbb84f8e63a26763394e8083e1dd58f66d693`  
		Last Modified: Thu, 11 Jun 2026 01:20:46 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:latest` - unknown; unknown

```console
$ docker pull spiped@sha256:e786ed555ddf93e97965e805339e0e57e642ee1b6992efb0a38706feed7d6111
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3634384 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:678d30be6a2af3135f4751e15d6b35b82e2cd1dbc9a6858fa252aa22ea5487f6`

```dockerfile
```

-	Layers:
	-	`sha256:f416dd4fb0aef1763e3288e5f7435905aa2cacf86c5d53d1ff62343b3aee11b4`  
		Last Modified: Thu, 11 Jun 2026 01:20:45 GMT  
		Size: 3.6 MB (3619296 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6a02acc670c38ba874d76cb8784856b12a90aa7e49311ee73beff9aa2761b4c8`  
		Last Modified: Thu, 11 Jun 2026 01:20:45 GMT  
		Size: 15.1 KB (15088 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:latest` - linux; arm variant v7

```console
$ docker pull spiped@sha256:079fbf73e349c36cc2b4d55e664f1d5a60b482fa43a1021f0ea8cb3e38b490fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.8 MB (31798135 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:959018a10d28c5d1dde8c33184f543a1293c46376550688e906dbae7ddf55228`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 01:21:52 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Thu, 11 Jun 2026 01:21:55 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 01:22:18 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Thu, 11 Jun 2026 01:22:18 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Thu, 11 Jun 2026 01:22:18 GMT
VOLUME [/spiped]
# Thu, 11 Jun 2026 01:22:18 GMT
WORKDIR /spiped
# Thu, 11 Jun 2026 01:22:18 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Thu, 11 Jun 2026 01:22:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 11 Jun 2026 01:22:18 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:4bd6ddea06d5009ee47ddb0f254a2569aff0230c005869ebd416b20295d945c0`  
		Last Modified: Wed, 10 Jun 2026 23:42:34 GMT  
		Size: 26.2 MB (26211004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51bb869011c6d164e974fe820179933094dcc281df7a55480fc4077277232c77`  
		Last Modified: Thu, 11 Jun 2026 01:22:25 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:422e823bc0c6498856622e79affa11c1598652143bfa7f350dc04a8bae10a58a`  
		Last Modified: Thu, 11 Jun 2026 01:22:25 GMT  
		Size: 827.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fadeadb89fb7f698439cd322f47ba897a03fd1551ffe3fcf76d75f5383cd472`  
		Last Modified: Thu, 11 Jun 2026 01:22:25 GMT  
		Size: 5.6 MB (5584763 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3817b48e6549ab977fe0f1bbbb517045c499e8b6a3c28271dc05398321fe485d`  
		Last Modified: Thu, 11 Jun 2026 01:22:25 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a52c3658e003288d1598c728ef7ab0c5167ce43d1e20bf855db1dde18f30b339`  
		Last Modified: Thu, 11 Jun 2026 01:22:27 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:latest` - unknown; unknown

```console
$ docker pull spiped@sha256:4660d6bee86fba733a44735e9cea0b5dfa13410ac081e02edbed22229736f4ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3633504 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f7dd6ebfec69dc7720608ae6a9b0c5af682ff982f3ce0440ed4f3bf904f4c5f`

```dockerfile
```

-	Layers:
	-	`sha256:d25034d6fee06e5ff09bdc9004cbe4b4a4e9d9ed95b0624f5000cb9e580a086e`  
		Last Modified: Thu, 11 Jun 2026 01:22:25 GMT  
		Size: 3.6 MB (3618417 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:deb1d9d6f39ee38fed21b5f4de28c58d8058b0810a5cd7893d92d295084642d1`  
		Last Modified: Thu, 11 Jun 2026 01:22:25 GMT  
		Size: 15.1 KB (15087 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:latest` - linux; arm64 variant v8

```console
$ docker pull spiped@sha256:b666025eb8bf9bd288d28306188f384cf5e1cf793252a3092ed8467ea174a7c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.4 MB (36384823 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2b7f7df51ecb422ed1c09aa176c982afa86a96f6e553daf85ffd468ca5f3846`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 00:38:14 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Thu, 11 Jun 2026 00:38:16 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:38:39 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Thu, 11 Jun 2026 00:38:39 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Thu, 11 Jun 2026 00:38:39 GMT
VOLUME [/spiped]
# Thu, 11 Jun 2026 00:38:39 GMT
WORKDIR /spiped
# Thu, 11 Jun 2026 00:38:39 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Thu, 11 Jun 2026 00:38:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 11 Jun 2026 00:38:39 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:a25cd16f2d8653f652f8292b34b21bfbabdc85d6b39861a24b85f0896df1a95e`  
		Last Modified: Wed, 10 Jun 2026 23:40:16 GMT  
		Size: 30.1 MB (30148530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af99214715c4dd89b01b22d803c733a8cdeff8b516b64dcbc4039e3bb73edf81`  
		Last Modified: Thu, 11 Jun 2026 00:38:46 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cb7f2ca44a46746d13284bd66cb8d509327101aa851a60e2f4562b4c0b43fe4`  
		Last Modified: Thu, 11 Jun 2026 00:38:46 GMT  
		Size: 828.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fc568496a63b54431809869a1a353a056bd0286efc252ed16943213148d8e78`  
		Last Modified: Thu, 11 Jun 2026 00:38:46 GMT  
		Size: 6.2 MB (6233926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62455682699c33f1af511f11805177432eb0df675093f3a55be46e8069d099ad`  
		Last Modified: Thu, 11 Jun 2026 00:38:46 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1337cf4ae97e82beefcd0736801f263b58faa5acea8bbd02b6fb1610b3c08a69`  
		Last Modified: Thu, 11 Jun 2026 00:38:47 GMT  
		Size: 336.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:latest` - unknown; unknown

```console
$ docker pull spiped@sha256:28fd7f18765bc97e01aed948eb208846037e2fdc5be5b01c7b60a1dab0ecc29d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3636446 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:caaed5bb2a83f15f132837c8042bc95288ce03bd799f9d4a49b960975af17bea`

```dockerfile
```

-	Layers:
	-	`sha256:f4119ebc6f5a2232c489599390a07000eb50a2325250846032e65737506b59fb`  
		Last Modified: Thu, 11 Jun 2026 00:38:46 GMT  
		Size: 3.6 MB (3621330 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ff1ae5a7dd30d786394e331ae8fd4a26444a7fab07e0f0f35bd0d9f9e8aa11f4`  
		Last Modified: Thu, 11 Jun 2026 00:38:46 GMT  
		Size: 15.1 KB (15116 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:latest` - linux; 386

```console
$ docker pull spiped@sha256:02f4ba23c22e1271ac47e549272f9bb9b73d515c584ef6657b10b34089186119
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.7 MB (37746372 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c77be7a202c7361655d5298662fbd58b4ac13a280d8eea6d0e5696277b5d6dc2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 00:44:31 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Thu, 11 Jun 2026 00:44:34 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:45:03 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Thu, 11 Jun 2026 00:45:03 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Thu, 11 Jun 2026 00:45:03 GMT
VOLUME [/spiped]
# Thu, 11 Jun 2026 00:45:03 GMT
WORKDIR /spiped
# Thu, 11 Jun 2026 00:45:03 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Thu, 11 Jun 2026 00:45:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 11 Jun 2026 00:45:03 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:720f951a68f4f9ab464e52b53cf88cfb86bc876b3f00956d000420777ab93c0c`  
		Last Modified: Wed, 10 Jun 2026 23:40:30 GMT  
		Size: 31.3 MB (31301194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96b36e957fa28b38d49b885ce8ff4366a6bfcb98bf38aa1dd3dd51c9b7cd333c`  
		Last Modified: Thu, 11 Jun 2026 00:45:10 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3aae632d05299c9dee2bec97ea596046cf5c7c15eff6529e97937627b28994fa`  
		Last Modified: Thu, 11 Jun 2026 00:45:10 GMT  
		Size: 828.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd7f7718fe56cea19c8269279c48994d7ae792b5209abc4faef63781a55560f4`  
		Last Modified: Thu, 11 Jun 2026 00:45:11 GMT  
		Size: 6.4 MB (6442811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96e529f830d838d84290e5326067c74dc889693a3954cd9a7dbd43c0b583c23f`  
		Last Modified: Thu, 11 Jun 2026 00:45:10 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fe774eab45468f5459c9ea3e437c826c9c3d130cbc49f077eef0338b91a9edd`  
		Last Modified: Thu, 11 Jun 2026 00:45:12 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:latest` - unknown; unknown

```console
$ docker pull spiped@sha256:43aeb04090782a915b6e9289e6133f1f0327b7465670b94e07f481b847c4025b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3635377 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd02b428a54369d078699f646a6c58bb59205a7d8e90fd308ef1b652598d64f9`

```dockerfile
```

-	Layers:
	-	`sha256:20700448f422d0e1e5f84b34dcae83618e79e0454a188609c16921611a98ff5a`  
		Last Modified: Thu, 11 Jun 2026 00:45:10 GMT  
		Size: 3.6 MB (3620431 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b8c3c92718b75b733828274ef1f0c3ac60a2665e98431b090587ac61fa798684`  
		Last Modified: Thu, 11 Jun 2026 00:45:10 GMT  
		Size: 14.9 KB (14946 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:latest` - linux; ppc64le

```console
$ docker pull spiped@sha256:77a28ff7796938b2e628dcb8466cba0a9b9e9209373514b53eb9500a4eb54179
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.4 MB (40449493 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5c663351cf736af7041bf6dab200f7240abda1f91a38cc9154e15ecc605051b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 04:42:39 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Thu, 11 Jun 2026 04:42:43 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 04:43:31 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Thu, 11 Jun 2026 04:43:31 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Thu, 11 Jun 2026 04:43:31 GMT
VOLUME [/spiped]
# Thu, 11 Jun 2026 04:43:31 GMT
WORKDIR /spiped
# Thu, 11 Jun 2026 04:43:31 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Thu, 11 Jun 2026 04:43:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 11 Jun 2026 04:43:31 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:9d6b2e320e2b74843186d830e8202c50ebfaeccf823d239e3e3e349a8a508d80`  
		Last Modified: Thu, 11 Jun 2026 00:24:42 GMT  
		Size: 33.6 MB (33606340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae397a9bd78994d17d78508ffe6c90b95321c279f11d71546a6690cf7b3bfa56`  
		Last Modified: Thu, 11 Jun 2026 04:43:44 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:527c0346e0be1cff6e959785d2ead56a024d388a5f5b49668bb10ef02df87e5b`  
		Last Modified: Thu, 11 Jun 2026 04:43:44 GMT  
		Size: 825.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfb798ab52e9baacaca51304c7ae7bd07e22ffa204c22fa1ee3f600faa9d384c`  
		Last Modified: Thu, 11 Jun 2026 04:43:45 GMT  
		Size: 6.8 MB (6840786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9e2eda05f5b8c55e69e0f5f7b8411ef18adfa257a0964e74893e13aa8460231`  
		Last Modified: Thu, 11 Jun 2026 04:43:44 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89c91b4a125ec65053187500a3042ba5cf4b3d3c3757a5130a5b6a469502146e`  
		Last Modified: Thu, 11 Jun 2026 04:43:45 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:latest` - unknown; unknown

```console
$ docker pull spiped@sha256:cde6ed1dd2ca8f029ced3770c7fd29bfed2a5e054b7f88c1c2828ea61ae0d53a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3637067 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f348c1d24e29a4dd183acde8c7db1a7186ed71bf6cc2b0deb230af07b7e3608`

```dockerfile
```

-	Layers:
	-	`sha256:9028cc214c0ddc113b07afbc6b1c7d125225085781875688e233501b5e4f6973`  
		Last Modified: Thu, 11 Jun 2026 04:43:45 GMT  
		Size: 3.6 MB (3622039 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:23b0df7ce9f0c385bfc283502819fb193952bc81b97402aae117279766c4435f`  
		Last Modified: Thu, 11 Jun 2026 04:43:44 GMT  
		Size: 15.0 KB (15028 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:latest` - linux; riscv64

```console
$ docker pull spiped@sha256:d1196bf05f6d34c1b33d0f44d558a64dacbac606da8ede3854f0f56b7da88dd7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.6 MB (37640838 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:257f964733ff5e0fb249561928b63d968d0ea7e0f22a1650497b8f634a78b7b1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1781049600'
# Sat, 13 Jun 2026 02:38:34 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Sat, 13 Jun 2026 02:39:05 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 13 Jun 2026 02:42:10 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Sat, 13 Jun 2026 02:42:10 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Sat, 13 Jun 2026 02:42:10 GMT
VOLUME [/spiped]
# Sat, 13 Jun 2026 02:42:10 GMT
WORKDIR /spiped
# Sat, 13 Jun 2026 02:42:10 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sat, 13 Jun 2026 02:42:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 13 Jun 2026 02:42:10 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:0b510fe8545cab831b696965b5a825649c5c945581e912d31a08a0b30ff940c0`  
		Last Modified: Thu, 11 Jun 2026 03:01:06 GMT  
		Size: 28.3 MB (28282305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f639c6130c8aca0f837b171cb0a0d45c790c5d7bf9518eff2b8ff95b48f104c`  
		Last Modified: Sat, 13 Jun 2026 02:43:23 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07e14a8d467e3dc32c3ec2a585b788255e6272eeaa9763d004943122f7248c27`  
		Last Modified: Sat, 13 Jun 2026 02:43:23 GMT  
		Size: 822.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d41b9627a0c3fc9b82eb3a3347a368ac72d11d19f3ff135e81910be58f7ced5`  
		Last Modified: Sat, 13 Jun 2026 02:43:24 GMT  
		Size: 9.4 MB (9356169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4946ccd28be72a02f3c71907db8b182219a80ff46301e8a09fdd946d52683dd8`  
		Last Modified: Sat, 13 Jun 2026 02:43:23 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f74e027caa4d5bd042803e1c5847e795634af08a895bf7099c444bcdf51c4cc`  
		Last Modified: Sat, 13 Jun 2026 02:43:24 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:latest` - unknown; unknown

```console
$ docker pull spiped@sha256:bd59a45c25ec7d4b80d63933dffd3bd86372d97041734ebbf62964d8a991e093
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3628474 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0ed4a489648532fba6cde1d7e88a809bdb98383c98aee19aaba7a5a947fbd77`

```dockerfile
```

-	Layers:
	-	`sha256:d44a97abcbeafd6a6ec2dd69c997db68246839a5985937d49f3c1d5fbc99a495`  
		Last Modified: Sat, 13 Jun 2026 02:43:24 GMT  
		Size: 3.6 MB (3613445 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:de64e5286a1b72fafa9b68c701bf6ba016f164bdfaf60538499d95770fbf3f6a`  
		Last Modified: Sat, 13 Jun 2026 02:43:23 GMT  
		Size: 15.0 KB (15029 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:latest` - linux; s390x

```console
$ docker pull spiped@sha256:bd22ee71a9e9236e2ca69180ad51c06cf6d8e35afbd4add081b0d2f764edc08e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.0 MB (35975833 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1ad1052f1364f10f7a17a6666de217cbde8ab8c0e0ac3499018c5cd72b4ee17`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 01:43:42 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Thu, 11 Jun 2026 01:43:44 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 01:44:01 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Thu, 11 Jun 2026 01:44:01 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Thu, 11 Jun 2026 01:44:01 GMT
VOLUME [/spiped]
# Thu, 11 Jun 2026 01:44:01 GMT
WORKDIR /spiped
# Thu, 11 Jun 2026 01:44:01 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Thu, 11 Jun 2026 01:44:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 11 Jun 2026 01:44:01 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:760dcf74fdfe93300ce15b5b23adf9aa4af45b6ba9d69925863198f64881a537`  
		Last Modified: Wed, 10 Jun 2026 23:42:35 GMT  
		Size: 29.9 MB (29851354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbee78aca287a132f4560c3c136874e9fd2eb76d548257a9d3a3df8c901bcc4f`  
		Last Modified: Thu, 11 Jun 2026 01:44:13 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:592a34f021f7dfd15ace5226ae509b1158c586b704884d60433770343a082992`  
		Last Modified: Thu, 11 Jun 2026 01:44:13 GMT  
		Size: 828.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb3568250ea65438eb60733aee26c97620a46d0a35f1724cad1b6cdf7fbcc023`  
		Last Modified: Thu, 11 Jun 2026 01:44:13 GMT  
		Size: 6.1 MB (6122111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b205eccacc5cb65c52b6fa4618ba96b957fd2f8a2f5423e2653cc1b280d2f23`  
		Last Modified: Thu, 11 Jun 2026 01:44:13 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02c73a6752a874142787522de11c367cd55d46e4661d6e3216d3509660bc3091`  
		Last Modified: Thu, 11 Jun 2026 01:44:14 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:latest` - unknown; unknown

```console
$ docker pull spiped@sha256:b9ccb006c7597035afc395814bcd5e176f1c6747e8cdcbb2e2e99a609798685c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3633647 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0955f426902eecb0ba4cee729a5abb10364e89f0579f841377a2401fdd89f43`

```dockerfile
```

-	Layers:
	-	`sha256:bc258d4741b882519b7d7392f726369c450df7d38b8a5f5b761096da236e6d1a`  
		Last Modified: Thu, 11 Jun 2026 01:44:13 GMT  
		Size: 3.6 MB (3618665 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9e8ebd7ccddfecb937db9fd26d8850a9b8222af37b614601c7b7e2d424a147fa`  
		Last Modified: Thu, 11 Jun 2026 01:44:13 GMT  
		Size: 15.0 KB (14982 bytes)  
		MIME: application/vnd.in-toto+json
