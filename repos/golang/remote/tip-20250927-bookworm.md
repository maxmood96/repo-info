## `golang:tip-20250927-bookworm`

```console
$ docker pull golang@sha256:56fd4207c41dee7abc039e791aa69c05374c6740c719b4bd85212d8b990bef1b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 14
	-	linux; amd64
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

### `golang:tip-20250927-bookworm` - linux; amd64

```console
$ docker pull golang@sha256:2509e9f12747a2527c5440db8c29e1ab9b0bcf2f3506cf857bf5bda2ffa21493
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **313.2 MB (313167274 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d2f74cbbe99321e8a64e15988c730ad557127acffe0862382935d90873c7aa3`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1759104000'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Sep 2025 05:23:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Sep 2025 05:23:19 GMT
ENV GOTOOLCHAIN=local
# Mon, 29 Sep 2025 05:23:19 GMT
ENV GOPATH=/go
# Mon, 29 Sep 2025 05:23:19 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 29 Sep 2025 05:23:19 GMT
COPY /target/ / # buildkit
# Mon, 29 Sep 2025 05:23:19 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 29 Sep 2025 05:23:19 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:c6b11972fd12973831818babf60f1ffc1c4047507943d132dffc612884022858`  
		Last Modified: Mon, 29 Sep 2025 23:34:14 GMT  
		Size: 48.5 MB (48480557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db3dba6026a3c551d6b8e98308c073fff4fd569fd2fc61f21384cb996da82c9e`  
		Last Modified: Tue, 30 Sep 2025 01:43:53 GMT  
		Size: 24.0 MB (24025876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fb1b35a6fc14463ada297f3f0605409cbfe29368b38fd5d1e41f7dcf29bb6fb`  
		Last Modified: Tue, 30 Sep 2025 03:17:35 GMT  
		Size: 64.4 MB (64397411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af851db41feafa7a0ca6aad176753fddc95a1a625277350544fd9f7294c483d8`  
		Last Modified: Tue, 30 Sep 2025 09:57:15 GMT  
		Size: 92.4 MB (92401742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd392ccd6779e7a888cee1ecce65db01995a1886c75ae75a375deb44486fd071`  
		Last Modified: Mon, 29 Sep 2025 20:26:43 GMT  
		Size: 83.9 MB (83861530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5932b543ff61404483b7b9959e33fc10abbc49c8672e8780065e1112dc0c140`  
		Last Modified: Tue, 30 Sep 2025 09:57:07 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20250927-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:97b2e9ff3aed23a84b66c896b5e2f16c4ed6e4d94c6cb1023530a2169197d67b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10523345 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d16238d5accd91f6878e757902e2c5d9b45085b19ec49dd785c7a0e703989255`

```dockerfile
```

-	Layers:
	-	`sha256:d3e33eb633c2e506e02f37540eaa35c685a9d90edb833f0d9d0403dcd719fba7`  
		Last Modified: Wed, 01 Oct 2025 14:24:04 GMT  
		Size: 10.5 MB (10494916 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8af489b82f02490a6fe97751e3edfd926183ec9dd1b6e8c7b0a7378d1bf36b55`  
		Last Modified: Wed, 01 Oct 2025 14:24:05 GMT  
		Size: 28.4 KB (28429 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20250927-bookworm` - linux; arm variant v7

```console
$ docker pull golang@sha256:f7cce5dab173adced2c4b6b39e024bcf560565027d3b37ced408e0b78b66401d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.9 MB (272929009 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7a6c1ba3320c3b76b478fcc11a71ae1e7a04ae94a28cf1ded6a62103253ffb1`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1757289600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Sep 2025 05:23:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Sep 2025 05:23:19 GMT
ENV GOTOOLCHAIN=local
# Mon, 29 Sep 2025 05:23:19 GMT
ENV GOPATH=/go
# Mon, 29 Sep 2025 05:23:19 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 29 Sep 2025 05:23:19 GMT
COPY /target/ / # buildkit
# Mon, 29 Sep 2025 05:23:19 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 29 Sep 2025 05:23:19 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:66de9a3b6b96c15de3235377e1618295643161d16058e17bde51f54951c6ec21`  
		Last Modified: Mon, 08 Sep 2025 21:14:33 GMT  
		Size: 44.2 MB (44195998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0efd1e8889a5c39ed7ad3628cf08e3daff474f9ff5b33972b323c79f306440f8`  
		Last Modified: Mon, 08 Sep 2025 23:37:54 GMT  
		Size: 21.9 MB (21931079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1ad8fb006981127731180a5d548f700fd609cacd7e365cb66fbcaf2fd1e979c`  
		Last Modified: Tue, 09 Sep 2025 06:17:59 GMT  
		Size: 59.7 MB (59652826 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd9b903d00ac4a31d2e0ff4e58d5550b761883f9b9e9278a135008587ab44c78`  
		Last Modified: Mon, 29 Sep 2025 18:04:30 GMT  
		Size: 66.3 MB (66255113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2eea36933200b5f141ab18c26e141eacf675fe2778fc8f3cca0727236a934dcf`  
		Last Modified: Mon, 29 Sep 2025 18:04:27 GMT  
		Size: 80.9 MB (80893837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81e3534c65552e07990c7403bab56a0994ebfe6fc0e5bcecc9e35d004c7abc73`  
		Last Modified: Mon, 29 Sep 2025 18:04:23 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20250927-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:6e634c74db94971a41b7b73521e5382f0f294f6192894f4feb2a5db79b6d6b7d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10330155 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94cb8c6d2663b51dc17bfab4789affa40cf9ec48d87d841aecc285516d48ac41`

```dockerfile
```

-	Layers:
	-	`sha256:e2489fbb20f48a6812bd7619e510123cdaf06196d3ce1cf7fd2c70c33f25eb0a`  
		Last Modified: Mon, 29 Sep 2025 20:24:56 GMT  
		Size: 10.3 MB (10301614 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bfe77317a1217668a6a73616df9c0b9cce542c707e918fe5ba1e2815a26cb4e1`  
		Last Modified: Mon, 29 Sep 2025 20:24:57 GMT  
		Size: 28.5 KB (28541 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20250927-bookworm` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:24086b9d212cf00d759c89bb1e02287ab01339a36400ce9ba2f0ae9ec86643d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **302.6 MB (302611304 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19580cbd662fa7231ef3b393d352175ee150dbe99d473da5e46140d189f38c69`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1759104000'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Sep 2025 05:23:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Sep 2025 05:23:19 GMT
ENV GOTOOLCHAIN=local
# Mon, 29 Sep 2025 05:23:19 GMT
ENV GOPATH=/go
# Mon, 29 Sep 2025 05:23:19 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 29 Sep 2025 05:23:19 GMT
COPY /target/ / # buildkit
# Mon, 29 Sep 2025 05:23:19 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 29 Sep 2025 05:23:19 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:f7b43f0d0a8b99591b27457b368e70a582002600d32503fd07798c1bee7cd134`  
		Last Modified: Mon, 29 Sep 2025 23:34:16 GMT  
		Size: 48.4 MB (48358915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b261306f7eb1436ff95e3b9d948f5373b0dcf6ca1223aaa4c2fb303b03e744c`  
		Last Modified: Tue, 30 Sep 2025 00:56:21 GMT  
		Size: 23.6 MB (23594734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0a2f93f2f0e198bff671333b38213c36ed741b7f552b83c033cf63f52b58c0e`  
		Last Modified: Tue, 30 Sep 2025 01:19:31 GMT  
		Size: 64.4 MB (64371209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c48967be62093f7cad15543157ab67e005e7dba7d15b01e967265f529aa6617f`  
		Last Modified: Tue, 30 Sep 2025 03:20:15 GMT  
		Size: 86.5 MB (86471517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e94a779ece8baaa3a2b9ccff68843c683bfb8ad46a4cbd1f1c29fcc7f5e6802e`  
		Last Modified: Mon, 29 Sep 2025 18:02:35 GMT  
		Size: 79.8 MB (79814772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:171626f74e12ac6f6ad5fb2719689777f979a69c21d273fabb8222f905b0c4ab`  
		Last Modified: Tue, 30 Sep 2025 03:20:05 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20250927-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:67c8181e287da688f579ed03e844022ae06b35d3e4684b89d568dc52256c55c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10551305 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:894bc6148383bd9d77fae5a27a2027da434ea1a281ae6e07ba77cbbc1afe733c`

```dockerfile
```

-	Layers:
	-	`sha256:08ef6fdc5e13f468fefc4233d7e12998fb178b843ad05ce8510bbca74b54afa2`  
		Last Modified: Wed, 01 Oct 2025 11:36:26 GMT  
		Size: 10.5 MB (10522740 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b071adca3ba97dd66e43e82637eb614a8c51b7aee7c6aa7cb57bf5030b11bd1a`  
		Last Modified: Wed, 01 Oct 2025 11:36:27 GMT  
		Size: 28.6 KB (28565 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20250927-bookworm` - linux; 386

```console
$ docker pull golang@sha256:5262b9d5bebc9cd5f161629df0f61186c92ffe5d7c1922db13a2ca4c34821ae9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **312.9 MB (312915026 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:992d74cdd99d26e9612e7091039cfc9f101aca863c7654ee73787d0d8f61a1d0`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1759104000'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Sep 2025 05:23:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Sep 2025 05:23:19 GMT
ENV GOTOOLCHAIN=local
# Mon, 29 Sep 2025 05:23:19 GMT
ENV GOPATH=/go
# Mon, 29 Sep 2025 05:23:19 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 29 Sep 2025 05:23:19 GMT
COPY /target/ / # buildkit
# Mon, 29 Sep 2025 05:23:19 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 29 Sep 2025 05:23:19 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:2212ccc79525753c3f36994bd936e194dcec09d69b21786be4caa60f697693d8`  
		Last Modified: Mon, 29 Sep 2025 23:34:26 GMT  
		Size: 49.5 MB (49466651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:304a8a7ec291d92cb9effbdbbb7bb5864ca1d87b5e149ee45db584ed39cfc4eb`  
		Last Modified: Tue, 30 Sep 2025 00:20:19 GMT  
		Size: 24.9 MB (24860635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:963263603b7fae742ca79dc45230eee7f46d0be670e6738f50212dea9f77470b`  
		Last Modified: Tue, 30 Sep 2025 01:18:20 GMT  
		Size: 66.2 MB (66233435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce9596e82646759fd467f57d7961e3069c23472e42ef4069bbd7436339d093a8`  
		Last Modified: Tue, 30 Sep 2025 03:18:09 GMT  
		Size: 89.8 MB (89823459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fe29e58b8c06a986ae5ca92831db1a0d8e315d4140a28e6305b3b9513f262ee`  
		Last Modified: Mon, 29 Sep 2025 22:06:46 GMT  
		Size: 82.5 MB (82530689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5729c219a3192bbd686d846e3eea6446f70a09f4bbb4aa366816b4dcbfc537df`  
		Last Modified: Tue, 30 Sep 2025 03:18:03 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20250927-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:b93b6c01f9b393409b8c24220a9066bb4ddae15a633ef4cfbc8f235b91faf041
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10502895 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:549a023b7d0e518f7fa6b9aa2cbb5cdd3700fe66b12f298e421466e0dff293bf`

```dockerfile
```

-	Layers:
	-	`sha256:fee7ce8062ca907fb999cecf91c245cc2db2e6e2ad4f63b2f6e435e914e07524`  
		Last Modified: Wed, 01 Oct 2025 17:27:13 GMT  
		Size: 10.5 MB (10474499 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e869734479f864d0ef6769a6a944fe1c3d24712b2fc49852903fa4c27559f425`  
		Last Modified: Wed, 01 Oct 2025 17:27:13 GMT  
		Size: 28.4 KB (28396 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20250927-bookworm` - linux; mips64le

```console
$ docker pull golang@sha256:b534f5ea5ac7aa657420fc62db89ccbb7fb7e9d07feaba4db0a0f6abddf83b2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **284.4 MB (284393576 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e857def491c096c357a2662894e65689c623a9cce89e9d999f405878af80970`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1757289600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Sep 2025 05:23:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Sep 2025 05:23:19 GMT
ENV GOTOOLCHAIN=local
# Mon, 29 Sep 2025 05:23:19 GMT
ENV GOPATH=/go
# Mon, 29 Sep 2025 05:23:19 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 29 Sep 2025 05:23:19 GMT
COPY /target/ / # buildkit
# Mon, 29 Sep 2025 05:23:19 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 29 Sep 2025 05:23:19 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:32b0a76df497911c1adc85f7748d78b916d66733f6d0c87cdc6e9eb06317a625`  
		Last Modified: Mon, 08 Sep 2025 21:14:25 GMT  
		Size: 48.8 MB (48760780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b4b1410ff953e9baafd271cda9e27ee11dab33c7404024b5d7f0a941e7606c4`  
		Last Modified: Tue, 09 Sep 2025 04:22:26 GMT  
		Size: 23.6 MB (23611387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee49a4f2d47eca9eb39dcaf1cce76f6da099edc10cb571b790f8588eb5731614`  
		Last Modified: Tue, 09 Sep 2025 17:57:06 GMT  
		Size: 63.3 MB (63309380 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2399203c3f138949b9c739767b010496dee12253a25cf54ee57e03160f9ff7d2`  
		Last Modified: Tue, 09 Sep 2025 19:26:08 GMT  
		Size: 70.0 MB (69979855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b6844b679a5f5edf47ba45ef98949fc5932d7a14f3cc5aef05938c51a025fd7`  
		Last Modified: Mon, 29 Sep 2025 20:26:12 GMT  
		Size: 78.7 MB (78732016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9a7861b61a29a39a5085636624a6a7b69738cf34e68e5eaaba4df0c9634a5af`  
		Last Modified: Mon, 29 Sep 2025 18:11:07 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20250927-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:0b99ae93dd6ed1270ecdfef138ed70e68d6b698aae84ed351c42668fd0d3fa59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.2 KB (27167 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed754e511fd7a3bfaeec003dd3d21dd301c1651c709ea90b1744b5bf84a20cf4`

```dockerfile
```

-	Layers:
	-	`sha256:2802ef00fc404d01458a87965207d2e034c6fc4484f9a594096ff09284a5c999`  
		Last Modified: Mon, 29 Sep 2025 20:25:22 GMT  
		Size: 27.2 KB (27167 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20250927-bookworm` - linux; ppc64le

```console
$ docker pull golang@sha256:242061e636f4b2e6a00eff370fdaa145125a0ec9e857d2313f75b9f15a19dcc8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **319.5 MB (319467014 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e1468642998b945d18d70ab493d6061ce73f9345bb58e4a57d2bba3e8bc647b`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1757289600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Sep 2025 05:23:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Sep 2025 05:23:19 GMT
ENV GOTOOLCHAIN=local
# Mon, 29 Sep 2025 05:23:19 GMT
ENV GOPATH=/go
# Mon, 29 Sep 2025 05:23:19 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 29 Sep 2025 05:23:19 GMT
COPY /target/ / # buildkit
# Mon, 29 Sep 2025 05:23:19 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 29 Sep 2025 05:23:19 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:64b8116dd43c29a2a4aa3131cb4895af0a7267cc5883e3761556e54c369be9af`  
		Last Modified: Mon, 08 Sep 2025 21:22:08 GMT  
		Size: 52.3 MB (52326822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a66b92467bcafecf194d3c4efbee466dcb9b2010a0899f7d2b928f9afed69de0`  
		Last Modified: Tue, 09 Sep 2025 04:47:21 GMT  
		Size: 25.7 MB (25668980 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12aad37d5c4461745e898b391fa21157366a7f13cf28ff4bbb1e1434d87664d3`  
		Last Modified: Tue, 09 Sep 2025 15:23:55 GMT  
		Size: 69.8 MB (69845800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e533edb5c1951f178a74ec317d4b91d8db06d10d5f71b22a8b84191ac90e2a8`  
		Last Modified: Mon, 29 Sep 2025 18:12:39 GMT  
		Size: 90.4 MB (90417664 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c4682e6be6673e7aa33301c5b30874cd778044246d060f0fbf3c29475651b8b`  
		Last Modified: Mon, 29 Sep 2025 18:07:23 GMT  
		Size: 81.2 MB (81207592 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe525bfad3f2ec9302393345d69aa84361e7868a0fbe7ae2226cf711a5463a45`  
		Last Modified: Mon, 29 Sep 2025 18:12:13 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20250927-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:65e0bd1083adbcfe20f729d129690d91a5badd8dd60b6442e9491d204442fcac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10495872 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b9215fb16a51b6653a9e0f3d5e104fe5c9fa0deb414b055fb8fe5be8a5e966e`

```dockerfile
```

-	Layers:
	-	`sha256:aff588f88e20c6a31b1778082a348943b6ba38d86cb42f91a825386fd0d2aaea`  
		Last Modified: Mon, 29 Sep 2025 20:25:26 GMT  
		Size: 10.5 MB (10467397 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:da8f91d13a070e414e867739032dfe137c6a6fe24da1a43f41524ae064c65d99`  
		Last Modified: Mon, 29 Sep 2025 20:25:27 GMT  
		Size: 28.5 KB (28475 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20250927-bookworm` - linux; s390x

```console
$ docker pull golang@sha256:8585c532d58ec1be41cf7534bfeaeeeba945e96f39eccbaafdeb3e4c1c451dce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.1 MB (286107506 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2be3c375e137e131ffe46619f5ef132b925d3c3e38351495fcd88eea5622c13b`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1757289600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Sep 2025 05:23:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Sep 2025 05:23:19 GMT
ENV GOTOOLCHAIN=local
# Mon, 29 Sep 2025 05:23:19 GMT
ENV GOPATH=/go
# Mon, 29 Sep 2025 05:23:19 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 29 Sep 2025 05:23:19 GMT
COPY /target/ / # buildkit
# Mon, 29 Sep 2025 05:23:19 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 29 Sep 2025 05:23:19 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:67e2d91fae4fd9af13e4e364bf8120dcca7856e8273995cc0651acae70b27e8e`  
		Last Modified: Mon, 08 Sep 2025 21:18:01 GMT  
		Size: 47.1 MB (47137539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b60f0c679ec7b70d7fa5065a6e28276437547a7d43502b4e016c2e85aed8c84c`  
		Last Modified: Tue, 09 Sep 2025 01:20:52 GMT  
		Size: 24.0 MB (24023865 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93ed122f74eb7bf77b1109cb95e13be357040ccb22119f5f02e566a491bcc45e`  
		Last Modified: Tue, 09 Sep 2025 17:52:15 GMT  
		Size: 63.5 MB (63501842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f6b2573b7cad65080b47a2853b48cf03a97b7d5b2e7585be66bfadc8fda786c`  
		Last Modified: Mon, 29 Sep 2025 18:10:22 GMT  
		Size: 69.0 MB (69006102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02ed6e6981e4c029c9853a9bbba242bc2c9b41f236141c1f10c1334ce58549f0`  
		Last Modified: Mon, 29 Sep 2025 18:05:39 GMT  
		Size: 82.4 MB (82438002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:455d7b0e3655fd19c360c5c4cb77be688f6142478f05cfd133348dc2129a81bf`  
		Last Modified: Mon, 29 Sep 2025 18:10:17 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20250927-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:58ca9a21ccd9e4ff7432b2882a04864adade93cdfa00862cb2e343532febacd4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 MB (10355103 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12f2f61dd237639a16208a90d500c93ecb662e8d6839a75eeb96f11270c02462`

```dockerfile
```

-	Layers:
	-	`sha256:1336bf6a445cd5ac57bdcc6690e63589aaf859ac8f4c38e835910e86808c42d4`  
		Last Modified: Mon, 29 Sep 2025 20:25:33 GMT  
		Size: 10.3 MB (10326674 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1256bcfead2d14eafc3f0e8becfa03f4d885e5e2799fc6ad74b2ba62277da949`  
		Last Modified: Mon, 29 Sep 2025 20:25:34 GMT  
		Size: 28.4 KB (28429 bytes)  
		MIME: application/vnd.in-toto+json
