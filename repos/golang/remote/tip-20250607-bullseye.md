## `golang:tip-20250607-bullseye`

```console
$ docker pull golang@sha256:82138db0bf3fb6a43be0d3ca56636824d5f62f08516b63827ae31c16fa5f705f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `golang:tip-20250607-bullseye` - linux; amd64

```console
$ docker pull golang@sha256:844564cd05ee2bc02c56bb2a98733aa4668d515c4e3d992613c47b7e07622a46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **293.5 MB (293456733 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca15017445b4993b2430958ecd7b6f9295cdc58657f597d4857cb885fdc64642`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1749513600'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Jun 2025 05:23:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Jun 2025 05:23:21 GMT
ENV GOTOOLCHAIN=local
# Mon, 09 Jun 2025 05:23:21 GMT
ENV GOPATH=/go
# Mon, 09 Jun 2025 05:23:21 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Jun 2025 05:23:21 GMT
COPY /target/ / # buildkit
# Mon, 09 Jun 2025 05:23:21 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 09 Jun 2025 05:23:21 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:72049b7b8f2615e8b5167a09158b78d10a3b79a1ac60ce60cb5528a8c7723090`  
		Last Modified: Tue, 10 Jun 2025 23:24:16 GMT  
		Size: 53.8 MB (53754782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cac8156a957a8b63a670ed89130a2e1eedf5c1b2a939f33a952c4159b4ebcb0a`  
		Last Modified: Tue, 10 Jun 2025 23:36:44 GMT  
		Size: 15.8 MB (15765139 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2678613884c2f141cc551880b1a1587f0c890606a900bbac5a1ace2645be657`  
		Last Modified: Wed, 11 Jun 2025 00:02:35 GMT  
		Size: 54.8 MB (54757363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d82486623c2d6d840b4cb7ad98c2b067fa96cbf0d634dbb523cf1346e35e0666`  
		Last Modified: Wed, 11 Jun 2025 05:29:36 GMT  
		Size: 86.0 MB (86021733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7cc635c4b2a5c576a8a73069e117f29a377ce38e81427c57d725fc1f78f5ae3`  
		Last Modified: Mon, 09 Jun 2025 22:08:44 GMT  
		Size: 83.2 MB (83157558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f8d157fb74e46a3e6c616e58816ac5ab7ced61b407196d267923db5d8ed668b`  
		Last Modified: Wed, 11 Jun 2025 02:33:01 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20250607-bullseye` - unknown; unknown

```console
$ docker pull golang@sha256:ac41d27ec833353e9ee6ec3e9b788f104ab38df041b199847cb27ab51cabf2b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10509221 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06112d2ad5c7b450925d53404aa1c58257f11cffd50db65aa60ccf5e30f8d57e`

```dockerfile
```

-	Layers:
	-	`sha256:dc0ba706dc431af5275f1d2a76cbba7e2de87be05901ebca6bd892cc3708e0e3`  
		Last Modified: Wed, 11 Jun 2025 05:23:30 GMT  
		Size: 10.5 MB (10482164 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5a8137a2ebd45ef262f1c904834f9d9b6d1d702a854aa1cb8c6c474ecc1ded5c`  
		Last Modified: Wed, 11 Jun 2025 05:23:31 GMT  
		Size: 27.1 KB (27057 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20250607-bullseye` - linux; arm variant v7

```console
$ docker pull golang@sha256:fe9d17bac3b48895c632f5d5ff9dc767320c387b98474c49069ca71bd2da6cca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **259.8 MB (259752290 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2e95817a8e41513329427d760070a269a0318acc65bd33385133b52333345af`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1747699200'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Jun 2025 05:23:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Jun 2025 05:23:21 GMT
ENV GOTOOLCHAIN=local
# Mon, 09 Jun 2025 05:23:21 GMT
ENV GOPATH=/go
# Mon, 09 Jun 2025 05:23:21 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Jun 2025 05:23:21 GMT
COPY /target/ / # buildkit
# Mon, 09 Jun 2025 05:23:21 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 09 Jun 2025 05:23:21 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:2bf062f1f44f96722293994387f4b88016e2f0a9f49c7f09b2ceffefc7717199`  
		Last Modified: Tue, 03 Jun 2025 13:43:06 GMT  
		Size: 49.0 MB (49041988 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:933c7aef3dae867caad0cbafef5672fb39317c04b3bf8bff0868bf265098c4de`  
		Last Modified: Tue, 03 Jun 2025 14:32:56 GMT  
		Size: 14.9 MB (14880519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c0144e65734487c61a592b9ecd7d576c77bc270bd5d65049de36718f77416c6`  
		Last Modified: Tue, 03 Jun 2025 14:32:58 GMT  
		Size: 50.6 MB (50631322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fd4739ceb6e38b56a017a3579cc385de56e1cf7fc98c2c4b4dabd966a9c123d`  
		Last Modified: Tue, 03 Jun 2025 20:02:27 GMT  
		Size: 64.9 MB (64942454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfdbba4495ee849a32b1868921c9f94170c36c552299b715ecef8d63f110b4be`  
		Last Modified: Mon, 09 Jun 2025 22:17:51 GMT  
		Size: 80.3 MB (80255849 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92dd3652dc88d5b8bc2663675d89ded540553e154120fcb81d57e3da7fd94287`  
		Last Modified: Mon, 09 Jun 2025 22:20:45 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20250607-bullseye` - unknown; unknown

```console
$ docker pull golang@sha256:5a4228eb82cd9cd91a9636ae8f720146d158b29d423e692af214e4e8de79ac46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10314538 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f36de113d603dbdafc802910c39e3e512706142b27a2beffa560e25dc375323d`

```dockerfile
```

-	Layers:
	-	`sha256:c947696cac47cdf9fa93359743ff8907674fea2cbc6ad9b595f1a592a3ecc975`  
		Last Modified: Mon, 09 Jun 2025 23:24:42 GMT  
		Size: 10.3 MB (10287373 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:df356b462a304b1ac905d5dd69b9f213aa74223adf56051f1ea297ab1ea22873`  
		Last Modified: Mon, 09 Jun 2025 23:24:43 GMT  
		Size: 27.2 KB (27165 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20250607-bullseye` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:08fb25f7cc9831269184c87493e54a45e3ec990d2d4edb0ae3c29fee28e3b11a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **288.3 MB (288347207 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3ae52d0837402a0421d448521733b9d509c8b2e604c78792cdb09f68099554d`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1747699200'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Jun 2025 05:23:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Jun 2025 05:23:21 GMT
ENV GOTOOLCHAIN=local
# Mon, 09 Jun 2025 05:23:21 GMT
ENV GOPATH=/go
# Mon, 09 Jun 2025 05:23:21 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Jun 2025 05:23:21 GMT
COPY /target/ / # buildkit
# Mon, 09 Jun 2025 05:23:21 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 09 Jun 2025 05:23:21 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:b2737025fe8da5b868f566cb4e3dc3330028cee06c83db854f56467eca6e09b8`  
		Last Modified: Tue, 03 Jun 2025 13:30:20 GMT  
		Size: 52.2 MB (52247755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a602f78cf8d696db9521d18affb7ecdb79ff690533efae26e3bdb1544cb1752`  
		Last Modified: Tue, 03 Jun 2025 13:31:09 GMT  
		Size: 15.8 MB (15750382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98c1b27af19f7550ac0d9c38bf6bcf26ba7eb53984e7e5e0886342816133c76e`  
		Last Modified: Tue, 03 Jun 2025 13:30:17 GMT  
		Size: 54.9 MB (54853236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8aa4f13c9f2ba35edbb5cc356335d05db12609ba76252d1006e9168557548c91`  
		Last Modified: Tue, 03 Jun 2025 13:56:16 GMT  
		Size: 86.4 MB (86354667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9018e4f62f0690ad9682f8c2f1f9edb62acf90f09cff841cc366e0feec33aa3`  
		Last Modified: Mon, 09 Jun 2025 22:08:25 GMT  
		Size: 79.1 MB (79141010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b05c89154610626b65148803a95e2ed8373baeab60a8066d4bd2e08cb131aa3`  
		Last Modified: Mon, 09 Jun 2025 22:10:01 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20250607-bullseye` - unknown; unknown

```console
$ docker pull golang@sha256:5732cf2c66dd734d7a9b87a088df03608e636eb4888e553bcecd573efd0b2bc7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10511880 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c694ff0ca014b8e4b38dadc3547fc4e2d7835b253db63e1c89265328076da09`

```dockerfile
```

-	Layers:
	-	`sha256:5fe17a92ee0720d1d7c652b576a700f45858672a74dd71fa1cc0204ae7c844b5`  
		Last Modified: Mon, 09 Jun 2025 23:24:51 GMT  
		Size: 10.5 MB (10484688 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c13f3b8cead39000cce402d9e541630f6e6f9b5646daa72ce386f4446e925507`  
		Last Modified: Mon, 09 Jun 2025 23:24:52 GMT  
		Size: 27.2 KB (27192 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20250607-bullseye` - linux; 386

```console
$ docker pull golang@sha256:4b126417d8baf4a39fa0cf71bc76556bd72320dedfb51ce0f789b1a892c63e4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **296.4 MB (296352515 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97f4a39027da13758f1d2c5d9ab51407124e656b3dced1c87ebcfa8c14431ea0`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1749513600'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Jun 2025 05:23:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Jun 2025 05:23:21 GMT
ENV GOTOOLCHAIN=local
# Mon, 09 Jun 2025 05:23:21 GMT
ENV GOPATH=/go
# Mon, 09 Jun 2025 05:23:21 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Jun 2025 05:23:21 GMT
COPY /target/ / # buildkit
# Mon, 09 Jun 2025 05:23:21 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 09 Jun 2025 05:23:21 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:e516fc486459913e83d7e1f35cc45b6e3bed5cabe1eab9f1598665e153a14d6f`  
		Last Modified: Tue, 10 Jun 2025 23:24:19 GMT  
		Size: 54.7 MB (54690012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10e7c1ed34c380b4c9e9f08e94b0f7b9bf90a0e8c42de246cb4b2159e2126fef`  
		Last Modified: Wed, 11 Jun 2025 00:00:47 GMT  
		Size: 16.3 MB (16268617 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e3a34392e433938214bbf2cba34365a474d819c470686803059c6d8390cf680`  
		Last Modified: Wed, 11 Jun 2025 01:13:31 GMT  
		Size: 56.0 MB (56049939 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d34f7537f2d9ae29f2ebb3d220b8c8405490be041aa88ba050cece3367509647`  
		Last Modified: Wed, 11 Jun 2025 02:20:53 GMT  
		Size: 87.4 MB (87448062 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:390b4524b05c1706d1b72e8575c65245c59334a3e5a6eaa54af3aee803a8d9ca`  
		Last Modified: Tue, 10 Jun 2025 00:21:15 GMT  
		Size: 81.9 MB (81895727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:569f5bada9beb331334bb795c30e7d6924068f130f75d37bd70866636bf043c0`  
		Last Modified: Wed, 11 Jun 2025 02:20:43 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20250607-bullseye` - unknown; unknown

```console
$ docker pull golang@sha256:073dda2a17b6001b09a35bb66e17d0a6018798aa20d4582209f7e5f7837b9aee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10498525 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5643dd1a0344e958ab2315d268d81ae29f237c4c345aecdd66658328b46836b`

```dockerfile
```

-	Layers:
	-	`sha256:3eee3b0c4e6121d49e8ddcbbae7f01a55cc5a06bfb4f63b26f7d86fea1bca999`  
		Last Modified: Wed, 11 Jun 2025 05:23:49 GMT  
		Size: 10.5 MB (10471501 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6037c597926436d3b64d0c1ee10c14043ac09fa231e45cdc500d0a9dd2597c21`  
		Last Modified: Wed, 11 Jun 2025 05:23:50 GMT  
		Size: 27.0 KB (27024 bytes)  
		MIME: application/vnd.in-toto+json
