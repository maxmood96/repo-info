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
$ docker pull spiped@sha256:eae5c3dfb8127c952913e3baabc3945915ed9fe7263a8928e60ee6f9f6c4d090
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
	-	linux; mips64le
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `spiped:1` - linux; amd64

```console
$ docker pull spiped@sha256:c98a4a33bc9da8d56f0d5163a75842ce1c6c2db4ab21e159b3bde195afd59adc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.1 MB (37087849 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4355dd26bbc1d77f98e7c0ac73eacf4bc8915d2d20786bfbb00b17e33f21fa17`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 02 Apr 2025 21:12:22 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1747699200'
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
	-	`sha256:61320b01ae5e0798393ef25f2dc72faf43703e60ba089b07d7170acbabbf8f62`  
		Last Modified: Wed, 21 May 2025 22:27:39 GMT  
		Size: 28.2 MB (28225330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b236b995fe25e62e0a9b025d43ed6aeb0d706dda8c314117fcf6638ebdc7e2b`  
		Last Modified: Wed, 21 May 2025 23:20:12 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe7a90816c2d64d22fdbae87a108eb3343157d21eabfdd8a0362fb7c337c99ab`  
		Last Modified: Wed, 21 May 2025 23:20:12 GMT  
		Size: 2.4 MB (2402177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e20521234d5fd2df1eb25c23579bae7d5636fcce182618943e02ef5ab794963`  
		Last Modified: Wed, 21 May 2025 23:20:12 GMT  
		Size: 6.5 MB (6458802 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8c3b16ce6622a837772fdf6d18fc84b976e8694098211b2e9a4383a62931558`  
		Last Modified: Wed, 21 May 2025 23:20:12 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75351b1571732d8e2e27dfde274116dd0037459b25301366b27c9402ede4aae3`  
		Last Modified: Wed, 21 May 2025 23:20:13 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1` - unknown; unknown

```console
$ docker pull spiped@sha256:38fba8cf5966d1da5219266d88064e3aaceb887d32420638d2f0135dbbfd4ca5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3553217 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d442efde223bd171e1f3b5bdd7d6301e1ce2df0c1ea291f621d582ff0136ad75`

```dockerfile
```

-	Layers:
	-	`sha256:0c32ff8bf0f89bea9948bda0ad2c06ecc23437d5eefe99e0003e3c0eae7be3a8`  
		Last Modified: Wed, 21 May 2025 23:20:12 GMT  
		Size: 3.5 MB (3538177 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:faed6139c10365db1a206a064e87b5765026aa41bba89ab1a43fbcf5befd26ce`  
		Last Modified: Wed, 21 May 2025 23:20:12 GMT  
		Size: 15.0 KB (15040 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1` - linux; arm variant v5

```console
$ docker pull spiped@sha256:799111c4807c2fea831489b691e498f914d9a30c2f65688bf798574eec5db8c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.9 MB (32904241 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f9e5e8afcac44ab7363c93359b12a1c8dfb1867ed4df01c19777a222ce48c0f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 02 Apr 2025 21:12:22 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1747699200'
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
	-	`sha256:fab452a77ecb21a2e30922ab3eed19310b6d56763bcfc4e4bd31f28d9747f745`  
		Last Modified: Wed, 21 May 2025 22:27:58 GMT  
		Size: 25.8 MB (25756898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf5fcb13f4fae5c0701ae97175c1fde5a265e39ab7420ed78e63dc654b097e65`  
		Last Modified: Thu, 22 May 2025 01:12:54 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9556b3c226c521d39ced715dacdb0ddd196bf05f5846d3732d60e8a3f55a1de`  
		Last Modified: Thu, 22 May 2025 01:12:54 GMT  
		Size: 2.0 MB (1998268 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce40ec37f30dc6d7d5a1ed74cf1f1bae7f1a05eb87b99e62d9b4c27a28051931`  
		Last Modified: Thu, 22 May 2025 01:12:55 GMT  
		Size: 5.1 MB (5147533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4b23094f6c0b0b7beabfe549bc26fad9124341fe7251635a2286ad9d50c488e`  
		Last Modified: Thu, 22 May 2025 01:12:54 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f314f72e5ab08b9522e8df48d487f9c5448dd07a3c496be756e549d855a92e7c`  
		Last Modified: Thu, 22 May 2025 01:12:55 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1` - unknown; unknown

```console
$ docker pull spiped@sha256:9cf2a6d75f36284a1051b375e26316cc1e1a134adaff1f248a8d390552e88dd5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3524157 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3a141429766668432eef187e965dabf4459daabd05cb999129f21ee65ed20c6`

```dockerfile
```

-	Layers:
	-	`sha256:6a32a05c66630aa10a22096368b76df8bd67aaf342c8dd930619b45a1888cbc4`  
		Last Modified: Thu, 22 May 2025 01:12:54 GMT  
		Size: 3.5 MB (3509015 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:41b70d9c48c2c437462d07be8fc990b465281e5c418124d21004a253d959aa18`  
		Last Modified: Thu, 22 May 2025 01:12:54 GMT  
		Size: 15.1 KB (15142 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1` - linux; arm variant v7

```console
$ docker pull spiped@sha256:bd88168940017d415031d65c8b562a450fb598c60cf7e38ede2eebc4e622eed3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.7 MB (30679570 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:334bd5bd9fc6f29c24ec13b8cda836e7cb1c5e76c363b01a5ae63808e03e7cf0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 02 Apr 2025 21:12:22 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1747699200'
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
	-	`sha256:3726bc5cceb817ddfc7c2e1dbdfb4900fc6e27b680d63b8d751b06952753b6a1`  
		Last Modified: Wed, 21 May 2025 22:27:58 GMT  
		Size: 23.9 MB (23932922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28497644b53abef7026a25140f5b20b9e5f984102c735a18f9ad13b06d325d06`  
		Last Modified: Thu, 22 May 2025 02:11:46 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c06616ca963aeb60b1926e7a4505f5587eb632014d17e10775734237f64bfdd5`  
		Last Modified: Thu, 22 May 2025 02:11:46 GMT  
		Size: 1.9 MB (1856406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0454a735cab512a3994c19f6461e13b792aa7d4ae6f2f7b7beefad87c86e1619`  
		Last Modified: Thu, 22 May 2025 02:11:46 GMT  
		Size: 4.9 MB (4888699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c30c741ba1d6aa6d7e8a8bb49b3f73d5cfc41cc58cc9f1ee0d0222ef1eb61e3`  
		Last Modified: Thu, 22 May 2025 02:11:46 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efa2405c063638356b662a29deb560323db64a04302d8fb7b4e41e40832595be`  
		Last Modified: Thu, 22 May 2025 02:11:47 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1` - unknown; unknown

```console
$ docker pull spiped@sha256:67903915b9908ceec6eff9982d5e47b52aed66b921141fb35e158bef999cc642
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3523340 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e202a4f6c6a60f84bb42ff7184ed9b6fc409d848ff7be381fd3aeecfd2229b7e`

```dockerfile
```

-	Layers:
	-	`sha256:798416b4b99780fb82d37f69a61f55757da43446999fd396b2345a89f61b9717`  
		Last Modified: Thu, 22 May 2025 02:11:46 GMT  
		Size: 3.5 MB (3508198 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:16fe3f5accbcda69a4f3d2d1a7e95d1755dbdf53436e1dafd5996ebc9dc0ebda`  
		Last Modified: Thu, 22 May 2025 02:11:46 GMT  
		Size: 15.1 KB (15142 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1` - linux; arm64 variant v8

```console
$ docker pull spiped@sha256:d5cafb803c9a0da7ab4771f49d9cdb8a8cdcb3ff719bcbb09e016d458b52edae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.8 MB (35805923 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4433b4b2209f95a137ec9d4fc3da9f0399b1a927010b07100f4d2cb33f01eec6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 02 Apr 2025 21:12:22 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1747699200'
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
	-	`sha256:b16f1b16678093d11ecfece1004207a40f9bc1b7d9d1d16a070c1db552038818`  
		Last Modified: Wed, 21 May 2025 22:27:55 GMT  
		Size: 28.1 MB (28065280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58d7aa0e5553a8e1676ebb9a1e8b4e211d5e24d00e206dd06e9dc931036210a8`  
		Last Modified: Thu, 22 May 2025 02:26:31 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b01b22375091a64a96ee1ad4e57158b3b3a3403ba79cab1a56af7fcaf2c4fd4b`  
		Last Modified: Thu, 22 May 2025 02:26:32 GMT  
		Size: 2.2 MB (2247441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cf33c8dbe86b945cd509593f45ace969c1839a8dee7d1828092b41632af9837`  
		Last Modified: Thu, 22 May 2025 02:26:32 GMT  
		Size: 5.5 MB (5491661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa6e1ae6c666fd43ad0bb5cbd1d595c4f6774a7621a81e94f751dba1447227a4`  
		Last Modified: Thu, 22 May 2025 02:26:32 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25be54df2c26151d78b7c6bcc8b71f10a49ca87573849bc5561334e83d854f56`  
		Last Modified: Thu, 22 May 2025 02:26:33 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1` - unknown; unknown

```console
$ docker pull spiped@sha256:76bf26d851cd8fc562b888569d70024625766d5c1b77df5d31a5d5045d909e7a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3524578 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:232fb12c6174ddf70b733574174d96ac46893cfd76e8ecaf5a3d2a2d55139191`

```dockerfile
```

-	Layers:
	-	`sha256:863430707bd172ac83c08ecfc72f18ec0a9e85de22d979a70542342ba06ead69`  
		Last Modified: Thu, 22 May 2025 02:26:32 GMT  
		Size: 3.5 MB (3509405 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cc3c4313ab583feefd96c652f06140e88ab6b676b233c9b4c5ead13c712d32ce`  
		Last Modified: Thu, 22 May 2025 02:26:31 GMT  
		Size: 15.2 KB (15173 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1` - linux; 386

```console
$ docker pull spiped@sha256:de2d0f62127be81d4c417ee09c2e83dcc650d781e485052c53b4d83e7e41c305
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.6 MB (37566353 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e29b46d435dc73b21b5f638b8b87840b502cba5421b87b459851dd558cbb504`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 02 Apr 2025 21:12:22 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1747699200'
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
	-	`sha256:7d0eb60defa1a32d12e94bc0d7c2c578881c578aeec0c1d786ef5a19c72a34ab`  
		Last Modified: Wed, 21 May 2025 22:27:56 GMT  
		Size: 29.2 MB (29207487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fc34ae407ddfd8aa872313e98808f6d037d29874d733022ebeb03c21b075b9d`  
		Last Modified: Wed, 21 May 2025 23:19:31 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea1121e956c060196b27bf2cb1c7c4834fd0683b4d013d49729246105637c7e6`  
		Last Modified: Wed, 21 May 2025 23:19:31 GMT  
		Size: 2.4 MB (2400579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58c083d4e9d3c172b7e2dff742a55d190d7deea62d62e77c68be78ebe005756f`  
		Last Modified: Wed, 21 May 2025 23:19:31 GMT  
		Size: 6.0 MB (5956747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95924c7d3bb09f7d740e28a65b589259ca71ed83b9907221ab77e5710964fa84`  
		Last Modified: Wed, 21 May 2025 23:19:31 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af2e19c16d9e608f72faf9f7145bd18f20be31aa8254201cdc30e14098b0ab90`  
		Last Modified: Wed, 21 May 2025 23:19:32 GMT  
		Size: 336.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1` - unknown; unknown

```console
$ docker pull spiped@sha256:0e4e1e2182c7414a91dbedc4eee31dc2f23267ca32cb3bc1d1af586c79a15511
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3547159 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:488c249ee13b017bc6d2db92c2455dddf8636b7f8dda1f17d1c32ad46e3f1bc3`

```dockerfile
```

-	Layers:
	-	`sha256:5a933c5783118b861dc28e67218f04f000686e48be72186367702865e0819555`  
		Last Modified: Wed, 21 May 2025 23:19:31 GMT  
		Size: 3.5 MB (3532156 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a135b975223fb9944b6870b3f284f6d0e1276e5223c8b3790aec5292925ac030`  
		Last Modified: Wed, 21 May 2025 23:19:31 GMT  
		Size: 15.0 KB (15003 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1` - linux; mips64le

```console
$ docker pull spiped@sha256:e08a5f574ff6e4c4889083b74ad49f5f1fa5c4909a77fd7f0118f9e4537b2f64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.2 MB (36169243 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81d9271e2536f4b9e06788180f5f1808dc6e92f6183d5cf57c5ac1f4a073b894`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 02 Apr 2025 21:12:22 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1747699200'
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
	-	`sha256:48541e37cd82678078df221c38fde515e820c13a623449b699d224f60f15dae8`  
		Last Modified: Wed, 21 May 2025 22:28:22 GMT  
		Size: 28.5 MB (28511850 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3803a240d8e659370e2fab860baf71e6845bb1657afea9964a9455a06816584f`  
		Last Modified: Thu, 22 May 2025 06:14:35 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:058aa8bad24612579286f5eae085472a3a9f63436aa5165ce779f2d1f73c9e99`  
		Last Modified: Thu, 22 May 2025 06:14:36 GMT  
		Size: 1.8 MB (1842259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60712b0a5b50c33b45964a94fca078484dff5c1bc25928f8b19642a8fdddc723`  
		Last Modified: Thu, 22 May 2025 06:14:36 GMT  
		Size: 5.8 MB (5813592 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f03381e56cdea6e5c69ba962656f3b8ee6708f99bbbe90c8cb59805dec2821f`  
		Last Modified: Thu, 22 May 2025 06:14:35 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0030e45312f412d88429defd5484aa7c1354487911afb2c33273fd71e177e9ed`  
		Last Modified: Thu, 22 May 2025 06:14:36 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1` - unknown; unknown

```console
$ docker pull spiped@sha256:376d3c3cf802ddebdca18c0302bdc8f66c2a6eb3b23346b26c5205f7932dcce1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 KB (14897 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90459617b1bb9aa0a1d2cf5c37b8ad8d23c16eb4f14aacb08afabd9b233b117f`

```dockerfile
```

-	Layers:
	-	`sha256:307900282127ed9322c5ccab5de1df5096b6a0b07bd4395c5b9cb9b8599934bc`  
		Last Modified: Thu, 22 May 2025 06:14:35 GMT  
		Size: 14.9 KB (14897 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1` - linux; ppc64le

```console
$ docker pull spiped@sha256:a7321ff5fec2afbb779a0acf6da6d63f5c5d332938ad6bf260c611ae4a5b1c06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.1 MB (41093723 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15a62507992ef6fb0e12abeb88eb5ecf00ad31cb2d3eb2e89b8f8f14130d29e6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 02 Apr 2025 21:12:22 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1747699200'
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
	-	`sha256:701606535a7233566815cc9ad5f3e5853b443be5476286f6799008053dc2b03b`  
		Last Modified: Wed, 21 May 2025 22:28:16 GMT  
		Size: 32.1 MB (32066912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28a6c81eea611329e12a0cc8737d8ee2c5ada1b8e3aaef98d8acd2741b37d917`  
		Last Modified: Thu, 22 May 2025 07:17:33 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0fc1affdf757c274e7e67536481196cb883110fb5bfd979782fb8383777bfa6`  
		Last Modified: Thu, 22 May 2025 07:17:33 GMT  
		Size: 2.6 MB (2583887 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4db9a308ee6bef1c8241a16cb77c39894f524896d99e85f384dd7eb7a4756ff1`  
		Last Modified: Thu, 22 May 2025 07:17:33 GMT  
		Size: 6.4 MB (6441381 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c37f165cfd98289d815cf96acad45a8ed3cd5f2558537aebefbb0c7c359d0f9e`  
		Last Modified: Thu, 22 May 2025 07:17:33 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f805d8994580dac40f982b71b4ae42685005eeb1438bd76e132c9307532dedd`  
		Last Modified: Thu, 22 May 2025 07:17:34 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1` - unknown; unknown

```console
$ docker pull spiped@sha256:1cfcf23833ca373cc8000f5f9998d74ccf00ecca9ad0fb786e5172d2fcfd39af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3539050 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:789d0ff26873a3c16d1516a64b5521540d3e27924324dd582fbed08e96e970a9`

```dockerfile
```

-	Layers:
	-	`sha256:8b1a9eceb4ec95f4f5b6806a7ec405ea988499e1a2ec48b26ff0ede6b066b2a4`  
		Last Modified: Thu, 22 May 2025 07:17:33 GMT  
		Size: 3.5 MB (3523962 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ae9055586249d83d4bc0597f9cd6f6a21d3b9bf8c399b22bc90d82eed114d347`  
		Last Modified: Thu, 22 May 2025 07:17:33 GMT  
		Size: 15.1 KB (15088 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1` - linux; s390x

```console
$ docker pull spiped@sha256:313c5fbddb0f36164ff9ff07b8afb014aae1fba0aded0128c2058a6960b944dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.3 MB (34345786 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be0c786c61c197ff161771dfba4eecaca2e88d0ad743f2abe498c7758f082708`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 02 Apr 2025 21:12:22 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1747699200'
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
	-	`sha256:fb6e196ef379785f6b759a20e90d74fe0566b240771695f724c27a44aa6cd3ce`  
		Last Modified: Wed, 21 May 2025 22:28:38 GMT  
		Size: 26.9 MB (26882808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38ceb32ec1a8749e974fe5929ea6dff22bcee11dafd2fc667579323da38876f1`  
		Last Modified: Thu, 22 May 2025 00:53:41 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2f56657b11e71e77f7914f81ccb09da12e157355a9c2bfa3ad990780f7ee481`  
		Last Modified: Thu, 22 May 2025 00:53:41 GMT  
		Size: 2.1 MB (2069161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d37a680b670b7565d1e108f473912336f74759acbde356e1baffcebb55ab778`  
		Last Modified: Thu, 22 May 2025 00:53:41 GMT  
		Size: 5.4 MB (5392277 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec75588e715a05902adcfb5629f1851cf0d29ddf5ae3f281b75fdc0a40e98fb6`  
		Last Modified: Thu, 22 May 2025 00:53:41 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0e2d58562f243d49496f4f3e52abfbea3ebecc55c6401ecd80a648029bac830`  
		Last Modified: Thu, 22 May 2025 00:53:42 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1` - unknown; unknown

```console
$ docker pull spiped@sha256:5de6955b949dbe4e3cd91755329d2cb433e60f90fb15863b8bbab4c4f414cd9d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3541403 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d51372649bab5e76ddd19982bc703b786c8dc5b940231eeb5b6fa54327a2e1d`

```dockerfile
```

-	Layers:
	-	`sha256:7ddaee20724beee644d4580292cd7c349e170f436b4a509a76ba3ecb3b2337e0`  
		Last Modified: Thu, 22 May 2025 00:53:41 GMT  
		Size: 3.5 MB (3526363 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0371bae7cc54c2d437162fb10d62d7bc577205878fe8e5d855cbf8030eb4ca81`  
		Last Modified: Thu, 22 May 2025 00:53:41 GMT  
		Size: 15.0 KB (15040 bytes)  
		MIME: application/vnd.in-toto+json

## `spiped:1-alpine`

```console
$ docker pull spiped@sha256:19cab0821b57af25c5e04f34834de199acba4d5a909887ce0f093a3200c51243
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
$ docker pull spiped@sha256:622df849c8857cb4538c0b252cf0b5e94d10a2b5af1222af4d54ce9016270049
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3759161 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83432e0291e920e3ef7ce3c7690aba0f53cf7250e10452315d154dccfe1df29f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Wed, 02 Apr 2025 21:12:22 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
RUN apk add --no-cache libssl3 # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Wed, 02 Apr 2025 21:12:22 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
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
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 12:05:35 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:114b63918a29534fea2f0cc34ca9459cf360301d5cc6e425a943254bd857bdfd`  
		Last Modified: Wed, 02 Apr 2025 22:08:24 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4e3893b92c8e046b61bf235250bedbecb6eca134316b11bfb15c8cd1b337f3d`  
		Last Modified: Wed, 02 Apr 2025 22:08:24 GMT  
		Size: 7.9 KB (7914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fc9dd67e9904979842828a3e75301a0c379da1bb45dc75cdc2bd6631a028a32`  
		Last Modified: Wed, 02 Apr 2025 22:08:24 GMT  
		Size: 107.6 KB (107617 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fff4e9164a4259b4803c6d934508ad8476b4416d7097f2cbe68db83e91a69ab0`  
		Last Modified: Wed, 02 Apr 2025 22:08:24 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba3edaa59ccf7fe4418cc9f918ad66772163c1de22c3afd74314e1beee778bc5`  
		Last Modified: Wed, 02 Apr 2025 22:08:24 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:7ddf892427f7350fc633c5740ef8895f88d29ce3651ae3347a7ae8ed45e86fcf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.1 KB (94124 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc93f0f4d7a7ab59381d2ca94b5c48169a0eb0d534f6e06db48944a6a1cd9aef`

```dockerfile
```

-	Layers:
	-	`sha256:6dd8a7492609939d1b2f1cbf941b9c4607360ff5f25aaad3a379b6be4dde9aca`  
		Last Modified: Wed, 02 Apr 2025 22:08:24 GMT  
		Size: 79.8 KB (79822 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0122061363abb1f4f3d5cb12184c88a3d21d651f9a1aeaf7e10ac5934d6919da`  
		Last Modified: Wed, 02 Apr 2025 22:08:24 GMT  
		Size: 14.3 KB (14302 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1-alpine` - linux; arm variant v6

```console
$ docker pull spiped@sha256:022488b36873fd89f1a451ed66a2b4aed67a9ddb352d2bd608cf892376ae8972
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3463148 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33792a429e90fd9ea05a651fefc730ad65a8006e4c32639a335044afbd4c5952`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armhf.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Wed, 02 Apr 2025 21:12:22 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
RUN apk add --no-cache libssl3 # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Wed, 02 Apr 2025 21:12:22 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
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
	-	`sha256:76099982f06682e28a60c3b774ef20931d07b0a2f551203484e633d8c0361ee7`  
		Last Modified: Fri, 14 Feb 2025 18:28:03 GMT  
		Size: 3.4 MB (3364731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:066b47e1325b9f6db29d2d135e8ce6b8fcbf90a8f37138d1f3356a294928613b`  
		Last Modified: Fri, 14 Feb 2025 22:09:56 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:014f6178dbec0d9fa86b0b438929f32378f60d88338518b7952956c6aa1b5cb7`  
		Last Modified: Fri, 14 Feb 2025 22:09:56 GMT  
		Size: 7.9 KB (7917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbc93d94752878827fd3532056a9d5c692ac38ff04c63b32f88673aa8964416a`  
		Last Modified: Wed, 02 Apr 2025 21:50:27 GMT  
		Size: 89.1 KB (89120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc26ca6070e6d3cc776fbb063b850e250863b079bb9b4fedcf001b518f004387`  
		Last Modified: Wed, 02 Apr 2025 21:50:27 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb66a68852a74dbb6d6be32e7fd436e99a797bb5340892e84aacf1474567e04a`  
		Last Modified: Wed, 02 Apr 2025 21:50:27 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:8cc6f6a6d91b5f59a3cfa4d8bef00dd3556faac0bcc6400c61260c9e8730e0c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.2 KB (14186 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b8d4b9bee6645579beaf8fbe1c143f10516e131664def6ca2c559cfa1f31504`

```dockerfile
```

-	Layers:
	-	`sha256:3263ee3077e76a9dbb13eecc31527a10d5efdefe3d39ec4c458f0e1132247531`  
		Last Modified: Wed, 02 Apr 2025 21:50:26 GMT  
		Size: 14.2 KB (14186 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1-alpine` - linux; arm variant v7

```console
$ docker pull spiped@sha256:dee3984d26da4f0e8f36051324b3037dc9ccbe1860bc73d0c20cb5d580b67ec8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3189083 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14664fb61592fe16a4ad57c810d3b1649982058dd7505d05565d350c40e2ea78`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armv7.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Wed, 02 Apr 2025 21:12:22 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
RUN apk add --no-cache libssl3 # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Wed, 02 Apr 2025 21:12:22 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
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
	-	`sha256:85f3b18f9f5a8655db86c6dfb02bb01011ffef63d10a173843c5c65c3e9137b7`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.1 MB (3098123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e8fb51fad1dc40f454b85c84a615197e58cde8fdc5f21b35dc45af3c97d1fa7`  
		Last Modified: Wed, 02 Apr 2025 21:51:13 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ef3321472ab9d21d883d24b575a54b890a3e93b9b0a5b44204d21656d78680a`  
		Last Modified: Wed, 02 Apr 2025 21:51:13 GMT  
		Size: 7.9 KB (7928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:caa2395c1ed98837c525acd35fd9fdccb1a68a1b50574550c75f56789cdcefe6`  
		Last Modified: Wed, 02 Apr 2025 21:51:13 GMT  
		Size: 81.7 KB (81650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1631d9b9eaabe691dc7301f342ee863beab1cba416bc55834b0dcd64d811d52e`  
		Last Modified: Wed, 02 Apr 2025 21:51:13 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16aa8ceacc34b79b201841242c1d739910f64d43a16351ecd1b4e063785ae3d7`  
		Last Modified: Wed, 02 Apr 2025 21:51:14 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:01fc29e009708c7ec4e299f0ab229f389ceb7f44379a0e50e9c4116c11ac1887
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.3 KB (94259 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46d3a8021f9021b79e00c3aa6168baba8e1d2d75d1c2107977f5af4eaa46e39a`

```dockerfile
```

-	Layers:
	-	`sha256:44cabd4b7cd6d156567d0a5c80d300c59411572e356ff5c2bf8ddb27a1f9f941`  
		Last Modified: Wed, 02 Apr 2025 21:51:13 GMT  
		Size: 79.9 KB (79858 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:abc6d037c51e675c4900f1eaeb5150e1f382d37f0f1b0f592f7bae802181c645`  
		Last Modified: Wed, 02 Apr 2025 21:51:13 GMT  
		Size: 14.4 KB (14401 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1-alpine` - linux; arm64 variant v8

```console
$ docker pull spiped@sha256:9bf1fb1b6d22643c494712c0e64d1180ae0f262b6b8970f3e2d8dcef3fef6a57
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4102905 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb9c2bd1fb5fe20d7cbaf48186ea092dbc2d13b35d73505074e36eda2950836b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Wed, 02 Apr 2025 21:12:22 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
RUN apk add --no-cache libssl3 # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Wed, 02 Apr 2025 21:12:22 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
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
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 12:05:33 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fcfdf5e57fbe5c7d9308257021972c3c8049235b8418078c63b52659f3c141c`  
		Last Modified: Wed, 02 Apr 2025 21:51:29 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:860d1ac7e6f5ff9e4c32fa1aa64bcf81c200cb1e7e28b8d5ed59a0614cecead6`  
		Last Modified: Wed, 02 Apr 2025 21:51:30 GMT  
		Size: 7.9 KB (7920 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29683b13029a57b0b382b6e15838ae6d55e7fb4e17335eb9458398a3b28cc51c`  
		Last Modified: Wed, 02 Apr 2025 21:51:30 GMT  
		Size: 100.6 KB (100575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fcdf172b649e9fc88d25bf9587c92d962a199e6c7a0e1a98c2ec6c89c54aacb`  
		Last Modified: Wed, 02 Apr 2025 21:51:30 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52a43ba3519841070ae5d0384c94c52fc8d37791bfa6e9ad35b22b8b9702d29a`  
		Last Modified: Wed, 02 Apr 2025 21:51:31 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:43a680d67479907610aad7509796ef596f5fed0d289448130c1196039d21ded2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.3 KB (94314 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b365f16aaf205dfc1b9640897e812784f27ed48fde6a42a374087e79452d0922`

```dockerfile
```

-	Layers:
	-	`sha256:4eb7794745d2b89ac646620f0f7c4237fc16799b36487de5b5f09a981ec8188f`  
		Last Modified: Wed, 02 Apr 2025 21:51:30 GMT  
		Size: 79.9 KB (79878 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9823c97e3177ff4bc824966f8e095cc5f8a3ab0acacb35eeeea76a628c98b570`  
		Last Modified: Wed, 02 Apr 2025 21:51:30 GMT  
		Size: 14.4 KB (14436 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1-alpine` - linux; 386

```console
$ docker pull spiped@sha256:10f7aa16af762acbfb63005c00877699fa29c2e4bb04d75d1d70ec20a60f5453
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3593008 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:caa790ea4f84c7bd9a039089ae50b44f58ea302f037ea74e3b405bc3febd96b5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Wed, 02 Apr 2025 21:12:22 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
RUN apk add --no-cache libssl3 # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Wed, 02 Apr 2025 21:12:22 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
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
	-	`sha256:69aa61ccf55e5bf8e7a069b89e8afb42b4f3443b3785868795af8046d810d608`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.5 MB (3463623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13e7ff7711b41a9071a294c97e4058917e28c3c7e20059009e0b630880394156`  
		Last Modified: Wed, 02 Apr 2025 21:51:03 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ce2dc85c8b1ec7a6c1ad258c05589aa70dba5fe5290558cc0e4548d1bcdd5de`  
		Last Modified: Wed, 02 Apr 2025 21:51:03 GMT  
		Size: 7.9 KB (7913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0af8ae2ced3573d3e4de1a677b4b5a3c011895466b9c210fd74fe255cb8d77b8`  
		Last Modified: Wed, 02 Apr 2025 21:51:03 GMT  
		Size: 120.1 KB (120090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfa87e2679113a95903cfd2867ff588bcf12b0fd8ddfac21b77727f8b7d3d894`  
		Last Modified: Wed, 02 Apr 2025 21:51:03 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d22470fcb8710e32223fea8e79f0b28488b0ab51c65567241c529bd203b95215`  
		Last Modified: Wed, 02 Apr 2025 21:51:04 GMT  
		Size: 336.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:766834152c333f40d598d1f36bd56d11f810d2e19ed86d7e91571b9367515fee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.1 KB (94062 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef8983e1e4860bdae956bb8f365e0bcc2f2cf38f76ce6566d65f6937140d1443`

```dockerfile
```

-	Layers:
	-	`sha256:0344d1265ed83fac16730c24d70471283f93d11c5749243cdcf7ba8e3cf80a76`  
		Last Modified: Wed, 02 Apr 2025 21:51:03 GMT  
		Size: 79.8 KB (79797 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:de475a73cdee8c96006bf8d6c10118db82ed20c810abe06bd1dcb3b224bfaf98`  
		Last Modified: Wed, 02 Apr 2025 21:51:03 GMT  
		Size: 14.3 KB (14265 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1-alpine` - linux; ppc64le

```console
$ docker pull spiped@sha256:88487ee5729022576bc8477226c823b846fcb546e116fd1817a9b49c7a8248df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3696294 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e37765c7075b9c5e9f7aa70b2b311f8eb578373a5b127e41648ff035f02b2de`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-ppc64le.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Wed, 02 Apr 2025 21:12:22 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
RUN apk add --no-cache libssl3 # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Wed, 02 Apr 2025 21:12:22 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
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
	-	`sha256:184b14480d317057da092a0994ad6baf4b2df588108f43969f8fd56f021af2c6`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.6 MB (3574345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f29133aa5ac2dc7f7caf05bec17a3f120b130b0a9f8a931b87d42bda5e00ee7`  
		Last Modified: Wed, 02 Apr 2025 21:53:15 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ceed22f9dc598f4a83d2574a1236b9eb55845a886691ca27d260af8e52d0a5b8`  
		Last Modified: Wed, 02 Apr 2025 21:53:15 GMT  
		Size: 7.9 KB (7921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e550c947cd96d7d5dbfd565fa3ae85434cb2481820d65ac92504416d056beea9`  
		Last Modified: Wed, 02 Apr 2025 21:53:15 GMT  
		Size: 112.6 KB (112643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47cfc80ff9405d7424905e6aa74f541ec5830861bef1b1218605b7d66fcec7b9`  
		Last Modified: Wed, 02 Apr 2025 21:53:15 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b0e844805fa1d0d457d1513e5b9d92436e3ab8e65548a31fbbc18ed1c2c743b`  
		Last Modified: Wed, 02 Apr 2025 21:53:16 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:fdca1b5f72932ee6bcfc55a37feb9c860f41b530efa43e63aec701932b3cf4da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.3 KB (92255 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58422f604e757b9c7c12519d56f597a89ae27e12f2339cf2cc67b4b5a19bb384`

```dockerfile
```

-	Layers:
	-	`sha256:2df4c6cf5666abc03d36c3ff177b1360db4c2531a9cd9923b404e7ff491bec9b`  
		Last Modified: Wed, 02 Apr 2025 21:53:15 GMT  
		Size: 77.9 KB (77905 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a7ad33b282085052031ca00d32c203a26ce45455daf796d327bb6cdbdcf3e8aa`  
		Last Modified: Wed, 02 Apr 2025 21:53:15 GMT  
		Size: 14.3 KB (14350 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1-alpine` - linux; riscv64

```console
$ docker pull spiped@sha256:d93e8574bb82dd81dafcf25f7625ed7818c3a0e31066bbddf64006b83d78aba9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3459532 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11a635f525ddca22947829af6f197712b92c46682f40c9dbe63063aa381f9a9c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-riscv64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Wed, 02 Apr 2025 21:12:22 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
RUN apk add --no-cache libssl3 # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Wed, 02 Apr 2025 21:12:22 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
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
	-	`sha256:7df33f7ad8beb367ac09bdd1b2f220db3ee2bbdda14a6310d1340e5628b5ba88`  
		Last Modified: Fri, 14 Feb 2025 18:56:36 GMT  
		Size: 3.4 MB (3351439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a279c5ee271afcec6d3150e694efda4e5d36691f2d7ebe160636c0ab5a79b1ec`  
		Last Modified: Wed, 02 Apr 2025 21:53:03 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:015b70b993c8cc00dfe1e78ec875878062b451bd4ec2b326794c36444cb3105e`  
		Last Modified: Wed, 02 Apr 2025 21:53:03 GMT  
		Size: 7.9 KB (7904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87d040e2d542829d397e472ec2982c4857e357fe408f645da0693ef90321e2c7`  
		Last Modified: Wed, 02 Apr 2025 21:53:03 GMT  
		Size: 98.8 KB (98804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a0e579239e2446edd70320e6ec295380d239d0b2fb8045fbda0d7753c161f59`  
		Last Modified: Wed, 02 Apr 2025 21:53:03 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f11cda2eddc9aaf6455435d16dfafc74f718d637e59cb8c549b1310659e0f68`  
		Last Modified: Wed, 02 Apr 2025 21:53:04 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:6ef91094d879feac7520f82fdd946b0c798b74a1208a22482597eb403e08bd3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.2 KB (92248 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54c9ad713acd2272c15e5bd4e3532ba9df6910776b9db0bb063b585453f134ab`

```dockerfile
```

-	Layers:
	-	`sha256:b046cc017c3f020547f0314366d83fb03c8803458406b56bdd3904750ccb915b`  
		Last Modified: Wed, 02 Apr 2025 21:53:03 GMT  
		Size: 77.9 KB (77901 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:de0c335e4f12af3686646881008f04ba3bc438d3f15fbd38fbc3998d12514728`  
		Last Modified: Wed, 02 Apr 2025 21:53:03 GMT  
		Size: 14.3 KB (14347 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1-alpine` - linux; s390x

```console
$ docker pull spiped@sha256:8e1cc9b73ed1eb178d6d22338fc661c8f3386b5d33086e11fca8483e38bc0123
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3573772 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9100e7b9db6a61a9d6818b301afcaf1e2753a632dba5e84dbdf9ea416bfe685b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-s390x.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Wed, 02 Apr 2025 21:12:22 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
RUN apk add --no-cache libssl3 # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Wed, 02 Apr 2025 21:12:22 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
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
	-	`sha256:c1a599607158512214777614f916f8193d29fd34b656d47dfc26314af01e2af4`  
		Last Modified: Fri, 14 Feb 2025 12:05:25 GMT  
		Size: 3.5 MB (3467567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:408f712244d227bb17176b3c9833183d94d7e5078a0071c6bb815f7c6acd044b`  
		Last Modified: Wed, 02 Apr 2025 21:52:19 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce3d2b3d93cf3babc3c2c43519cfac5c89b009dddf9f6329ccb604067e1c25d0`  
		Last Modified: Wed, 02 Apr 2025 21:52:19 GMT  
		Size: 7.9 KB (7919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:924f34f1a30b83eb8fe0d105f78a3ddb08291d7062c11e0a807ca3576dd2e638`  
		Last Modified: Wed, 02 Apr 2025 21:52:19 GMT  
		Size: 96.9 KB (96901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eaa01324514a5afcdaa7ba2727d95863ff56033c4f01975371de7c453ccdf8e1`  
		Last Modified: Wed, 02 Apr 2025 21:52:19 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b3162a370a5d0aff74dea2a1ddb49f120b995ec42d4b29c7bcb3c2f10a91fc1`  
		Last Modified: Wed, 02 Apr 2025 21:52:20 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:97f9242d5c7292f0782ce10a5d3a0549df652a9380a4f408bf9ede75116a30aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.2 KB (92170 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77e792a9515a7540fa01538367eccf186ff2dd8158a7dccadf4d37f635a3679c`

```dockerfile
```

-	Layers:
	-	`sha256:7c31c769211e50a701dc70ffd6261e2d0664c6f3b50fd444ad2665b22b1d6e5c`  
		Last Modified: Wed, 02 Apr 2025 21:52:19 GMT  
		Size: 77.9 KB (77871 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4988863227d01a39c5e290493124efb4304413f32a12e6879ffda4c3a86afd0d`  
		Last Modified: Wed, 02 Apr 2025 21:52:20 GMT  
		Size: 14.3 KB (14299 bytes)  
		MIME: application/vnd.in-toto+json

## `spiped:1.6`

```console
$ docker pull spiped@sha256:eae5c3dfb8127c952913e3baabc3945915ed9fe7263a8928e60ee6f9f6c4d090
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
	-	linux; mips64le
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `spiped:1.6` - linux; amd64

```console
$ docker pull spiped@sha256:c98a4a33bc9da8d56f0d5163a75842ce1c6c2db4ab21e159b3bde195afd59adc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.1 MB (37087849 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4355dd26bbc1d77f98e7c0ac73eacf4bc8915d2d20786bfbb00b17e33f21fa17`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 02 Apr 2025 21:12:22 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1747699200'
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
	-	`sha256:61320b01ae5e0798393ef25f2dc72faf43703e60ba089b07d7170acbabbf8f62`  
		Last Modified: Wed, 21 May 2025 22:27:39 GMT  
		Size: 28.2 MB (28225330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b236b995fe25e62e0a9b025d43ed6aeb0d706dda8c314117fcf6638ebdc7e2b`  
		Last Modified: Wed, 21 May 2025 23:20:12 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe7a90816c2d64d22fdbae87a108eb3343157d21eabfdd8a0362fb7c337c99ab`  
		Last Modified: Wed, 21 May 2025 23:20:12 GMT  
		Size: 2.4 MB (2402177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e20521234d5fd2df1eb25c23579bae7d5636fcce182618943e02ef5ab794963`  
		Last Modified: Wed, 21 May 2025 23:20:12 GMT  
		Size: 6.5 MB (6458802 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8c3b16ce6622a837772fdf6d18fc84b976e8694098211b2e9a4383a62931558`  
		Last Modified: Wed, 21 May 2025 23:20:12 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75351b1571732d8e2e27dfde274116dd0037459b25301366b27c9402ede4aae3`  
		Last Modified: Wed, 21 May 2025 23:20:13 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6` - unknown; unknown

```console
$ docker pull spiped@sha256:38fba8cf5966d1da5219266d88064e3aaceb887d32420638d2f0135dbbfd4ca5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3553217 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d442efde223bd171e1f3b5bdd7d6301e1ce2df0c1ea291f621d582ff0136ad75`

```dockerfile
```

-	Layers:
	-	`sha256:0c32ff8bf0f89bea9948bda0ad2c06ecc23437d5eefe99e0003e3c0eae7be3a8`  
		Last Modified: Wed, 21 May 2025 23:20:12 GMT  
		Size: 3.5 MB (3538177 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:faed6139c10365db1a206a064e87b5765026aa41bba89ab1a43fbcf5befd26ce`  
		Last Modified: Wed, 21 May 2025 23:20:12 GMT  
		Size: 15.0 KB (15040 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6` - linux; arm variant v5

```console
$ docker pull spiped@sha256:799111c4807c2fea831489b691e498f914d9a30c2f65688bf798574eec5db8c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.9 MB (32904241 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f9e5e8afcac44ab7363c93359b12a1c8dfb1867ed4df01c19777a222ce48c0f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 02 Apr 2025 21:12:22 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1747699200'
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
	-	`sha256:fab452a77ecb21a2e30922ab3eed19310b6d56763bcfc4e4bd31f28d9747f745`  
		Last Modified: Wed, 21 May 2025 22:27:58 GMT  
		Size: 25.8 MB (25756898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf5fcb13f4fae5c0701ae97175c1fde5a265e39ab7420ed78e63dc654b097e65`  
		Last Modified: Thu, 22 May 2025 01:12:54 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9556b3c226c521d39ced715dacdb0ddd196bf05f5846d3732d60e8a3f55a1de`  
		Last Modified: Thu, 22 May 2025 01:12:54 GMT  
		Size: 2.0 MB (1998268 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce40ec37f30dc6d7d5a1ed74cf1f1bae7f1a05eb87b99e62d9b4c27a28051931`  
		Last Modified: Thu, 22 May 2025 01:12:55 GMT  
		Size: 5.1 MB (5147533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4b23094f6c0b0b7beabfe549bc26fad9124341fe7251635a2286ad9d50c488e`  
		Last Modified: Thu, 22 May 2025 01:12:54 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f314f72e5ab08b9522e8df48d487f9c5448dd07a3c496be756e549d855a92e7c`  
		Last Modified: Thu, 22 May 2025 01:12:55 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6` - unknown; unknown

```console
$ docker pull spiped@sha256:9cf2a6d75f36284a1051b375e26316cc1e1a134adaff1f248a8d390552e88dd5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3524157 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3a141429766668432eef187e965dabf4459daabd05cb999129f21ee65ed20c6`

```dockerfile
```

-	Layers:
	-	`sha256:6a32a05c66630aa10a22096368b76df8bd67aaf342c8dd930619b45a1888cbc4`  
		Last Modified: Thu, 22 May 2025 01:12:54 GMT  
		Size: 3.5 MB (3509015 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:41b70d9c48c2c437462d07be8fc990b465281e5c418124d21004a253d959aa18`  
		Last Modified: Thu, 22 May 2025 01:12:54 GMT  
		Size: 15.1 KB (15142 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6` - linux; arm variant v7

```console
$ docker pull spiped@sha256:bd88168940017d415031d65c8b562a450fb598c60cf7e38ede2eebc4e622eed3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.7 MB (30679570 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:334bd5bd9fc6f29c24ec13b8cda836e7cb1c5e76c363b01a5ae63808e03e7cf0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 02 Apr 2025 21:12:22 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1747699200'
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
	-	`sha256:3726bc5cceb817ddfc7c2e1dbdfb4900fc6e27b680d63b8d751b06952753b6a1`  
		Last Modified: Wed, 21 May 2025 22:27:58 GMT  
		Size: 23.9 MB (23932922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28497644b53abef7026a25140f5b20b9e5f984102c735a18f9ad13b06d325d06`  
		Last Modified: Thu, 22 May 2025 02:11:46 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c06616ca963aeb60b1926e7a4505f5587eb632014d17e10775734237f64bfdd5`  
		Last Modified: Thu, 22 May 2025 02:11:46 GMT  
		Size: 1.9 MB (1856406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0454a735cab512a3994c19f6461e13b792aa7d4ae6f2f7b7beefad87c86e1619`  
		Last Modified: Thu, 22 May 2025 02:11:46 GMT  
		Size: 4.9 MB (4888699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c30c741ba1d6aa6d7e8a8bb49b3f73d5cfc41cc58cc9f1ee0d0222ef1eb61e3`  
		Last Modified: Thu, 22 May 2025 02:11:46 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efa2405c063638356b662a29deb560323db64a04302d8fb7b4e41e40832595be`  
		Last Modified: Thu, 22 May 2025 02:11:47 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6` - unknown; unknown

```console
$ docker pull spiped@sha256:67903915b9908ceec6eff9982d5e47b52aed66b921141fb35e158bef999cc642
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3523340 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e202a4f6c6a60f84bb42ff7184ed9b6fc409d848ff7be381fd3aeecfd2229b7e`

```dockerfile
```

-	Layers:
	-	`sha256:798416b4b99780fb82d37f69a61f55757da43446999fd396b2345a89f61b9717`  
		Last Modified: Thu, 22 May 2025 02:11:46 GMT  
		Size: 3.5 MB (3508198 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:16fe3f5accbcda69a4f3d2d1a7e95d1755dbdf53436e1dafd5996ebc9dc0ebda`  
		Last Modified: Thu, 22 May 2025 02:11:46 GMT  
		Size: 15.1 KB (15142 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6` - linux; arm64 variant v8

```console
$ docker pull spiped@sha256:d5cafb803c9a0da7ab4771f49d9cdb8a8cdcb3ff719bcbb09e016d458b52edae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.8 MB (35805923 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4433b4b2209f95a137ec9d4fc3da9f0399b1a927010b07100f4d2cb33f01eec6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 02 Apr 2025 21:12:22 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1747699200'
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
	-	`sha256:b16f1b16678093d11ecfece1004207a40f9bc1b7d9d1d16a070c1db552038818`  
		Last Modified: Wed, 21 May 2025 22:27:55 GMT  
		Size: 28.1 MB (28065280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58d7aa0e5553a8e1676ebb9a1e8b4e211d5e24d00e206dd06e9dc931036210a8`  
		Last Modified: Thu, 22 May 2025 02:26:31 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b01b22375091a64a96ee1ad4e57158b3b3a3403ba79cab1a56af7fcaf2c4fd4b`  
		Last Modified: Thu, 22 May 2025 02:26:32 GMT  
		Size: 2.2 MB (2247441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cf33c8dbe86b945cd509593f45ace969c1839a8dee7d1828092b41632af9837`  
		Last Modified: Thu, 22 May 2025 02:26:32 GMT  
		Size: 5.5 MB (5491661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa6e1ae6c666fd43ad0bb5cbd1d595c4f6774a7621a81e94f751dba1447227a4`  
		Last Modified: Thu, 22 May 2025 02:26:32 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25be54df2c26151d78b7c6bcc8b71f10a49ca87573849bc5561334e83d854f56`  
		Last Modified: Thu, 22 May 2025 02:26:33 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6` - unknown; unknown

```console
$ docker pull spiped@sha256:76bf26d851cd8fc562b888569d70024625766d5c1b77df5d31a5d5045d909e7a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3524578 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:232fb12c6174ddf70b733574174d96ac46893cfd76e8ecaf5a3d2a2d55139191`

```dockerfile
```

-	Layers:
	-	`sha256:863430707bd172ac83c08ecfc72f18ec0a9e85de22d979a70542342ba06ead69`  
		Last Modified: Thu, 22 May 2025 02:26:32 GMT  
		Size: 3.5 MB (3509405 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cc3c4313ab583feefd96c652f06140e88ab6b676b233c9b4c5ead13c712d32ce`  
		Last Modified: Thu, 22 May 2025 02:26:31 GMT  
		Size: 15.2 KB (15173 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6` - linux; 386

```console
$ docker pull spiped@sha256:de2d0f62127be81d4c417ee09c2e83dcc650d781e485052c53b4d83e7e41c305
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.6 MB (37566353 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e29b46d435dc73b21b5f638b8b87840b502cba5421b87b459851dd558cbb504`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 02 Apr 2025 21:12:22 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1747699200'
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
	-	`sha256:7d0eb60defa1a32d12e94bc0d7c2c578881c578aeec0c1d786ef5a19c72a34ab`  
		Last Modified: Wed, 21 May 2025 22:27:56 GMT  
		Size: 29.2 MB (29207487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fc34ae407ddfd8aa872313e98808f6d037d29874d733022ebeb03c21b075b9d`  
		Last Modified: Wed, 21 May 2025 23:19:31 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea1121e956c060196b27bf2cb1c7c4834fd0683b4d013d49729246105637c7e6`  
		Last Modified: Wed, 21 May 2025 23:19:31 GMT  
		Size: 2.4 MB (2400579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58c083d4e9d3c172b7e2dff742a55d190d7deea62d62e77c68be78ebe005756f`  
		Last Modified: Wed, 21 May 2025 23:19:31 GMT  
		Size: 6.0 MB (5956747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95924c7d3bb09f7d740e28a65b589259ca71ed83b9907221ab77e5710964fa84`  
		Last Modified: Wed, 21 May 2025 23:19:31 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af2e19c16d9e608f72faf9f7145bd18f20be31aa8254201cdc30e14098b0ab90`  
		Last Modified: Wed, 21 May 2025 23:19:32 GMT  
		Size: 336.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6` - unknown; unknown

```console
$ docker pull spiped@sha256:0e4e1e2182c7414a91dbedc4eee31dc2f23267ca32cb3bc1d1af586c79a15511
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3547159 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:488c249ee13b017bc6d2db92c2455dddf8636b7f8dda1f17d1c32ad46e3f1bc3`

```dockerfile
```

-	Layers:
	-	`sha256:5a933c5783118b861dc28e67218f04f000686e48be72186367702865e0819555`  
		Last Modified: Wed, 21 May 2025 23:19:31 GMT  
		Size: 3.5 MB (3532156 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a135b975223fb9944b6870b3f284f6d0e1276e5223c8b3790aec5292925ac030`  
		Last Modified: Wed, 21 May 2025 23:19:31 GMT  
		Size: 15.0 KB (15003 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6` - linux; mips64le

```console
$ docker pull spiped@sha256:e08a5f574ff6e4c4889083b74ad49f5f1fa5c4909a77fd7f0118f9e4537b2f64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.2 MB (36169243 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81d9271e2536f4b9e06788180f5f1808dc6e92f6183d5cf57c5ac1f4a073b894`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 02 Apr 2025 21:12:22 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1747699200'
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
	-	`sha256:48541e37cd82678078df221c38fde515e820c13a623449b699d224f60f15dae8`  
		Last Modified: Wed, 21 May 2025 22:28:22 GMT  
		Size: 28.5 MB (28511850 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3803a240d8e659370e2fab860baf71e6845bb1657afea9964a9455a06816584f`  
		Last Modified: Thu, 22 May 2025 06:14:35 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:058aa8bad24612579286f5eae085472a3a9f63436aa5165ce779f2d1f73c9e99`  
		Last Modified: Thu, 22 May 2025 06:14:36 GMT  
		Size: 1.8 MB (1842259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60712b0a5b50c33b45964a94fca078484dff5c1bc25928f8b19642a8fdddc723`  
		Last Modified: Thu, 22 May 2025 06:14:36 GMT  
		Size: 5.8 MB (5813592 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f03381e56cdea6e5c69ba962656f3b8ee6708f99bbbe90c8cb59805dec2821f`  
		Last Modified: Thu, 22 May 2025 06:14:35 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0030e45312f412d88429defd5484aa7c1354487911afb2c33273fd71e177e9ed`  
		Last Modified: Thu, 22 May 2025 06:14:36 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6` - unknown; unknown

```console
$ docker pull spiped@sha256:376d3c3cf802ddebdca18c0302bdc8f66c2a6eb3b23346b26c5205f7932dcce1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 KB (14897 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90459617b1bb9aa0a1d2cf5c37b8ad8d23c16eb4f14aacb08afabd9b233b117f`

```dockerfile
```

-	Layers:
	-	`sha256:307900282127ed9322c5ccab5de1df5096b6a0b07bd4395c5b9cb9b8599934bc`  
		Last Modified: Thu, 22 May 2025 06:14:35 GMT  
		Size: 14.9 KB (14897 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6` - linux; ppc64le

```console
$ docker pull spiped@sha256:a7321ff5fec2afbb779a0acf6da6d63f5c5d332938ad6bf260c611ae4a5b1c06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.1 MB (41093723 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15a62507992ef6fb0e12abeb88eb5ecf00ad31cb2d3eb2e89b8f8f14130d29e6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 02 Apr 2025 21:12:22 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1747699200'
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
	-	`sha256:701606535a7233566815cc9ad5f3e5853b443be5476286f6799008053dc2b03b`  
		Last Modified: Wed, 21 May 2025 22:28:16 GMT  
		Size: 32.1 MB (32066912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28a6c81eea611329e12a0cc8737d8ee2c5ada1b8e3aaef98d8acd2741b37d917`  
		Last Modified: Thu, 22 May 2025 07:17:33 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0fc1affdf757c274e7e67536481196cb883110fb5bfd979782fb8383777bfa6`  
		Last Modified: Thu, 22 May 2025 07:17:33 GMT  
		Size: 2.6 MB (2583887 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4db9a308ee6bef1c8241a16cb77c39894f524896d99e85f384dd7eb7a4756ff1`  
		Last Modified: Thu, 22 May 2025 07:17:33 GMT  
		Size: 6.4 MB (6441381 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c37f165cfd98289d815cf96acad45a8ed3cd5f2558537aebefbb0c7c359d0f9e`  
		Last Modified: Thu, 22 May 2025 07:17:33 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f805d8994580dac40f982b71b4ae42685005eeb1438bd76e132c9307532dedd`  
		Last Modified: Thu, 22 May 2025 07:17:34 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6` - unknown; unknown

```console
$ docker pull spiped@sha256:1cfcf23833ca373cc8000f5f9998d74ccf00ecca9ad0fb786e5172d2fcfd39af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3539050 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:789d0ff26873a3c16d1516a64b5521540d3e27924324dd582fbed08e96e970a9`

```dockerfile
```

-	Layers:
	-	`sha256:8b1a9eceb4ec95f4f5b6806a7ec405ea988499e1a2ec48b26ff0ede6b066b2a4`  
		Last Modified: Thu, 22 May 2025 07:17:33 GMT  
		Size: 3.5 MB (3523962 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ae9055586249d83d4bc0597f9cd6f6a21d3b9bf8c399b22bc90d82eed114d347`  
		Last Modified: Thu, 22 May 2025 07:17:33 GMT  
		Size: 15.1 KB (15088 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6` - linux; s390x

```console
$ docker pull spiped@sha256:313c5fbddb0f36164ff9ff07b8afb014aae1fba0aded0128c2058a6960b944dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.3 MB (34345786 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be0c786c61c197ff161771dfba4eecaca2e88d0ad743f2abe498c7758f082708`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 02 Apr 2025 21:12:22 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1747699200'
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
	-	`sha256:fb6e196ef379785f6b759a20e90d74fe0566b240771695f724c27a44aa6cd3ce`  
		Last Modified: Wed, 21 May 2025 22:28:38 GMT  
		Size: 26.9 MB (26882808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38ceb32ec1a8749e974fe5929ea6dff22bcee11dafd2fc667579323da38876f1`  
		Last Modified: Thu, 22 May 2025 00:53:41 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2f56657b11e71e77f7914f81ccb09da12e157355a9c2bfa3ad990780f7ee481`  
		Last Modified: Thu, 22 May 2025 00:53:41 GMT  
		Size: 2.1 MB (2069161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d37a680b670b7565d1e108f473912336f74759acbde356e1baffcebb55ab778`  
		Last Modified: Thu, 22 May 2025 00:53:41 GMT  
		Size: 5.4 MB (5392277 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec75588e715a05902adcfb5629f1851cf0d29ddf5ae3f281b75fdc0a40e98fb6`  
		Last Modified: Thu, 22 May 2025 00:53:41 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0e2d58562f243d49496f4f3e52abfbea3ebecc55c6401ecd80a648029bac830`  
		Last Modified: Thu, 22 May 2025 00:53:42 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6` - unknown; unknown

```console
$ docker pull spiped@sha256:5de6955b949dbe4e3cd91755329d2cb433e60f90fb15863b8bbab4c4f414cd9d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3541403 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d51372649bab5e76ddd19982bc703b786c8dc5b940231eeb5b6fa54327a2e1d`

```dockerfile
```

-	Layers:
	-	`sha256:7ddaee20724beee644d4580292cd7c349e170f436b4a509a76ba3ecb3b2337e0`  
		Last Modified: Thu, 22 May 2025 00:53:41 GMT  
		Size: 3.5 MB (3526363 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0371bae7cc54c2d437162fb10d62d7bc577205878fe8e5d855cbf8030eb4ca81`  
		Last Modified: Thu, 22 May 2025 00:53:41 GMT  
		Size: 15.0 KB (15040 bytes)  
		MIME: application/vnd.in-toto+json

## `spiped:1.6-alpine`

```console
$ docker pull spiped@sha256:19cab0821b57af25c5e04f34834de199acba4d5a909887ce0f093a3200c51243
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
$ docker pull spiped@sha256:622df849c8857cb4538c0b252cf0b5e94d10a2b5af1222af4d54ce9016270049
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3759161 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83432e0291e920e3ef7ce3c7690aba0f53cf7250e10452315d154dccfe1df29f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Wed, 02 Apr 2025 21:12:22 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
RUN apk add --no-cache libssl3 # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Wed, 02 Apr 2025 21:12:22 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
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
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 12:05:35 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:114b63918a29534fea2f0cc34ca9459cf360301d5cc6e425a943254bd857bdfd`  
		Last Modified: Wed, 02 Apr 2025 22:08:24 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4e3893b92c8e046b61bf235250bedbecb6eca134316b11bfb15c8cd1b337f3d`  
		Last Modified: Wed, 02 Apr 2025 22:08:24 GMT  
		Size: 7.9 KB (7914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fc9dd67e9904979842828a3e75301a0c379da1bb45dc75cdc2bd6631a028a32`  
		Last Modified: Wed, 02 Apr 2025 22:08:24 GMT  
		Size: 107.6 KB (107617 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fff4e9164a4259b4803c6d934508ad8476b4416d7097f2cbe68db83e91a69ab0`  
		Last Modified: Wed, 02 Apr 2025 22:08:24 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba3edaa59ccf7fe4418cc9f918ad66772163c1de22c3afd74314e1beee778bc5`  
		Last Modified: Wed, 02 Apr 2025 22:08:24 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:7ddf892427f7350fc633c5740ef8895f88d29ce3651ae3347a7ae8ed45e86fcf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.1 KB (94124 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc93f0f4d7a7ab59381d2ca94b5c48169a0eb0d534f6e06db48944a6a1cd9aef`

```dockerfile
```

-	Layers:
	-	`sha256:6dd8a7492609939d1b2f1cbf941b9c4607360ff5f25aaad3a379b6be4dde9aca`  
		Last Modified: Wed, 02 Apr 2025 22:08:24 GMT  
		Size: 79.8 KB (79822 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0122061363abb1f4f3d5cb12184c88a3d21d651f9a1aeaf7e10ac5934d6919da`  
		Last Modified: Wed, 02 Apr 2025 22:08:24 GMT  
		Size: 14.3 KB (14302 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6-alpine` - linux; arm variant v6

```console
$ docker pull spiped@sha256:022488b36873fd89f1a451ed66a2b4aed67a9ddb352d2bd608cf892376ae8972
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3463148 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33792a429e90fd9ea05a651fefc730ad65a8006e4c32639a335044afbd4c5952`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armhf.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Wed, 02 Apr 2025 21:12:22 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
RUN apk add --no-cache libssl3 # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Wed, 02 Apr 2025 21:12:22 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
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
	-	`sha256:76099982f06682e28a60c3b774ef20931d07b0a2f551203484e633d8c0361ee7`  
		Last Modified: Fri, 14 Feb 2025 18:28:03 GMT  
		Size: 3.4 MB (3364731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:066b47e1325b9f6db29d2d135e8ce6b8fcbf90a8f37138d1f3356a294928613b`  
		Last Modified: Fri, 14 Feb 2025 22:09:56 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:014f6178dbec0d9fa86b0b438929f32378f60d88338518b7952956c6aa1b5cb7`  
		Last Modified: Fri, 14 Feb 2025 22:09:56 GMT  
		Size: 7.9 KB (7917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbc93d94752878827fd3532056a9d5c692ac38ff04c63b32f88673aa8964416a`  
		Last Modified: Wed, 02 Apr 2025 21:50:27 GMT  
		Size: 89.1 KB (89120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc26ca6070e6d3cc776fbb063b850e250863b079bb9b4fedcf001b518f004387`  
		Last Modified: Wed, 02 Apr 2025 21:50:27 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb66a68852a74dbb6d6be32e7fd436e99a797bb5340892e84aacf1474567e04a`  
		Last Modified: Wed, 02 Apr 2025 21:50:27 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:8cc6f6a6d91b5f59a3cfa4d8bef00dd3556faac0bcc6400c61260c9e8730e0c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.2 KB (14186 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b8d4b9bee6645579beaf8fbe1c143f10516e131664def6ca2c559cfa1f31504`

```dockerfile
```

-	Layers:
	-	`sha256:3263ee3077e76a9dbb13eecc31527a10d5efdefe3d39ec4c458f0e1132247531`  
		Last Modified: Wed, 02 Apr 2025 21:50:26 GMT  
		Size: 14.2 KB (14186 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6-alpine` - linux; arm variant v7

```console
$ docker pull spiped@sha256:dee3984d26da4f0e8f36051324b3037dc9ccbe1860bc73d0c20cb5d580b67ec8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3189083 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14664fb61592fe16a4ad57c810d3b1649982058dd7505d05565d350c40e2ea78`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armv7.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Wed, 02 Apr 2025 21:12:22 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
RUN apk add --no-cache libssl3 # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Wed, 02 Apr 2025 21:12:22 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
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
	-	`sha256:85f3b18f9f5a8655db86c6dfb02bb01011ffef63d10a173843c5c65c3e9137b7`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.1 MB (3098123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e8fb51fad1dc40f454b85c84a615197e58cde8fdc5f21b35dc45af3c97d1fa7`  
		Last Modified: Wed, 02 Apr 2025 21:51:13 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ef3321472ab9d21d883d24b575a54b890a3e93b9b0a5b44204d21656d78680a`  
		Last Modified: Wed, 02 Apr 2025 21:51:13 GMT  
		Size: 7.9 KB (7928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:caa2395c1ed98837c525acd35fd9fdccb1a68a1b50574550c75f56789cdcefe6`  
		Last Modified: Wed, 02 Apr 2025 21:51:13 GMT  
		Size: 81.7 KB (81650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1631d9b9eaabe691dc7301f342ee863beab1cba416bc55834b0dcd64d811d52e`  
		Last Modified: Wed, 02 Apr 2025 21:51:13 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16aa8ceacc34b79b201841242c1d739910f64d43a16351ecd1b4e063785ae3d7`  
		Last Modified: Wed, 02 Apr 2025 21:51:14 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:01fc29e009708c7ec4e299f0ab229f389ceb7f44379a0e50e9c4116c11ac1887
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.3 KB (94259 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46d3a8021f9021b79e00c3aa6168baba8e1d2d75d1c2107977f5af4eaa46e39a`

```dockerfile
```

-	Layers:
	-	`sha256:44cabd4b7cd6d156567d0a5c80d300c59411572e356ff5c2bf8ddb27a1f9f941`  
		Last Modified: Wed, 02 Apr 2025 21:51:13 GMT  
		Size: 79.9 KB (79858 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:abc6d037c51e675c4900f1eaeb5150e1f382d37f0f1b0f592f7bae802181c645`  
		Last Modified: Wed, 02 Apr 2025 21:51:13 GMT  
		Size: 14.4 KB (14401 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6-alpine` - linux; arm64 variant v8

```console
$ docker pull spiped@sha256:9bf1fb1b6d22643c494712c0e64d1180ae0f262b6b8970f3e2d8dcef3fef6a57
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4102905 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb9c2bd1fb5fe20d7cbaf48186ea092dbc2d13b35d73505074e36eda2950836b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Wed, 02 Apr 2025 21:12:22 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
RUN apk add --no-cache libssl3 # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Wed, 02 Apr 2025 21:12:22 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
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
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 12:05:33 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fcfdf5e57fbe5c7d9308257021972c3c8049235b8418078c63b52659f3c141c`  
		Last Modified: Wed, 02 Apr 2025 21:51:29 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:860d1ac7e6f5ff9e4c32fa1aa64bcf81c200cb1e7e28b8d5ed59a0614cecead6`  
		Last Modified: Wed, 02 Apr 2025 21:51:30 GMT  
		Size: 7.9 KB (7920 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29683b13029a57b0b382b6e15838ae6d55e7fb4e17335eb9458398a3b28cc51c`  
		Last Modified: Wed, 02 Apr 2025 21:51:30 GMT  
		Size: 100.6 KB (100575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fcdf172b649e9fc88d25bf9587c92d962a199e6c7a0e1a98c2ec6c89c54aacb`  
		Last Modified: Wed, 02 Apr 2025 21:51:30 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52a43ba3519841070ae5d0384c94c52fc8d37791bfa6e9ad35b22b8b9702d29a`  
		Last Modified: Wed, 02 Apr 2025 21:51:31 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:43a680d67479907610aad7509796ef596f5fed0d289448130c1196039d21ded2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.3 KB (94314 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b365f16aaf205dfc1b9640897e812784f27ed48fde6a42a374087e79452d0922`

```dockerfile
```

-	Layers:
	-	`sha256:4eb7794745d2b89ac646620f0f7c4237fc16799b36487de5b5f09a981ec8188f`  
		Last Modified: Wed, 02 Apr 2025 21:51:30 GMT  
		Size: 79.9 KB (79878 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9823c97e3177ff4bc824966f8e095cc5f8a3ab0acacb35eeeea76a628c98b570`  
		Last Modified: Wed, 02 Apr 2025 21:51:30 GMT  
		Size: 14.4 KB (14436 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6-alpine` - linux; 386

```console
$ docker pull spiped@sha256:10f7aa16af762acbfb63005c00877699fa29c2e4bb04d75d1d70ec20a60f5453
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3593008 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:caa790ea4f84c7bd9a039089ae50b44f58ea302f037ea74e3b405bc3febd96b5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Wed, 02 Apr 2025 21:12:22 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
RUN apk add --no-cache libssl3 # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Wed, 02 Apr 2025 21:12:22 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
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
	-	`sha256:69aa61ccf55e5bf8e7a069b89e8afb42b4f3443b3785868795af8046d810d608`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.5 MB (3463623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13e7ff7711b41a9071a294c97e4058917e28c3c7e20059009e0b630880394156`  
		Last Modified: Wed, 02 Apr 2025 21:51:03 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ce2dc85c8b1ec7a6c1ad258c05589aa70dba5fe5290558cc0e4548d1bcdd5de`  
		Last Modified: Wed, 02 Apr 2025 21:51:03 GMT  
		Size: 7.9 KB (7913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0af8ae2ced3573d3e4de1a677b4b5a3c011895466b9c210fd74fe255cb8d77b8`  
		Last Modified: Wed, 02 Apr 2025 21:51:03 GMT  
		Size: 120.1 KB (120090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfa87e2679113a95903cfd2867ff588bcf12b0fd8ddfac21b77727f8b7d3d894`  
		Last Modified: Wed, 02 Apr 2025 21:51:03 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d22470fcb8710e32223fea8e79f0b28488b0ab51c65567241c529bd203b95215`  
		Last Modified: Wed, 02 Apr 2025 21:51:04 GMT  
		Size: 336.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:766834152c333f40d598d1f36bd56d11f810d2e19ed86d7e91571b9367515fee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.1 KB (94062 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef8983e1e4860bdae956bb8f365e0bcc2f2cf38f76ce6566d65f6937140d1443`

```dockerfile
```

-	Layers:
	-	`sha256:0344d1265ed83fac16730c24d70471283f93d11c5749243cdcf7ba8e3cf80a76`  
		Last Modified: Wed, 02 Apr 2025 21:51:03 GMT  
		Size: 79.8 KB (79797 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:de475a73cdee8c96006bf8d6c10118db82ed20c810abe06bd1dcb3b224bfaf98`  
		Last Modified: Wed, 02 Apr 2025 21:51:03 GMT  
		Size: 14.3 KB (14265 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6-alpine` - linux; ppc64le

```console
$ docker pull spiped@sha256:88487ee5729022576bc8477226c823b846fcb546e116fd1817a9b49c7a8248df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3696294 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e37765c7075b9c5e9f7aa70b2b311f8eb578373a5b127e41648ff035f02b2de`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-ppc64le.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Wed, 02 Apr 2025 21:12:22 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
RUN apk add --no-cache libssl3 # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Wed, 02 Apr 2025 21:12:22 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
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
	-	`sha256:184b14480d317057da092a0994ad6baf4b2df588108f43969f8fd56f021af2c6`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.6 MB (3574345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f29133aa5ac2dc7f7caf05bec17a3f120b130b0a9f8a931b87d42bda5e00ee7`  
		Last Modified: Wed, 02 Apr 2025 21:53:15 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ceed22f9dc598f4a83d2574a1236b9eb55845a886691ca27d260af8e52d0a5b8`  
		Last Modified: Wed, 02 Apr 2025 21:53:15 GMT  
		Size: 7.9 KB (7921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e550c947cd96d7d5dbfd565fa3ae85434cb2481820d65ac92504416d056beea9`  
		Last Modified: Wed, 02 Apr 2025 21:53:15 GMT  
		Size: 112.6 KB (112643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47cfc80ff9405d7424905e6aa74f541ec5830861bef1b1218605b7d66fcec7b9`  
		Last Modified: Wed, 02 Apr 2025 21:53:15 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b0e844805fa1d0d457d1513e5b9d92436e3ab8e65548a31fbbc18ed1c2c743b`  
		Last Modified: Wed, 02 Apr 2025 21:53:16 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:fdca1b5f72932ee6bcfc55a37feb9c860f41b530efa43e63aec701932b3cf4da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.3 KB (92255 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58422f604e757b9c7c12519d56f597a89ae27e12f2339cf2cc67b4b5a19bb384`

```dockerfile
```

-	Layers:
	-	`sha256:2df4c6cf5666abc03d36c3ff177b1360db4c2531a9cd9923b404e7ff491bec9b`  
		Last Modified: Wed, 02 Apr 2025 21:53:15 GMT  
		Size: 77.9 KB (77905 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a7ad33b282085052031ca00d32c203a26ce45455daf796d327bb6cdbdcf3e8aa`  
		Last Modified: Wed, 02 Apr 2025 21:53:15 GMT  
		Size: 14.3 KB (14350 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6-alpine` - linux; riscv64

```console
$ docker pull spiped@sha256:d93e8574bb82dd81dafcf25f7625ed7818c3a0e31066bbddf64006b83d78aba9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3459532 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11a635f525ddca22947829af6f197712b92c46682f40c9dbe63063aa381f9a9c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-riscv64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Wed, 02 Apr 2025 21:12:22 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
RUN apk add --no-cache libssl3 # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Wed, 02 Apr 2025 21:12:22 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
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
	-	`sha256:7df33f7ad8beb367ac09bdd1b2f220db3ee2bbdda14a6310d1340e5628b5ba88`  
		Last Modified: Fri, 14 Feb 2025 18:56:36 GMT  
		Size: 3.4 MB (3351439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a279c5ee271afcec6d3150e694efda4e5d36691f2d7ebe160636c0ab5a79b1ec`  
		Last Modified: Wed, 02 Apr 2025 21:53:03 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:015b70b993c8cc00dfe1e78ec875878062b451bd4ec2b326794c36444cb3105e`  
		Last Modified: Wed, 02 Apr 2025 21:53:03 GMT  
		Size: 7.9 KB (7904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87d040e2d542829d397e472ec2982c4857e357fe408f645da0693ef90321e2c7`  
		Last Modified: Wed, 02 Apr 2025 21:53:03 GMT  
		Size: 98.8 KB (98804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a0e579239e2446edd70320e6ec295380d239d0b2fb8045fbda0d7753c161f59`  
		Last Modified: Wed, 02 Apr 2025 21:53:03 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f11cda2eddc9aaf6455435d16dfafc74f718d637e59cb8c549b1310659e0f68`  
		Last Modified: Wed, 02 Apr 2025 21:53:04 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:6ef91094d879feac7520f82fdd946b0c798b74a1208a22482597eb403e08bd3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.2 KB (92248 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54c9ad713acd2272c15e5bd4e3532ba9df6910776b9db0bb063b585453f134ab`

```dockerfile
```

-	Layers:
	-	`sha256:b046cc017c3f020547f0314366d83fb03c8803458406b56bdd3904750ccb915b`  
		Last Modified: Wed, 02 Apr 2025 21:53:03 GMT  
		Size: 77.9 KB (77901 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:de0c335e4f12af3686646881008f04ba3bc438d3f15fbd38fbc3998d12514728`  
		Last Modified: Wed, 02 Apr 2025 21:53:03 GMT  
		Size: 14.3 KB (14347 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6-alpine` - linux; s390x

```console
$ docker pull spiped@sha256:8e1cc9b73ed1eb178d6d22338fc661c8f3386b5d33086e11fca8483e38bc0123
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3573772 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9100e7b9db6a61a9d6818b301afcaf1e2753a632dba5e84dbdf9ea416bfe685b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-s390x.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Wed, 02 Apr 2025 21:12:22 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
RUN apk add --no-cache libssl3 # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Wed, 02 Apr 2025 21:12:22 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
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
	-	`sha256:c1a599607158512214777614f916f8193d29fd34b656d47dfc26314af01e2af4`  
		Last Modified: Fri, 14 Feb 2025 12:05:25 GMT  
		Size: 3.5 MB (3467567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:408f712244d227bb17176b3c9833183d94d7e5078a0071c6bb815f7c6acd044b`  
		Last Modified: Wed, 02 Apr 2025 21:52:19 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce3d2b3d93cf3babc3c2c43519cfac5c89b009dddf9f6329ccb604067e1c25d0`  
		Last Modified: Wed, 02 Apr 2025 21:52:19 GMT  
		Size: 7.9 KB (7919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:924f34f1a30b83eb8fe0d105f78a3ddb08291d7062c11e0a807ca3576dd2e638`  
		Last Modified: Wed, 02 Apr 2025 21:52:19 GMT  
		Size: 96.9 KB (96901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eaa01324514a5afcdaa7ba2727d95863ff56033c4f01975371de7c453ccdf8e1`  
		Last Modified: Wed, 02 Apr 2025 21:52:19 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b3162a370a5d0aff74dea2a1ddb49f120b995ec42d4b29c7bcb3c2f10a91fc1`  
		Last Modified: Wed, 02 Apr 2025 21:52:20 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:97f9242d5c7292f0782ce10a5d3a0549df652a9380a4f408bf9ede75116a30aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.2 KB (92170 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77e792a9515a7540fa01538367eccf186ff2dd8158a7dccadf4d37f635a3679c`

```dockerfile
```

-	Layers:
	-	`sha256:7c31c769211e50a701dc70ffd6261e2d0664c6f3b50fd444ad2665b22b1d6e5c`  
		Last Modified: Wed, 02 Apr 2025 21:52:19 GMT  
		Size: 77.9 KB (77871 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4988863227d01a39c5e290493124efb4304413f32a12e6879ffda4c3a86afd0d`  
		Last Modified: Wed, 02 Apr 2025 21:52:20 GMT  
		Size: 14.3 KB (14299 bytes)  
		MIME: application/vnd.in-toto+json

## `spiped:1.6.4`

```console
$ docker pull spiped@sha256:eae5c3dfb8127c952913e3baabc3945915ed9fe7263a8928e60ee6f9f6c4d090
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
	-	linux; mips64le
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `spiped:1.6.4` - linux; amd64

```console
$ docker pull spiped@sha256:c98a4a33bc9da8d56f0d5163a75842ce1c6c2db4ab21e159b3bde195afd59adc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.1 MB (37087849 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4355dd26bbc1d77f98e7c0ac73eacf4bc8915d2d20786bfbb00b17e33f21fa17`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 02 Apr 2025 21:12:22 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1747699200'
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
	-	`sha256:61320b01ae5e0798393ef25f2dc72faf43703e60ba089b07d7170acbabbf8f62`  
		Last Modified: Wed, 21 May 2025 22:27:39 GMT  
		Size: 28.2 MB (28225330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b236b995fe25e62e0a9b025d43ed6aeb0d706dda8c314117fcf6638ebdc7e2b`  
		Last Modified: Wed, 21 May 2025 23:20:12 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe7a90816c2d64d22fdbae87a108eb3343157d21eabfdd8a0362fb7c337c99ab`  
		Last Modified: Wed, 21 May 2025 23:20:12 GMT  
		Size: 2.4 MB (2402177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e20521234d5fd2df1eb25c23579bae7d5636fcce182618943e02ef5ab794963`  
		Last Modified: Wed, 21 May 2025 23:20:12 GMT  
		Size: 6.5 MB (6458802 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8c3b16ce6622a837772fdf6d18fc84b976e8694098211b2e9a4383a62931558`  
		Last Modified: Wed, 21 May 2025 23:20:12 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75351b1571732d8e2e27dfde274116dd0037459b25301366b27c9402ede4aae3`  
		Last Modified: Wed, 21 May 2025 23:20:13 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6.4` - unknown; unknown

```console
$ docker pull spiped@sha256:38fba8cf5966d1da5219266d88064e3aaceb887d32420638d2f0135dbbfd4ca5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3553217 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d442efde223bd171e1f3b5bdd7d6301e1ce2df0c1ea291f621d582ff0136ad75`

```dockerfile
```

-	Layers:
	-	`sha256:0c32ff8bf0f89bea9948bda0ad2c06ecc23437d5eefe99e0003e3c0eae7be3a8`  
		Last Modified: Wed, 21 May 2025 23:20:12 GMT  
		Size: 3.5 MB (3538177 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:faed6139c10365db1a206a064e87b5765026aa41bba89ab1a43fbcf5befd26ce`  
		Last Modified: Wed, 21 May 2025 23:20:12 GMT  
		Size: 15.0 KB (15040 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6.4` - linux; arm variant v5

```console
$ docker pull spiped@sha256:799111c4807c2fea831489b691e498f914d9a30c2f65688bf798574eec5db8c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.9 MB (32904241 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f9e5e8afcac44ab7363c93359b12a1c8dfb1867ed4df01c19777a222ce48c0f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 02 Apr 2025 21:12:22 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1747699200'
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
	-	`sha256:fab452a77ecb21a2e30922ab3eed19310b6d56763bcfc4e4bd31f28d9747f745`  
		Last Modified: Wed, 21 May 2025 22:27:58 GMT  
		Size: 25.8 MB (25756898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf5fcb13f4fae5c0701ae97175c1fde5a265e39ab7420ed78e63dc654b097e65`  
		Last Modified: Thu, 22 May 2025 01:12:54 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9556b3c226c521d39ced715dacdb0ddd196bf05f5846d3732d60e8a3f55a1de`  
		Last Modified: Thu, 22 May 2025 01:12:54 GMT  
		Size: 2.0 MB (1998268 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce40ec37f30dc6d7d5a1ed74cf1f1bae7f1a05eb87b99e62d9b4c27a28051931`  
		Last Modified: Thu, 22 May 2025 01:12:55 GMT  
		Size: 5.1 MB (5147533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4b23094f6c0b0b7beabfe549bc26fad9124341fe7251635a2286ad9d50c488e`  
		Last Modified: Thu, 22 May 2025 01:12:54 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f314f72e5ab08b9522e8df48d487f9c5448dd07a3c496be756e549d855a92e7c`  
		Last Modified: Thu, 22 May 2025 01:12:55 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6.4` - unknown; unknown

```console
$ docker pull spiped@sha256:9cf2a6d75f36284a1051b375e26316cc1e1a134adaff1f248a8d390552e88dd5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3524157 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3a141429766668432eef187e965dabf4459daabd05cb999129f21ee65ed20c6`

```dockerfile
```

-	Layers:
	-	`sha256:6a32a05c66630aa10a22096368b76df8bd67aaf342c8dd930619b45a1888cbc4`  
		Last Modified: Thu, 22 May 2025 01:12:54 GMT  
		Size: 3.5 MB (3509015 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:41b70d9c48c2c437462d07be8fc990b465281e5c418124d21004a253d959aa18`  
		Last Modified: Thu, 22 May 2025 01:12:54 GMT  
		Size: 15.1 KB (15142 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6.4` - linux; arm variant v7

```console
$ docker pull spiped@sha256:bd88168940017d415031d65c8b562a450fb598c60cf7e38ede2eebc4e622eed3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.7 MB (30679570 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:334bd5bd9fc6f29c24ec13b8cda836e7cb1c5e76c363b01a5ae63808e03e7cf0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 02 Apr 2025 21:12:22 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1747699200'
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
	-	`sha256:3726bc5cceb817ddfc7c2e1dbdfb4900fc6e27b680d63b8d751b06952753b6a1`  
		Last Modified: Wed, 21 May 2025 22:27:58 GMT  
		Size: 23.9 MB (23932922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28497644b53abef7026a25140f5b20b9e5f984102c735a18f9ad13b06d325d06`  
		Last Modified: Thu, 22 May 2025 02:11:46 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c06616ca963aeb60b1926e7a4505f5587eb632014d17e10775734237f64bfdd5`  
		Last Modified: Thu, 22 May 2025 02:11:46 GMT  
		Size: 1.9 MB (1856406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0454a735cab512a3994c19f6461e13b792aa7d4ae6f2f7b7beefad87c86e1619`  
		Last Modified: Thu, 22 May 2025 02:11:46 GMT  
		Size: 4.9 MB (4888699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c30c741ba1d6aa6d7e8a8bb49b3f73d5cfc41cc58cc9f1ee0d0222ef1eb61e3`  
		Last Modified: Thu, 22 May 2025 02:11:46 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efa2405c063638356b662a29deb560323db64a04302d8fb7b4e41e40832595be`  
		Last Modified: Thu, 22 May 2025 02:11:47 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6.4` - unknown; unknown

```console
$ docker pull spiped@sha256:67903915b9908ceec6eff9982d5e47b52aed66b921141fb35e158bef999cc642
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3523340 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e202a4f6c6a60f84bb42ff7184ed9b6fc409d848ff7be381fd3aeecfd2229b7e`

```dockerfile
```

-	Layers:
	-	`sha256:798416b4b99780fb82d37f69a61f55757da43446999fd396b2345a89f61b9717`  
		Last Modified: Thu, 22 May 2025 02:11:46 GMT  
		Size: 3.5 MB (3508198 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:16fe3f5accbcda69a4f3d2d1a7e95d1755dbdf53436e1dafd5996ebc9dc0ebda`  
		Last Modified: Thu, 22 May 2025 02:11:46 GMT  
		Size: 15.1 KB (15142 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6.4` - linux; arm64 variant v8

```console
$ docker pull spiped@sha256:d5cafb803c9a0da7ab4771f49d9cdb8a8cdcb3ff719bcbb09e016d458b52edae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.8 MB (35805923 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4433b4b2209f95a137ec9d4fc3da9f0399b1a927010b07100f4d2cb33f01eec6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 02 Apr 2025 21:12:22 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1747699200'
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
	-	`sha256:b16f1b16678093d11ecfece1004207a40f9bc1b7d9d1d16a070c1db552038818`  
		Last Modified: Wed, 21 May 2025 22:27:55 GMT  
		Size: 28.1 MB (28065280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58d7aa0e5553a8e1676ebb9a1e8b4e211d5e24d00e206dd06e9dc931036210a8`  
		Last Modified: Thu, 22 May 2025 02:26:31 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b01b22375091a64a96ee1ad4e57158b3b3a3403ba79cab1a56af7fcaf2c4fd4b`  
		Last Modified: Thu, 22 May 2025 02:26:32 GMT  
		Size: 2.2 MB (2247441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cf33c8dbe86b945cd509593f45ace969c1839a8dee7d1828092b41632af9837`  
		Last Modified: Thu, 22 May 2025 02:26:32 GMT  
		Size: 5.5 MB (5491661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa6e1ae6c666fd43ad0bb5cbd1d595c4f6774a7621a81e94f751dba1447227a4`  
		Last Modified: Thu, 22 May 2025 02:26:32 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25be54df2c26151d78b7c6bcc8b71f10a49ca87573849bc5561334e83d854f56`  
		Last Modified: Thu, 22 May 2025 02:26:33 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6.4` - unknown; unknown

```console
$ docker pull spiped@sha256:76bf26d851cd8fc562b888569d70024625766d5c1b77df5d31a5d5045d909e7a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3524578 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:232fb12c6174ddf70b733574174d96ac46893cfd76e8ecaf5a3d2a2d55139191`

```dockerfile
```

-	Layers:
	-	`sha256:863430707bd172ac83c08ecfc72f18ec0a9e85de22d979a70542342ba06ead69`  
		Last Modified: Thu, 22 May 2025 02:26:32 GMT  
		Size: 3.5 MB (3509405 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cc3c4313ab583feefd96c652f06140e88ab6b676b233c9b4c5ead13c712d32ce`  
		Last Modified: Thu, 22 May 2025 02:26:31 GMT  
		Size: 15.2 KB (15173 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6.4` - linux; 386

```console
$ docker pull spiped@sha256:de2d0f62127be81d4c417ee09c2e83dcc650d781e485052c53b4d83e7e41c305
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.6 MB (37566353 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e29b46d435dc73b21b5f638b8b87840b502cba5421b87b459851dd558cbb504`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 02 Apr 2025 21:12:22 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1747699200'
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
	-	`sha256:7d0eb60defa1a32d12e94bc0d7c2c578881c578aeec0c1d786ef5a19c72a34ab`  
		Last Modified: Wed, 21 May 2025 22:27:56 GMT  
		Size: 29.2 MB (29207487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fc34ae407ddfd8aa872313e98808f6d037d29874d733022ebeb03c21b075b9d`  
		Last Modified: Wed, 21 May 2025 23:19:31 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea1121e956c060196b27bf2cb1c7c4834fd0683b4d013d49729246105637c7e6`  
		Last Modified: Wed, 21 May 2025 23:19:31 GMT  
		Size: 2.4 MB (2400579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58c083d4e9d3c172b7e2dff742a55d190d7deea62d62e77c68be78ebe005756f`  
		Last Modified: Wed, 21 May 2025 23:19:31 GMT  
		Size: 6.0 MB (5956747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95924c7d3bb09f7d740e28a65b589259ca71ed83b9907221ab77e5710964fa84`  
		Last Modified: Wed, 21 May 2025 23:19:31 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af2e19c16d9e608f72faf9f7145bd18f20be31aa8254201cdc30e14098b0ab90`  
		Last Modified: Wed, 21 May 2025 23:19:32 GMT  
		Size: 336.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6.4` - unknown; unknown

```console
$ docker pull spiped@sha256:0e4e1e2182c7414a91dbedc4eee31dc2f23267ca32cb3bc1d1af586c79a15511
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3547159 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:488c249ee13b017bc6d2db92c2455dddf8636b7f8dda1f17d1c32ad46e3f1bc3`

```dockerfile
```

-	Layers:
	-	`sha256:5a933c5783118b861dc28e67218f04f000686e48be72186367702865e0819555`  
		Last Modified: Wed, 21 May 2025 23:19:31 GMT  
		Size: 3.5 MB (3532156 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a135b975223fb9944b6870b3f284f6d0e1276e5223c8b3790aec5292925ac030`  
		Last Modified: Wed, 21 May 2025 23:19:31 GMT  
		Size: 15.0 KB (15003 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6.4` - linux; mips64le

```console
$ docker pull spiped@sha256:e08a5f574ff6e4c4889083b74ad49f5f1fa5c4909a77fd7f0118f9e4537b2f64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.2 MB (36169243 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81d9271e2536f4b9e06788180f5f1808dc6e92f6183d5cf57c5ac1f4a073b894`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 02 Apr 2025 21:12:22 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1747699200'
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
	-	`sha256:48541e37cd82678078df221c38fde515e820c13a623449b699d224f60f15dae8`  
		Last Modified: Wed, 21 May 2025 22:28:22 GMT  
		Size: 28.5 MB (28511850 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3803a240d8e659370e2fab860baf71e6845bb1657afea9964a9455a06816584f`  
		Last Modified: Thu, 22 May 2025 06:14:35 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:058aa8bad24612579286f5eae085472a3a9f63436aa5165ce779f2d1f73c9e99`  
		Last Modified: Thu, 22 May 2025 06:14:36 GMT  
		Size: 1.8 MB (1842259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60712b0a5b50c33b45964a94fca078484dff5c1bc25928f8b19642a8fdddc723`  
		Last Modified: Thu, 22 May 2025 06:14:36 GMT  
		Size: 5.8 MB (5813592 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f03381e56cdea6e5c69ba962656f3b8ee6708f99bbbe90c8cb59805dec2821f`  
		Last Modified: Thu, 22 May 2025 06:14:35 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0030e45312f412d88429defd5484aa7c1354487911afb2c33273fd71e177e9ed`  
		Last Modified: Thu, 22 May 2025 06:14:36 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6.4` - unknown; unknown

```console
$ docker pull spiped@sha256:376d3c3cf802ddebdca18c0302bdc8f66c2a6eb3b23346b26c5205f7932dcce1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 KB (14897 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90459617b1bb9aa0a1d2cf5c37b8ad8d23c16eb4f14aacb08afabd9b233b117f`

```dockerfile
```

-	Layers:
	-	`sha256:307900282127ed9322c5ccab5de1df5096b6a0b07bd4395c5b9cb9b8599934bc`  
		Last Modified: Thu, 22 May 2025 06:14:35 GMT  
		Size: 14.9 KB (14897 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6.4` - linux; ppc64le

```console
$ docker pull spiped@sha256:a7321ff5fec2afbb779a0acf6da6d63f5c5d332938ad6bf260c611ae4a5b1c06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.1 MB (41093723 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15a62507992ef6fb0e12abeb88eb5ecf00ad31cb2d3eb2e89b8f8f14130d29e6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 02 Apr 2025 21:12:22 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1747699200'
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
	-	`sha256:701606535a7233566815cc9ad5f3e5853b443be5476286f6799008053dc2b03b`  
		Last Modified: Wed, 21 May 2025 22:28:16 GMT  
		Size: 32.1 MB (32066912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28a6c81eea611329e12a0cc8737d8ee2c5ada1b8e3aaef98d8acd2741b37d917`  
		Last Modified: Thu, 22 May 2025 07:17:33 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0fc1affdf757c274e7e67536481196cb883110fb5bfd979782fb8383777bfa6`  
		Last Modified: Thu, 22 May 2025 07:17:33 GMT  
		Size: 2.6 MB (2583887 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4db9a308ee6bef1c8241a16cb77c39894f524896d99e85f384dd7eb7a4756ff1`  
		Last Modified: Thu, 22 May 2025 07:17:33 GMT  
		Size: 6.4 MB (6441381 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c37f165cfd98289d815cf96acad45a8ed3cd5f2558537aebefbb0c7c359d0f9e`  
		Last Modified: Thu, 22 May 2025 07:17:33 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f805d8994580dac40f982b71b4ae42685005eeb1438bd76e132c9307532dedd`  
		Last Modified: Thu, 22 May 2025 07:17:34 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6.4` - unknown; unknown

```console
$ docker pull spiped@sha256:1cfcf23833ca373cc8000f5f9998d74ccf00ecca9ad0fb786e5172d2fcfd39af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3539050 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:789d0ff26873a3c16d1516a64b5521540d3e27924324dd582fbed08e96e970a9`

```dockerfile
```

-	Layers:
	-	`sha256:8b1a9eceb4ec95f4f5b6806a7ec405ea988499e1a2ec48b26ff0ede6b066b2a4`  
		Last Modified: Thu, 22 May 2025 07:17:33 GMT  
		Size: 3.5 MB (3523962 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ae9055586249d83d4bc0597f9cd6f6a21d3b9bf8c399b22bc90d82eed114d347`  
		Last Modified: Thu, 22 May 2025 07:17:33 GMT  
		Size: 15.1 KB (15088 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6.4` - linux; s390x

```console
$ docker pull spiped@sha256:313c5fbddb0f36164ff9ff07b8afb014aae1fba0aded0128c2058a6960b944dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.3 MB (34345786 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be0c786c61c197ff161771dfba4eecaca2e88d0ad743f2abe498c7758f082708`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 02 Apr 2025 21:12:22 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1747699200'
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
	-	`sha256:fb6e196ef379785f6b759a20e90d74fe0566b240771695f724c27a44aa6cd3ce`  
		Last Modified: Wed, 21 May 2025 22:28:38 GMT  
		Size: 26.9 MB (26882808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38ceb32ec1a8749e974fe5929ea6dff22bcee11dafd2fc667579323da38876f1`  
		Last Modified: Thu, 22 May 2025 00:53:41 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2f56657b11e71e77f7914f81ccb09da12e157355a9c2bfa3ad990780f7ee481`  
		Last Modified: Thu, 22 May 2025 00:53:41 GMT  
		Size: 2.1 MB (2069161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d37a680b670b7565d1e108f473912336f74759acbde356e1baffcebb55ab778`  
		Last Modified: Thu, 22 May 2025 00:53:41 GMT  
		Size: 5.4 MB (5392277 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec75588e715a05902adcfb5629f1851cf0d29ddf5ae3f281b75fdc0a40e98fb6`  
		Last Modified: Thu, 22 May 2025 00:53:41 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0e2d58562f243d49496f4f3e52abfbea3ebecc55c6401ecd80a648029bac830`  
		Last Modified: Thu, 22 May 2025 00:53:42 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6.4` - unknown; unknown

```console
$ docker pull spiped@sha256:5de6955b949dbe4e3cd91755329d2cb433e60f90fb15863b8bbab4c4f414cd9d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3541403 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d51372649bab5e76ddd19982bc703b786c8dc5b940231eeb5b6fa54327a2e1d`

```dockerfile
```

-	Layers:
	-	`sha256:7ddaee20724beee644d4580292cd7c349e170f436b4a509a76ba3ecb3b2337e0`  
		Last Modified: Thu, 22 May 2025 00:53:41 GMT  
		Size: 3.5 MB (3526363 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0371bae7cc54c2d437162fb10d62d7bc577205878fe8e5d855cbf8030eb4ca81`  
		Last Modified: Thu, 22 May 2025 00:53:41 GMT  
		Size: 15.0 KB (15040 bytes)  
		MIME: application/vnd.in-toto+json

## `spiped:1.6.4-alpine`

```console
$ docker pull spiped@sha256:19cab0821b57af25c5e04f34834de199acba4d5a909887ce0f093a3200c51243
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
$ docker pull spiped@sha256:622df849c8857cb4538c0b252cf0b5e94d10a2b5af1222af4d54ce9016270049
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3759161 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83432e0291e920e3ef7ce3c7690aba0f53cf7250e10452315d154dccfe1df29f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Wed, 02 Apr 2025 21:12:22 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
RUN apk add --no-cache libssl3 # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Wed, 02 Apr 2025 21:12:22 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
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
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 12:05:35 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:114b63918a29534fea2f0cc34ca9459cf360301d5cc6e425a943254bd857bdfd`  
		Last Modified: Wed, 02 Apr 2025 22:08:24 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4e3893b92c8e046b61bf235250bedbecb6eca134316b11bfb15c8cd1b337f3d`  
		Last Modified: Wed, 02 Apr 2025 22:08:24 GMT  
		Size: 7.9 KB (7914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fc9dd67e9904979842828a3e75301a0c379da1bb45dc75cdc2bd6631a028a32`  
		Last Modified: Wed, 02 Apr 2025 22:08:24 GMT  
		Size: 107.6 KB (107617 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fff4e9164a4259b4803c6d934508ad8476b4416d7097f2cbe68db83e91a69ab0`  
		Last Modified: Wed, 02 Apr 2025 22:08:24 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba3edaa59ccf7fe4418cc9f918ad66772163c1de22c3afd74314e1beee778bc5`  
		Last Modified: Wed, 02 Apr 2025 22:08:24 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6.4-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:7ddf892427f7350fc633c5740ef8895f88d29ce3651ae3347a7ae8ed45e86fcf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.1 KB (94124 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc93f0f4d7a7ab59381d2ca94b5c48169a0eb0d534f6e06db48944a6a1cd9aef`

```dockerfile
```

-	Layers:
	-	`sha256:6dd8a7492609939d1b2f1cbf941b9c4607360ff5f25aaad3a379b6be4dde9aca`  
		Last Modified: Wed, 02 Apr 2025 22:08:24 GMT  
		Size: 79.8 KB (79822 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0122061363abb1f4f3d5cb12184c88a3d21d651f9a1aeaf7e10ac5934d6919da`  
		Last Modified: Wed, 02 Apr 2025 22:08:24 GMT  
		Size: 14.3 KB (14302 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6.4-alpine` - linux; arm variant v6

```console
$ docker pull spiped@sha256:022488b36873fd89f1a451ed66a2b4aed67a9ddb352d2bd608cf892376ae8972
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3463148 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33792a429e90fd9ea05a651fefc730ad65a8006e4c32639a335044afbd4c5952`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armhf.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Wed, 02 Apr 2025 21:12:22 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
RUN apk add --no-cache libssl3 # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Wed, 02 Apr 2025 21:12:22 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
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
	-	`sha256:76099982f06682e28a60c3b774ef20931d07b0a2f551203484e633d8c0361ee7`  
		Last Modified: Fri, 14 Feb 2025 18:28:03 GMT  
		Size: 3.4 MB (3364731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:066b47e1325b9f6db29d2d135e8ce6b8fcbf90a8f37138d1f3356a294928613b`  
		Last Modified: Fri, 14 Feb 2025 22:09:56 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:014f6178dbec0d9fa86b0b438929f32378f60d88338518b7952956c6aa1b5cb7`  
		Last Modified: Fri, 14 Feb 2025 22:09:56 GMT  
		Size: 7.9 KB (7917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbc93d94752878827fd3532056a9d5c692ac38ff04c63b32f88673aa8964416a`  
		Last Modified: Wed, 02 Apr 2025 21:50:27 GMT  
		Size: 89.1 KB (89120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc26ca6070e6d3cc776fbb063b850e250863b079bb9b4fedcf001b518f004387`  
		Last Modified: Wed, 02 Apr 2025 21:50:27 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb66a68852a74dbb6d6be32e7fd436e99a797bb5340892e84aacf1474567e04a`  
		Last Modified: Wed, 02 Apr 2025 21:50:27 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6.4-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:8cc6f6a6d91b5f59a3cfa4d8bef00dd3556faac0bcc6400c61260c9e8730e0c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.2 KB (14186 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b8d4b9bee6645579beaf8fbe1c143f10516e131664def6ca2c559cfa1f31504`

```dockerfile
```

-	Layers:
	-	`sha256:3263ee3077e76a9dbb13eecc31527a10d5efdefe3d39ec4c458f0e1132247531`  
		Last Modified: Wed, 02 Apr 2025 21:50:26 GMT  
		Size: 14.2 KB (14186 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6.4-alpine` - linux; arm variant v7

```console
$ docker pull spiped@sha256:dee3984d26da4f0e8f36051324b3037dc9ccbe1860bc73d0c20cb5d580b67ec8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3189083 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14664fb61592fe16a4ad57c810d3b1649982058dd7505d05565d350c40e2ea78`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armv7.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Wed, 02 Apr 2025 21:12:22 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
RUN apk add --no-cache libssl3 # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Wed, 02 Apr 2025 21:12:22 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
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
	-	`sha256:85f3b18f9f5a8655db86c6dfb02bb01011ffef63d10a173843c5c65c3e9137b7`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.1 MB (3098123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e8fb51fad1dc40f454b85c84a615197e58cde8fdc5f21b35dc45af3c97d1fa7`  
		Last Modified: Wed, 02 Apr 2025 21:51:13 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ef3321472ab9d21d883d24b575a54b890a3e93b9b0a5b44204d21656d78680a`  
		Last Modified: Wed, 02 Apr 2025 21:51:13 GMT  
		Size: 7.9 KB (7928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:caa2395c1ed98837c525acd35fd9fdccb1a68a1b50574550c75f56789cdcefe6`  
		Last Modified: Wed, 02 Apr 2025 21:51:13 GMT  
		Size: 81.7 KB (81650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1631d9b9eaabe691dc7301f342ee863beab1cba416bc55834b0dcd64d811d52e`  
		Last Modified: Wed, 02 Apr 2025 21:51:13 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16aa8ceacc34b79b201841242c1d739910f64d43a16351ecd1b4e063785ae3d7`  
		Last Modified: Wed, 02 Apr 2025 21:51:14 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6.4-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:01fc29e009708c7ec4e299f0ab229f389ceb7f44379a0e50e9c4116c11ac1887
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.3 KB (94259 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46d3a8021f9021b79e00c3aa6168baba8e1d2d75d1c2107977f5af4eaa46e39a`

```dockerfile
```

-	Layers:
	-	`sha256:44cabd4b7cd6d156567d0a5c80d300c59411572e356ff5c2bf8ddb27a1f9f941`  
		Last Modified: Wed, 02 Apr 2025 21:51:13 GMT  
		Size: 79.9 KB (79858 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:abc6d037c51e675c4900f1eaeb5150e1f382d37f0f1b0f592f7bae802181c645`  
		Last Modified: Wed, 02 Apr 2025 21:51:13 GMT  
		Size: 14.4 KB (14401 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6.4-alpine` - linux; arm64 variant v8

```console
$ docker pull spiped@sha256:9bf1fb1b6d22643c494712c0e64d1180ae0f262b6b8970f3e2d8dcef3fef6a57
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4102905 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb9c2bd1fb5fe20d7cbaf48186ea092dbc2d13b35d73505074e36eda2950836b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Wed, 02 Apr 2025 21:12:22 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
RUN apk add --no-cache libssl3 # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Wed, 02 Apr 2025 21:12:22 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
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
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 12:05:33 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fcfdf5e57fbe5c7d9308257021972c3c8049235b8418078c63b52659f3c141c`  
		Last Modified: Wed, 02 Apr 2025 21:51:29 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:860d1ac7e6f5ff9e4c32fa1aa64bcf81c200cb1e7e28b8d5ed59a0614cecead6`  
		Last Modified: Wed, 02 Apr 2025 21:51:30 GMT  
		Size: 7.9 KB (7920 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29683b13029a57b0b382b6e15838ae6d55e7fb4e17335eb9458398a3b28cc51c`  
		Last Modified: Wed, 02 Apr 2025 21:51:30 GMT  
		Size: 100.6 KB (100575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fcdf172b649e9fc88d25bf9587c92d962a199e6c7a0e1a98c2ec6c89c54aacb`  
		Last Modified: Wed, 02 Apr 2025 21:51:30 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52a43ba3519841070ae5d0384c94c52fc8d37791bfa6e9ad35b22b8b9702d29a`  
		Last Modified: Wed, 02 Apr 2025 21:51:31 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6.4-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:43a680d67479907610aad7509796ef596f5fed0d289448130c1196039d21ded2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.3 KB (94314 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b365f16aaf205dfc1b9640897e812784f27ed48fde6a42a374087e79452d0922`

```dockerfile
```

-	Layers:
	-	`sha256:4eb7794745d2b89ac646620f0f7c4237fc16799b36487de5b5f09a981ec8188f`  
		Last Modified: Wed, 02 Apr 2025 21:51:30 GMT  
		Size: 79.9 KB (79878 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9823c97e3177ff4bc824966f8e095cc5f8a3ab0acacb35eeeea76a628c98b570`  
		Last Modified: Wed, 02 Apr 2025 21:51:30 GMT  
		Size: 14.4 KB (14436 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6.4-alpine` - linux; 386

```console
$ docker pull spiped@sha256:10f7aa16af762acbfb63005c00877699fa29c2e4bb04d75d1d70ec20a60f5453
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3593008 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:caa790ea4f84c7bd9a039089ae50b44f58ea302f037ea74e3b405bc3febd96b5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Wed, 02 Apr 2025 21:12:22 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
RUN apk add --no-cache libssl3 # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Wed, 02 Apr 2025 21:12:22 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
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
	-	`sha256:69aa61ccf55e5bf8e7a069b89e8afb42b4f3443b3785868795af8046d810d608`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.5 MB (3463623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13e7ff7711b41a9071a294c97e4058917e28c3c7e20059009e0b630880394156`  
		Last Modified: Wed, 02 Apr 2025 21:51:03 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ce2dc85c8b1ec7a6c1ad258c05589aa70dba5fe5290558cc0e4548d1bcdd5de`  
		Last Modified: Wed, 02 Apr 2025 21:51:03 GMT  
		Size: 7.9 KB (7913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0af8ae2ced3573d3e4de1a677b4b5a3c011895466b9c210fd74fe255cb8d77b8`  
		Last Modified: Wed, 02 Apr 2025 21:51:03 GMT  
		Size: 120.1 KB (120090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfa87e2679113a95903cfd2867ff588bcf12b0fd8ddfac21b77727f8b7d3d894`  
		Last Modified: Wed, 02 Apr 2025 21:51:03 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d22470fcb8710e32223fea8e79f0b28488b0ab51c65567241c529bd203b95215`  
		Last Modified: Wed, 02 Apr 2025 21:51:04 GMT  
		Size: 336.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6.4-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:766834152c333f40d598d1f36bd56d11f810d2e19ed86d7e91571b9367515fee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.1 KB (94062 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef8983e1e4860bdae956bb8f365e0bcc2f2cf38f76ce6566d65f6937140d1443`

```dockerfile
```

-	Layers:
	-	`sha256:0344d1265ed83fac16730c24d70471283f93d11c5749243cdcf7ba8e3cf80a76`  
		Last Modified: Wed, 02 Apr 2025 21:51:03 GMT  
		Size: 79.8 KB (79797 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:de475a73cdee8c96006bf8d6c10118db82ed20c810abe06bd1dcb3b224bfaf98`  
		Last Modified: Wed, 02 Apr 2025 21:51:03 GMT  
		Size: 14.3 KB (14265 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6.4-alpine` - linux; ppc64le

```console
$ docker pull spiped@sha256:88487ee5729022576bc8477226c823b846fcb546e116fd1817a9b49c7a8248df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3696294 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e37765c7075b9c5e9f7aa70b2b311f8eb578373a5b127e41648ff035f02b2de`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-ppc64le.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Wed, 02 Apr 2025 21:12:22 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
RUN apk add --no-cache libssl3 # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Wed, 02 Apr 2025 21:12:22 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
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
	-	`sha256:184b14480d317057da092a0994ad6baf4b2df588108f43969f8fd56f021af2c6`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.6 MB (3574345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f29133aa5ac2dc7f7caf05bec17a3f120b130b0a9f8a931b87d42bda5e00ee7`  
		Last Modified: Wed, 02 Apr 2025 21:53:15 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ceed22f9dc598f4a83d2574a1236b9eb55845a886691ca27d260af8e52d0a5b8`  
		Last Modified: Wed, 02 Apr 2025 21:53:15 GMT  
		Size: 7.9 KB (7921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e550c947cd96d7d5dbfd565fa3ae85434cb2481820d65ac92504416d056beea9`  
		Last Modified: Wed, 02 Apr 2025 21:53:15 GMT  
		Size: 112.6 KB (112643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47cfc80ff9405d7424905e6aa74f541ec5830861bef1b1218605b7d66fcec7b9`  
		Last Modified: Wed, 02 Apr 2025 21:53:15 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b0e844805fa1d0d457d1513e5b9d92436e3ab8e65548a31fbbc18ed1c2c743b`  
		Last Modified: Wed, 02 Apr 2025 21:53:16 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6.4-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:fdca1b5f72932ee6bcfc55a37feb9c860f41b530efa43e63aec701932b3cf4da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.3 KB (92255 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58422f604e757b9c7c12519d56f597a89ae27e12f2339cf2cc67b4b5a19bb384`

```dockerfile
```

-	Layers:
	-	`sha256:2df4c6cf5666abc03d36c3ff177b1360db4c2531a9cd9923b404e7ff491bec9b`  
		Last Modified: Wed, 02 Apr 2025 21:53:15 GMT  
		Size: 77.9 KB (77905 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a7ad33b282085052031ca00d32c203a26ce45455daf796d327bb6cdbdcf3e8aa`  
		Last Modified: Wed, 02 Apr 2025 21:53:15 GMT  
		Size: 14.3 KB (14350 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6.4-alpine` - linux; riscv64

```console
$ docker pull spiped@sha256:d93e8574bb82dd81dafcf25f7625ed7818c3a0e31066bbddf64006b83d78aba9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3459532 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11a635f525ddca22947829af6f197712b92c46682f40c9dbe63063aa381f9a9c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-riscv64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Wed, 02 Apr 2025 21:12:22 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
RUN apk add --no-cache libssl3 # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Wed, 02 Apr 2025 21:12:22 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
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
	-	`sha256:7df33f7ad8beb367ac09bdd1b2f220db3ee2bbdda14a6310d1340e5628b5ba88`  
		Last Modified: Fri, 14 Feb 2025 18:56:36 GMT  
		Size: 3.4 MB (3351439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a279c5ee271afcec6d3150e694efda4e5d36691f2d7ebe160636c0ab5a79b1ec`  
		Last Modified: Wed, 02 Apr 2025 21:53:03 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:015b70b993c8cc00dfe1e78ec875878062b451bd4ec2b326794c36444cb3105e`  
		Last Modified: Wed, 02 Apr 2025 21:53:03 GMT  
		Size: 7.9 KB (7904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87d040e2d542829d397e472ec2982c4857e357fe408f645da0693ef90321e2c7`  
		Last Modified: Wed, 02 Apr 2025 21:53:03 GMT  
		Size: 98.8 KB (98804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a0e579239e2446edd70320e6ec295380d239d0b2fb8045fbda0d7753c161f59`  
		Last Modified: Wed, 02 Apr 2025 21:53:03 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f11cda2eddc9aaf6455435d16dfafc74f718d637e59cb8c549b1310659e0f68`  
		Last Modified: Wed, 02 Apr 2025 21:53:04 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6.4-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:6ef91094d879feac7520f82fdd946b0c798b74a1208a22482597eb403e08bd3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.2 KB (92248 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54c9ad713acd2272c15e5bd4e3532ba9df6910776b9db0bb063b585453f134ab`

```dockerfile
```

-	Layers:
	-	`sha256:b046cc017c3f020547f0314366d83fb03c8803458406b56bdd3904750ccb915b`  
		Last Modified: Wed, 02 Apr 2025 21:53:03 GMT  
		Size: 77.9 KB (77901 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:de0c335e4f12af3686646881008f04ba3bc438d3f15fbd38fbc3998d12514728`  
		Last Modified: Wed, 02 Apr 2025 21:53:03 GMT  
		Size: 14.3 KB (14347 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6.4-alpine` - linux; s390x

```console
$ docker pull spiped@sha256:8e1cc9b73ed1eb178d6d22338fc661c8f3386b5d33086e11fca8483e38bc0123
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3573772 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9100e7b9db6a61a9d6818b301afcaf1e2753a632dba5e84dbdf9ea416bfe685b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-s390x.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Wed, 02 Apr 2025 21:12:22 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
RUN apk add --no-cache libssl3 # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Wed, 02 Apr 2025 21:12:22 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
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
	-	`sha256:c1a599607158512214777614f916f8193d29fd34b656d47dfc26314af01e2af4`  
		Last Modified: Fri, 14 Feb 2025 12:05:25 GMT  
		Size: 3.5 MB (3467567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:408f712244d227bb17176b3c9833183d94d7e5078a0071c6bb815f7c6acd044b`  
		Last Modified: Wed, 02 Apr 2025 21:52:19 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce3d2b3d93cf3babc3c2c43519cfac5c89b009dddf9f6329ccb604067e1c25d0`  
		Last Modified: Wed, 02 Apr 2025 21:52:19 GMT  
		Size: 7.9 KB (7919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:924f34f1a30b83eb8fe0d105f78a3ddb08291d7062c11e0a807ca3576dd2e638`  
		Last Modified: Wed, 02 Apr 2025 21:52:19 GMT  
		Size: 96.9 KB (96901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eaa01324514a5afcdaa7ba2727d95863ff56033c4f01975371de7c453ccdf8e1`  
		Last Modified: Wed, 02 Apr 2025 21:52:19 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b3162a370a5d0aff74dea2a1ddb49f120b995ec42d4b29c7bcb3c2f10a91fc1`  
		Last Modified: Wed, 02 Apr 2025 21:52:20 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6.4-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:97f9242d5c7292f0782ce10a5d3a0549df652a9380a4f408bf9ede75116a30aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.2 KB (92170 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77e792a9515a7540fa01538367eccf186ff2dd8158a7dccadf4d37f635a3679c`

```dockerfile
```

-	Layers:
	-	`sha256:7c31c769211e50a701dc70ffd6261e2d0664c6f3b50fd444ad2665b22b1d6e5c`  
		Last Modified: Wed, 02 Apr 2025 21:52:19 GMT  
		Size: 77.9 KB (77871 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4988863227d01a39c5e290493124efb4304413f32a12e6879ffda4c3a86afd0d`  
		Last Modified: Wed, 02 Apr 2025 21:52:20 GMT  
		Size: 14.3 KB (14299 bytes)  
		MIME: application/vnd.in-toto+json

## `spiped:alpine`

```console
$ docker pull spiped@sha256:19cab0821b57af25c5e04f34834de199acba4d5a909887ce0f093a3200c51243
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
$ docker pull spiped@sha256:622df849c8857cb4538c0b252cf0b5e94d10a2b5af1222af4d54ce9016270049
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3759161 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83432e0291e920e3ef7ce3c7690aba0f53cf7250e10452315d154dccfe1df29f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Wed, 02 Apr 2025 21:12:22 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
RUN apk add --no-cache libssl3 # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Wed, 02 Apr 2025 21:12:22 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
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
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 12:05:35 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:114b63918a29534fea2f0cc34ca9459cf360301d5cc6e425a943254bd857bdfd`  
		Last Modified: Wed, 02 Apr 2025 22:08:24 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4e3893b92c8e046b61bf235250bedbecb6eca134316b11bfb15c8cd1b337f3d`  
		Last Modified: Wed, 02 Apr 2025 22:08:24 GMT  
		Size: 7.9 KB (7914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fc9dd67e9904979842828a3e75301a0c379da1bb45dc75cdc2bd6631a028a32`  
		Last Modified: Wed, 02 Apr 2025 22:08:24 GMT  
		Size: 107.6 KB (107617 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fff4e9164a4259b4803c6d934508ad8476b4416d7097f2cbe68db83e91a69ab0`  
		Last Modified: Wed, 02 Apr 2025 22:08:24 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba3edaa59ccf7fe4418cc9f918ad66772163c1de22c3afd74314e1beee778bc5`  
		Last Modified: Wed, 02 Apr 2025 22:08:24 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:7ddf892427f7350fc633c5740ef8895f88d29ce3651ae3347a7ae8ed45e86fcf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.1 KB (94124 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc93f0f4d7a7ab59381d2ca94b5c48169a0eb0d534f6e06db48944a6a1cd9aef`

```dockerfile
```

-	Layers:
	-	`sha256:6dd8a7492609939d1b2f1cbf941b9c4607360ff5f25aaad3a379b6be4dde9aca`  
		Last Modified: Wed, 02 Apr 2025 22:08:24 GMT  
		Size: 79.8 KB (79822 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0122061363abb1f4f3d5cb12184c88a3d21d651f9a1aeaf7e10ac5934d6919da`  
		Last Modified: Wed, 02 Apr 2025 22:08:24 GMT  
		Size: 14.3 KB (14302 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:alpine` - linux; arm variant v6

```console
$ docker pull spiped@sha256:022488b36873fd89f1a451ed66a2b4aed67a9ddb352d2bd608cf892376ae8972
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3463148 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33792a429e90fd9ea05a651fefc730ad65a8006e4c32639a335044afbd4c5952`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armhf.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Wed, 02 Apr 2025 21:12:22 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
RUN apk add --no-cache libssl3 # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Wed, 02 Apr 2025 21:12:22 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
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
	-	`sha256:76099982f06682e28a60c3b774ef20931d07b0a2f551203484e633d8c0361ee7`  
		Last Modified: Fri, 14 Feb 2025 18:28:03 GMT  
		Size: 3.4 MB (3364731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:066b47e1325b9f6db29d2d135e8ce6b8fcbf90a8f37138d1f3356a294928613b`  
		Last Modified: Fri, 14 Feb 2025 22:09:56 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:014f6178dbec0d9fa86b0b438929f32378f60d88338518b7952956c6aa1b5cb7`  
		Last Modified: Fri, 14 Feb 2025 22:09:56 GMT  
		Size: 7.9 KB (7917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbc93d94752878827fd3532056a9d5c692ac38ff04c63b32f88673aa8964416a`  
		Last Modified: Wed, 02 Apr 2025 21:50:27 GMT  
		Size: 89.1 KB (89120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc26ca6070e6d3cc776fbb063b850e250863b079bb9b4fedcf001b518f004387`  
		Last Modified: Wed, 02 Apr 2025 21:50:27 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb66a68852a74dbb6d6be32e7fd436e99a797bb5340892e84aacf1474567e04a`  
		Last Modified: Wed, 02 Apr 2025 21:50:27 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:8cc6f6a6d91b5f59a3cfa4d8bef00dd3556faac0bcc6400c61260c9e8730e0c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.2 KB (14186 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b8d4b9bee6645579beaf8fbe1c143f10516e131664def6ca2c559cfa1f31504`

```dockerfile
```

-	Layers:
	-	`sha256:3263ee3077e76a9dbb13eecc31527a10d5efdefe3d39ec4c458f0e1132247531`  
		Last Modified: Wed, 02 Apr 2025 21:50:26 GMT  
		Size: 14.2 KB (14186 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:alpine` - linux; arm variant v7

```console
$ docker pull spiped@sha256:dee3984d26da4f0e8f36051324b3037dc9ccbe1860bc73d0c20cb5d580b67ec8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3189083 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14664fb61592fe16a4ad57c810d3b1649982058dd7505d05565d350c40e2ea78`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armv7.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Wed, 02 Apr 2025 21:12:22 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
RUN apk add --no-cache libssl3 # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Wed, 02 Apr 2025 21:12:22 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
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
	-	`sha256:85f3b18f9f5a8655db86c6dfb02bb01011ffef63d10a173843c5c65c3e9137b7`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.1 MB (3098123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e8fb51fad1dc40f454b85c84a615197e58cde8fdc5f21b35dc45af3c97d1fa7`  
		Last Modified: Wed, 02 Apr 2025 21:51:13 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ef3321472ab9d21d883d24b575a54b890a3e93b9b0a5b44204d21656d78680a`  
		Last Modified: Wed, 02 Apr 2025 21:51:13 GMT  
		Size: 7.9 KB (7928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:caa2395c1ed98837c525acd35fd9fdccb1a68a1b50574550c75f56789cdcefe6`  
		Last Modified: Wed, 02 Apr 2025 21:51:13 GMT  
		Size: 81.7 KB (81650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1631d9b9eaabe691dc7301f342ee863beab1cba416bc55834b0dcd64d811d52e`  
		Last Modified: Wed, 02 Apr 2025 21:51:13 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16aa8ceacc34b79b201841242c1d739910f64d43a16351ecd1b4e063785ae3d7`  
		Last Modified: Wed, 02 Apr 2025 21:51:14 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:01fc29e009708c7ec4e299f0ab229f389ceb7f44379a0e50e9c4116c11ac1887
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.3 KB (94259 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46d3a8021f9021b79e00c3aa6168baba8e1d2d75d1c2107977f5af4eaa46e39a`

```dockerfile
```

-	Layers:
	-	`sha256:44cabd4b7cd6d156567d0a5c80d300c59411572e356ff5c2bf8ddb27a1f9f941`  
		Last Modified: Wed, 02 Apr 2025 21:51:13 GMT  
		Size: 79.9 KB (79858 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:abc6d037c51e675c4900f1eaeb5150e1f382d37f0f1b0f592f7bae802181c645`  
		Last Modified: Wed, 02 Apr 2025 21:51:13 GMT  
		Size: 14.4 KB (14401 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:alpine` - linux; arm64 variant v8

```console
$ docker pull spiped@sha256:9bf1fb1b6d22643c494712c0e64d1180ae0f262b6b8970f3e2d8dcef3fef6a57
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4102905 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb9c2bd1fb5fe20d7cbaf48186ea092dbc2d13b35d73505074e36eda2950836b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Wed, 02 Apr 2025 21:12:22 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
RUN apk add --no-cache libssl3 # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Wed, 02 Apr 2025 21:12:22 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
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
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 12:05:33 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fcfdf5e57fbe5c7d9308257021972c3c8049235b8418078c63b52659f3c141c`  
		Last Modified: Wed, 02 Apr 2025 21:51:29 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:860d1ac7e6f5ff9e4c32fa1aa64bcf81c200cb1e7e28b8d5ed59a0614cecead6`  
		Last Modified: Wed, 02 Apr 2025 21:51:30 GMT  
		Size: 7.9 KB (7920 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29683b13029a57b0b382b6e15838ae6d55e7fb4e17335eb9458398a3b28cc51c`  
		Last Modified: Wed, 02 Apr 2025 21:51:30 GMT  
		Size: 100.6 KB (100575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fcdf172b649e9fc88d25bf9587c92d962a199e6c7a0e1a98c2ec6c89c54aacb`  
		Last Modified: Wed, 02 Apr 2025 21:51:30 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52a43ba3519841070ae5d0384c94c52fc8d37791bfa6e9ad35b22b8b9702d29a`  
		Last Modified: Wed, 02 Apr 2025 21:51:31 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:43a680d67479907610aad7509796ef596f5fed0d289448130c1196039d21ded2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.3 KB (94314 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b365f16aaf205dfc1b9640897e812784f27ed48fde6a42a374087e79452d0922`

```dockerfile
```

-	Layers:
	-	`sha256:4eb7794745d2b89ac646620f0f7c4237fc16799b36487de5b5f09a981ec8188f`  
		Last Modified: Wed, 02 Apr 2025 21:51:30 GMT  
		Size: 79.9 KB (79878 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9823c97e3177ff4bc824966f8e095cc5f8a3ab0acacb35eeeea76a628c98b570`  
		Last Modified: Wed, 02 Apr 2025 21:51:30 GMT  
		Size: 14.4 KB (14436 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:alpine` - linux; 386

```console
$ docker pull spiped@sha256:10f7aa16af762acbfb63005c00877699fa29c2e4bb04d75d1d70ec20a60f5453
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3593008 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:caa790ea4f84c7bd9a039089ae50b44f58ea302f037ea74e3b405bc3febd96b5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Wed, 02 Apr 2025 21:12:22 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
RUN apk add --no-cache libssl3 # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Wed, 02 Apr 2025 21:12:22 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
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
	-	`sha256:69aa61ccf55e5bf8e7a069b89e8afb42b4f3443b3785868795af8046d810d608`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.5 MB (3463623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13e7ff7711b41a9071a294c97e4058917e28c3c7e20059009e0b630880394156`  
		Last Modified: Wed, 02 Apr 2025 21:51:03 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ce2dc85c8b1ec7a6c1ad258c05589aa70dba5fe5290558cc0e4548d1bcdd5de`  
		Last Modified: Wed, 02 Apr 2025 21:51:03 GMT  
		Size: 7.9 KB (7913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0af8ae2ced3573d3e4de1a677b4b5a3c011895466b9c210fd74fe255cb8d77b8`  
		Last Modified: Wed, 02 Apr 2025 21:51:03 GMT  
		Size: 120.1 KB (120090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfa87e2679113a95903cfd2867ff588bcf12b0fd8ddfac21b77727f8b7d3d894`  
		Last Modified: Wed, 02 Apr 2025 21:51:03 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d22470fcb8710e32223fea8e79f0b28488b0ab51c65567241c529bd203b95215`  
		Last Modified: Wed, 02 Apr 2025 21:51:04 GMT  
		Size: 336.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:766834152c333f40d598d1f36bd56d11f810d2e19ed86d7e91571b9367515fee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.1 KB (94062 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef8983e1e4860bdae956bb8f365e0bcc2f2cf38f76ce6566d65f6937140d1443`

```dockerfile
```

-	Layers:
	-	`sha256:0344d1265ed83fac16730c24d70471283f93d11c5749243cdcf7ba8e3cf80a76`  
		Last Modified: Wed, 02 Apr 2025 21:51:03 GMT  
		Size: 79.8 KB (79797 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:de475a73cdee8c96006bf8d6c10118db82ed20c810abe06bd1dcb3b224bfaf98`  
		Last Modified: Wed, 02 Apr 2025 21:51:03 GMT  
		Size: 14.3 KB (14265 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:alpine` - linux; ppc64le

```console
$ docker pull spiped@sha256:88487ee5729022576bc8477226c823b846fcb546e116fd1817a9b49c7a8248df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3696294 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e37765c7075b9c5e9f7aa70b2b311f8eb578373a5b127e41648ff035f02b2de`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-ppc64le.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Wed, 02 Apr 2025 21:12:22 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
RUN apk add --no-cache libssl3 # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Wed, 02 Apr 2025 21:12:22 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
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
	-	`sha256:184b14480d317057da092a0994ad6baf4b2df588108f43969f8fd56f021af2c6`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.6 MB (3574345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f29133aa5ac2dc7f7caf05bec17a3f120b130b0a9f8a931b87d42bda5e00ee7`  
		Last Modified: Wed, 02 Apr 2025 21:53:15 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ceed22f9dc598f4a83d2574a1236b9eb55845a886691ca27d260af8e52d0a5b8`  
		Last Modified: Wed, 02 Apr 2025 21:53:15 GMT  
		Size: 7.9 KB (7921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e550c947cd96d7d5dbfd565fa3ae85434cb2481820d65ac92504416d056beea9`  
		Last Modified: Wed, 02 Apr 2025 21:53:15 GMT  
		Size: 112.6 KB (112643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47cfc80ff9405d7424905e6aa74f541ec5830861bef1b1218605b7d66fcec7b9`  
		Last Modified: Wed, 02 Apr 2025 21:53:15 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b0e844805fa1d0d457d1513e5b9d92436e3ab8e65548a31fbbc18ed1c2c743b`  
		Last Modified: Wed, 02 Apr 2025 21:53:16 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:fdca1b5f72932ee6bcfc55a37feb9c860f41b530efa43e63aec701932b3cf4da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.3 KB (92255 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58422f604e757b9c7c12519d56f597a89ae27e12f2339cf2cc67b4b5a19bb384`

```dockerfile
```

-	Layers:
	-	`sha256:2df4c6cf5666abc03d36c3ff177b1360db4c2531a9cd9923b404e7ff491bec9b`  
		Last Modified: Wed, 02 Apr 2025 21:53:15 GMT  
		Size: 77.9 KB (77905 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a7ad33b282085052031ca00d32c203a26ce45455daf796d327bb6cdbdcf3e8aa`  
		Last Modified: Wed, 02 Apr 2025 21:53:15 GMT  
		Size: 14.3 KB (14350 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:alpine` - linux; riscv64

```console
$ docker pull spiped@sha256:d93e8574bb82dd81dafcf25f7625ed7818c3a0e31066bbddf64006b83d78aba9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3459532 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11a635f525ddca22947829af6f197712b92c46682f40c9dbe63063aa381f9a9c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-riscv64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Wed, 02 Apr 2025 21:12:22 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
RUN apk add --no-cache libssl3 # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Wed, 02 Apr 2025 21:12:22 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
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
	-	`sha256:7df33f7ad8beb367ac09bdd1b2f220db3ee2bbdda14a6310d1340e5628b5ba88`  
		Last Modified: Fri, 14 Feb 2025 18:56:36 GMT  
		Size: 3.4 MB (3351439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a279c5ee271afcec6d3150e694efda4e5d36691f2d7ebe160636c0ab5a79b1ec`  
		Last Modified: Wed, 02 Apr 2025 21:53:03 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:015b70b993c8cc00dfe1e78ec875878062b451bd4ec2b326794c36444cb3105e`  
		Last Modified: Wed, 02 Apr 2025 21:53:03 GMT  
		Size: 7.9 KB (7904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87d040e2d542829d397e472ec2982c4857e357fe408f645da0693ef90321e2c7`  
		Last Modified: Wed, 02 Apr 2025 21:53:03 GMT  
		Size: 98.8 KB (98804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a0e579239e2446edd70320e6ec295380d239d0b2fb8045fbda0d7753c161f59`  
		Last Modified: Wed, 02 Apr 2025 21:53:03 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f11cda2eddc9aaf6455435d16dfafc74f718d637e59cb8c549b1310659e0f68`  
		Last Modified: Wed, 02 Apr 2025 21:53:04 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:6ef91094d879feac7520f82fdd946b0c798b74a1208a22482597eb403e08bd3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.2 KB (92248 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54c9ad713acd2272c15e5bd4e3532ba9df6910776b9db0bb063b585453f134ab`

```dockerfile
```

-	Layers:
	-	`sha256:b046cc017c3f020547f0314366d83fb03c8803458406b56bdd3904750ccb915b`  
		Last Modified: Wed, 02 Apr 2025 21:53:03 GMT  
		Size: 77.9 KB (77901 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:de0c335e4f12af3686646881008f04ba3bc438d3f15fbd38fbc3998d12514728`  
		Last Modified: Wed, 02 Apr 2025 21:53:03 GMT  
		Size: 14.3 KB (14347 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:alpine` - linux; s390x

```console
$ docker pull spiped@sha256:8e1cc9b73ed1eb178d6d22338fc661c8f3386b5d33086e11fca8483e38bc0123
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3573772 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9100e7b9db6a61a9d6818b301afcaf1e2753a632dba5e84dbdf9ea416bfe685b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-s390x.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Wed, 02 Apr 2025 21:12:22 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
RUN apk add --no-cache libssl3 # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Wed, 02 Apr 2025 21:12:22 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
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
	-	`sha256:c1a599607158512214777614f916f8193d29fd34b656d47dfc26314af01e2af4`  
		Last Modified: Fri, 14 Feb 2025 12:05:25 GMT  
		Size: 3.5 MB (3467567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:408f712244d227bb17176b3c9833183d94d7e5078a0071c6bb815f7c6acd044b`  
		Last Modified: Wed, 02 Apr 2025 21:52:19 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce3d2b3d93cf3babc3c2c43519cfac5c89b009dddf9f6329ccb604067e1c25d0`  
		Last Modified: Wed, 02 Apr 2025 21:52:19 GMT  
		Size: 7.9 KB (7919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:924f34f1a30b83eb8fe0d105f78a3ddb08291d7062c11e0a807ca3576dd2e638`  
		Last Modified: Wed, 02 Apr 2025 21:52:19 GMT  
		Size: 96.9 KB (96901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eaa01324514a5afcdaa7ba2727d95863ff56033c4f01975371de7c453ccdf8e1`  
		Last Modified: Wed, 02 Apr 2025 21:52:19 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b3162a370a5d0aff74dea2a1ddb49f120b995ec42d4b29c7bcb3c2f10a91fc1`  
		Last Modified: Wed, 02 Apr 2025 21:52:20 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:97f9242d5c7292f0782ce10a5d3a0549df652a9380a4f408bf9ede75116a30aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.2 KB (92170 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77e792a9515a7540fa01538367eccf186ff2dd8158a7dccadf4d37f635a3679c`

```dockerfile
```

-	Layers:
	-	`sha256:7c31c769211e50a701dc70ffd6261e2d0664c6f3b50fd444ad2665b22b1d6e5c`  
		Last Modified: Wed, 02 Apr 2025 21:52:19 GMT  
		Size: 77.9 KB (77871 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4988863227d01a39c5e290493124efb4304413f32a12e6879ffda4c3a86afd0d`  
		Last Modified: Wed, 02 Apr 2025 21:52:20 GMT  
		Size: 14.3 KB (14299 bytes)  
		MIME: application/vnd.in-toto+json

## `spiped:latest`

```console
$ docker pull spiped@sha256:eae5c3dfb8127c952913e3baabc3945915ed9fe7263a8928e60ee6f9f6c4d090
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
	-	linux; mips64le
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `spiped:latest` - linux; amd64

```console
$ docker pull spiped@sha256:c98a4a33bc9da8d56f0d5163a75842ce1c6c2db4ab21e159b3bde195afd59adc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.1 MB (37087849 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4355dd26bbc1d77f98e7c0ac73eacf4bc8915d2d20786bfbb00b17e33f21fa17`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 02 Apr 2025 21:12:22 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1747699200'
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
	-	`sha256:61320b01ae5e0798393ef25f2dc72faf43703e60ba089b07d7170acbabbf8f62`  
		Last Modified: Wed, 21 May 2025 22:27:39 GMT  
		Size: 28.2 MB (28225330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b236b995fe25e62e0a9b025d43ed6aeb0d706dda8c314117fcf6638ebdc7e2b`  
		Last Modified: Wed, 21 May 2025 23:20:12 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe7a90816c2d64d22fdbae87a108eb3343157d21eabfdd8a0362fb7c337c99ab`  
		Last Modified: Wed, 21 May 2025 23:20:12 GMT  
		Size: 2.4 MB (2402177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e20521234d5fd2df1eb25c23579bae7d5636fcce182618943e02ef5ab794963`  
		Last Modified: Wed, 21 May 2025 23:20:12 GMT  
		Size: 6.5 MB (6458802 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8c3b16ce6622a837772fdf6d18fc84b976e8694098211b2e9a4383a62931558`  
		Last Modified: Wed, 21 May 2025 23:20:12 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75351b1571732d8e2e27dfde274116dd0037459b25301366b27c9402ede4aae3`  
		Last Modified: Wed, 21 May 2025 23:20:13 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:latest` - unknown; unknown

```console
$ docker pull spiped@sha256:38fba8cf5966d1da5219266d88064e3aaceb887d32420638d2f0135dbbfd4ca5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3553217 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d442efde223bd171e1f3b5bdd7d6301e1ce2df0c1ea291f621d582ff0136ad75`

```dockerfile
```

-	Layers:
	-	`sha256:0c32ff8bf0f89bea9948bda0ad2c06ecc23437d5eefe99e0003e3c0eae7be3a8`  
		Last Modified: Wed, 21 May 2025 23:20:12 GMT  
		Size: 3.5 MB (3538177 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:faed6139c10365db1a206a064e87b5765026aa41bba89ab1a43fbcf5befd26ce`  
		Last Modified: Wed, 21 May 2025 23:20:12 GMT  
		Size: 15.0 KB (15040 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:latest` - linux; arm variant v5

```console
$ docker pull spiped@sha256:799111c4807c2fea831489b691e498f914d9a30c2f65688bf798574eec5db8c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.9 MB (32904241 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f9e5e8afcac44ab7363c93359b12a1c8dfb1867ed4df01c19777a222ce48c0f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 02 Apr 2025 21:12:22 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1747699200'
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
	-	`sha256:fab452a77ecb21a2e30922ab3eed19310b6d56763bcfc4e4bd31f28d9747f745`  
		Last Modified: Wed, 21 May 2025 22:27:58 GMT  
		Size: 25.8 MB (25756898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf5fcb13f4fae5c0701ae97175c1fde5a265e39ab7420ed78e63dc654b097e65`  
		Last Modified: Thu, 22 May 2025 01:12:54 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9556b3c226c521d39ced715dacdb0ddd196bf05f5846d3732d60e8a3f55a1de`  
		Last Modified: Thu, 22 May 2025 01:12:54 GMT  
		Size: 2.0 MB (1998268 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce40ec37f30dc6d7d5a1ed74cf1f1bae7f1a05eb87b99e62d9b4c27a28051931`  
		Last Modified: Thu, 22 May 2025 01:12:55 GMT  
		Size: 5.1 MB (5147533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4b23094f6c0b0b7beabfe549bc26fad9124341fe7251635a2286ad9d50c488e`  
		Last Modified: Thu, 22 May 2025 01:12:54 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f314f72e5ab08b9522e8df48d487f9c5448dd07a3c496be756e549d855a92e7c`  
		Last Modified: Thu, 22 May 2025 01:12:55 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:latest` - unknown; unknown

```console
$ docker pull spiped@sha256:9cf2a6d75f36284a1051b375e26316cc1e1a134adaff1f248a8d390552e88dd5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3524157 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3a141429766668432eef187e965dabf4459daabd05cb999129f21ee65ed20c6`

```dockerfile
```

-	Layers:
	-	`sha256:6a32a05c66630aa10a22096368b76df8bd67aaf342c8dd930619b45a1888cbc4`  
		Last Modified: Thu, 22 May 2025 01:12:54 GMT  
		Size: 3.5 MB (3509015 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:41b70d9c48c2c437462d07be8fc990b465281e5c418124d21004a253d959aa18`  
		Last Modified: Thu, 22 May 2025 01:12:54 GMT  
		Size: 15.1 KB (15142 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:latest` - linux; arm variant v7

```console
$ docker pull spiped@sha256:bd88168940017d415031d65c8b562a450fb598c60cf7e38ede2eebc4e622eed3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.7 MB (30679570 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:334bd5bd9fc6f29c24ec13b8cda836e7cb1c5e76c363b01a5ae63808e03e7cf0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 02 Apr 2025 21:12:22 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1747699200'
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
	-	`sha256:3726bc5cceb817ddfc7c2e1dbdfb4900fc6e27b680d63b8d751b06952753b6a1`  
		Last Modified: Wed, 21 May 2025 22:27:58 GMT  
		Size: 23.9 MB (23932922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28497644b53abef7026a25140f5b20b9e5f984102c735a18f9ad13b06d325d06`  
		Last Modified: Thu, 22 May 2025 02:11:46 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c06616ca963aeb60b1926e7a4505f5587eb632014d17e10775734237f64bfdd5`  
		Last Modified: Thu, 22 May 2025 02:11:46 GMT  
		Size: 1.9 MB (1856406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0454a735cab512a3994c19f6461e13b792aa7d4ae6f2f7b7beefad87c86e1619`  
		Last Modified: Thu, 22 May 2025 02:11:46 GMT  
		Size: 4.9 MB (4888699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c30c741ba1d6aa6d7e8a8bb49b3f73d5cfc41cc58cc9f1ee0d0222ef1eb61e3`  
		Last Modified: Thu, 22 May 2025 02:11:46 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efa2405c063638356b662a29deb560323db64a04302d8fb7b4e41e40832595be`  
		Last Modified: Thu, 22 May 2025 02:11:47 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:latest` - unknown; unknown

```console
$ docker pull spiped@sha256:67903915b9908ceec6eff9982d5e47b52aed66b921141fb35e158bef999cc642
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3523340 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e202a4f6c6a60f84bb42ff7184ed9b6fc409d848ff7be381fd3aeecfd2229b7e`

```dockerfile
```

-	Layers:
	-	`sha256:798416b4b99780fb82d37f69a61f55757da43446999fd396b2345a89f61b9717`  
		Last Modified: Thu, 22 May 2025 02:11:46 GMT  
		Size: 3.5 MB (3508198 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:16fe3f5accbcda69a4f3d2d1a7e95d1755dbdf53436e1dafd5996ebc9dc0ebda`  
		Last Modified: Thu, 22 May 2025 02:11:46 GMT  
		Size: 15.1 KB (15142 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:latest` - linux; arm64 variant v8

```console
$ docker pull spiped@sha256:d5cafb803c9a0da7ab4771f49d9cdb8a8cdcb3ff719bcbb09e016d458b52edae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.8 MB (35805923 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4433b4b2209f95a137ec9d4fc3da9f0399b1a927010b07100f4d2cb33f01eec6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 02 Apr 2025 21:12:22 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1747699200'
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
	-	`sha256:b16f1b16678093d11ecfece1004207a40f9bc1b7d9d1d16a070c1db552038818`  
		Last Modified: Wed, 21 May 2025 22:27:55 GMT  
		Size: 28.1 MB (28065280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58d7aa0e5553a8e1676ebb9a1e8b4e211d5e24d00e206dd06e9dc931036210a8`  
		Last Modified: Thu, 22 May 2025 02:26:31 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b01b22375091a64a96ee1ad4e57158b3b3a3403ba79cab1a56af7fcaf2c4fd4b`  
		Last Modified: Thu, 22 May 2025 02:26:32 GMT  
		Size: 2.2 MB (2247441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cf33c8dbe86b945cd509593f45ace969c1839a8dee7d1828092b41632af9837`  
		Last Modified: Thu, 22 May 2025 02:26:32 GMT  
		Size: 5.5 MB (5491661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa6e1ae6c666fd43ad0bb5cbd1d595c4f6774a7621a81e94f751dba1447227a4`  
		Last Modified: Thu, 22 May 2025 02:26:32 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25be54df2c26151d78b7c6bcc8b71f10a49ca87573849bc5561334e83d854f56`  
		Last Modified: Thu, 22 May 2025 02:26:33 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:latest` - unknown; unknown

```console
$ docker pull spiped@sha256:76bf26d851cd8fc562b888569d70024625766d5c1b77df5d31a5d5045d909e7a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3524578 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:232fb12c6174ddf70b733574174d96ac46893cfd76e8ecaf5a3d2a2d55139191`

```dockerfile
```

-	Layers:
	-	`sha256:863430707bd172ac83c08ecfc72f18ec0a9e85de22d979a70542342ba06ead69`  
		Last Modified: Thu, 22 May 2025 02:26:32 GMT  
		Size: 3.5 MB (3509405 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cc3c4313ab583feefd96c652f06140e88ab6b676b233c9b4c5ead13c712d32ce`  
		Last Modified: Thu, 22 May 2025 02:26:31 GMT  
		Size: 15.2 KB (15173 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:latest` - linux; 386

```console
$ docker pull spiped@sha256:de2d0f62127be81d4c417ee09c2e83dcc650d781e485052c53b4d83e7e41c305
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.6 MB (37566353 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e29b46d435dc73b21b5f638b8b87840b502cba5421b87b459851dd558cbb504`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 02 Apr 2025 21:12:22 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1747699200'
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
	-	`sha256:7d0eb60defa1a32d12e94bc0d7c2c578881c578aeec0c1d786ef5a19c72a34ab`  
		Last Modified: Wed, 21 May 2025 22:27:56 GMT  
		Size: 29.2 MB (29207487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fc34ae407ddfd8aa872313e98808f6d037d29874d733022ebeb03c21b075b9d`  
		Last Modified: Wed, 21 May 2025 23:19:31 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea1121e956c060196b27bf2cb1c7c4834fd0683b4d013d49729246105637c7e6`  
		Last Modified: Wed, 21 May 2025 23:19:31 GMT  
		Size: 2.4 MB (2400579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58c083d4e9d3c172b7e2dff742a55d190d7deea62d62e77c68be78ebe005756f`  
		Last Modified: Wed, 21 May 2025 23:19:31 GMT  
		Size: 6.0 MB (5956747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95924c7d3bb09f7d740e28a65b589259ca71ed83b9907221ab77e5710964fa84`  
		Last Modified: Wed, 21 May 2025 23:19:31 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af2e19c16d9e608f72faf9f7145bd18f20be31aa8254201cdc30e14098b0ab90`  
		Last Modified: Wed, 21 May 2025 23:19:32 GMT  
		Size: 336.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:latest` - unknown; unknown

```console
$ docker pull spiped@sha256:0e4e1e2182c7414a91dbedc4eee31dc2f23267ca32cb3bc1d1af586c79a15511
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3547159 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:488c249ee13b017bc6d2db92c2455dddf8636b7f8dda1f17d1c32ad46e3f1bc3`

```dockerfile
```

-	Layers:
	-	`sha256:5a933c5783118b861dc28e67218f04f000686e48be72186367702865e0819555`  
		Last Modified: Wed, 21 May 2025 23:19:31 GMT  
		Size: 3.5 MB (3532156 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a135b975223fb9944b6870b3f284f6d0e1276e5223c8b3790aec5292925ac030`  
		Last Modified: Wed, 21 May 2025 23:19:31 GMT  
		Size: 15.0 KB (15003 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:latest` - linux; mips64le

```console
$ docker pull spiped@sha256:e08a5f574ff6e4c4889083b74ad49f5f1fa5c4909a77fd7f0118f9e4537b2f64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.2 MB (36169243 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81d9271e2536f4b9e06788180f5f1808dc6e92f6183d5cf57c5ac1f4a073b894`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 02 Apr 2025 21:12:22 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1747699200'
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
	-	`sha256:48541e37cd82678078df221c38fde515e820c13a623449b699d224f60f15dae8`  
		Last Modified: Wed, 21 May 2025 22:28:22 GMT  
		Size: 28.5 MB (28511850 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3803a240d8e659370e2fab860baf71e6845bb1657afea9964a9455a06816584f`  
		Last Modified: Thu, 22 May 2025 06:14:35 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:058aa8bad24612579286f5eae085472a3a9f63436aa5165ce779f2d1f73c9e99`  
		Last Modified: Thu, 22 May 2025 06:14:36 GMT  
		Size: 1.8 MB (1842259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60712b0a5b50c33b45964a94fca078484dff5c1bc25928f8b19642a8fdddc723`  
		Last Modified: Thu, 22 May 2025 06:14:36 GMT  
		Size: 5.8 MB (5813592 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f03381e56cdea6e5c69ba962656f3b8ee6708f99bbbe90c8cb59805dec2821f`  
		Last Modified: Thu, 22 May 2025 06:14:35 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0030e45312f412d88429defd5484aa7c1354487911afb2c33273fd71e177e9ed`  
		Last Modified: Thu, 22 May 2025 06:14:36 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:latest` - unknown; unknown

```console
$ docker pull spiped@sha256:376d3c3cf802ddebdca18c0302bdc8f66c2a6eb3b23346b26c5205f7932dcce1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 KB (14897 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90459617b1bb9aa0a1d2cf5c37b8ad8d23c16eb4f14aacb08afabd9b233b117f`

```dockerfile
```

-	Layers:
	-	`sha256:307900282127ed9322c5ccab5de1df5096b6a0b07bd4395c5b9cb9b8599934bc`  
		Last Modified: Thu, 22 May 2025 06:14:35 GMT  
		Size: 14.9 KB (14897 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:latest` - linux; ppc64le

```console
$ docker pull spiped@sha256:a7321ff5fec2afbb779a0acf6da6d63f5c5d332938ad6bf260c611ae4a5b1c06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.1 MB (41093723 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15a62507992ef6fb0e12abeb88eb5ecf00ad31cb2d3eb2e89b8f8f14130d29e6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 02 Apr 2025 21:12:22 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1747699200'
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
	-	`sha256:701606535a7233566815cc9ad5f3e5853b443be5476286f6799008053dc2b03b`  
		Last Modified: Wed, 21 May 2025 22:28:16 GMT  
		Size: 32.1 MB (32066912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28a6c81eea611329e12a0cc8737d8ee2c5ada1b8e3aaef98d8acd2741b37d917`  
		Last Modified: Thu, 22 May 2025 07:17:33 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0fc1affdf757c274e7e67536481196cb883110fb5bfd979782fb8383777bfa6`  
		Last Modified: Thu, 22 May 2025 07:17:33 GMT  
		Size: 2.6 MB (2583887 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4db9a308ee6bef1c8241a16cb77c39894f524896d99e85f384dd7eb7a4756ff1`  
		Last Modified: Thu, 22 May 2025 07:17:33 GMT  
		Size: 6.4 MB (6441381 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c37f165cfd98289d815cf96acad45a8ed3cd5f2558537aebefbb0c7c359d0f9e`  
		Last Modified: Thu, 22 May 2025 07:17:33 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f805d8994580dac40f982b71b4ae42685005eeb1438bd76e132c9307532dedd`  
		Last Modified: Thu, 22 May 2025 07:17:34 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:latest` - unknown; unknown

```console
$ docker pull spiped@sha256:1cfcf23833ca373cc8000f5f9998d74ccf00ecca9ad0fb786e5172d2fcfd39af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3539050 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:789d0ff26873a3c16d1516a64b5521540d3e27924324dd582fbed08e96e970a9`

```dockerfile
```

-	Layers:
	-	`sha256:8b1a9eceb4ec95f4f5b6806a7ec405ea988499e1a2ec48b26ff0ede6b066b2a4`  
		Last Modified: Thu, 22 May 2025 07:17:33 GMT  
		Size: 3.5 MB (3523962 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ae9055586249d83d4bc0597f9cd6f6a21d3b9bf8c399b22bc90d82eed114d347`  
		Last Modified: Thu, 22 May 2025 07:17:33 GMT  
		Size: 15.1 KB (15088 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:latest` - linux; s390x

```console
$ docker pull spiped@sha256:313c5fbddb0f36164ff9ff07b8afb014aae1fba0aded0128c2058a6960b944dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.3 MB (34345786 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be0c786c61c197ff161771dfba4eecaca2e88d0ad743f2abe498c7758f082708`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 02 Apr 2025 21:12:22 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1747699200'
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
	-	`sha256:fb6e196ef379785f6b759a20e90d74fe0566b240771695f724c27a44aa6cd3ce`  
		Last Modified: Wed, 21 May 2025 22:28:38 GMT  
		Size: 26.9 MB (26882808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38ceb32ec1a8749e974fe5929ea6dff22bcee11dafd2fc667579323da38876f1`  
		Last Modified: Thu, 22 May 2025 00:53:41 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2f56657b11e71e77f7914f81ccb09da12e157355a9c2bfa3ad990780f7ee481`  
		Last Modified: Thu, 22 May 2025 00:53:41 GMT  
		Size: 2.1 MB (2069161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d37a680b670b7565d1e108f473912336f74759acbde356e1baffcebb55ab778`  
		Last Modified: Thu, 22 May 2025 00:53:41 GMT  
		Size: 5.4 MB (5392277 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec75588e715a05902adcfb5629f1851cf0d29ddf5ae3f281b75fdc0a40e98fb6`  
		Last Modified: Thu, 22 May 2025 00:53:41 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0e2d58562f243d49496f4f3e52abfbea3ebecc55c6401ecd80a648029bac830`  
		Last Modified: Thu, 22 May 2025 00:53:42 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:latest` - unknown; unknown

```console
$ docker pull spiped@sha256:5de6955b949dbe4e3cd91755329d2cb433e60f90fb15863b8bbab4c4f414cd9d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3541403 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d51372649bab5e76ddd19982bc703b786c8dc5b940231eeb5b6fa54327a2e1d`

```dockerfile
```

-	Layers:
	-	`sha256:7ddaee20724beee644d4580292cd7c349e170f436b4a509a76ba3ecb3b2337e0`  
		Last Modified: Thu, 22 May 2025 00:53:41 GMT  
		Size: 3.5 MB (3526363 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0371bae7cc54c2d437162fb10d62d7bc577205878fe8e5d855cbf8030eb4ca81`  
		Last Modified: Thu, 22 May 2025 00:53:41 GMT  
		Size: 15.0 KB (15040 bytes)  
		MIME: application/vnd.in-toto+json
