## `golang:tip-20250815-trixie`

```console
$ docker pull golang@sha256:adc08dd4cdb8e208743beb974a5ccf57ec365802bbd4ecee64ec61e1409d83f8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `golang:tip-20250815-trixie` - linux; amd64

```console
$ docker pull golang@sha256:c5a83c0e53be15e5ce2ebcf8844043296eae78fe6804565345c27e046b356231
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **327.9 MB (327858269 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b08efef0dbe4db37c347fbe77dcc0f268616382ae35b164c3cf253249b3bfd3`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1754870400'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Mon, 18 Aug 2025 05:23:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 18 Aug 2025 05:23:18 GMT
ENV GOTOOLCHAIN=local
# Mon, 18 Aug 2025 05:23:18 GMT
ENV GOPATH=/go
# Mon, 18 Aug 2025 05:23:18 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 18 Aug 2025 05:23:18 GMT
COPY /target/ / # buildkit
# Mon, 18 Aug 2025 05:23:18 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 18 Aug 2025 05:23:18 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:80b7316254b3093eb3c7ac44bb6c34bde013f27947c1ed8d8afe456b957ebfdb`  
		Last Modified: Tue, 12 Aug 2025 20:45:14 GMT  
		Size: 49.3 MB (49278280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36e4db86de6eba33869491caa7946b80dd71c255f1940e96a9f755cc2b1f3829`  
		Last Modified: Tue, 12 Aug 2025 22:14:12 GMT  
		Size: 25.6 MB (25612940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ea45766c6449310ca2fc621a7e00bedb4b9b803a7fbfe2607efce6d2e07e435`  
		Last Modified: Tue, 12 Aug 2025 22:15:03 GMT  
		Size: 67.8 MB (67777316 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:832263fb6d84d256c2af1cf13b333eb935a8d20a960077e7e7c2a9cdc7e7d8a2`  
		Last Modified: Mon, 18 Aug 2025 18:21:20 GMT  
		Size: 102.1 MB (102055347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c981e030468965854d1b7da64b902a546cf410e421543877a0dbcd1eb3b5506d`  
		Last Modified: Mon, 18 Aug 2025 19:09:02 GMT  
		Size: 83.1 MB (83134228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59490ac08d841aae9298054368a8ac2680e7c30aee12a2cc8ccc645c6466c41d`  
		Last Modified: Mon, 18 Aug 2025 18:21:02 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20250815-trixie` - unknown; unknown

```console
$ docker pull golang@sha256:1da019ac4ccc3925ae09ac40f5784240462619862cb8c59366a94fedd0b60863
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10805950 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd419f554a72dc660105cb7ba7699b18edd2b14fabb8018349eba4ce53ddf2d1`

```dockerfile
```

-	Layers:
	-	`sha256:b3343fbc10461cac59d4a4dcebb113c01700b6b776d439b1ce4e138fa13efcc1`  
		Last Modified: Mon, 18 Aug 2025 20:23:22 GMT  
		Size: 10.8 MB (10778310 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5b5aa5418f5d8ec92d876b0a79091aa5591b590f636f1bc66afd2d0294b6eee7`  
		Last Modified: Mon, 18 Aug 2025 20:23:23 GMT  
		Size: 27.6 KB (27640 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20250815-trixie` - linux; arm variant v7

```console
$ docker pull golang@sha256:583db6cf5bada82ecbea923b96a199690022eded4d703f8e8096e763999bb63a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **284.9 MB (284902199 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2763f4dba0b10dcd60627239192372e11ef37f7b41f647a7425f9c28227749fb`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1754870400'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Mon, 18 Aug 2025 05:23:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 18 Aug 2025 05:23:18 GMT
ENV GOTOOLCHAIN=local
# Mon, 18 Aug 2025 05:23:18 GMT
ENV GOPATH=/go
# Mon, 18 Aug 2025 05:23:18 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 18 Aug 2025 05:23:18 GMT
COPY /target/ / # buildkit
# Mon, 18 Aug 2025 05:23:18 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 18 Aug 2025 05:23:18 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:58382c67f397ebdc005890f56dc436f7798aeeee2e0d603ba02e89d6243c138b`  
		Last Modified: Tue, 12 Aug 2025 20:51:59 GMT  
		Size: 45.7 MB (45712631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce72873bc1bfa1e9338237d9573d1640f6647f61a1636bbd71d8128d16503087`  
		Last Modified: Wed, 13 Aug 2025 00:16:54 GMT  
		Size: 23.6 MB (23613045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbe0a58e6c2887b271354fa2e1067ff7e829f063163f76c4a3d4f1da179eb22e`  
		Last Modified: Wed, 13 Aug 2025 06:50:21 GMT  
		Size: 62.7 MB (62718501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39bf1e0378255d85ce69e42b8c2b4e52765a17bb9940e69e2993debcac329de3`  
		Last Modified: Thu, 14 Aug 2025 05:24:37 GMT  
		Size: 72.7 MB (72699087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65db35adfd1c26b9fd865e957c7ac16cfbd5d2925f26a2f01840bdbea9cb3b72`  
		Last Modified: Mon, 18 Aug 2025 23:18:49 GMT  
		Size: 80.2 MB (80158777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bce776dcc76398faf1b807a1dbb0d013463f8f5ca96a312cf290157f72184cd`  
		Last Modified: Mon, 18 Aug 2025 23:18:45 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20250815-trixie` - unknown; unknown

```console
$ docker pull golang@sha256:e41d084a5794c101e168dc53c4a1b5ec2c73e962ac8663c22cd10f5da01e097b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10600842 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:411fb2fbaaa74e861cb40f4ea8f67d7688e561289338c5acd5b3a883da037e09`

```dockerfile
```

-	Layers:
	-	`sha256:31b7d07c14bff2c3b66e009d79e38986ad81b46b8f4ad5a218ea580ecd34289e`  
		Last Modified: Tue, 19 Aug 2025 02:23:28 GMT  
		Size: 10.6 MB (10574199 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bb4c9b59990c8496fb8916665a824577eb6083d8389d96be9e552ef238ef2440`  
		Last Modified: Tue, 19 Aug 2025 02:23:29 GMT  
		Size: 26.6 KB (26643 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20250815-trixie` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:ab42f6f8eb34f22c1da59b92e7dc5407a1cb669797fb81821bca3d66a89aca0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **316.2 MB (316164701 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d518bd90f9cc3cc2bbb2b77528d7d8cfcd332b6e2c8c11e13d88856b25de5ae6`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1754870400'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Mon, 18 Aug 2025 05:23:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 18 Aug 2025 05:23:18 GMT
ENV GOTOOLCHAIN=local
# Mon, 18 Aug 2025 05:23:18 GMT
ENV GOPATH=/go
# Mon, 18 Aug 2025 05:23:18 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 18 Aug 2025 05:23:18 GMT
COPY /target/ / # buildkit
# Mon, 18 Aug 2025 05:23:18 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 18 Aug 2025 05:23:18 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:d1e40442030765a3ac5d135c39154d052eba20953ea0e5d35a066f7722cdd93d`  
		Last Modified: Tue, 12 Aug 2025 22:12:36 GMT  
		Size: 49.6 MB (49641603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9923852056eb09462c3344515191318e7aa33ff28057c946bc41a414ee57df0b`  
		Last Modified: Wed, 13 Aug 2025 07:30:07 GMT  
		Size: 25.0 MB (25014610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bcc8bff74cbeacbac9c6869b6a9def273b93cc67de196b347688de2a9185de0`  
		Last Modified: Wed, 13 Aug 2025 15:31:50 GMT  
		Size: 67.6 MB (67593628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a38f855563f91752e11284ea714640e18ae4af134118c677a0e4f6300dda76a9`  
		Last Modified: Mon, 18 Aug 2025 22:12:08 GMT  
		Size: 94.8 MB (94782080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a9a962081772d9ddd06f0164791e2d37e59bd0091e1d2b79d410ab8b218794c`  
		Last Modified: Mon, 18 Aug 2025 22:12:08 GMT  
		Size: 79.1 MB (79132623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be282096a405f301d6d073816336aca98b6628a68a82b9043958d712bc1a8c51`  
		Last Modified: Mon, 18 Aug 2025 22:11:59 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20250815-trixie` - unknown; unknown

```console
$ docker pull golang@sha256:35f03d464ff59e08ef817460ba97dd90b25fa78d5955e182ae3671e5128fb799
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.9 MB (10904756 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d28ab9f7aa7c6ba21a281e6f5c9d215369169afc7ce65c7c4d5effb1aa389144`

```dockerfile
```

-	Layers:
	-	`sha256:134946be866b38dccd66bb5fc6f067de83fb59991b6461dbd91f827e63a3b9aa`  
		Last Modified: Mon, 18 Aug 2025 23:23:30 GMT  
		Size: 10.9 MB (10876961 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c98677603867f101b4afa5ea758061c2048b12ba66c44282a5602dc724231276`  
		Last Modified: Mon, 18 Aug 2025 23:23:31 GMT  
		Size: 27.8 KB (27795 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20250815-trixie` - linux; 386

```console
$ docker pull golang@sha256:75b9cb24f69155cf9959cd2b636262834ac108d608c77debf13bd932db069567
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **329.6 MB (329619202 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:906d52d18ed73c12aa6cf7152c5ae49a245c5da8928ddd0406cdb0e8e6fe0b2c`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1754870400'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Mon, 18 Aug 2025 05:23:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 18 Aug 2025 05:23:18 GMT
ENV GOTOOLCHAIN=local
# Mon, 18 Aug 2025 05:23:18 GMT
ENV GOPATH=/go
# Mon, 18 Aug 2025 05:23:18 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 18 Aug 2025 05:23:18 GMT
COPY /target/ / # buildkit
# Mon, 18 Aug 2025 05:23:18 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 18 Aug 2025 05:23:18 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:3d9f8c7ff550056ffe2cca57d7110ae0306e74220a891574e97ddc10ba49823d`  
		Last Modified: Tue, 12 Aug 2025 20:45:17 GMT  
		Size: 50.8 MB (50794258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cde29e7bc69fcf496b5e5df92d7d82da6ff9f4877784085c4dcba73f6ee6a1ea`  
		Last Modified: Tue, 12 Aug 2025 21:20:38 GMT  
		Size: 26.8 MB (26772559 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebd9904337df106e0852d247e06047929e66d5097f2d2c13861e2e31ecc63f4b`  
		Last Modified: Tue, 12 Aug 2025 22:15:57 GMT  
		Size: 69.8 MB (69794753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e677d1b98bb7a56ff89d7f2a2732666e248692ad3e5dd6eedc0602da1a3d98dd`  
		Last Modified: Mon, 18 Aug 2025 18:21:51 GMT  
		Size: 100.5 MB (100498379 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82670d3acf9adce43c089b894a11312540a785c816af45b90edbb17d606892e6`  
		Last Modified: Mon, 18 Aug 2025 19:08:00 GMT  
		Size: 81.8 MB (81759095 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d27a45c74d4d571b13c659bd27cd3e0aca6693119444d2c6f57aa133841e812a`  
		Last Modified: Mon, 18 Aug 2025 18:21:36 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20250815-trixie` - unknown; unknown

```console
$ docker pull golang@sha256:31a46d65638a4471ab89bb34c1977799459f61d7343d5f5832d553aff039016b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10777173 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f70429cd6bae066e03345a522b70fb7a84a24efa23ba85b0cb53d7341bac4439`

```dockerfile
```

-	Layers:
	-	`sha256:21ccc35bdcb7eba0e74aa3c51c09903e6f3183623c73be06e7b5398146ba11e7`  
		Last Modified: Mon, 18 Aug 2025 20:23:33 GMT  
		Size: 10.7 MB (10749576 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7df6cc82924be057927e55c4fa86574f9339a3c6b5f4da935a55d3ade98f3fd8`  
		Last Modified: Mon, 18 Aug 2025 20:23:34 GMT  
		Size: 27.6 KB (27597 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20250815-trixie` - linux; ppc64le

```console
$ docker pull golang@sha256:320227c433e23ade94e738151630e98a74fec23b331b65ea4acef500e7bb3069
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **326.4 MB (326357367 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2803b0ab4b7f8c614d621369152f62f1631e3fe79e41d362ff4b0fe06c9ab03`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1754870400'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Mon, 18 Aug 2025 05:23:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 18 Aug 2025 05:23:18 GMT
ENV GOTOOLCHAIN=local
# Mon, 18 Aug 2025 05:23:18 GMT
ENV GOPATH=/go
# Mon, 18 Aug 2025 05:23:18 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 18 Aug 2025 05:23:18 GMT
COPY /target/ / # buildkit
# Mon, 18 Aug 2025 05:23:18 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 18 Aug 2025 05:23:18 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:befe77620590f63939f5bcadadc9f45832981822c9c901f057eb4e86f733c29a`  
		Last Modified: Wed, 13 Aug 2025 00:32:04 GMT  
		Size: 53.1 MB (53103384 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0a327675583423e2c44eae4c02a88be15dbeac36073deb88700ba487e0c0e35`  
		Last Modified: Wed, 13 Aug 2025 15:15:16 GMT  
		Size: 27.0 MB (26992868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:daf20d9e1e5f16d7552d637dd4a12484b22e52928311f81dd13c82b6838c2ae7`  
		Last Modified: Wed, 13 Aug 2025 21:23:59 GMT  
		Size: 73.0 MB (73018659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1037a602432b02dffae5109bfeab34a4c0255e20d818837d98c6749a505d7106`  
		Last Modified: Mon, 18 Aug 2025 21:57:49 GMT  
		Size: 92.8 MB (92760867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d39b86dffb1db621a8fcea400d6f61123247f5d28fb771a6f68ef42e85a595f`  
		Last Modified: Mon, 18 Aug 2025 21:57:49 GMT  
		Size: 80.5 MB (80481431 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11539af5ef6f537e541729f75d81315837e7ba18e74fe27a64139f92162b01bd`  
		Last Modified: Mon, 18 Aug 2025 21:57:44 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20250815-trixie` - unknown; unknown

```console
$ docker pull golang@sha256:2aab82d2be4522682f178c1fb469613788452b42da92ebde22b750167d50fedc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10801787 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57ae87168747c6bd8166d63080ded7f33bf102d6bee953d1736e1f380fd1d8ac`

```dockerfile
```

-	Layers:
	-	`sha256:1ea0b9cbf94a3b8ca33547ace1b4f4d34eb563d61fb36a2aa3930503bc6c269d`  
		Last Modified: Mon, 18 Aug 2025 23:23:44 GMT  
		Size: 10.8 MB (10774094 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a52423c746278ca72425b975424e2bd6f64a7ea6ea67457ea93ca7c21d514294`  
		Last Modified: Mon, 18 Aug 2025 23:23:45 GMT  
		Size: 27.7 KB (27693 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20250815-trixie` - linux; s390x

```console
$ docker pull golang@sha256:69d38210e67923a78bc7f7978cd70f2fa1f84e43239a4c09a1d1a3f70d100e85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **302.3 MB (302311597 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:144299cb09b0a192be48c74f0d33ca0063e74e32f881d2436a24f0ec3925ef18`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1754870400'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Mon, 18 Aug 2025 05:23:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 18 Aug 2025 05:23:18 GMT
ENV GOTOOLCHAIN=local
# Mon, 18 Aug 2025 05:23:18 GMT
ENV GOPATH=/go
# Mon, 18 Aug 2025 05:23:18 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 18 Aug 2025 05:23:18 GMT
COPY /target/ / # buildkit
# Mon, 18 Aug 2025 05:23:18 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 18 Aug 2025 05:23:18 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:c3b791adea90b39bc59919a9959b7f44f65aa3364a03dd0271a5ff658488877f`  
		Last Modified: Tue, 12 Aug 2025 20:59:03 GMT  
		Size: 49.3 MB (49345161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c47181ddd75754adfc74e4f58b4a898ec33ad906976b71219b567efd19470677`  
		Last Modified: Wed, 13 Aug 2025 03:27:04 GMT  
		Size: 26.8 MB (26779580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:415f63d435cf750f4bda1af6afa07ce9f812fa19c74e6f9f050da85f47eb36e7`  
		Last Modified: Wed, 13 Aug 2025 17:21:16 GMT  
		Size: 68.6 MB (68619998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8586b50ef06fb7762874a215a50c841f6e028fc9a32e90e6b8cb14d824e0adbc`  
		Last Modified: Mon, 18 Aug 2025 18:40:19 GMT  
		Size: 75.9 MB (75869298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3316bff964f9f759871a9216a703323b51e64d4b58eb53b6a858e7831c8cd357`  
		Last Modified: Mon, 18 Aug 2025 18:40:20 GMT  
		Size: 81.7 MB (81697402 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56f14beeceae07824bc7331235c43e89f70397973358bb875e40a74917046e25`  
		Last Modified: Mon, 18 Aug 2025 18:40:09 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20250815-trixie` - unknown; unknown

```console
$ docker pull golang@sha256:b5c273100c3184c54c90c5006287d3dea899a4be0fe832062d100d8d6090dc1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10616343 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:885a31ec239c092d3644f53cb065f85ac189fcd853a854fb41e74364b3499a64`

```dockerfile
```

-	Layers:
	-	`sha256:0a42b98061d9cffa2e053b82ba8115c5d799ca8e991c114f6892ba1c7649967c`  
		Last Modified: Mon, 18 Aug 2025 20:23:45 GMT  
		Size: 10.6 MB (10588710 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:176518f8a1909c55a98796033f0b889beba4b54396a06f8288a613213445985f`  
		Last Modified: Mon, 18 Aug 2025 20:23:46 GMT  
		Size: 27.6 KB (27633 bytes)  
		MIME: application/vnd.in-toto+json
