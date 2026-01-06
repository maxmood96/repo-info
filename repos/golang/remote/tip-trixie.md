## `golang:tip-trixie`

```console
$ docker pull golang@sha256:8d4fec73a6c76e19359944baae185800571ec0266e7b4abc2b305fa0f8362b70
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
$ docker pull golang@sha256:fb8deadf380848da503eee01de64ff8637bfd2b877c4fbb28469ac95fec01bc6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **339.8 MB (339838541 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c895d5fd72e3cf9a973b58c33fac470dbaec1d3c3ca4733577d9f8b80b066b13`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1766966400'
# Mon, 29 Dec 2025 23:47:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 30 Dec 2025 01:23:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Mon, 05 Jan 2026 20:11:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 05 Jan 2026 20:13:13 GMT
ENV GOTOOLCHAIN=local
# Mon, 05 Jan 2026 20:13:13 GMT
ENV GOPATH=/go
# Mon, 05 Jan 2026 20:13:13 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 05 Jan 2026 20:13:13 GMT
COPY /target/ / # buildkit
# Mon, 05 Jan 2026 20:13:15 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 05 Jan 2026 20:13:15 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:281b80c799ded5b9a390d2e8c59930db01ee395ab809dd34259897c660751f4e`  
		Last Modified: Mon, 29 Dec 2025 22:31:07 GMT  
		Size: 49.3 MB (49289587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15f14138abe4f09d3ef3953105144728056046ae469ae21e8e42749bacd67cca`  
		Last Modified: Mon, 29 Dec 2025 23:47:42 GMT  
		Size: 25.6 MB (25613989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:378c64c4458002be86f2d86c5768ae9ec0cff69afac7d1444e50206dc4566fa9`  
		Last Modified: Tue, 30 Dec 2025 01:24:00 GMT  
		Size: 67.8 MB (67777233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fe39c30358f134159a00f197271b048425f279534ea678da67fec5727b79c56`  
		Last Modified: Mon, 05 Jan 2026 20:14:14 GMT  
		Size: 102.1 MB (102108867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fff8d0c9ecfcf551b6bfe3152ed041603d59cea546df67e4bc43073bc9a2f5e7`  
		Last Modified: Mon, 05 Jan 2026 20:14:07 GMT  
		Size: 95.0 MB (95048707 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8e445285f682bf70d4f2c404cd484b4bd337a158bd5cd4342fd3bf1e669553e`  
		Last Modified: Mon, 05 Jan 2026 20:13:56 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-trixie` - unknown; unknown

```console
$ docker pull golang@sha256:8abdc42aa417b02b8971250631ff1d7c4efde9937cdf7f8ec78ca913951d39b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10813477 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75039a657772517e5e4c5fff6cd1221cd6f6da7076ddcfa0038fb2d07772ec82`

```dockerfile
```

-	Layers:
	-	`sha256:37f20324b9a1be260270333f70f62069219036adf16c5c36964e473f3377d950`  
		Last Modified: Mon, 05 Jan 2026 21:23:55 GMT  
		Size: 10.8 MB (10784508 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:904130546c5287d0e254a06fcfb5f4e7c14d13d0f1eb05e912ca4d3548de9cbd`  
		Last Modified: Mon, 05 Jan 2026 21:23:56 GMT  
		Size: 29.0 KB (28969 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-trixie` - linux; arm variant v7

```console
$ docker pull golang@sha256:8f7d7014d8fa2361759ead5a606458af463b64e78d179183b75b96061533b405
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.9 MB (295932474 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de6920343312c241fde0d896e683e5bbf4c9f5ca779540ba4f0596afad228768`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1766966400'
# Tue, 30 Dec 2025 00:35:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 30 Dec 2025 02:07:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Mon, 05 Jan 2026 20:13:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 05 Jan 2026 20:15:44 GMT
ENV GOTOOLCHAIN=local
# Mon, 05 Jan 2026 20:15:44 GMT
ENV GOPATH=/go
# Mon, 05 Jan 2026 20:15:44 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 05 Jan 2026 20:15:44 GMT
COPY /target/ / # buildkit
# Mon, 05 Jan 2026 20:15:47 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 05 Jan 2026 20:15:47 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:d20050ceedb84a03f8a4208462819500ff366fe1a69cdbba74b118aa8a38a87a`  
		Last Modified: Mon, 29 Dec 2025 22:28:10 GMT  
		Size: 45.7 MB (45718317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1468c2ee0f43e81d6e097b24054de66ae95db50d77cef08d1eabe51a5dab43cd`  
		Last Modified: Tue, 30 Dec 2025 00:36:02 GMT  
		Size: 23.6 MB (23619911 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fa494d16bf7a563003db4c95fa508ca504a77c791075afbc16c7f5a1be17761`  
		Last Modified: Tue, 30 Dec 2025 02:07:44 GMT  
		Size: 62.7 MB (62713662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a0c2e25c1ec196454cc60e5438ab6e209fe1400a407990fccaba0c2abd1997d`  
		Last Modified: Tue, 06 Jan 2026 02:33:20 GMT  
		Size: 72.8 MB (72754133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83e6b96a7f28bc62643bd07c2486d1581cdd92ecf9bab96beac98ff164054e9b`  
		Last Modified: Tue, 06 Jan 2026 02:36:10 GMT  
		Size: 91.1 MB (91126293 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16ffd08e07f711fb3e9dfa92be3d3b3e8c49b15829a8d30de49aa8e68bc2f39b`  
		Last Modified: Mon, 05 Jan 2026 20:16:25 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-trixie` - unknown; unknown

```console
$ docker pull golang@sha256:eab2c3ca140df8e2a418bfa5d42582f7274b9cc16d847d295cb10b8eb1548d3e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10609486 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a59934095938e10e8efe4c5b430694f480fca7f904e927be58f72de491a2f21`

```dockerfile
```

-	Layers:
	-	`sha256:7fd1d81463717d923bee30813ee683d28281400b3c7debccf3ac013b251abbb7`  
		Last Modified: Mon, 05 Jan 2026 21:24:04 GMT  
		Size: 10.6 MB (10580395 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ef4cd7bcd393fc5b2d24d82758017c1fb643a40350dc963e1f7d24c17478410c`  
		Last Modified: Mon, 05 Jan 2026 21:24:05 GMT  
		Size: 29.1 KB (29091 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-trixie` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:5722018c013493dbcb65061404a4dbecc8da78661c05847be887913ff1838242
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **330.6 MB (330644126 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f64f64d7749ea4ae9ebde5e5a8ade3dad0e43b9bab561016b004306018c7072`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1766966400'
# Mon, 29 Dec 2025 23:47:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 30 Dec 2025 01:25:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Mon, 05 Jan 2026 20:11:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 05 Jan 2026 20:12:38 GMT
ENV GOTOOLCHAIN=local
# Mon, 05 Jan 2026 20:12:38 GMT
ENV GOPATH=/go
# Mon, 05 Jan 2026 20:12:38 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 05 Jan 2026 20:12:38 GMT
COPY /target/ / # buildkit
# Mon, 05 Jan 2026 20:12:41 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 05 Jan 2026 20:12:41 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:5785abec2864dcd8d343ccd872458a50ffb2a61739bc46a79709c68c455cb8fc`  
		Last Modified: Mon, 29 Dec 2025 22:30:57 GMT  
		Size: 49.7 MB (49650193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dce2d1ead36d47118631ae52b25fc39c1aa005c68093dd34e456927908318c52`  
		Last Modified: Mon, 29 Dec 2025 23:47:57 GMT  
		Size: 25.0 MB (25021045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5d9404781930ac9b1a80bc4d3e616b480ed1eeab70b8545e9988a3a11d00783`  
		Last Modified: Tue, 30 Dec 2025 01:26:07 GMT  
		Size: 67.6 MB (67583784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f478454ffcac5ff13580e3a622693484e588a795e8b305bca5ece5fe9c1648cc`  
		Last Modified: Tue, 06 Jan 2026 00:09:54 GMT  
		Size: 98.3 MB (98254477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32ea799c03d09b63583e3ebd313f2aacd577c4821e87f618e936a7b9c3c7ca14`  
		Last Modified: Mon, 05 Jan 2026 20:13:38 GMT  
		Size: 90.1 MB (90134470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a4120579443f864f2704f75dd3e9d143f45b50496ef3952eae23f0797595edc`  
		Last Modified: Mon, 05 Jan 2026 20:13:23 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-trixie` - unknown; unknown

```console
$ docker pull golang@sha256:82d92b6db9fcd8ea64677b265f2614d6efd2094f8895ff593cbb31fa00081284
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.9 MB (10934087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1945165f0dd2b4761c6c6ae9ecd7357ea92dc335e5f1260a360011882f2b17d8`

```dockerfile
```

-	Layers:
	-	`sha256:e19db79539582c64d10b6258b240a02e34c2c87ccfae916e76314716288587ad`  
		Last Modified: Mon, 05 Jan 2026 21:24:15 GMT  
		Size: 10.9 MB (10904963 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5c6144d5575938ac2e4305dcad074d20575249a1ef04de04e225bcd966e6faf6`  
		Last Modified: Mon, 05 Jan 2026 21:24:17 GMT  
		Size: 29.1 KB (29124 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-trixie` - linux; 386

```console
$ docker pull golang@sha256:e02ec855c4cdfa3201d99d91acc89a08d257a16c5475ad4d7203ca0544af314a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **340.9 MB (340873217 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ccf68693f6b159d2f16bc8248e4d9018535ca8c3f63885a4040de23676b9399`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1766966400'
# Mon, 29 Dec 2025 23:47:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 30 Dec 2025 00:34:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Mon, 05 Jan 2026 20:12:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 05 Jan 2026 20:14:42 GMT
ENV GOTOOLCHAIN=local
# Mon, 05 Jan 2026 20:14:42 GMT
ENV GOPATH=/go
# Mon, 05 Jan 2026 20:14:42 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 05 Jan 2026 20:14:42 GMT
COPY /target/ / # buildkit
# Mon, 05 Jan 2026 20:14:44 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 05 Jan 2026 20:14:44 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:7ba68d5e03a08e607fe00d0a9f5d3925adc34700fc401165e5513c0d55ae9d2e`  
		Last Modified: Mon, 29 Dec 2025 22:27:39 GMT  
		Size: 50.8 MB (50801684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fabb00c990eb2d1ca8a4037bb0b9c6e0d0d8b6c6fb47372c8ec75cd65588cdd8`  
		Last Modified: Mon, 29 Dec 2025 23:47:40 GMT  
		Size: 26.8 MB (26776375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fc67c159b6d502873d04e7b21d326f226b1fd89576f5d5cd1b817d74d68fee4`  
		Last Modified: Tue, 30 Dec 2025 00:34:34 GMT  
		Size: 69.8 MB (69794792 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:486936558c961a37bdad248aed41e701eb2a91f2e58485b3febd2054f25df864`  
		Last Modified: Mon, 05 Jan 2026 20:15:37 GMT  
		Size: 100.6 MB (100555397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea7adeeca0c05b570f562d36e2ca80fe92bff9d338efdfb31d2c7a616347bb0c`  
		Last Modified: Mon, 05 Jan 2026 20:15:35 GMT  
		Size: 92.9 MB (92944811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7ea2709c960833092d733c0ea59bbf03b48edcd53c45b65e99be83e88b36dea`  
		Last Modified: Mon, 05 Jan 2026 20:15:27 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-trixie` - unknown; unknown

```console
$ docker pull golang@sha256:250dd8ac54c2102a23556c4da2729179ce3078f9796307efe7c407925ba5147c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10784697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad04d365bc7f76cc729993744cf9f2f5b0f0a54e349007e41dd27af47f620805`

```dockerfile
```

-	Layers:
	-	`sha256:ddcdbf8b0947c887c25e052d9efc724279ca3a27138d4d40477886f67b4f68c4`  
		Last Modified: Mon, 05 Jan 2026 21:24:26 GMT  
		Size: 10.8 MB (10755772 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b83e96d5391f213a6ebd19a7fda8876b7f1255fbf7bfd421c5fff15793c47b06`  
		Last Modified: Mon, 05 Jan 2026 21:24:27 GMT  
		Size: 28.9 KB (28925 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-trixie` - linux; ppc64le

```console
$ docker pull golang@sha256:e6ac12d6d63df87d418ae0f82e7d48598cc51191457bf8cad66b177ed98dbb15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **337.6 MB (337632615 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1611d30bd2b1e6eb806395971faa81ca548c6362498d24dc943821c6b06ed55f`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1766966400'
# Tue, 30 Dec 2025 03:18:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 30 Dec 2025 08:22:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 30 Dec 2025 10:23:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 05 Jan 2026 20:13:42 GMT
ENV GOTOOLCHAIN=local
# Mon, 05 Jan 2026 20:13:42 GMT
ENV GOPATH=/go
# Mon, 05 Jan 2026 20:13:42 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 05 Jan 2026 20:13:42 GMT
COPY /target/ / # buildkit
# Mon, 05 Jan 2026 20:13:51 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 05 Jan 2026 20:13:52 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:d586c84fb9377f9b3f4030e2c3e1e9ff7b1a23a68b8abc2c48a43163a3589257`  
		Last Modified: Tue, 30 Dec 2025 01:51:01 GMT  
		Size: 53.1 MB (53108485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd44afe623a2af1e017b0756e314b5b0882afdc551ddbb8ab4a0e0d718eb8f20`  
		Last Modified: Tue, 30 Dec 2025 03:19:14 GMT  
		Size: 27.0 MB (26996817 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1464b5ef37e07d88bfdddc49e0cb0b76c46c151a0ee23e6a2bd75bd6783f9790`  
		Last Modified: Tue, 30 Dec 2025 08:23:35 GMT  
		Size: 73.0 MB (73031008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32c305b2563d5a320b2f5d542cb42b58b482a07941244656f1dd066b0fb90900`  
		Last Modified: Tue, 30 Dec 2025 10:25:02 GMT  
		Size: 92.8 MB (92815505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cd0091ff10375737167c3b5f9f5d9decb460a2e2aef6a9ae134067abb7cbf2b`  
		Last Modified: Mon, 05 Jan 2026 20:15:39 GMT  
		Size: 91.7 MB (91680642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4ceb1c604e886374029d4147565c0001f8016321f5cfd6f82c9d05220c0db72`  
		Last Modified: Mon, 05 Jan 2026 20:15:27 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-trixie` - unknown; unknown

```console
$ docker pull golang@sha256:77eea0b4701194d966a5833e88cfe91e0e38f0da8cb9ec74137dba2a0cab99c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10809315 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1bbce4e010ceb620e63f5c5656e800eed51ce1cd1a9112154e36f3a576753e6`

```dockerfile
```

-	Layers:
	-	`sha256:ea0245e7d3e7fe86c99f625ca8fe175ddac2a32656c1aa9ce1762d1868841f32`  
		Last Modified: Mon, 05 Jan 2026 21:24:37 GMT  
		Size: 10.8 MB (10780294 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f34a03a9c28f13ac9fe468335e965923bb12ae89f07cf5f14dd6a559cb9b1331`  
		Last Modified: Mon, 05 Jan 2026 21:24:38 GMT  
		Size: 29.0 KB (29021 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-trixie` - linux; riscv64

```console
$ docker pull golang@sha256:4227b64b234ea11f6fc98f6266e3fb5a8f989cf916c05dfdbdd38183b10f77fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **363.3 MB (363293476 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c104e5c5e1534220ae2ab104e6d994efc7941de17712943a63fc1090b5cd4918`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1766966400'
# Wed, 31 Dec 2025 10:16:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Thu, 01 Jan 2026 12:43:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Fri, 02 Jan 2026 20:23:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 06 Jan 2026 01:07:38 GMT
ENV GOTOOLCHAIN=local
# Tue, 06 Jan 2026 01:07:38 GMT
ENV GOPATH=/go
# Tue, 06 Jan 2026 01:07:38 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 06 Jan 2026 01:07:38 GMT
COPY /target/ / # buildkit
# Tue, 06 Jan 2026 01:07:55 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 06 Jan 2026 01:07:55 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:aaf3ef12aa0c431a6203a456b21b1e30e26cb56dfc257b8bca2efe1ba7c531de`  
		Last Modified: Tue, 30 Dec 2025 00:51:33 GMT  
		Size: 47.8 MB (47771153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc3f7933c6ef71f06a1f0f33145f157cbfe6df70a0a3efc496c514e6bf0f3c52`  
		Last Modified: Wed, 31 Dec 2025 10:17:43 GMT  
		Size: 25.0 MB (24953863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e727fba04feac92f30181733d92a9aab095f91af402efca58918b26fc389037e`  
		Last Modified: Thu, 01 Jan 2026 12:46:54 GMT  
		Size: 66.7 MB (66660576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83b560385f3861ed5a056fb65f6efa479b98fb4edb93cd21d11160f19961a6e0`  
		Last Modified: Fri, 02 Jan 2026 20:32:15 GMT  
		Size: 131.6 MB (131594843 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0c89a20e33326bd3dc067a98c23f95a9f71a46db050c57b5d95bf4165852889`  
		Last Modified: Tue, 06 Jan 2026 01:15:07 GMT  
		Size: 92.3 MB (92312883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a854a0e7ecb9ef44b4aa62f32b01bf67fd4beb6d7776cb78b502c99f40235383`  
		Last Modified: Tue, 06 Jan 2026 01:14:59 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-trixie` - unknown; unknown

```console
$ docker pull golang@sha256:82940c3600f37b2b532932f72d57cd3c099955dd153506477a2ff52555ad4686
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.9 MB (10883154 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:845399ab2348e5670bef91a3be11398e46548c4d1812aa5e35d6334024744123`

```dockerfile
```

-	Layers:
	-	`sha256:33d146c0d9911e481f3fb6176fe62f919ed36b93944794e58b8a3e0cabe21fc0`  
		Last Modified: Tue, 06 Jan 2026 03:24:05 GMT  
		Size: 10.9 MB (10854127 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9a823c4dc98b1ef77e153dc72ea02fc1734c629a85254b4c97fc4f4510311ece`  
		Last Modified: Tue, 06 Jan 2026 03:24:06 GMT  
		Size: 29.0 KB (29027 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-trixie` - linux; s390x

```console
$ docker pull golang@sha256:f040a37a6a62767a71903484333ad4f6f4a6f0fea9772b0dda28facb3107c81b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **314.9 MB (314906990 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc115a2ba02f32c3f8f3b2cd5db2b626dbd249fa5692b3baf1f11c536bbebad4`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1766966400'
# Tue, 30 Dec 2025 04:14:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 30 Dec 2025 06:03:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Mon, 05 Jan 2026 20:14:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 05 Jan 2026 20:13:53 GMT
ENV GOTOOLCHAIN=local
# Mon, 05 Jan 2026 20:13:53 GMT
ENV GOPATH=/go
# Mon, 05 Jan 2026 20:13:53 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 05 Jan 2026 20:13:53 GMT
COPY /target/ / # buildkit
# Mon, 05 Jan 2026 20:14:04 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 05 Jan 2026 20:14:04 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:85bc4a4d1f4e52a33d42907057e0ab87c5eb2560b332d94f6e9d7da79c0c76b8`  
		Last Modified: Tue, 30 Dec 2025 03:26:29 GMT  
		Size: 49.3 MB (49345959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7ac6efd7cfec1d611dcf0011d64b56f69fe5f6fe47195e090cb8c04e2584e93`  
		Last Modified: Tue, 30 Dec 2025 04:14:36 GMT  
		Size: 26.8 MB (26786464 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:978ec2f50f1462efd64a546370da30e382c7f6044ad53993a4af33689f25341a`  
		Last Modified: Tue, 30 Dec 2025 06:04:24 GMT  
		Size: 68.6 MB (68630336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6456995ae6524fffc7b4ebe4332c1913baad4a63bb1876c47a776c976b1b6d2`  
		Last Modified: Mon, 05 Jan 2026 20:14:50 GMT  
		Size: 75.9 MB (75919580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65c1a057ff0ba348d0b96ad5fd481980beed6ee225e3440d5e3c814a12014a9d`  
		Last Modified: Mon, 05 Jan 2026 20:14:55 GMT  
		Size: 94.2 MB (94224494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8d780a347f44b66c0d60d8a4709e94891f98abb411cc6877d5103569eaf31c4`  
		Last Modified: Mon, 05 Jan 2026 20:14:43 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-trixie` - unknown; unknown

```console
$ docker pull golang@sha256:2487094a535d046b1f6971b2a6e75e6b0a65f4b79ca150169b6939b413dc5d7e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10623872 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a8887f70a25bbf79a1b085d8fddc117830d25af6af6b575c6dce82ffed08735`

```dockerfile
```

-	Layers:
	-	`sha256:d6c3e68e44c6b306ea2fa69fc52bf4bb82f0415e93f5a3a4d1688d0558d9f82f`  
		Last Modified: Mon, 05 Jan 2026 21:24:47 GMT  
		Size: 10.6 MB (10594908 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4137c971a75a640749d857ef8f112be4ed070c0c34c335c49adb12cdca2ebb33`  
		Last Modified: Mon, 05 Jan 2026 21:24:48 GMT  
		Size: 29.0 KB (28964 bytes)  
		MIME: application/vnd.in-toto+json
