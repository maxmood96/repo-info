## `golang:tip-20260530-bookworm`

```console
$ docker pull golang@sha256:7cbcbf7b76ec16eb5dfbdc317cd8ce0bda93ef9fa6745aceb8612748f69f7676
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

### `golang:tip-20260530-bookworm` - linux; amd64

```console
$ docker pull golang@sha256:56f839975df3d85755dc251c5980bf587679a0d17e5635e0a4a2e9b44465e4ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **331.4 MB (331426845 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:507956297984a3a58bbe56b75517fe80b6291472b1293d0bc22e9ae9a62aab62`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1779062400'
# Tue, 19 May 2026 23:23:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 May 2026 00:26:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 16:39:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 16:41:59 GMT
ENV GOTOOLCHAIN=local
# Tue, 02 Jun 2026 16:41:59 GMT
ENV GOPATH=/go
# Tue, 02 Jun 2026 16:41:59 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jun 2026 16:41:59 GMT
COPY /target/ / # buildkit
# Tue, 02 Jun 2026 16:42:02 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 02 Jun 2026 16:42:02 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:4887723d153cfd7fd9e356c8730311c36a64e4f9329f9d3ae1929e05715f2e73`  
		Last Modified: Tue, 19 May 2026 22:36:12 GMT  
		Size: 48.5 MB (48495432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e51c50554dce9c9549d76c40bfea45780a8342aea81ba8b270ba1bf46a2aec5`  
		Last Modified: Tue, 19 May 2026 23:23:20 GMT  
		Size: 24.0 MB (24043374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a234579dfb0d2a4c7e869bc6c39c06f306aa019f90ec3e79f682671badaeb4f3`  
		Last Modified: Wed, 20 May 2026 00:26:20 GMT  
		Size: 64.4 MB (64404451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:711c06b3f22f5debc7aaa6b12404d2ebba5bdc8680fdee266cdb9c3423baca69`  
		Last Modified: Tue, 02 Jun 2026 16:42:29 GMT  
		Size: 92.5 MB (92481269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e23f29da6194068cf9bcb9d5261ce3db2ba9613e69bf068059cae42650df5c10`  
		Last Modified: Tue, 02 Jun 2026 16:41:24 GMT  
		Size: 102.0 MB (102002162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:640cefbc230cca6ce1e699b6f066a0ce3ce18296f9bdf22d36a86823e240dbc3`  
		Last Modified: Tue, 02 Jun 2026 16:42:25 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20260530-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:07a56b7b7aa99d3dee3ab628c152c8bd5c43de8440e0d59797e1b71313fc105f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10525445 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1fd6eb568d46810b212527163c7b4f38227e5510f70ba41b533072d6d9c3fd4f`

```dockerfile
```

-	Layers:
	-	`sha256:f8e8037508a1124d21988840328f4347d916c9a82586a1fbedadd5aae7a79620`  
		Last Modified: Tue, 02 Jun 2026 16:42:27 GMT  
		Size: 10.5 MB (10497055 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b48cccb5152d21204a3635f7b872bbe5af630889fe88f04db2b1005a6b8e4e5b`  
		Last Modified: Tue, 02 Jun 2026 16:42:26 GMT  
		Size: 28.4 KB (28390 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20260530-bookworm` - linux; arm variant v7

```console
$ docker pull golang@sha256:2bc55f461af5e2a7d7030cec14b3e2acba70d75687a34d7743ea57a972ae76dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.9 MB (289875340 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0d72cc366daff25c801c20cf2ea19369fa8a91060a3d06050ea908a6725a216`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1779062400'
# Wed, 20 May 2026 00:02:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 May 2026 01:33:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 16:39:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 16:42:54 GMT
ENV GOTOOLCHAIN=local
# Tue, 02 Jun 2026 16:42:54 GMT
ENV GOPATH=/go
# Tue, 02 Jun 2026 16:42:54 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jun 2026 16:42:54 GMT
COPY /target/ / # buildkit
# Tue, 02 Jun 2026 16:42:57 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 02 Jun 2026 16:42:57 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:1af0b8b84389f4347663cc563bc1f6d59fe6d6f21081f428bafa1a09f6a276ce`  
		Last Modified: Tue, 19 May 2026 22:35:59 GMT  
		Size: 44.2 MB (44209154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a61246c0a5a0fe9fe8cdc1bfde0fdfa49ffafcc94cba31f4aecc0c34bc346064`  
		Last Modified: Wed, 20 May 2026 00:02:11 GMT  
		Size: 22.0 MB (21950133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c56a54e4354794da97ac9fe5173f689d775d13afa792e8b390e49425c3caa6b5`  
		Last Modified: Wed, 20 May 2026 01:34:11 GMT  
		Size: 59.7 MB (59661818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:088d1a53dc1aaa6ab78e9d8c272f28a3510e9189bd024c724307f4821831e82a`  
		Last Modified: Tue, 02 Jun 2026 16:43:22 GMT  
		Size: 66.3 MB (66339022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c820ebe5b5536b95e87912c5dc1f2663a3e9f184b88c7a174fffa610cef8238c`  
		Last Modified: Tue, 02 Jun 2026 16:42:07 GMT  
		Size: 97.7 MB (97715056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07b2a6ec69ff1c5e954131c465b304361b3a52da201a0e89316825fa1e089c8b`  
		Last Modified: Tue, 02 Jun 2026 16:43:20 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20260530-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:23d38ebf5fd2a9f5656e7ff1324632c7728756884c17484361c651678ec9d88e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10332249 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43813993f2910bfeb16b4b7b62e8132de5e71bd42de5c8e60da1e845f2ad4c6f`

```dockerfile
```

-	Layers:
	-	`sha256:8e4107626af0a749377ac1cfb907c4b4f37bc11884cc6247660d52debd063c65`  
		Last Modified: Tue, 02 Jun 2026 16:43:20 GMT  
		Size: 10.3 MB (10303751 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c00a17768e1bd61cc6a2b70c74fdd3140e004869eaed62e31a2c5e992ca69848`  
		Last Modified: Tue, 02 Jun 2026 16:43:20 GMT  
		Size: 28.5 KB (28498 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20260530-bookworm` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:ab644499f1b811e49c40262b405fa59d26a7fe46ea0352a125a28d811ebac19f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **319.5 MB (319469821 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4982fa1ed4ddec1a0e63cb7e31af0ba0f88ad02b9b08c67b27acaa575d0282f7`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1779062400'
# Tue, 19 May 2026 23:26:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 May 2026 00:26:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 16:40:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 16:41:56 GMT
ENV GOTOOLCHAIN=local
# Tue, 02 Jun 2026 16:41:56 GMT
ENV GOPATH=/go
# Tue, 02 Jun 2026 16:41:56 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jun 2026 16:41:56 GMT
COPY /target/ / # buildkit
# Tue, 02 Jun 2026 16:41:59 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 02 Jun 2026 16:41:59 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:1fbcdab7270278c1f989ae72190255d85d2117e990efb76cde6eb206b803672c`  
		Last Modified: Tue, 19 May 2026 22:36:02 GMT  
		Size: 48.4 MB (48379432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3daebbc198bd7b84bdd72840d7f4ded251896f03b9a9f880894e95e926bc543`  
		Last Modified: Tue, 19 May 2026 23:26:38 GMT  
		Size: 23.6 MB (23613394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35c669ec0346d48159cb837d6257098593cd53e61de677d9c0426474d36e1c5e`  
		Last Modified: Wed, 20 May 2026 00:27:16 GMT  
		Size: 64.5 MB (64487655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86950f01ce13905c8b8421b71349f939558e0fdbf7233592e069ff2955e2e9f1`  
		Last Modified: Tue, 02 Jun 2026 16:42:25 GMT  
		Size: 86.6 MB (86554600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a15ffb09d61853e3fb3628a4cb3b2d395b59e27aec015f8f1626a8b2ce9bb2f2`  
		Last Modified: Tue, 02 Jun 2026 16:41:30 GMT  
		Size: 96.4 MB (96434582 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a8fc85bb11992562284319ed8ffcf4989a66e58c995c3b4feb79e03bee1ba50`  
		Last Modified: Tue, 02 Jun 2026 16:42:22 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20260530-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:2a03fb68277defe76321e075bab79482a7acd8749c0b0daa87e2303e73c6e0ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10553401 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dda8b7d38e490660de3f99819f689ebeb1a3e4d907b119fab5f04e56ecd3d499`

```dockerfile
```

-	Layers:
	-	`sha256:8e1e70ecdb5dd6e57c1d854952655af965efd3eb1d3e6dad13a01e257bd67735`  
		Last Modified: Tue, 02 Jun 2026 16:42:23 GMT  
		Size: 10.5 MB (10524879 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:041d10ed7e45adba7c8200a1faef98e16d4b7a5d299f23f19adbaf3ed3f8928a`  
		Last Modified: Tue, 02 Jun 2026 16:42:22 GMT  
		Size: 28.5 KB (28522 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20260530-bookworm` - linux; 386

```console
$ docker pull golang@sha256:d5b8fde03ef44952879409339708aff7244ac3dc29cf49c4c1b6c0810cc04e2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **330.3 MB (330280179 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f357d6b337273aa0d00ec8f790d3a71f3ca0ffc65030bdabbc60125951c0eb9c`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1779062400'
# Tue, 19 May 2026 23:24:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 May 2026 02:44:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 16:39:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 16:42:16 GMT
ENV GOTOOLCHAIN=local
# Tue, 02 Jun 2026 16:42:16 GMT
ENV GOPATH=/go
# Tue, 02 Jun 2026 16:42:16 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jun 2026 16:42:16 GMT
COPY /target/ / # buildkit
# Tue, 02 Jun 2026 16:42:19 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 02 Jun 2026 16:42:19 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:8bf11fb6e89cfb8d682f511fb7d1b795e747af9c12a192f45f6e50ae7ca54f50`  
		Last Modified: Tue, 19 May 2026 22:36:20 GMT  
		Size: 49.5 MB (49483120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db105b3a1c2456422c428304ae93436fac4214751cb65053af119fa6d81d85dd`  
		Last Modified: Tue, 19 May 2026 23:24:59 GMT  
		Size: 24.9 MB (24879482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9e2a05321daf588afd8b06b380f7ea0a3d7c0de2097ec6f355a74453e7ec6af`  
		Last Modified: Wed, 20 May 2026 02:45:13 GMT  
		Size: 66.2 MB (66243865 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4025b2f777580250150f2467b8607eab899e8d3860df0fa51668df0f0d03abdb`  
		Last Modified: Tue, 02 Jun 2026 16:42:45 GMT  
		Size: 89.9 MB (89904025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79f630b89f59dc6a4b85d53c6ab2696f0b52ea5d937a0bd9344e6c06fc5883a6`  
		Last Modified: Tue, 02 Jun 2026 16:42:33 GMT  
		Size: 99.8 MB (99769529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5f73445c8731b2bebc7aee56abd617889e7e43a9f3591ef99397ca6a304e12e`  
		Last Modified: Tue, 02 Jun 2026 16:42:42 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20260530-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:06fe654b9ad68e9ccbe0770093fd97a6a5b3e57bca09e2add2835c869f6c6af1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10504987 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc3f9214120a813bab50829020dc5e9a3dffc5dc04da85943170457bb7d51398`

```dockerfile
```

-	Layers:
	-	`sha256:8f170855d2cf9ecb1066ce466791bd4541c284fad7eba0e309564ced17177cf5`  
		Last Modified: Tue, 02 Jun 2026 16:42:43 GMT  
		Size: 10.5 MB (10476635 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3d8f072ddd3faf3fafd238c3f9c467af5c3292de8cb39e54177ad2178d585c6e`  
		Last Modified: Tue, 02 Jun 2026 16:42:42 GMT  
		Size: 28.4 KB (28352 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20260530-bookworm` - linux; mips64le

```console
$ docker pull golang@sha256:38e727abeca3301a334e0a1d513294cd453920a018f6d63d4ff152d7cbac2fab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.2 MB (301203889 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a93525eadef79c5fdbcdddd9716424d876f0c1790becf3c468e24d4b3694ffc`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1779062400'
# Wed, 20 May 2026 10:04:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 May 2026 15:11:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 May 2026 16:19:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 17:02:47 GMT
ENV GOTOOLCHAIN=local
# Tue, 02 Jun 2026 17:02:47 GMT
ENV GOPATH=/go
# Tue, 02 Jun 2026 17:02:47 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jun 2026 17:02:47 GMT
COPY /target/ / # buildkit
# Tue, 02 Jun 2026 17:03:02 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 02 Jun 2026 17:03:04 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:813eaff938e8991b3dd16851af2c46dd2ffc5bb600e30ff866dd5a60502fbffa`  
		Last Modified: Tue, 19 May 2026 22:35:13 GMT  
		Size: 48.8 MB (48786239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2853b2ecd2cc91271c3528597da43fc45c41515894834d1de212a390afbf0ade`  
		Last Modified: Wed, 20 May 2026 10:05:32 GMT  
		Size: 23.6 MB (23621201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71bf4bd887b67ee95b1804bd893717310da36bddd5a598cce7e9b621ff52ee05`  
		Last Modified: Wed, 20 May 2026 15:12:43 GMT  
		Size: 63.3 MB (63316337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2d8edfd178bcf28b946d64eb3ad538d4ee96dacac854fd44ba3af295e68b368`  
		Last Modified: Wed, 20 May 2026 16:21:18 GMT  
		Size: 70.1 MB (70084514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:148b142c54d1b941c7d66610cd7d81d650defd945cece98d1cf8e78c64810a19`  
		Last Modified: Tue, 02 Jun 2026 17:05:09 GMT  
		Size: 95.4 MB (95395440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d6b083f3b10354ecd6706af3be6a7c925f39002aba5104f12f55c91d99df3c4`  
		Last Modified: Tue, 02 Jun 2026 17:04:59 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20260530-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:3250748eeca0ccd53a4d60135ae6bfcb840981c8684b03624c9a225f8d20b598
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.1 KB (27124 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b816634e2cdfc34cbbe520cba6306373f2fef0e64e74d48d215e444878260ca`

```dockerfile
```

-	Layers:
	-	`sha256:5fbe6ed6ae6799f7401dc967d0813087edd8dae29bd1730e42bdd331d25ece31`  
		Last Modified: Tue, 02 Jun 2026 17:04:59 GMT  
		Size: 27.1 KB (27124 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20260530-bookworm` - linux; ppc64le

```console
$ docker pull golang@sha256:c4128c8c6c7bfc7ec83978413a72d7c8ab64b75bd75389a97565e6c6fd5d7bcc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **336.8 MB (336763049 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3364976da63edea22dd3ef69e70be7b872b4a542835da5517d9d32c9a1f2f2a9`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1779062400'
# Wed, 20 May 2026 01:13:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 May 2026 06:50:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 16:42:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 16:41:50 GMT
ENV GOTOOLCHAIN=local
# Tue, 02 Jun 2026 16:41:50 GMT
ENV GOPATH=/go
# Tue, 02 Jun 2026 16:41:50 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jun 2026 16:41:50 GMT
COPY /target/ / # buildkit
# Tue, 02 Jun 2026 16:42:16 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 02 Jun 2026 16:42:16 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:b3943e183051423c3dc79fa53ad6d50fff9621945bbfc636eec039b14ead2b66`  
		Last Modified: Tue, 19 May 2026 22:35:10 GMT  
		Size: 52.3 MB (52340199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4f46c910cb3dd366a8b080c77b15459d7465da54412b3570454cddcaf0cdf40`  
		Last Modified: Wed, 20 May 2026 01:13:39 GMT  
		Size: 25.7 MB (25686466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d67cb71cd5984ee53ab56bef57a29d3b0ef6e8939c352146b1efe66402d4c7ff`  
		Last Modified: Wed, 20 May 2026 06:51:27 GMT  
		Size: 69.9 MB (69853485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0548bbd70587587ebc4a21c63b5f4bd00f3fc220c1a3dc53c1a1b9debf81aa66`  
		Last Modified: Tue, 02 Jun 2026 16:43:17 GMT  
		Size: 90.5 MB (90495650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4a76d2265265ac98a5752cfbf5ed880207c013050351547f0c225cf8c995ca0`  
		Last Modified: Tue, 02 Jun 2026 16:43:17 GMT  
		Size: 98.4 MB (98387092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be0c71357c78f0cd543af45505a0c076218de1899f138e814aa5b496421765b2`  
		Last Modified: Tue, 02 Jun 2026 16:43:13 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20260530-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:9217fe6c4730e7d1a304cba536376d6c7be62805086f2aaf3c66a3209d790920
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10497972 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8dcf83e616b7aca3926e090b9d0e8e4453963536c19b4693037a30bad0c2a6b`

```dockerfile
```

-	Layers:
	-	`sha256:161f434b6d97af0a454541bba90ef61618c9214d0a71a61b87ebe11fc3a663e0`  
		Last Modified: Tue, 02 Jun 2026 16:43:13 GMT  
		Size: 10.5 MB (10469540 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dbf3097d16ab2d07ef2462bad0e1c55d41bd559d0b20c81a5f158ea29d806449`  
		Last Modified: Tue, 02 Jun 2026 16:43:12 GMT  
		Size: 28.4 KB (28432 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20260530-bookworm` - linux; s390x

```console
$ docker pull golang@sha256:403ed4c2f02685da76b4367ccb8943a1b2561c742cb1643a520ec4fd972fc3b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **304.2 MB (304234923 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0694092e2892aa67e4937401bae8e59f5aa4d8b427600889bdec39ce8624168c`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1779062400'
# Wed, 20 May 2026 00:17:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 May 2026 02:05:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 16:42:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 16:41:57 GMT
ENV GOTOOLCHAIN=local
# Tue, 02 Jun 2026 16:41:57 GMT
ENV GOPATH=/go
# Tue, 02 Jun 2026 16:41:57 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jun 2026 16:41:57 GMT
COPY /target/ / # buildkit
# Tue, 02 Jun 2026 16:42:09 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 02 Jun 2026 16:42:10 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:e0fc2c7a6bb12f7a9b333cc117b6ea5fa5cf251c5fa4dd298303beee01028f59`  
		Last Modified: Tue, 19 May 2026 22:35:39 GMT  
		Size: 47.2 MB (47155589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d79feab17202415ba0b431eca0e903b1c895e662e755c4c9f1b5678ad8eb605f`  
		Last Modified: Wed, 20 May 2026 00:18:12 GMT  
		Size: 24.0 MB (24039201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:511ade0407a6db3c4a6853a735563e5fb22577aaaa32942a9458cc0c09942583`  
		Last Modified: Wed, 20 May 2026 02:05:37 GMT  
		Size: 63.5 MB (63498321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6f90b46dcc8622719e19e9e04b1bcb5bc39309966d69636e349c233ba832e30`  
		Last Modified: Tue, 02 Jun 2026 16:42:45 GMT  
		Size: 69.1 MB (69088003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cca767cc33ca0e2036ed1bd1b9a5ecdd963a3598306969640db0e92025a10887`  
		Last Modified: Tue, 02 Jun 2026 16:42:28 GMT  
		Size: 100.5 MB (100453651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b23dbe836c3f55f02add78bfdd7b4bfc8403faa6dd93ed0015a3ddb579acb6aa`  
		Last Modified: Tue, 02 Jun 2026 16:42:43 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20260530-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:83aeac03da10607c3221222e5534624e8fe3e75f7d632f8a67789d1ee62dbbf9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 MB (10357951 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ea1242c908bd967033cf112b169ca58c6e3696edaab1b4bc8c8f000f71d88c9`

```dockerfile
```

-	Layers:
	-	`sha256:b3f386fa2aad74f5b4a8aa3ad3cc3452962041cf7e5745864872d06ad6db606b`  
		Last Modified: Tue, 02 Jun 2026 16:42:43 GMT  
		Size: 10.3 MB (10329561 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7fa22aaac55be0a25192285e10af000ac5d5473bdd700aedb599d9dc60c68e0d`  
		Last Modified: Tue, 02 Jun 2026 16:42:43 GMT  
		Size: 28.4 KB (28390 bytes)  
		MIME: application/vnd.in-toto+json
