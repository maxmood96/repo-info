## `golang:tip-trixie`

```console
$ docker pull golang@sha256:d053e6ae50872c2e16f69774772f21a1e5133a1b236ff166a060de2fac4bf80c
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
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `golang:tip-trixie` - linux; amd64

```console
$ docker pull golang@sha256:e847a48793ecf4d5f3baf3a9a48c044a3904968983f0f61a65595a1410bb656a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **338.9 MB (338870526 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51c65fcbde1e3ca5cdd3a69e6aabc16e338a9d405440a3c990901b3e9af9619e`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 01:47:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 07 Apr 2026 02:43:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 07 Apr 2026 04:21:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 04:22:53 GMT
ENV GOTOOLCHAIN=local
# Tue, 07 Apr 2026 04:22:53 GMT
ENV GOPATH=/go
# Tue, 07 Apr 2026 04:22:53 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 04:22:53 GMT
COPY /target/ / # buildkit
# Tue, 07 Apr 2026 04:22:56 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 07 Apr 2026 04:22:56 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:a7730063fcfe708b222d34c4f07d633dfe087a28c05c4daaab2fa9943854c155`  
		Last Modified: Tue, 07 Apr 2026 00:11:35 GMT  
		Size: 49.3 MB (49297833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f33970743aee750df25f6c661132b7401c8fefe930e5f4803f4c8b6f567a6b55`  
		Last Modified: Tue, 07 Apr 2026 01:47:22 GMT  
		Size: 25.6 MB (25621678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5397da1d1537c4d725f3090c5688a582e14eeaf7743d75d9b38bad1649554987`  
		Last Modified: Tue, 07 Apr 2026 02:43:39 GMT  
		Size: 67.8 MB (67780708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a854c6475d7f805ed9b2b5909b6bf8ab2a1a29df1955eddd2003c9e097ef6de4`  
		Last Modified: Tue, 07 Apr 2026 04:23:22 GMT  
		Size: 102.2 MB (102169736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8966583daebf02f7188b966cc8cfaaff27cf5fc1ff9b30af37d939f77e22335f`  
		Last Modified: Mon, 06 Apr 2026 18:41:36 GMT  
		Size: 94.0 MB (94000413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1cccdbee76315ff12a49baba80d77ca42ab804f7a88a335c4d3bd2255e95da7`  
		Last Modified: Tue, 07 Apr 2026 04:23:19 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-trixie` - unknown; unknown

```console
$ docker pull golang@sha256:f0c6b25e91cb325062f1a3e08b5b3449372a03e90e0dd6cb1f662550a175162e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10814628 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88f422dd44c9bdaea556d9d7913b07b8eb2953937e1acaa75835ef814f925cae`

```dockerfile
```

-	Layers:
	-	`sha256:0f42cffb123c9e4c872f9ba1c608ce56836352f136cb8d544d4625207f02f323`  
		Last Modified: Tue, 07 Apr 2026 04:23:20 GMT  
		Size: 10.8 MB (10785659 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7500b9ab3fe86a0646680d2f682ed7cae9679e1ee787011cdb4a8ca1b14e10a3`  
		Last Modified: Tue, 07 Apr 2026 04:23:19 GMT  
		Size: 29.0 KB (28969 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-trixie` - linux; arm variant v7

```console
$ docker pull golang@sha256:c5adde58919e7f208a83b24a0bcc92ae09dc317bdb4d8ba7d554ca3cbb8c497e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.0 MB (295034714 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f287b6da7f0bbe00fa8e3c4706af0246711ad91825487a1acb365704d599b7cc`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 02:02:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 07 Apr 2026 03:49:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 07 Apr 2026 05:19:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 05:21:47 GMT
ENV GOTOOLCHAIN=local
# Tue, 07 Apr 2026 05:21:47 GMT
ENV GOPATH=/go
# Tue, 07 Apr 2026 05:21:47 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 05:21:47 GMT
COPY /target/ / # buildkit
# Tue, 07 Apr 2026 05:21:50 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 07 Apr 2026 05:21:50 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:5b74af671a0d47dbd638dd4965926230c96ef85f87e920309332aae3ff83292c`  
		Last Modified: Tue, 07 Apr 2026 01:00:01 GMT  
		Size: 45.7 MB (45732997 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b56e67d94360d76080a847d9e2746fc095d0663156f501d28fa6443bb38156e1`  
		Last Modified: Tue, 07 Apr 2026 02:02:17 GMT  
		Size: 23.6 MB (23636973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8868f799858ac0f14507e60a2ff0757894394681e874e60066914254664b5431`  
		Last Modified: Tue, 07 Apr 2026 03:50:05 GMT  
		Size: 62.7 MB (62722704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afe4096becf18b72fc7e1b3733ff42423c8cae420dc546a666ac148c0247aaa8`  
		Last Modified: Tue, 07 Apr 2026 05:22:15 GMT  
		Size: 72.8 MB (72805174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:866705b29d2f18b79748f9fadfbe79c21fa37d231a94fa79b6aae3edf75ac398`  
		Last Modified: Mon, 06 Apr 2026 18:42:37 GMT  
		Size: 90.1 MB (90136708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9219e034a747f159a74b336058758ab2666ce722d3c2795b1eb88c1f7f5fcfcf`  
		Last Modified: Tue, 07 Apr 2026 05:22:13 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-trixie` - unknown; unknown

```console
$ docker pull golang@sha256:428a1a028ecdd76e9221bb036bed3e74d271af7e7204343c4701dbb8dccb03bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10610638 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:278e7e07e0da1bdd65fa2d2f5a062b7a26496290da89c171655051750c0c7fb6`

```dockerfile
```

-	Layers:
	-	`sha256:b2c8243238e25687fc1f45a38c2c72f4a0ac63197bd8b96dbdf2185ede4a7e32`  
		Last Modified: Tue, 07 Apr 2026 05:22:14 GMT  
		Size: 10.6 MB (10581546 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6a921ae6ee9f0f692e4f9c3e279c974f5fc18449a37f2aadad2a875dbd3fa3ae`  
		Last Modified: Tue, 07 Apr 2026 05:22:13 GMT  
		Size: 29.1 KB (29092 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-trixie` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:3ab0056acb02d5459f65f5a956fe845b87873e814649f9b1b35b5e54740d54c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **329.7 MB (329675812 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d0d1d7de9591b19506bf245104b383bb20ea900660024510ab982ff6d669e6d`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 01:50:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 07 Apr 2026 02:53:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 07 Apr 2026 04:22:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 04:23:45 GMT
ENV GOTOOLCHAIN=local
# Tue, 07 Apr 2026 04:23:45 GMT
ENV GOPATH=/go
# Tue, 07 Apr 2026 04:23:45 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 04:23:45 GMT
COPY /target/ / # buildkit
# Tue, 07 Apr 2026 04:23:48 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 07 Apr 2026 04:23:48 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:912041a7b9f63b6550d3a3949c43e45f74a36a2f80c727e70e41cbe851de2d20`  
		Last Modified: Tue, 07 Apr 2026 00:11:19 GMT  
		Size: 49.7 MB (49665256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:277ee5883c1f173b0485b465221ddea5443b64c95935146f0bb3655baee3647d`  
		Last Modified: Tue, 07 Apr 2026 01:50:26 GMT  
		Size: 25.0 MB (25023654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6084ed286765ee022e8f8d9df76b9a2bd97a3224c379e905079f3bb11e1e48ca`  
		Last Modified: Tue, 07 Apr 2026 02:54:15 GMT  
		Size: 67.6 MB (67591915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9b4c6ab08d84062e3560476197c429c79bbb203f56d2873b743cd6991643cd5`  
		Last Modified: Tue, 07 Apr 2026 04:24:14 GMT  
		Size: 98.3 MB (98309873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06ffa2ba5933aea1f1c364c6a791a91c9e49057e35639f30985503d0547a7466`  
		Last Modified: Mon, 06 Apr 2026 18:41:04 GMT  
		Size: 89.1 MB (89084955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:685336058339beb76585899b9d6d0cb10feedc8950b1148e3b4871289be2513e`  
		Last Modified: Tue, 07 Apr 2026 04:24:11 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-trixie` - unknown; unknown

```console
$ docker pull golang@sha256:c68afe3483858f259ad92f3dbfb103c7d2b2e345d3032f3800bbd410212b8c42
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.9 MB (10935237 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ee7f098aebd809b8d71bf666fffd9e1292e5aa9f6593e21e6063fca01057666`

```dockerfile
```

-	Layers:
	-	`sha256:305088103f84e3ec55af6846cfe81c5cf381bc9b72d75726fac201913eaa658b`  
		Last Modified: Tue, 07 Apr 2026 04:24:12 GMT  
		Size: 10.9 MB (10906114 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:78bff8a6437638053cab1719ffaee88075f5bee6a6c193b26f3ec02cf18eb28c`  
		Last Modified: Tue, 07 Apr 2026 04:24:12 GMT  
		Size: 29.1 KB (29123 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-trixie` - linux; 386

```console
$ docker pull golang@sha256:a5f338e61090350967df90e785e8942e5afbea50b3d2b80ce56920e4dc7d0911
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **339.8 MB (339847721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25944051fc27d2bede4b56bbf2c8486851926a30299e15d542c178f6decf849b`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 01:46:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 07 Apr 2026 02:41:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 07 Apr 2026 04:17:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 04:19:46 GMT
ENV GOTOOLCHAIN=local
# Tue, 07 Apr 2026 04:19:46 GMT
ENV GOPATH=/go
# Tue, 07 Apr 2026 04:19:46 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 04:19:46 GMT
COPY /target/ / # buildkit
# Tue, 07 Apr 2026 04:19:49 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 07 Apr 2026 04:19:49 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:cdc6802f3021d1c2b9488d1de8ce2706686229997f4dcbab2461da2a3a1f115f`  
		Last Modified: Tue, 07 Apr 2026 00:11:26 GMT  
		Size: 50.8 MB (50819088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:467268048a14f0a2f523ec4fcb1cff704a19d6fe503c164c3374551f40e80aac`  
		Last Modified: Tue, 07 Apr 2026 01:46:39 GMT  
		Size: 26.8 MB (26783379 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68da593751d4ac5330362be2da2c6b0a17a5769b721979ff3214f729c53b720f`  
		Last Modified: Tue, 07 Apr 2026 02:41:41 GMT  
		Size: 69.8 MB (69795302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6513bdba9a487b52fd70a15cda97449d36bc1a5cac98608dbf689159eb544abe`  
		Last Modified: Tue, 07 Apr 2026 04:20:16 GMT  
		Size: 100.6 MB (100608026 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:434b82e2680f4d14426f015346712b6e5f30c486655039ad7e1ec71d21151434`  
		Last Modified: Mon, 06 Apr 2026 18:41:48 GMT  
		Size: 91.8 MB (91841768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c082a0c10c8e2e485850c416b4dade9e6f6812869499ac3c6a8bf46aaac36745`  
		Last Modified: Tue, 07 Apr 2026 04:20:13 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-trixie` - unknown; unknown

```console
$ docker pull golang@sha256:37361e9f8a039869037a7c07d3166a876bea1c30edceeedfcc90fbdea39410d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10785848 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07f43d45e612df63985d9ad645d92db26b93b604c8eb9fbb89cc2f41b7076ac9`

```dockerfile
```

-	Layers:
	-	`sha256:dd3f6468a56727254287d0618af7a06b372a0211b4bbf7fe46c804fd8d31a052`  
		Last Modified: Tue, 07 Apr 2026 04:20:14 GMT  
		Size: 10.8 MB (10756922 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cb01c107a1b37346bbf1b30e13523e2d5c366fd49018d44fa0c333d6b61dea6c`  
		Last Modified: Tue, 07 Apr 2026 04:20:13 GMT  
		Size: 28.9 KB (28926 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-trixie` - linux; ppc64le

```console
$ docker pull golang@sha256:bd9a2f0978b14e964c6e77509fec2751b952aaa9e9f805df0fe1cd056c2db1e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **336.8 MB (336838749 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc5df26a85f5881a33a0c20f5e0851d59ca260abf6b27594266faa5af89ca8ca`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1773619200'
# Tue, 17 Mar 2026 01:50:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 17 Mar 2026 06:05:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Mon, 30 Mar 2026 17:50:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 06 Apr 2026 18:57:14 GMT
ENV GOTOOLCHAIN=local
# Mon, 06 Apr 2026 18:57:14 GMT
ENV GOPATH=/go
# Mon, 06 Apr 2026 18:57:14 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 06 Apr 2026 18:57:14 GMT
COPY /target/ / # buildkit
# Mon, 06 Apr 2026 18:57:25 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 06 Apr 2026 18:57:25 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:616ed6c40b4f1136ebcda954e46e021bcee567aad248468321da4f4065f4a14d`  
		Last Modified: Mon, 16 Mar 2026 21:55:32 GMT  
		Size: 53.1 MB (53118350 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e76fd6649d6d35f910f2df9456726122ef27f29bb48c2f6e7ffbc7d318e0c0f`  
		Last Modified: Tue, 17 Mar 2026 01:51:12 GMT  
		Size: 27.0 MB (27013391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7e880a549306a0c27a7c0db6951a348b972ff41cbbc4c467d5d3c95c7797075`  
		Last Modified: Tue, 17 Mar 2026 06:06:09 GMT  
		Size: 73.0 MB (73033284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f19b2c0d1e3ca01e04689568b491176564ea4a25d80d79e56f5e79a395c2725b`  
		Last Modified: Mon, 30 Mar 2026 17:51:23 GMT  
		Size: 92.9 MB (92870771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6cc368d4f4523089f91977c543e8d1f1e4d28e3b0d524ab4ee1d1ce21debe4d`  
		Last Modified: Mon, 06 Apr 2026 18:58:20 GMT  
		Size: 90.8 MB (90802796 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22f7068803954658af696c60660babbeafbf6eb5ba5eb108a15a29964190a0c1`  
		Last Modified: Mon, 06 Apr 2026 18:58:17 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-trixie` - unknown; unknown

```console
$ docker pull golang@sha256:ed63a3ffbd41ff9a6e7449e1acf0f14d2bb409c729d5ec308710ae52e9d7751a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10810468 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59dbaf42dfa0854ae26780844365b5f72f7ecfc39364e03a6aabe1ddb140df91`

```dockerfile
```

-	Layers:
	-	`sha256:755c41fb7e0792538b82155a9637ba7741e262d061f3d516874fde29ee57f21a`  
		Last Modified: Mon, 06 Apr 2026 18:58:18 GMT  
		Size: 10.8 MB (10781447 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5c3adf74973a0ee91563abf4136f137b81cd5f74b421a0a6cf181e60262dfbf9`  
		Last Modified: Mon, 06 Apr 2026 18:58:17 GMT  
		Size: 29.0 KB (29021 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-trixie` - linux; riscv64

```console
$ docker pull golang@sha256:b0aa841e2ca357d75ebf81f239535a1149d19b56514fabe7cace87bb9b073dc9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **362.2 MB (362159828 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d326428a4f7feb2aa62891f1eda40bd5e6803ae1e34babb3a034ecd4ee3a222`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1773619200'
# Wed, 18 Mar 2026 05:11:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Thu, 19 Mar 2026 05:31:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Sat, 21 Mar 2026 04:55:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 30 Mar 2026 18:23:56 GMT
ENV GOTOOLCHAIN=local
# Mon, 30 Mar 2026 18:23:56 GMT
ENV GOPATH=/go
# Mon, 30 Mar 2026 18:23:56 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 30 Mar 2026 18:23:56 GMT
COPY /target/ / # buildkit
# Mon, 30 Mar 2026 18:24:13 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 30 Mar 2026 18:24:14 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:90acba8ac92ad141ae919a99e64549b2f417e5b2ec79f1a99dbc8efba0fea96b`  
		Last Modified: Mon, 16 Mar 2026 22:09:11 GMT  
		Size: 47.8 MB (47792328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8d52d7ab982f4bfd5cfc38caa0eefe3bfddcb1b2f76f02a38e1b10725b762ee`  
		Last Modified: Wed, 18 Mar 2026 05:13:23 GMT  
		Size: 25.0 MB (24954925 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fc9a450c15c86147b6c308f2cb25a618ec75f2ab5a64203aa728b5e309ab137`  
		Last Modified: Thu, 19 Mar 2026 05:35:26 GMT  
		Size: 66.7 MB (66662504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a9c3d8cb0eb3839f60f443c07c78a4e233d415f3d669a49057b1e5f1b8cb424`  
		Last Modified: Sat, 21 Mar 2026 05:03:52 GMT  
		Size: 131.7 MB (131650375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b6e70b1853c9d42c6bcadfebf9fcf629114d0890e516270d3e090097d9a57f9`  
		Last Modified: Mon, 30 Mar 2026 18:30:56 GMT  
		Size: 91.1 MB (91099540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4959cdbfb7a2089aed29e3e820777655dddc157d9325abb7f203faf1d6b21ffb`  
		Last Modified: Mon, 30 Mar 2026 18:30:40 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-trixie` - unknown; unknown

```console
$ docker pull golang@sha256:28c3d9c17b26d7eec8e0834ab7d6f9a9f24ff8f84715c9b69a50a9463b413351
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.9 MB (10884303 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0dd8771f3369dfb3472a9730b8186c08337c943916cbfe6ab628d00c655193d`

```dockerfile
```

-	Layers:
	-	`sha256:1e659411d760c64c158d64798869be5156cec426de937e41214fb044afda50b8`  
		Last Modified: Mon, 30 Mar 2026 18:30:43 GMT  
		Size: 10.9 MB (10855280 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8091309a98e98978e9d48ad8e4046f545714313a49ff255994fd6326e8de85d0`  
		Last Modified: Mon, 30 Mar 2026 18:30:40 GMT  
		Size: 29.0 KB (29023 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-trixie` - linux; s390x

```console
$ docker pull golang@sha256:ec2b31dcdbe3cbfbc7d1cfea0f65d1c37f93fd97f415aee8bfc689aad0a60c0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **314.0 MB (313960290 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:559a3ab506ed8bce4bdb3ba1699843cb51c31e4aa83fdbb567b45d23de02eaa9`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 03:05:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 07 Apr 2026 04:54:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 07 Apr 2026 06:01:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 06 Apr 2026 20:02:38 GMT
ENV GOTOOLCHAIN=local
# Mon, 06 Apr 2026 20:02:38 GMT
ENV GOPATH=/go
# Mon, 06 Apr 2026 20:02:38 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 06 Apr 2026 20:02:38 GMT
COPY /target/ / # buildkit
# Tue, 07 Apr 2026 08:05:56 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 07 Apr 2026 08:05:56 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:99ccdb9e0b0ce79a36cbcc433fd972b049c1e4e84d217954de0e89224b1fb094`  
		Last Modified: Tue, 07 Apr 2026 00:13:49 GMT  
		Size: 49.4 MB (49365104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5e9a487bea803d0a108535f515bb38cbace4ed2fd0cf55a04f448d8a910181b`  
		Last Modified: Tue, 07 Apr 2026 03:05:59 GMT  
		Size: 26.8 MB (26803044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:528b42c01b5de7637ae2e011d2f9775f913b01f72b9797773d410bb0d8b437e3`  
		Last Modified: Tue, 07 Apr 2026 04:55:14 GMT  
		Size: 68.6 MB (68627207 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de09fb86ca93d03c7033a68934d3836b7d73a92db92a91d8e192cade1e2b3477`  
		Last Modified: Tue, 07 Apr 2026 06:02:25 GMT  
		Size: 76.0 MB (75981910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:caa7bb14b36d862c74817ebfb57b26695332f89670a6fc97f1c869402d1de33e`  
		Last Modified: Mon, 06 Apr 2026 20:04:12 GMT  
		Size: 93.2 MB (93182867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f63e646812303a9e565e4405730de90652312f31e822b259e93d4e010853c2bc`  
		Last Modified: Tue, 07 Apr 2026 08:06:22 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-trixie` - unknown; unknown

```console
$ docker pull golang@sha256:08157e445f2687516fbfc95757e294f32477a76361829a6c0753ad17803b42b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10625023 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f343f70091897acd7f6cba2e9e48f5594defed2c23488ec59577bf20ee076317`

```dockerfile
```

-	Layers:
	-	`sha256:5e8fb0ef8bf006d7ad21f208edaee1d1e197a896bd0f762676e11e522facc65c`  
		Last Modified: Tue, 07 Apr 2026 08:06:22 GMT  
		Size: 10.6 MB (10596059 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4fdcf39b3dfe0dd001a907b2c005ddcb46aa76b6f67ee4f209563a1f6a83d72f`  
		Last Modified: Tue, 07 Apr 2026 08:06:22 GMT  
		Size: 29.0 KB (28964 bytes)  
		MIME: application/vnd.in-toto+json
