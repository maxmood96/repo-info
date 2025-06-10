## `golang:tip-20250607-bullseye`

```console
$ docker pull golang@sha256:6172c10358c5b68026b687678d15cd8b274f7f2a56d93d10208757d2f1c6bf03
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
$ docker pull golang@sha256:31dd6976c1ae2405a98e52fc23a63fd4fbad35c8a35c8947cfa0d1de2c3ee1ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **299.2 MB (299159046 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e48b0d622d2d4eff7645f9d9409fbda60f275c4336039e851f14adbef8d2342`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1747699200'
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
	-	`sha256:54107f2de180b7b6e9f909d2f1c6c18e10c700a6bd80a035d931768b06bb2905`  
		Last Modified: Tue, 03 Jun 2025 13:30:17 GMT  
		Size: 53.8 MB (53750195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06b6c820e694a6c19c297492ef4009391c7dfc83ecae735895f31a89e78b31fc`  
		Last Modified: Tue, 03 Jun 2025 13:30:14 GMT  
		Size: 15.8 MB (15764874 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a69a02035012d2783a66ac7ecc549af09c1718d81affa5f9c39abcf969da971`  
		Last Modified: Tue, 03 Jun 2025 13:30:17 GMT  
		Size: 54.8 MB (54757308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fde86e5a044bc37ecac674b4f7944f36231c2617f5a368fb824d3615023d0cc9`  
		Last Modified: Mon, 09 Jun 2025 22:08:58 GMT  
		Size: 91.7 MB (91728953 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7cc635c4b2a5c576a8a73069e117f29a377ce38e81427c57d725fc1f78f5ae3`  
		Last Modified: Mon, 09 Jun 2025 22:08:44 GMT  
		Size: 83.2 MB (83157558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e16f249f8e0b82237c22ce1155b41cfcae4c9111eabb8eec35ae658a58b8faa`  
		Last Modified: Mon, 09 Jun 2025 22:08:53 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20250607-bullseye` - unknown; unknown

```console
$ docker pull golang@sha256:ac223fcdeca439e99db647c98285120e4d0eef66925ed8451eabe0234acdb6fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10510462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:291ef623868af1923ab479a902c0b345ae70b53d8e09128549c213da5fa1835c`

```dockerfile
```

-	Layers:
	-	`sha256:31cd6912e4cd4b04bd9746b013fd1966130e835dd0cb403ad6fb708a59ff2e99`  
		Last Modified: Mon, 09 Jun 2025 23:24:33 GMT  
		Size: 10.5 MB (10483405 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:de50d7b5527e76710a9255c506b319aac036b6a75e5970e4105f1aec38528c87`  
		Last Modified: Mon, 09 Jun 2025 23:24:34 GMT  
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
$ docker pull golang@sha256:e664e722e035048262808d8a5e0f83b10ed0db2fac31f5c160ad72bfe94fb24d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.6 MB (301626318 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a1ddd5f7b83fb1fd13413bb13b1b2a57378dba2ef3e2f9174c1ca0dd8a0d794`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1747699200'
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
	-	`sha256:6c1a0525f904d970c0719d0ae307af1606eed8214108a47c9374eaffab5c71ae`  
		Last Modified: Tue, 03 Jun 2025 13:41:46 GMT  
		Size: 54.7 MB (54685782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bde5c2ebb13d7ca154f5cc8b4e26e7e3a669b8bac689ec15851b65e299a0fd6`  
		Last Modified: Tue, 03 Jun 2025 14:32:56 GMT  
		Size: 16.3 MB (16268487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72e052669a7dd77fed659f1b6d3fcf5171929214e8821aaf28744160fb71f4f1`  
		Last Modified: Tue, 03 Jun 2025 14:32:57 GMT  
		Size: 56.0 MB (56049779 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3786822eb8f9d183ea8c8c720cb265ee0bbb2915b014b89c87bd9738876ccfe`  
		Last Modified: Mon, 09 Jun 2025 22:09:37 GMT  
		Size: 92.7 MB (92726385 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:390b4524b05c1706d1b72e8575c65245c59334a3e5a6eaa54af3aee803a8d9ca`  
		Last Modified: Mon, 09 Jun 2025 22:08:55 GMT  
		Size: 81.9 MB (81895727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99ca9ee7185f6995d2dc922f0e5e50dc442a1a43ff3b80d3068a783856496268`  
		Last Modified: Mon, 09 Jun 2025 22:14:54 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20250607-bullseye` - unknown; unknown

```console
$ docker pull golang@sha256:a81e03fb63c0b9f94561c16b2dda29278f78d542895602c75781ed9cee313caf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10499766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2415e6ce9cd4fccf9a1efa086168055d6a60496becb7c04df3d878ad5711974`

```dockerfile
```

-	Layers:
	-	`sha256:ff292c116cd30223288660c903055ac6b594318e68f24f3d69dead06c39daa63`  
		Last Modified: Mon, 09 Jun 2025 23:24:59 GMT  
		Size: 10.5 MB (10472742 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d39ebe49feb3bcac685c59b56659637303395176f1e966a79e47ba7f8434168c`  
		Last Modified: Mon, 09 Jun 2025 23:25:00 GMT  
		Size: 27.0 KB (27024 bytes)  
		MIME: application/vnd.in-toto+json
