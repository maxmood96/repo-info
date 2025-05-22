## `spiped:latest`

```console
$ docker pull spiped@sha256:894d9a74af1bb7a0a7a4b32a0d61681989694bfe3dae23570b55480352f37feb
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
$ docker pull spiped@sha256:7b59b966359c15b2b444cbd7db131386a7bd57e1dcffb93bbc319b5bfd1116e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.2 MB (36170549 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77e331a266da0c6ae932d4a46a93bc6085a6a8408db10e34893ab94963a9ea6f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 02 Apr 2025 21:12:22 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1745798400'
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
	-	`sha256:901060d913f9d0bbb82847b3b60c3a263ed0dac4f75aa29161be6ed89b57082a`  
		Last Modified: Mon, 28 Apr 2025 21:11:19 GMT  
		Size: 28.5 MB (28514138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:424c53ab0b8fbaf65ba71ecf4003eb5d59260ac79469c0f090d2acbd3a577252`  
		Last Modified: Tue, 29 Apr 2025 12:41:15 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb901dbf0b4bc02e5e5e16116ee625a0e30ef562f1bb2707f4a18985f2897fe8`  
		Last Modified: Tue, 29 Apr 2025 12:41:16 GMT  
		Size: 1.8 MB (1841158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8aca531cd4b48c4f018e7a911425831e28e194e34eef49e617ac1216c2963a38`  
		Last Modified: Tue, 29 Apr 2025 12:41:16 GMT  
		Size: 5.8 MB (5813709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:461db4f5a67d86277d0b693957dc1f5b75079d3538234993e8f9f3aeb8184615`  
		Last Modified: Tue, 29 Apr 2025 12:41:15 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:928f440acf684d8378871bc6e47c211a13b245168a67d79f8bfbc742d3d02ea0`  
		Last Modified: Tue, 29 Apr 2025 12:41:16 GMT  
		Size: 341.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:latest` - unknown; unknown

```console
$ docker pull spiped@sha256:ad6245b303b1fe57aadb74ea8e7a71d0bf3bb86714ae2112cd84eeefeb713181
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 KB (14897 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4998ab04c42cd0a2fd7b0b4fe8fe53f1958a3162b716f9d8db258c02930761ad`

```dockerfile
```

-	Layers:
	-	`sha256:fd825a1c2831fa7094c155ed9d51c8496b2b0e835e0844ff4484032552517961`  
		Last Modified: Tue, 29 Apr 2025 12:41:15 GMT  
		Size: 14.9 KB (14897 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:latest` - linux; ppc64le

```console
$ docker pull spiped@sha256:b3481a69259fc79afd6bcf8a9d9433cc7dec92b5533a07274a05c87a2c088b19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.1 MB (41093464 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b3cf7f67f4d4b62632f0bb8718e0be15e6482718b4327cef25b41bc61dd4744`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 02 Apr 2025 21:12:22 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1745798400'
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
	-	`sha256:a53e75e229cd115b5249f6e60d40785f1bfff9e7ccc2df65672a6f67afd0e348`  
		Last Modified: Mon, 28 Apr 2025 21:22:04 GMT  
		Size: 32.1 MB (32068443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84219294fde49be16d67f322c956a8591f887d5a369a0b6c90a3d71020d297fe`  
		Last Modified: Tue, 29 Apr 2025 00:22:37 GMT  
		Size: 1.1 KB (1105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27e9db802ba5b0d2379fc74dc8d63d6cbd64031480e7458135748cb067e792eb`  
		Last Modified: Tue, 29 Apr 2025 00:22:37 GMT  
		Size: 2.6 MB (2582110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52fba0c2ee0a529d162909e00db89c1cfce676424e22852f0c72f0a4cbf87679`  
		Last Modified: Tue, 29 Apr 2025 00:22:37 GMT  
		Size: 6.4 MB (6441373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbc9501fc3b3e44597af142e453dce7403abae453404134ae71178b606681237`  
		Last Modified: Tue, 29 Apr 2025 00:22:37 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcbf06ee6bf6913e2b02996f2cb81a09d3ae7fdd8f3d460f76fc0315bc2422ce`  
		Last Modified: Tue, 29 Apr 2025 00:22:38 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:latest` - unknown; unknown

```console
$ docker pull spiped@sha256:dccf1ba9b950b7808ce26ffa6f8f5373f6ba920c8df60c53363aaaca1eba6a9c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3517939 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebeb3c6befdcc9a5c7ce521b070767547198cab6d20428c6a190956dd8bc9441`

```dockerfile
```

-	Layers:
	-	`sha256:45c3aaf97565733a46f03a8ddd5ddc61bdb35d3a410af4b72ccb547747befcd3`  
		Last Modified: Tue, 29 Apr 2025 00:22:37 GMT  
		Size: 3.5 MB (3502851 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fd9ff82401dc83c13fd1550a9364a937072b87e9557f8878f6faeca97b1a25ea`  
		Last Modified: Tue, 29 Apr 2025 00:22:37 GMT  
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
