## `golang:tip-20250927-bookworm`

```console
$ docker pull golang@sha256:69af918afed80f6139004a36cc99b77fc2e72b282a73ff7bfe112b0d1e501327
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
$ docker pull golang@sha256:834acbeaffc7ef33b83a806a271b511876810a7bd64bbe0e0f7f29b372a06b17
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.9 MB (272927758 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c8cdaa5f7302c17723af8e586e5d13dc014b0d91c83e3994d9192aa30f209c6`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1759104000'
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
	-	`sha256:03e514ef7fa283c62434ceaa5569a1dfd7eb8f0bc5744761a741cccd05a62353`  
		Last Modified: Mon, 29 Sep 2025 23:34:15 GMT  
		Size: 44.2 MB (44195923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8de0c6a4c275fbc1127f1e13a9f6de6ca4fdc975838d76828750e675f4b1fd24`  
		Last Modified: Tue, 30 Sep 2025 01:05:07 GMT  
		Size: 21.9 MB (21930710 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03c9e67a849318ef85c3217c9988076f862a279a4fa96c042c09b84353bac8b7`  
		Last Modified: Tue, 30 Sep 2025 02:39:14 GMT  
		Size: 59.7 MB (59652531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d169d5cce88dcaa313a66144353fb161b6186cbc4009a87e83ec26b2a4583aa2`  
		Last Modified: Tue, 30 Sep 2025 04:17:38 GMT  
		Size: 66.3 MB (66254599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2eea36933200b5f141ab18c26e141eacf675fe2778fc8f3cca0727236a934dcf`  
		Last Modified: Mon, 29 Sep 2025 18:04:27 GMT  
		Size: 80.9 MB (80893837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33fcc6cdc800cde2ab2ebe9072222c427b6199495de04a7b0865050d56aa7ae0`  
		Last Modified: Tue, 30 Sep 2025 04:17:26 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20250927-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:c1a5c17f05c8e0f4833e8e1b444594b050510ef2d14c64bf1420ae35d3510db7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10330155 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51f065debfc41a2d56617d9d62a7ffe7836c15fd4d85b548a7fe298541e80793`

```dockerfile
```

-	Layers:
	-	`sha256:1ac71e017104e15d5fb6473b0801855653ae94a34315eb1219f5135c63fe6164`  
		Last Modified: Wed, 01 Oct 2025 20:25:01 GMT  
		Size: 10.3 MB (10301614 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0587061dba4d481a7ddc2f67ac226209e5e0e5b92b7f92cbcfd381d6ca0ea44d`  
		Last Modified: Wed, 01 Oct 2025 20:25:02 GMT  
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
$ docker pull golang@sha256:426bdc9344bb407dc33c243c1c5909031efa70a8aa5ff6fab38cb3e78e9765e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **284.4 MB (284410734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1e84d8cc9bde559281889a4cac6319431cbbafff840e2e7a1c40b1afc483109`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1759104000'
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
	-	`sha256:7eacf7da1d9ca68e46013f3f56395614b995d68904a39e73d4a5bad90579014f`  
		Last Modified: Mon, 29 Sep 2025 23:33:18 GMT  
		Size: 48.8 MB (48760734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:300a1eca9595b83f733381d5f5c6ca135b5d5a79fcdb8204a00ace454f493a78`  
		Last Modified: Tue, 30 Sep 2025 16:39:43 GMT  
		Size: 23.6 MB (23611218 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d4ad543e1bb93773e8c6b716a20da76b363bb9d042051784870a3254e450de6`  
		Last Modified: Tue, 30 Sep 2025 20:27:52 GMT  
		Size: 63.3 MB (63309463 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b39be94b43c7b8fee0fdcf795208f91323ad52fb7cc0e21f16aaaac555d61b8`  
		Last Modified: Tue, 30 Sep 2025 22:53:31 GMT  
		Size: 70.0 MB (69997146 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b6844b679a5f5edf47ba45ef98949fc5932d7a14f3cc5aef05938c51a025fd7`  
		Last Modified: Mon, 29 Sep 2025 20:26:12 GMT  
		Size: 78.7 MB (78732016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b1f695ea7627b292f8033dd53c68bd2cb3ebe20ddf1fb5c4d215b8f8a8dbb66`  
		Last Modified: Wed, 01 Oct 2025 01:01:43 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20250927-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:07b9d34658c6099ddd1a279c5afff79f62451e7b2bea0d9c24e298d6bfbae2cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.3 KB (28283 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b120024e6b84f68bac057a2651089ec36cfc63f095b01a4689231fb398449f70`

```dockerfile
```

-	Layers:
	-	`sha256:06481365ec7285b956237871f691bd59da1bece3b03596a88feb1a74fe54ca89`  
		Last Modified: Wed, 01 Oct 2025 20:25:21 GMT  
		Size: 28.3 KB (28283 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20250927-bookworm` - linux; ppc64le

```console
$ docker pull golang@sha256:d2c4be30d73ba8dee780971ae6f39f6e69d1ffc16913f078ec485f7ec127972a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **319.5 MB (319466692 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e37407b9490ef0418835529944e7f7a04ffe6bfc015ef634ea46bc96c04a798`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1759104000'
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
	-	`sha256:812b25f785969d275d8c3962568c03f83ccc4df31b95f01c0646d79d6d5069f3`  
		Last Modified: Mon, 29 Sep 2025 23:33:30 GMT  
		Size: 52.3 MB (52326764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7f96d9492071bbcb8f94f1c41ed34bb1a985729d6a6ad6f8a6d10f9bd6e3f16`  
		Last Modified: Tue, 30 Sep 2025 02:24:29 GMT  
		Size: 25.7 MB (25668919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8559f87b306ba2a8705f64aa230b6840e422b552a6363650f02e37cde768fc14`  
		Last Modified: Tue, 30 Sep 2025 09:20:33 GMT  
		Size: 69.8 MB (69845543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6b9b052a32cc9593256d5096437790565c79483c5e1e301697d510145037fed`  
		Last Modified: Tue, 30 Sep 2025 19:48:33 GMT  
		Size: 90.4 MB (90417716 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c4682e6be6673e7aa33301c5b30874cd778044246d060f0fbf3c29475651b8b`  
		Last Modified: Mon, 29 Sep 2025 18:07:23 GMT  
		Size: 81.2 MB (81207592 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3eaa9b68dacac5139ef398b7b6a3e106bc4ae100e1591a2ce53d0efd056ab7f0`  
		Last Modified: Wed, 01 Oct 2025 01:49:24 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20250927-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:d0e6edc2dbc8d310e1a938babfe130a6d8be744f6514c791f727c01c667da1bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10495872 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e7df377568e897f0cd7ba5f2d358df39c6e78d164d681f67706ea7453c6671d`

```dockerfile
```

-	Layers:
	-	`sha256:4992683735b8e1f4cbc1db36aec8823b50fdeee1a4bcec895f66ac2d834d202d`  
		Last Modified: Wed, 01 Oct 2025 20:25:24 GMT  
		Size: 10.5 MB (10467397 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aa235f3051b5d21742961503b4ee977f911543c1a15cb2d9457d2dc543afe128`  
		Last Modified: Wed, 01 Oct 2025 20:25:25 GMT  
		Size: 28.5 KB (28475 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20250927-bookworm` - linux; s390x

```console
$ docker pull golang@sha256:d75f2e02799c661cbfe432439669ea1822c410153ebfaeedeeb61b2d63e383c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.1 MB (286106991 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e34d817ac4467ff6f5f171edc59cf10457b5e89e73fc78de252004895fbd2be`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1759104000'
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
	-	`sha256:87d1bec83b35277b636c6e05b9418301b2f025752d7539cecae442f0b94d8fbe`  
		Last Modified: Mon, 29 Sep 2025 23:33:26 GMT  
		Size: 47.1 MB (47137446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa2365377a8d4ecfdf70b8afc073fddfe487283a41bc28927b47a4757047f66c`  
		Last Modified: Tue, 30 Sep 2025 03:09:03 GMT  
		Size: 24.0 MB (24023716 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dc9730cf662a91a14b192c512ec1973efc8f7eabd745b63f8c6c877f23bf0d0`  
		Last Modified: Tue, 30 Sep 2025 09:32:19 GMT  
		Size: 63.5 MB (63501350 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08a4dbf2eab022c30a4f1ad0d69bb0be8e9a7b59d1d848c5eb4bcf43acac22ef`  
		Last Modified: Tue, 30 Sep 2025 23:54:17 GMT  
		Size: 69.0 MB (69006320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02ed6e6981e4c029c9853a9bbba242bc2c9b41f236141c1f10c1334ce58549f0`  
		Last Modified: Mon, 29 Sep 2025 18:05:39 GMT  
		Size: 82.4 MB (82438002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:738315edc341f10f5598db1a56e149e39fb0d7d1a976e81d851e069677e7ac24`  
		Last Modified: Tue, 30 Sep 2025 23:54:14 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20250927-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:48ebbf37bf25c7d5b89c1c77a3dd7da730cbfb8397731f2a516546b18e1022f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 MB (10355103 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94bd79df0221862d0c3c8b60693281b336d5d9cab8d7f22fd26b339bd09f76dc`

```dockerfile
```

-	Layers:
	-	`sha256:85f8db8208b704c426edf3401b8c0a7b4b71cb4723021468ba1c28fde0bf4087`  
		Last Modified: Wed, 01 Oct 2025 20:25:34 GMT  
		Size: 10.3 MB (10326674 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6454a9da702aefa1b3a5b387fcfd73c34b74e538bb98a0378afd43877fabecd0`  
		Last Modified: Wed, 01 Oct 2025 20:25:34 GMT  
		Size: 28.4 KB (28429 bytes)  
		MIME: application/vnd.in-toto+json
