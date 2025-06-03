## `golang:bullseye`

```console
$ docker pull golang@sha256:abe2e2bb9bc0342dd1ba2f719af5c6b3859ca9ad93a7d9bcdd21310bda0327e1
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

### `golang:bullseye` - linux; amd64

```console
$ docker pull golang@sha256:cfd54e3a16ef87fb5480e86e868a04b0111779ad980eb580f233dc15e1c7277c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.3 MB (289275849 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2143dfcfe7a916200e4fd19b72fb253a755d95429f70ef107a985a02e09b34ce`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1747699200'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 06 May 2025 18:58:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 06 May 2025 18:58:00 GMT
ENV GOLANG_VERSION=1.24.3
# Tue, 06 May 2025 18:58:00 GMT
ENV GOTOOLCHAIN=local
# Tue, 06 May 2025 18:58:00 GMT
ENV GOPATH=/go
# Tue, 06 May 2025 18:58:00 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 06 May 2025 18:58:00 GMT
COPY /target/ / # buildkit
# Tue, 06 May 2025 18:58:00 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 06 May 2025 18:58:00 GMT
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
	-	`sha256:bea1587665e8725bc043c5ac54fc67dafad2d085ed7129198276b2853fb0ac40`  
		Last Modified: Tue, 03 Jun 2025 13:35:36 GMT  
		Size: 86.0 MB (86021740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92b00dc8dfbaa6cd7e39d09d4f1c726259b4d9a29c697192955da032f472d642`  
		Last Modified: Thu, 08 May 2025 17:04:42 GMT  
		Size: 79.0 MB (78981573 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:100a70b12070191e481ef1898cfb82acc049d9060090ce527e64b0647da21d08`  
		Last Modified: Tue, 03 Jun 2025 13:30:42 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:bullseye` - unknown; unknown

```console
$ docker pull golang@sha256:f3a14e9e591c269e8ff1a4c952eed6821e524b61fca6bb07b4fda095f99a3384
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10339334 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9087c9a63f5f796ac27fe365d270a30d99a71af88462fbf36a8d2f944719dcb2`

```dockerfile
```

-	Layers:
	-	`sha256:a62feee4134b1c4fbd456b7b478f38f85e38feb87216de9dcb3eb694ef45cb86`  
		Last Modified: Tue, 03 Jun 2025 20:02:08 GMT  
		Size: 10.3 MB (10312866 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b5adf2a26371156f4132a9606fe3ac488885a7ca5e30ec6b94289e61ef479dbe`  
		Last Modified: Tue, 03 Jun 2025 20:02:02 GMT  
		Size: 26.5 KB (26468 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:bullseye` - linux; arm variant v7

```console
$ docker pull golang@sha256:1491313f96457287f8f28386758f2d78d4d0e44be2de8096381a3c2d7a134dc4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **256.6 MB (256640881 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e769a7a5d5ca021d9966e40554e1e4584ed96488119e958141d192c268d6afe7`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1747699200'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 06 May 2025 18:58:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 06 May 2025 18:58:00 GMT
ENV GOLANG_VERSION=1.24.3
# Tue, 06 May 2025 18:58:00 GMT
ENV GOTOOLCHAIN=local
# Tue, 06 May 2025 18:58:00 GMT
ENV GOPATH=/go
# Tue, 06 May 2025 18:58:00 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 06 May 2025 18:58:00 GMT
COPY /target/ / # buildkit
# Tue, 06 May 2025 18:58:00 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 06 May 2025 18:58:00 GMT
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
	-	`sha256:5f32012e82345c04270d988b1e520857596a775a43ec4b22744ab73bea39d15b`  
		Last Modified: Thu, 08 May 2025 17:05:42 GMT  
		Size: 77.1 MB (77144440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3811d3a989fba9b20c3ce3443ea73e3f47804a41bf8678cf1567d250c46d145`  
		Last Modified: Tue, 03 Jun 2025 20:02:20 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:bullseye` - unknown; unknown

```console
$ docker pull golang@sha256:802a9a509df9355e1955ed282df96378fe35cc7780cba37ea9dbf04fd504e225
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.1 MB (10144635 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3fd7c3c9a9f2a5c3bc64c035ce08b0b683f3da00e342e8d6419a1adf77453bfd`

```dockerfile
```

-	Layers:
	-	`sha256:a7eb31529ce29c2026ea5743b9b2c08808490396aaf309d795423167cba39bdd`  
		Last Modified: Tue, 03 Jun 2025 20:02:37 GMT  
		Size: 10.1 MB (10118066 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:53d7ffeb42e56715c64a700b1c8ea6431b9a5f3292fd824640ba4b2381e829f0`  
		Last Modified: Tue, 03 Jun 2025 20:02:35 GMT  
		Size: 26.6 KB (26569 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:bullseye` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:1bfe009ce21ed14f3cc4a5b1039d4a0e97415741f04c288c512fbb6612b04bba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **279.5 MB (279514227 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45c305eaa7bed487f077ad9b4d271a8ec89513979c9a9bab268e50bbf86ce392`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1747699200'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 06 May 2025 18:58:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 06 May 2025 18:58:00 GMT
ENV GOLANG_VERSION=1.24.3
# Tue, 06 May 2025 18:58:00 GMT
ENV GOTOOLCHAIN=local
# Tue, 06 May 2025 18:58:00 GMT
ENV GOPATH=/go
# Tue, 06 May 2025 18:58:00 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 06 May 2025 18:58:00 GMT
COPY /target/ / # buildkit
# Tue, 06 May 2025 18:58:00 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 06 May 2025 18:58:00 GMT
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
	-	`sha256:f41519a12560c95f617eb3a5e39d7dd12557b5ea48e2dae042d1138650d3b8d2`  
		Last Modified: Tue, 03 Jun 2025 13:31:52 GMT  
		Size: 81.4 MB (81432142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ae64884db43f30f8dbc9ec3362124d99c8bad23b957254ac52fb30413bd14a7`  
		Last Modified: Thu, 08 May 2025 17:04:53 GMT  
		Size: 75.2 MB (75230554 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b8c1238106e45d523179deb4527c172ef373d3df6b8c6bb41fe5871397bb5d7`  
		Last Modified: Tue, 03 Jun 2025 13:31:32 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:bullseye` - unknown; unknown

```console
$ docker pull golang@sha256:69f985122debde7ff87b09808948c4d94520709b1b0a376059130b27c8a81b7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10340774 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92c5d2a88733869a81d521e943518afe3e2309f67ab5079bb10a9835f4586105`

```dockerfile
```

-	Layers:
	-	`sha256:941526b9f8b61c40379b72ebc7f4ead1421d6082b381a6fdbf1be0e738f669cf`  
		Last Modified: Tue, 03 Jun 2025 20:02:52 GMT  
		Size: 10.3 MB (10314172 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4b2e82a483d1611806af22c0fecdbe71fcc5cfd9e5f0046390ea19df26d07a63`  
		Last Modified: Tue, 03 Jun 2025 20:02:50 GMT  
		Size: 26.6 KB (26602 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:bullseye` - linux; 386

```console
$ docker pull golang@sha256:b86a58d85bf933948ab503f8bfa073b00d24439ec187858d2bc9d8cc319d654c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.4 MB (291351915 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80cc4d012c8196439549455a00a36f01d30869f2b728b480590ae3b1652efd94`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1747699200'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 06 May 2025 18:58:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 06 May 2025 18:58:00 GMT
ENV GOLANG_VERSION=1.24.3
# Tue, 06 May 2025 18:58:00 GMT
ENV GOTOOLCHAIN=local
# Tue, 06 May 2025 18:58:00 GMT
ENV GOPATH=/go
# Tue, 06 May 2025 18:58:00 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 06 May 2025 18:58:00 GMT
COPY /target/ / # buildkit
# Tue, 06 May 2025 18:58:00 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 06 May 2025 18:58:00 GMT
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
	-	`sha256:f880733c6fc49ea55099c8eadd81e71f053c11de47ab8d4ed46d3c748b593f53`  
		Last Modified: Tue, 03 Jun 2025 20:03:10 GMT  
		Size: 87.4 MB (87447830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db714197af43811f01d03462392675e848884e82b9483811c21c83a08d3e7834`  
		Last Modified: Thu, 08 May 2025 17:05:08 GMT  
		Size: 76.9 MB (76899879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60ea627bebee0e86caf0676e97dd5c810d6a91e05c3442b82c9bdb4272b303e6`  
		Last Modified: Tue, 03 Jun 2025 20:03:00 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:bullseye` - unknown; unknown

```console
$ docker pull golang@sha256:32e96780bfc963113473f6821d41d8834db0808c299bb41d5b7b0062b37cccfd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10328605 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5228bd9b533da9abe522460eb99add763bdd12916f96e8410ad44f64bd64a986`

```dockerfile
```

-	Layers:
	-	`sha256:2351195af91407edca7e3ff86dbe48f73ecd0eab04c7fab4916c72b75d985655`  
		Last Modified: Tue, 03 Jun 2025 20:03:20 GMT  
		Size: 10.3 MB (10302173 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:73f25a893c6e3a2741af2dbf3ebff17d06983adcdb13845c1171055d1583718e`  
		Last Modified: Tue, 03 Jun 2025 20:03:18 GMT  
		Size: 26.4 KB (26432 bytes)  
		MIME: application/vnd.in-toto+json
