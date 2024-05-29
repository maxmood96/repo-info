## `spiped:1-alpine`

```console
$ docker pull spiped@sha256:73abb9981f67761ab2d1af997e78bedeaaa1ee6a369e8033d1d6e9b9bca32b98
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 8
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; riscv64
	-	linux; s390x

### `spiped:1-alpine` - linux; amd64

```console
$ docker pull spiped@sha256:07e3b4b9207f89998e572bed22a7f7954cc6492c8d8f21be279963f2cff7fc9b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3855418 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9201d18866bb1ce0bb8b2535a09c9746ee4710bbfc2f2c1ab380e1ab464c476`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 22 May 2024 18:18:11 GMT
ADD file:e3abcdba177145039cfef1ad882f9f81a612a24c9f044b19f713b95454d2e3f6 in / 
# Wed, 22 May 2024 18:18:12 GMT
CMD ["/bin/sh"]
# Fri, 24 May 2024 02:34:47 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Fri, 24 May 2024 02:34:48 GMT
RUN apk add --no-cache libssl3
# Fri, 24 May 2024 02:34:48 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Fri, 24 May 2024 02:34:59 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Fri, 24 May 2024 02:34:59 GMT
VOLUME [/spiped]
# Fri, 24 May 2024 02:34:59 GMT
WORKDIR /spiped
# Fri, 24 May 2024 02:34:59 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Fri, 24 May 2024 02:34:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 24 May 2024 02:34:59 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:d25f557d7f31bf7acfac935859b5153da41d13c41f2b468d16f729a5b883634f`  
		Last Modified: Wed, 22 May 2024 18:18:35 GMT  
		Size: 3.6 MB (3622094 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4b65a0cef07ed27e2dfa105666ab73da30ede8da8ec1d6a4aff22c6d64a5905`  
		Last Modified: Fri, 24 May 2024 02:35:13 GMT  
		Size: 984.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b79dadf24bbac85056299fdc71ca82aa8bdc1d5e88edfbaded02869e0b489815`  
		Last Modified: Fri, 24 May 2024 02:35:13 GMT  
		Size: 7.6 KB (7573 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef14f04bed6dd2107fa0c48cff8ac4c26d9c72582967c37fba6b6641ee53628a`  
		Last Modified: Fri, 24 May 2024 02:35:13 GMT  
		Size: 224.3 KB (224301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c512d6a117eb4435d549b47b5d8cae78953c96f8a91d9420fa806decbd655936`  
		Last Modified: Fri, 24 May 2024 02:35:13 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b384b7559504371850eed3815c8be24a48bbf848e4f8181a30e96853c6af3f1`  
		Last Modified: Fri, 24 May 2024 02:35:13 GMT  
		Size: 337.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1-alpine` - linux; arm variant v6

```console
$ docker pull spiped@sha256:5d9da313669f8f0048ec2e9eab6bf853600283a81b4ca96e692b10bdb3c72bdd
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3583090 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63ca2a16641057fa841612e468f82aa3487de7f1198cfad469dcf99446926816`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 22 May 2024 17:56:54 GMT
ADD file:5103c8a26cd2dfa76f84be7e1886df206b2131d04cf3079dfd1b6385cc796428 in / 
# Wed, 22 May 2024 17:56:55 GMT
CMD ["/bin/sh"]
# Sat, 25 May 2024 00:49:29 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Sat, 25 May 2024 00:49:30 GMT
RUN apk add --no-cache libssl3
# Sat, 25 May 2024 00:49:31 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Sat, 25 May 2024 09:53:04 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Sat, 25 May 2024 09:53:05 GMT
VOLUME [/spiped]
# Sat, 25 May 2024 09:53:05 GMT
WORKDIR /spiped
# Sat, 25 May 2024 09:53:05 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Sat, 25 May 2024 09:53:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 25 May 2024 09:53:05 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:b0da55d51ed2f4a2e9c4e3ca1e420bac26a1a37098e2f1437841049c51df7320`  
		Last Modified: Wed, 22 May 2024 17:57:17 GMT  
		Size: 3.4 MB (3365055 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cc224dd751252e9181a8cfc90f8cc478007dd80c5fcaf9c0e7365c5c5690cd6`  
		Last Modified: Sat, 25 May 2024 09:53:13 GMT  
		Size: 989.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d844205e2c4ed91d86c9d3b93ba94f73a6802f7d95e2637329e3171f1596051`  
		Last Modified: Sat, 25 May 2024 09:53:13 GMT  
		Size: 7.6 KB (7584 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf50783437084d308ea037a336c6b2adde912eb87c2d0910d52f8259d2ccd361`  
		Last Modified: Sat, 25 May 2024 09:53:13 GMT  
		Size: 209.0 KB (208990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e446f34a875f7f58e4f0ff44cdfc7c4fa476269342e24e5cd4b066bf0fd56db5`  
		Last Modified: Sat, 25 May 2024 09:53:13 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0973efe8383e26e010949975c4c577788da3b889331852a53e975fdd74591d73`  
		Last Modified: Sat, 25 May 2024 09:53:13 GMT  
		Size: 343.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1-alpine` - linux; arm variant v7

```console
$ docker pull spiped@sha256:bb684581db4fff4bf8a7b702e687e87a39ef3f4c6e10fd9596e77557450ddb7c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4266581 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9892e4679dcc1613fd8093b4783dc01f6fab1ea780a484b16f5ea70cb8c4f79f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Sat, 27 Jan 2024 00:15:02 GMT
ADD file:46464fd9557915ea434ccac5505de2df053c83ad36eb366d24d2ec8a8c74d466 in / 
# Sat, 27 Jan 2024 00:15:02 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 11:09:17 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Sat, 16 Mar 2024 11:09:20 GMT
RUN apk add --no-cache libssl1.1
# Sat, 16 Mar 2024 11:09:20 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Sat, 16 Mar 2024 11:09:33 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Sat, 16 Mar 2024 11:09:33 GMT
VOLUME [/spiped]
# Sat, 16 Mar 2024 11:09:34 GMT
WORKDIR /spiped
# Sat, 16 Mar 2024 11:09:34 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Sat, 16 Mar 2024 11:09:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 16 Mar 2024 11:09:35 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:19ffc66afc416e14f8733d680abfae4e1f6a3c90ae23c045857121fea320862b`  
		Last Modified: Sat, 27 Jan 2024 00:15:39 GMT  
		Size: 2.9 MB (2901392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6db0c643fe65a6404026b608dc6ae819a269e584901244c2e6cc7a70bf1e7d2`  
		Last Modified: Sat, 16 Mar 2024 11:09:51 GMT  
		Size: 1.3 KB (1273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16fc56cd1ee88e25c88d32ea53031b271337cf4fc319a3dd22c5fc91981a16b7`  
		Last Modified: Sat, 16 Mar 2024 11:09:52 GMT  
		Size: 1.2 MB (1163902 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e379b621d32076252239cb1ed60146f28aa41a66300eac408664d85b3ee06b51`  
		Last Modified: Sat, 16 Mar 2024 11:09:52 GMT  
		Size: 199.5 KB (199546 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9abe02cd52b4f7ac85fff10e652ab29ff74236c7288cd0351e29cefa5e34176d`  
		Last Modified: Sat, 16 Mar 2024 11:09:52 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37645012d50bbc320b56dda0788847ce06a8dcdc0cc9c1bf7f1902c6357f412c`  
		Last Modified: Sat, 16 Mar 2024 11:09:51 GMT  
		Size: 342.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1-alpine` - linux; arm64 variant v8

```console
$ docker pull spiped@sha256:ee22a4376163469a5478a77d3dd086da10e96bab2415e92cb213ce08dee1701e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4314784 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7161188ee6d2c07e0c2f1fc2a6fb5a02c590873473230245a1f9a46ad49f8791`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 22 May 2024 18:17:27 GMT
ADD file:ceadd994c6d8900884c4a44aa76cf187336921e29afeaa017c4a3d1fc066a6a3 in / 
# Wed, 22 May 2024 18:17:28 GMT
CMD ["/bin/sh"]
# Fri, 24 May 2024 01:17:09 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Fri, 24 May 2024 01:17:10 GMT
RUN apk add --no-cache libssl3
# Fri, 24 May 2024 01:17:10 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Fri, 24 May 2024 01:17:18 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Fri, 24 May 2024 01:17:18 GMT
VOLUME [/spiped]
# Fri, 24 May 2024 01:17:18 GMT
WORKDIR /spiped
# Fri, 24 May 2024 01:17:18 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Fri, 24 May 2024 01:17:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 24 May 2024 01:17:18 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:94747bd812346354fd5042870b6e44e5406880a4e6b5736a9cf9c753110df11b`  
		Last Modified: Wed, 22 May 2024 18:17:47 GMT  
		Size: 4.1 MB (4086776 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc4f90aa9bfc773d7ce92ca3bf50d8ae635c7d9f78892f0b93b65803c9d33b1a`  
		Last Modified: Fri, 24 May 2024 01:17:29 GMT  
		Size: 989.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d4b9605849ac73a8379695848d7a0520038c21b1c2ebf31e40beda1b53f9fe9`  
		Last Modified: Fri, 24 May 2024 01:17:30 GMT  
		Size: 7.6 KB (7583 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5099b3f4d764b8b79d94713e5d3320da1b4822ef27f9af0f3149655d12aa47d`  
		Last Modified: Fri, 24 May 2024 01:17:29 GMT  
		Size: 219.0 KB (218970 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08b21ae2d8249251716fb673e50c2e09cda47bc565d7eebd5fe3efa053d5eac6`  
		Last Modified: Fri, 24 May 2024 01:17:29 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:236abc558b7bcb1712f41161eaaaecbf399e7eaf1b2aa8094cddd334c4f6872e`  
		Last Modified: Fri, 24 May 2024 01:17:29 GMT  
		Size: 337.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1-alpine` - linux; 386

```console
$ docker pull spiped@sha256:ac9655daf19c8c0147be28fd461895ef3a1c79db08b596ed2d588b6a3c816504
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.8 MB (4826343 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a20ddadfdc5396a002ff71f7430163abb731e6890e7a49c16d77c5649e58dba2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Sat, 27 Jan 2024 00:38:23 GMT
ADD file:947294f5c09da3491734668abe74ce7c80f0034ae27d570578242b03ab6876a7 in / 
# Sat, 27 Jan 2024 00:38:23 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 05:07:58 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Sat, 16 Mar 2024 05:08:00 GMT
RUN apk add --no-cache libssl1.1
# Sat, 16 Mar 2024 05:08:00 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Sat, 16 Mar 2024 05:08:13 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Sat, 16 Mar 2024 05:08:13 GMT
VOLUME [/spiped]
# Sat, 16 Mar 2024 05:08:13 GMT
WORKDIR /spiped
# Sat, 16 Mar 2024 05:08:13 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Sat, 16 Mar 2024 05:08:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 16 Mar 2024 05:08:13 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:282e237e8e01cf628ae91590e0a44bcf58df98bbe01e9e62dadf2e94cd6301a0`  
		Last Modified: Sat, 27 Jan 2024 00:38:59 GMT  
		Size: 3.2 MB (3239065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7508806baeb68406329423224090a40940d296f944edc857b31946a1e0b2eb94`  
		Last Modified: Sat, 16 Mar 2024 05:08:25 GMT  
		Size: 1.3 KB (1270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d20d8676a55b9005ca166d422eafb181f4e0dd038fe4912102eb35278224336b`  
		Last Modified: Sat, 16 Mar 2024 05:08:25 GMT  
		Size: 1.4 MB (1353903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3a80dfc8677984adef1a26dd3a1761ea6cb42ae6b57a49cdf27458771baa848`  
		Last Modified: Sat, 16 Mar 2024 05:08:25 GMT  
		Size: 231.6 KB (231638 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62b2b104abfcd98f8e2aaab8be718007a2219883fc986e109873f9e777847b30`  
		Last Modified: Sat, 16 Mar 2024 05:08:25 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dae79c3a2a70ad960e3ab773fce80eea1b3cda5966da88a81b40895af47cda41`  
		Last Modified: Sat, 16 Mar 2024 05:08:25 GMT  
		Size: 338.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1-alpine` - linux; ppc64le

```console
$ docker pull spiped@sha256:91493c946db15eba4386b0b2a820f943dc3d29f55a1de28e4591c91dd27ac7d6
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4931989 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df4db55030112f4e2638c067c584a4edcb1f7199152e94e0a613f5f39364da85`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Sat, 27 Jan 2024 00:27:42 GMT
ADD file:9adfbd84cce437533ba2c9cac17cd508a477a1a94523005875b2f04ddac20112 in / 
# Sat, 27 Jan 2024 00:27:42 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 07:12:03 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Sat, 16 Mar 2024 07:12:06 GMT
RUN apk add --no-cache libssl1.1
# Sat, 16 Mar 2024 07:12:06 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Sat, 16 Mar 2024 07:12:15 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Sat, 16 Mar 2024 07:12:16 GMT
VOLUME [/spiped]
# Sat, 16 Mar 2024 07:12:16 GMT
WORKDIR /spiped
# Sat, 16 Mar 2024 07:12:17 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Sat, 16 Mar 2024 07:12:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 16 Mar 2024 07:12:17 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:08384a48688a8dcab52a530af58b9cbe1f870dd11e2ef2d0d645d658bd2ac537`  
		Last Modified: Sat, 27 Jan 2024 00:28:24 GMT  
		Size: 3.3 MB (3348487 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a46d463955fc02ba4f84639b3d043165a5c28c566c0a20033980b4f4c3faf760`  
		Last Modified: Sat, 16 Mar 2024 07:12:32 GMT  
		Size: 1.3 KB (1271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d43d878c69e3e371c35fe73ad27732a539ee52fe55145d7de6488abe3925845`  
		Last Modified: Sat, 16 Mar 2024 07:12:32 GMT  
		Size: 1.4 MB (1361743 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:357a363ee7e9be874a2cc0b6e345b8cc3922279c96fb5b46f586c41a80116c97`  
		Last Modified: Sat, 16 Mar 2024 07:12:32 GMT  
		Size: 220.0 KB (220020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a490aa09932ee227df910f1be26cc62c155abd010823121b17001e617c2d652`  
		Last Modified: Sat, 16 Mar 2024 07:12:32 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a702b0f7fce70e7a512f362b2fb211b08209ee54a29ed22266c16335f6d579b`  
		Last Modified: Sat, 16 Mar 2024 07:12:32 GMT  
		Size: 339.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1-alpine` - linux; riscv64

```console
$ docker pull spiped@sha256:cd5a4621afff483f36101ea9ebae88f7dcf25f86c2309d723bbd483be19ceafe
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3592834 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e812e801b6ae16522a84a7ab6f7556c16c0a15341d272fce6510208bf865f58`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 22 May 2024 17:57:29 GMT
ADD file:adedc612a3543e3a541be8e74c994fc3782e0f4a762ca77a1e29e6abfc81d7d8 in / 
# Wed, 22 May 2024 17:57:29 GMT
CMD ["/bin/sh"]
# Wed, 29 May 2024 04:22:05 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Wed, 29 May 2024 04:22:11 GMT
RUN apk add --no-cache libssl3
# Wed, 29 May 2024 04:22:12 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Wed, 29 May 2024 04:23:18 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Wed, 29 May 2024 04:23:18 GMT
VOLUME [/spiped]
# Wed, 29 May 2024 04:23:19 GMT
WORKDIR /spiped
# Wed, 29 May 2024 04:23:20 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Wed, 29 May 2024 04:23:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 29 May 2024 04:23:21 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:f280e85d15153a8f10f3fa47dd9d639e7a8fc6c1c8795d7123a32a0c36f16f55`  
		Last Modified: Wed, 22 May 2024 17:57:48 GMT  
		Size: 3.4 MB (3368560 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39c0c4f99ba3a3946abd6a4741459ac597ecf8393da29611c0c72c127c3c8fc6`  
		Last Modified: Wed, 29 May 2024 04:23:44 GMT  
		Size: 962.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffc5b031480a0383a5f02d1f22612813b1ffa3cfb8ac50bda5bca486fdbf7499`  
		Last Modified: Wed, 29 May 2024 04:23:44 GMT  
		Size: 7.6 KB (7584 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf1e17de0f3b7417191ea5c8f7779379c7965a389e87d7fddba3c8d28d6f854c`  
		Last Modified: Wed, 29 May 2024 04:23:44 GMT  
		Size: 215.3 KB (215290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6f7d27f6c07e7feb513acf854ddaee65e51ce92daf7c3918f1625aaec5fa14b`  
		Last Modified: Wed, 29 May 2024 04:23:44 GMT  
		Size: 95.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:668e20db4a7ebcccd41cb86827aeddf9cb92dfc787970bf9623b4779f5bf8559`  
		Last Modified: Wed, 29 May 2024 04:23:44 GMT  
		Size: 343.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1-alpine` - linux; s390x

```console
$ docker pull spiped@sha256:8dec41cbe81f417096082fdaa31bb95bdd7e36dfec4cc462a7e9462205ed2402
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3681097 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7fee6531c62c7ffe07b640d5ab5b763be7303e38a61c81bb6524855dec0ca243`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 22 May 2024 18:34:06 GMT
ADD file:97335440b04aac71ca64b9c889e64d1da1913c788e108b6481155248fc670f8b in / 
# Wed, 22 May 2024 18:34:07 GMT
CMD ["/bin/sh"]
# Fri, 24 May 2024 00:57:58 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Fri, 24 May 2024 00:57:59 GMT
RUN apk add --no-cache libssl3
# Fri, 24 May 2024 00:57:59 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Fri, 24 May 2024 00:58:05 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Fri, 24 May 2024 00:58:05 GMT
VOLUME [/spiped]
# Fri, 24 May 2024 00:58:05 GMT
WORKDIR /spiped
# Fri, 24 May 2024 00:58:05 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Fri, 24 May 2024 00:58:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 24 May 2024 00:58:06 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:3b8747b05489980f63da1d2b8e5a444c55777f69540394397b0bc1c76c3e41f2`  
		Last Modified: Wed, 22 May 2024 18:34:48 GMT  
		Size: 3.5 MB (3460340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c7d2acf9b7465edffd5a10fedbf230b30c81cb8b13eb3c7d97b4ba3dc542d17`  
		Last Modified: Fri, 24 May 2024 00:58:22 GMT  
		Size: 987.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17ffbc970af29f74dd00097324a2d43d0cd4ea77aee3bf1217ffe3b76397a889`  
		Last Modified: Fri, 24 May 2024 00:58:22 GMT  
		Size: 7.6 KB (7585 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bec7c94b7827b61d57438499589e4d6f5b1320a6bd0eee1a2226d3f8d22d81aa`  
		Last Modified: Fri, 24 May 2024 00:58:22 GMT  
		Size: 211.7 KB (211719 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ad9a1996f006554091faad0788cedfe9c37ce442aefa430c0d7b7a7eb402280`  
		Last Modified: Fri, 24 May 2024 00:58:22 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:531998ea71dc30b5a286d51c478a1a6f9ff8db7afc074c302dfe6bef2f5da69d`  
		Last Modified: Fri, 24 May 2024 00:58:22 GMT  
		Size: 337.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
