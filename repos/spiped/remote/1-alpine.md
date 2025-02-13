## `spiped:1-alpine`

```console
$ docker pull spiped@sha256:cff1ff69fc6f8904043ef5d9bb654e468a38fc671dedcecd1f568a1d61f1d634
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
$ docker pull spiped@sha256:2715ebbc20690dda6d438989f61f4eb4fb11162e932ba70cedc0c7f12b3c26f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3758631 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1ec86461245d72383c5662f686c25016cc299d589def9478af4205b484492be`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-x86_64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Sun, 26 Jan 2025 16:57:02 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
RUN apk add --no-cache libssl3 # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENV SPIPED_VERSION=1.6.3 SPIPED_DOWNLOAD_SHA256=70c53070dbbb10d1442754aeafb01b08ec829203d41023647dbf1a1435ee4a65
# Sun, 26 Jan 2025 16:57:02 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
VOLUME [/spiped]
# Sun, 26 Jan 2025 16:57:02 GMT
WORKDIR /spiped
# Sun, 26 Jan 2025 16:57:02 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 26 Jan 2025 16:57:02 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:1f3e46996e2966e4faa5846e56e76e3748b7315e2ded61476c24403d592134f0`  
		Last Modified: Tue, 14 Jan 2025 20:33:02 GMT  
		Size: 3.6 MB (3641715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b181c716ebe4d13478b33f2488cb40b954ba24081d61c5bc9d7f0605ba9d113`  
		Last Modified: Mon, 10 Feb 2025 19:01:15 GMT  
		Size: 962.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01ded10ce7d7c8e5d5eb05c5a7d5246a6a045996ee4f18dcc322d6600e68cd81`  
		Last Modified: Wed, 05 Feb 2025 18:07:44 GMT  
		Size: 7.9 KB (7907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84d46a15f052086577ecb502311cd9f4d176cd407ad00862e11dd7d6f8c2a868`  
		Last Modified: Wed, 05 Feb 2025 18:07:45 GMT  
		Size: 107.6 KB (107614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4b34221300809a19087f5d67a70e8167a72247feb52faa8c58a878f5af671d3`  
		Last Modified: Wed, 05 Feb 2025 18:07:44 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c89b10c18fcccf667446750b679723f2821a55bf5612caacbb8c510578e77e1`  
		Last Modified: Fri, 07 Feb 2025 21:20:26 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:6a640be7b02114db4704050ac59d1be28b1b8f1a10f0ce877865a41933bc6d1f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.1 KB (94117 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24283cd9a878c00f69d37c768fc27af4fe97d6fa56a0174f6b441c10746770b0`

```dockerfile
```

-	Layers:
	-	`sha256:f6e7df028e10774143b75638cf9a91ae4484ad9be9705a3ab7de160bfbeab308`  
		Last Modified: Tue, 28 Jan 2025 01:28:04 GMT  
		Size: 79.8 KB (79816 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:307857c2fc1847cc55f2ad19b9b6647658c5135c8b20a447ca114dfaf6cdb9b3`  
		Last Modified: Tue, 28 Jan 2025 01:28:04 GMT  
		Size: 14.3 KB (14301 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1-alpine` - linux; arm variant v6

```console
$ docker pull spiped@sha256:6f9bbe66f9f9620c0aad2b8b464d5f0912510b5fbbcce31e1458c51d8bdc36a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3462325 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24b357cad96475791645ca664e952dfc2be3a80db4daa6ebc50db2cdb2426d71`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-armhf.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Sun, 26 Jan 2025 16:57:02 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
RUN apk add --no-cache libssl3 # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENV SPIPED_VERSION=1.6.3 SPIPED_DOWNLOAD_SHA256=70c53070dbbb10d1442754aeafb01b08ec829203d41023647dbf1a1435ee4a65
# Sun, 26 Jan 2025 16:57:02 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
VOLUME [/spiped]
# Sun, 26 Jan 2025 16:57:02 GMT
WORKDIR /spiped
# Sun, 26 Jan 2025 16:57:02 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 26 Jan 2025 16:57:02 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:d3e229a4bb72770bd404e0f6590519a8e566146523e984834c6a3d82836f0069`  
		Last Modified: Tue, 14 Jan 2025 20:33:01 GMT  
		Size: 3.4 MB (3363879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fee72c2b1876a0156b7d396caf2dc29a0f8081b2b7a6733a3ff64d9527f586ea`  
		Last Modified: Tue, 21 Jan 2025 19:29:40 GMT  
		Size: 962.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1da6fb0facd6416135ae0db69e959ecf3e75cab6ea327aabb4ead163825dfc7`  
		Last Modified: Tue, 21 Jan 2025 19:29:40 GMT  
		Size: 7.9 KB (7914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0919c3817d8379bb41e1be06c4a9ce8b781a7c46fd9a118114bab8de444770a2`  
		Last Modified: Tue, 28 Jan 2025 01:40:36 GMT  
		Size: 89.1 KB (89138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:995e0d0ce3aa2cc891355694b9f4548ada6aa0f587ac1f8f95ff08b62f092ca3`  
		Last Modified: Tue, 28 Jan 2025 01:40:36 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c6048abcd79b046de58bebf91b3eb0b6d1d3cdef973e93188a86da2ad1ffe65`  
		Last Modified: Tue, 28 Jan 2025 01:40:36 GMT  
		Size: 336.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:3f840c3a9d83f847e5bb8879ed8d0fae64e2ab7849ae389421052f6925264c39
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.2 KB (14186 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71a31c54f0008afb75dde7c016b9771c6f37268270d33d98c57f6d4c46be550c`

```dockerfile
```

-	Layers:
	-	`sha256:e415d942102ceb25c19c03d57e7aad5f3e309c6a8aebe7422ef678a4f6a8c3c4`  
		Last Modified: Tue, 28 Jan 2025 01:40:36 GMT  
		Size: 14.2 KB (14186 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1-alpine` - linux; arm variant v7

```console
$ docker pull spiped@sha256:12817cd6117bed3cdf9e7e4b52de247dd1a87d2876d8dc7434e5115f0fc9a549
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3188067 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1cba0ff108ef4a8e8108d49bf7ccd596afac4a82110a7c14e80a001be5fa5bd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-armv7.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Sun, 26 Jan 2025 16:57:02 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
RUN apk add --no-cache libssl3 # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENV SPIPED_VERSION=1.6.3 SPIPED_DOWNLOAD_SHA256=70c53070dbbb10d1442754aeafb01b08ec829203d41023647dbf1a1435ee4a65
# Sun, 26 Jan 2025 16:57:02 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
VOLUME [/spiped]
# Sun, 26 Jan 2025 16:57:02 GMT
WORKDIR /spiped
# Sun, 26 Jan 2025 16:57:02 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 26 Jan 2025 16:57:02 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:824bc99f06f2c6bebc1172ff7e39d7a1cdbd077ec44632079a629f69e9db7abf`  
		Last Modified: Tue, 14 Jan 2025 20:33:57 GMT  
		Size: 3.1 MB (3097112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8ae962cfc489c298278551ba32bca1e0ed1f67cd05192848331b7c3ee926a77`  
		Last Modified: Tue, 21 Jan 2025 19:30:37 GMT  
		Size: 961.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1114d274ac423361940bdd6b0c7904acc23cb9903e6f1a2904b32a6b89f331c4`  
		Last Modified: Tue, 21 Jan 2025 19:30:37 GMT  
		Size: 7.9 KB (7915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51637362b800c4f96d7abb05ca7529a770947ee4b1e9623b35af4b936195f4a9`  
		Last Modified: Tue, 28 Jan 2025 01:37:32 GMT  
		Size: 81.6 KB (81648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b15074482593cb5d5f416eda5eadebe75a10ba5005975523c4c34e81f46e618`  
		Last Modified: Tue, 28 Jan 2025 01:37:33 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db71199d0efb2f82ed5530667b5595dd7a34230b43f8dd94dbe9c99654b1b9ae`  
		Last Modified: Tue, 28 Jan 2025 01:37:33 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:b5a94554ddb9da6514578c1b09075a2b4ab9c4410f3e3e231bae96919d45f4b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.3 KB (94253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2f515b3bed3192db05a2ad5b870421a369f4a33d6b7164dac00142ecf5bc150`

```dockerfile
```

-	Layers:
	-	`sha256:49f4a9e142d4f0bbdb2b6f12f002efa4735f8926b13589ba3a9a5a9ce1a027ef`  
		Last Modified: Tue, 28 Jan 2025 01:37:32 GMT  
		Size: 79.9 KB (79852 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5c72de5bccb3b20f12aaba84aa22f33c24e0ef214459867af7cbe28470672cb2`  
		Last Modified: Tue, 28 Jan 2025 01:37:32 GMT  
		Size: 14.4 KB (14401 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1-alpine` - linux; arm64 variant v8

```console
$ docker pull spiped@sha256:7bd7eff848bd7ecb4ebeafabcab07a01e40580fc27ad865b3b7dc5c3e8307bcd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4102233 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46380b40fc8cf495b0e4fe6bb439caf833e2bbaf42e79ccbccacbd21456f38f6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-aarch64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Sun, 26 Jan 2025 16:57:02 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
RUN apk add --no-cache libssl3 # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENV SPIPED_VERSION=1.6.3 SPIPED_DOWNLOAD_SHA256=70c53070dbbb10d1442754aeafb01b08ec829203d41023647dbf1a1435ee4a65
# Sun, 26 Jan 2025 16:57:02 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
VOLUME [/spiped]
# Sun, 26 Jan 2025 16:57:02 GMT
WORKDIR /spiped
# Sun, 26 Jan 2025 16:57:02 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 26 Jan 2025 16:57:02 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:52f827f723504aa3325bb5a54247f0dc4b92bb72569525bc951532c4ef679bd4`  
		Last Modified: Tue, 14 Jan 2025 20:33:00 GMT  
		Size: 4.0 MB (3992359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:987e71ee6cc5ab416ed1f0e49bb9a1696b4b5656b4d3fcc1feca517c7bbe5030`  
		Last Modified: Tue, 21 Jan 2025 19:50:56 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5faf545dafdf63442f66bf2d829b8ba0c5dd8fe81240a3298cbf9fee767c891`  
		Last Modified: Tue, 21 Jan 2025 19:50:56 GMT  
		Size: 7.9 KB (7921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7966823473fa57bd0c6c045474918109f56a52c519aa3ff2bbeb53a9bd43f890`  
		Last Modified: Tue, 28 Jan 2025 01:41:34 GMT  
		Size: 100.6 KB (100555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5487e20745df540295ba2a7d5c3230edfbc1657b671f349f920b261416279acc`  
		Last Modified: Tue, 28 Jan 2025 01:41:34 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9477716625dcd64617f5279d092cb746cef8275524ced557b548fac120fd1e9d`  
		Last Modified: Tue, 28 Jan 2025 01:41:35 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:bf674933baf7156a187fcab52df270880af433ca3e590a2d21c400137e505bb6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.3 KB (94308 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2e08d169c62b2f76c8f3d4eae8033be48d397c61a9f6edf7ecbdff2e94987c6`

```dockerfile
```

-	Layers:
	-	`sha256:c463f59b08554468e33ec7d67e5bf358a4422df9ba9c9e8a5c85545acbf01205`  
		Last Modified: Tue, 28 Jan 2025 01:41:34 GMT  
		Size: 79.9 KB (79872 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:55be9c8a835f959acbc00acf5a1a31119a99c2d3a92aba2088b8f3f0b9b7f56c`  
		Last Modified: Tue, 28 Jan 2025 01:41:34 GMT  
		Size: 14.4 KB (14436 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1-alpine` - linux; 386

```console
$ docker pull spiped@sha256:b310c392ab6f14391fb45b5af6ea15dbcbd23076e497d3d94c110d7b2087f4a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3592537 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4cbcf6cf269492e27066e7c7bbcb967e81247f0f3f3d09284672b28db7077ed8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-x86.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Sun, 26 Jan 2025 16:57:02 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
RUN apk add --no-cache libssl3 # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENV SPIPED_VERSION=1.6.3 SPIPED_DOWNLOAD_SHA256=70c53070dbbb10d1442754aeafb01b08ec829203d41023647dbf1a1435ee4a65
# Sun, 26 Jan 2025 16:57:02 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
VOLUME [/spiped]
# Sun, 26 Jan 2025 16:57:02 GMT
WORKDIR /spiped
# Sun, 26 Jan 2025 16:57:02 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 26 Jan 2025 16:57:02 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:dbaac2331104495e5df0818a1db05c402cfc13af140c75beccf51922d5f37ad5`  
		Last Modified: Tue, 14 Jan 2025 20:33:01 GMT  
		Size: 3.5 MB (3463126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:551001421d38a34944d1a96a5df258e75c389ab10abd35456cbb26915537f7fd`  
		Last Modified: Tue, 28 Jan 2025 01:28:28 GMT  
		Size: 962.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f72f77ecf249ccd9496811e0eb3c0cf489c7b7fdbfa9b09a800fc23ce9a5b86`  
		Last Modified: Tue, 28 Jan 2025 01:28:28 GMT  
		Size: 7.9 KB (7906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f78fa624f51e7a9f83ca9c71b40f866f13ab95ae1d6fb7f7fb39888ee08b23f5`  
		Last Modified: Tue, 28 Jan 2025 01:28:28 GMT  
		Size: 120.1 KB (120111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97b172e6f71ba4a3cd0b9d569cc026414ab5ff72c2c999047269348e63b5abaf`  
		Last Modified: Tue, 28 Jan 2025 01:28:28 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:102f42fb7496f67e41461243ea1a96721d75c60e36c3fc0bc0cc31f4a05a0a3f`  
		Last Modified: Tue, 28 Jan 2025 01:28:29 GMT  
		Size: 336.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:9927a6df5d8b7dbdb338658808aeddad5564ef5897b94b692df5dfa29b9abdef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.1 KB (94056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6d905998f2bfd41e52ca5677826d1ba128880dee6ab953a307411406c31b587`

```dockerfile
```

-	Layers:
	-	`sha256:aef24c41d2f2fe02d3f60245a4d8614488af106b27f1694638bb0aa63affdeec`  
		Last Modified: Tue, 28 Jan 2025 01:28:28 GMT  
		Size: 79.8 KB (79791 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e634c06318ef153f0dea3d1996b85ebfa8b5d1ae392ac0ae4aba4ce249a2d7ee`  
		Last Modified: Tue, 28 Jan 2025 01:28:28 GMT  
		Size: 14.3 KB (14265 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1-alpine` - linux; ppc64le

```console
$ docker pull spiped@sha256:884a0eb6ba4f64c3edda016b28d4bd99dba5200f5af5ac9cb6b72f18cb3a3a60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3695562 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18a09f14f9a1c5c8a4bc39f97cc1d4dfc2da04ebc3eb0e1c14ee25ecf135a583`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-ppc64le.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Sun, 26 Jan 2025 16:57:02 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
RUN apk add --no-cache libssl3 # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENV SPIPED_VERSION=1.6.3 SPIPED_DOWNLOAD_SHA256=70c53070dbbb10d1442754aeafb01b08ec829203d41023647dbf1a1435ee4a65
# Sun, 26 Jan 2025 16:57:02 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
VOLUME [/spiped]
# Sun, 26 Jan 2025 16:57:02 GMT
WORKDIR /spiped
# Sun, 26 Jan 2025 16:57:02 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 26 Jan 2025 16:57:02 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:244ac55e5ecd413dee99efe3ace7cb84420bfc9a727ec2327dae7805045d7470`  
		Last Modified: Tue, 14 Jan 2025 20:33:45 GMT  
		Size: 3.6 MB (3573601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2937ae7bb7a53c30739164fd8d6b1af5449b91bdeaacb11c09da360a795e967b`  
		Last Modified: Tue, 21 Jan 2025 19:31:28 GMT  
		Size: 962.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbed2b37b3a36511a8f8cde15ac74df12676c707a75cac7400604b533817a57b`  
		Last Modified: Tue, 21 Jan 2025 19:31:28 GMT  
		Size: 7.9 KB (7918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c2bb56ba626edfb899d02de6e190e018998d7573a673f6db87d5ef30de0a050`  
		Last Modified: Tue, 28 Jan 2025 01:43:33 GMT  
		Size: 112.6 KB (112648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85e93d7242196ad9ca14b560ce78c345dfa536c1a35de8044919beffdf4eb97a`  
		Last Modified: Tue, 28 Jan 2025 01:43:33 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd9e06feef4b6941cffa38f96ec7bf4e23040ea0baf7cf6f0a7345c46675eff3`  
		Last Modified: Tue, 28 Jan 2025 01:43:33 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:02029f95376d43c51ccddf3f8c8bbebb0671c8774aacfa19d44aee40f4773161
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.2 KB (92249 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4efe04e204e62e8c95b99341d61fcd033d068bcbce5868ae0ec1685e9f9da3e`

```dockerfile
```

-	Layers:
	-	`sha256:f198a76291582efc4f722539762e32a43b96a2acfb2de57f18adfa903c9b3c57`  
		Last Modified: Tue, 28 Jan 2025 01:43:33 GMT  
		Size: 77.9 KB (77899 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c32d956ebf079b702220519e8a308783736857197d7766e995bfbcd8c71dbf2c`  
		Last Modified: Tue, 28 Jan 2025 01:43:33 GMT  
		Size: 14.3 KB (14350 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1-alpine` - linux; riscv64

```console
$ docker pull spiped@sha256:756e00d72198e903bfd6356e80496c2936c64fa26149b3662c09c044393ac715
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3458360 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef3b076b4ea8c2964765a22bf8c5d8b2fb8141f171e1f335b628572524c3ab7a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-riscv64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Sun, 26 Jan 2025 16:57:02 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
RUN apk add --no-cache libssl3 # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENV SPIPED_VERSION=1.6.3 SPIPED_DOWNLOAD_SHA256=70c53070dbbb10d1442754aeafb01b08ec829203d41023647dbf1a1435ee4a65
# Sun, 26 Jan 2025 16:57:02 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
VOLUME [/spiped]
# Sun, 26 Jan 2025 16:57:02 GMT
WORKDIR /spiped
# Sun, 26 Jan 2025 16:57:02 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 26 Jan 2025 16:57:02 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:21a89fc8a7107842fa0935d999d700ca9a9df964110a7076d946b16f07a54de5`  
		Last Modified: Tue, 14 Jan 2025 20:35:37 GMT  
		Size: 3.4 MB (3350256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:410676c340782e10ad961429d12c4fc7bc22fe42e602f44af8fe4564583fa790`  
		Last Modified: Tue, 21 Jan 2025 19:47:10 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb03e5e951a5c0dc5098e3f3712ba683716c2830cd781627b8c589f37e35d49e`  
		Last Modified: Tue, 21 Jan 2025 19:47:10 GMT  
		Size: 7.9 KB (7900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25d4da436692d4ab0fd5035ee54eac03b05bf24df9aa3304a4cbb3e6bb7fb7de`  
		Last Modified: Tue, 28 Jan 2025 02:22:45 GMT  
		Size: 98.8 KB (98808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b11f3813ff058c0963785dcdc5c5f860f00840874673c02d724b273f844d53c`  
		Last Modified: Tue, 28 Jan 2025 02:22:45 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2d897b6a73cbb856ebfd058f311b8f0e39512fdede0d33460f38db93bb89b6c`  
		Last Modified: Tue, 28 Jan 2025 02:22:45 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:877a9cd3fe26f402674032844c26b7149200267a47a431963b72e3b4563d519c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.2 KB (92242 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93b37c1a9028694f866e7acc219fbf431ce5b97965a6f5489a14f064c84a12b1`

```dockerfile
```

-	Layers:
	-	`sha256:40546cca6e89cde845ebe9184ed940f3b4f38ba1e18049e3b36b047821e42722`  
		Last Modified: Tue, 28 Jan 2025 02:22:45 GMT  
		Size: 77.9 KB (77895 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:12a0377ea7376b0115517894b6c6f3d26482dcf699f270a21454fd463c994114`  
		Last Modified: Tue, 28 Jan 2025 02:22:45 GMT  
		Size: 14.3 KB (14347 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1-alpine` - linux; s390x

```console
$ docker pull spiped@sha256:496d1116424a4c78bad3fdd46c2db89305089a904ff0d42fcd07ffca4576a0b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3573080 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d32ae085c92ecf8421e7f161ab96951c317b5e771993504a3e09c8db10414930`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-s390x.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Sun, 26 Jan 2025 16:57:02 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
RUN apk add --no-cache libssl3 # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENV SPIPED_VERSION=1.6.3 SPIPED_DOWNLOAD_SHA256=70c53070dbbb10d1442754aeafb01b08ec829203d41023647dbf1a1435ee4a65
# Sun, 26 Jan 2025 16:57:02 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
VOLUME [/spiped]
# Sun, 26 Jan 2025 16:57:02 GMT
WORKDIR /spiped
# Sun, 26 Jan 2025 16:57:02 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 26 Jan 2025 16:57:02 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:b2af93686f9384c40cfe861d7173877bb2ee1675c3ee70181799693c34c8722f`  
		Last Modified: Tue, 14 Jan 2025 20:34:39 GMT  
		Size: 3.5 MB (3466867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d2d0ea9a1061fe840c13a046b93faaeb9dbcf4357f53a37b83747a395c05279`  
		Last Modified: Tue, 21 Jan 2025 19:32:37 GMT  
		Size: 962.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:068b14e90f05cd3c9537d5988b4bbe6abead4cac15a8b25d1959964036cdbb13`  
		Last Modified: Tue, 21 Jan 2025 19:32:37 GMT  
		Size: 7.9 KB (7909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3398f6409117bd2a57c6b304f740badcea613c5def606a7c072bcd0c73b061e0`  
		Last Modified: Tue, 28 Jan 2025 01:57:36 GMT  
		Size: 96.9 KB (96911 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a32ed7682792c020e13d8b547fdbb8c43a4956cb69969b8f5a2724202bbcb39d`  
		Last Modified: Tue, 28 Jan 2025 01:57:37 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff53239a6486b270ef8a57e32718cefe901786526573b780eb054d1ac053dc6e`  
		Last Modified: Tue, 28 Jan 2025 01:57:37 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:d66b26cdcd77f8b4437bcb47a340f63d583e754a794e2a822931eafa72152360
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.2 KB (92164 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6cdd7bbb43e56276987d1ae0048a6f92a4bca0ccdee9e8e670ddb9ea5e16cb9`

```dockerfile
```

-	Layers:
	-	`sha256:6fe581f275230ca3b53c4a9c2f8f4690c4edf45359ead5089d277953f8872d2a`  
		Last Modified: Tue, 28 Jan 2025 01:57:36 GMT  
		Size: 77.9 KB (77865 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c0280df9fd96cadb1c6e05a657e4d4caa094e820e2a85ddd2df85b36c0363d18`  
		Last Modified: Tue, 28 Jan 2025 01:57:36 GMT  
		Size: 14.3 KB (14299 bytes)  
		MIME: application/vnd.in-toto+json
