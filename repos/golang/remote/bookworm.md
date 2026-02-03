## `golang:bookworm`

```console
$ docker pull golang@sha256:52f27e9c1f64d44e8517e8e40db0476a0198647c551472e3655933a4b92e5c21
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

### `golang:bookworm` - linux; amd64

```console
$ docker pull golang@sha256:fae400019c7fb0400bca0b749fde2015f993ff0e0293ca6f8dbaf919650bb419
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.5 MB (289502168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:120f24054f0090d151c099f9c254ca52104037e84f6750c09643690be5510c09`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1768176000'
# Tue, 13 Jan 2026 02:08:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 03:53:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 19:31:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 19:31:01 GMT
ENV GOLANG_VERSION=1.25.6
# Thu, 15 Jan 2026 19:31:01 GMT
ENV GOTOOLCHAIN=local
# Thu, 15 Jan 2026 19:31:01 GMT
ENV GOPATH=/go
# Thu, 15 Jan 2026 19:31:01 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 15 Jan 2026 19:31:01 GMT
COPY /target/ / # buildkit
# Thu, 15 Jan 2026 19:31:05 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Thu, 15 Jan 2026 19:31:05 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:c1be109a62df95316ceac87ea501079f32e17f36b636865a860841b7db06100c`  
		Last Modified: Tue, 13 Jan 2026 00:41:15 GMT  
		Size: 48.5 MB (48481622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64538a062a61add8dc8b290fa69475e8902eb839c497a5f5dcd5a950422e493c`  
		Last Modified: Tue, 13 Jan 2026 02:09:00 GMT  
		Size: 24.0 MB (24036867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd1872fa12cc6b1145803f1a0679ca26cc65fa1b4e0ee389bfb30267594736b6`  
		Last Modified: Tue, 13 Jan 2026 03:53:27 GMT  
		Size: 64.4 MB (64395833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e232fbc8179a6afd48c44faf1a55868346a9748d392a36fa708a38fde2cbe4ea`  
		Last Modified: Thu, 15 Jan 2026 19:31:31 GMT  
		Size: 92.4 MB (92433398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20c503e035cd5c1ea67986d21ed1fb2f4305f801555c52f9f16ce0f0f5cf2e16`  
		Last Modified: Thu, 15 Jan 2026 19:31:09 GMT  
		Size: 60.2 MB (60154290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1bb226003e548404f71597f5e9b6fea18e4c8bd4959346f6dc6da69134a66e1`  
		Last Modified: Thu, 15 Jan 2026 19:31:20 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:e716cc9f6ca89dab606d6a5a0a28c257f3d2a796837e4e2653f457af7f3d2fa7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10524179 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6645c6c546af1b7acf9dfc8ee38025c982a55ede8d681e386c3b896fc8f539da`

```dockerfile
```

-	Layers:
	-	`sha256:1d92b835bfc97b02e0d0d8352abff67c03ede94887c4ef9e53d67b2937f85094`  
		Last Modified: Thu, 15 Jan 2026 19:31:28 GMT  
		Size: 10.5 MB (10496383 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f0a903c8cb4ad2ee09e3408cf5599f2d86b32a5721aae74e19aea0f74cff0a69`  
		Last Modified: Thu, 15 Jan 2026 19:31:28 GMT  
		Size: 27.8 KB (27796 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:bookworm` - linux; arm variant v7

```console
$ docker pull golang@sha256:2a11359f62236e9f48aea87f6ef869cc31689a8a8a39231d4d684c56a94db50e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **251.2 MB (251154944 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1ab0bcd212d31c12d1f2cf3636da326bb839efa050802bc8dc7bddcb278b3e5`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1768176000'
# Tue, 13 Jan 2026 02:57:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 04:24:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 19:31:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 19:30:50 GMT
ENV GOLANG_VERSION=1.25.6
# Thu, 15 Jan 2026 19:30:50 GMT
ENV GOTOOLCHAIN=local
# Thu, 15 Jan 2026 19:30:50 GMT
ENV GOPATH=/go
# Thu, 15 Jan 2026 19:30:50 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 15 Jan 2026 19:30:50 GMT
COPY /target/ / # buildkit
# Thu, 15 Jan 2026 19:31:36 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Thu, 15 Jan 2026 19:31:36 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:d1f8df344790c402ed8a818bba76e9111f5e212418c662cf0574919edf68933b`  
		Last Modified: Tue, 13 Jan 2026 00:42:02 GMT  
		Size: 44.2 MB (44198845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6b61baedfd715aa7493fd2550daee1914be821a60dd0067158988236109172a`  
		Last Modified: Tue, 13 Jan 2026 02:57:20 GMT  
		Size: 21.9 MB (21941488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a97f9f395cd1e9e02761196527b4253d5246be969781795c278996437891e5cf`  
		Last Modified: Tue, 13 Jan 2026 04:25:03 GMT  
		Size: 59.7 MB (59652006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04030ddfb9df8088de2d0050995ba5101bfe63a9cdda21947b2aae48df2e280d`  
		Last Modified: Thu, 15 Jan 2026 19:31:56 GMT  
		Size: 66.3 MB (66288637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9858bd230951a4669967b265976b2f7dbd9f374059998fadb8d8956bf7de2a2`  
		Last Modified: Thu, 15 Jan 2026 19:30:05 GMT  
		Size: 59.1 MB (59073810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bece4725239cdc17443a0c5c353372b564cae29f8bb2faccd334d717908add2`  
		Last Modified: Thu, 15 Jan 2026 19:31:52 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:119d2f5ecd3bcce4c80dc9e259f8c345173003f6c22bf6fda361557fbb6e0346
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10331000 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01b9a7d8d31b9f302148aae1b5e4821253ab8c8330ccc792660669caaa41beea`

```dockerfile
```

-	Layers:
	-	`sha256:a647317282e9f194119a10968708bfa29456321f4b1123b160e16ce7624076e7`  
		Last Modified: Thu, 15 Jan 2026 19:31:54 GMT  
		Size: 10.3 MB (10303097 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9bd0ee6e33366ca35f99083c319f240f85f797d77e1c6a4d11092d2dfa57d5ac`  
		Last Modified: Thu, 15 Jan 2026 19:31:54 GMT  
		Size: 27.9 KB (27903 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:bookworm` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:1efabe7cb767b0153c5aaff88b290d582ff9bdad452e1240e7a0dc8ead18d476
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **280.6 MB (280616183 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b642dc8c5cd54eb4f4219e85aaf215cb47ae316ef381ce374d69535e88cd821d`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 02:44:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 03:46:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 04:21:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 04:21:55 GMT
ENV GOLANG_VERSION=1.25.6
# Tue, 03 Feb 2026 04:21:55 GMT
ENV GOTOOLCHAIN=local
# Tue, 03 Feb 2026 04:21:55 GMT
ENV GOPATH=/go
# Tue, 03 Feb 2026 04:21:55 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Feb 2026 04:21:55 GMT
COPY /target/ / # buildkit
# Tue, 03 Feb 2026 04:22:00 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 03 Feb 2026 04:22:00 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:64e8f4c09e7ac936ecc3deb0e61613f653224c28b2e35fa9d8e6e11cbdb5f911`  
		Last Modified: Tue, 03 Feb 2026 01:13:22 GMT  
		Size: 48.4 MB (48365956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:404413e6e45accf116074dace885c7ccf2917479ae04f2f46c046b6ae1909254`  
		Last Modified: Tue, 03 Feb 2026 02:44:54 GMT  
		Size: 23.6 MB (23604842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1e9aa4982c2a67e202ea283fc3760e94d8d8b16966c616e01ad0238abbaac82`  
		Last Modified: Tue, 03 Feb 2026 03:46:50 GMT  
		Size: 64.5 MB (64479687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d461d84e8690415ec23828f563fc5f68b5877bb57f6ffcc1207c622da4e44952`  
		Last Modified: Tue, 03 Feb 2026 04:22:24 GMT  
		Size: 86.5 MB (86506345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:243a2f381e4cd3963e3af5194953e3e2807c452e833bf69397dee70610e428e6`  
		Last Modified: Thu, 15 Jan 2026 19:30:21 GMT  
		Size: 57.7 MB (57659196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:910f998782dbdf00fc18bca12bacfe89d896caf70c4e4e63b737d48ff1e49131`  
		Last Modified: Tue, 03 Feb 2026 04:22:22 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:b2376b5248c239b5cfc641ad94dadb0e249f0897f589ad9c62854db6b4a74884
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10552162 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:059f45f4374526742b333b716d31ac5408b2a275f96539e12c1ec7d83c7c4c1f`

```dockerfile
```

-	Layers:
	-	`sha256:0bddb42a78941243a5122cd11d30746f598c5a3cd77275075c332c2dd179ddad`  
		Last Modified: Tue, 03 Feb 2026 04:22:23 GMT  
		Size: 10.5 MB (10524231 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1f35126a1cae809f6aec75560a9205c891e7946c5b08a00b9c8b424272de0faa`  
		Last Modified: Tue, 03 Feb 2026 04:22:22 GMT  
		Size: 27.9 KB (27931 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:bookworm` - linux; 386

```console
$ docker pull golang@sha256:cae2d399c77e77b70e2135bc75038bee6a824876854420577399c8b6cf6de622
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.3 MB (289304990 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85f1448c02e3f192e4970bdca24eb65dff3ace3391556fd877b6abb0fbff481e`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1768176000'
# Tue, 13 Jan 2026 02:02:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 03:03:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 19:32:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 19:32:12 GMT
ENV GOLANG_VERSION=1.25.6
# Thu, 15 Jan 2026 19:32:12 GMT
ENV GOTOOLCHAIN=local
# Thu, 15 Jan 2026 19:32:12 GMT
ENV GOPATH=/go
# Thu, 15 Jan 2026 19:32:12 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 15 Jan 2026 19:32:12 GMT
COPY /target/ / # buildkit
# Thu, 15 Jan 2026 19:32:16 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Thu, 15 Jan 2026 19:32:16 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:2ec54d337d067729b748c8f421e417d2e02e79e9e0caf328deaa1b815a93c883`  
		Last Modified: Tue, 13 Jan 2026 00:41:57 GMT  
		Size: 49.5 MB (49468594 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63ef3b5e8322d4c8e5ca6198e931fb91c384bac3ef8aafd81a71617e9534b7ab`  
		Last Modified: Tue, 13 Jan 2026 02:02:14 GMT  
		Size: 24.9 MB (24871330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20be0f262f5ef3547fc45c5726dd33bf707569fc1cceccb9f87c4f4965c4f9ed`  
		Last Modified: Tue, 13 Jan 2026 03:03:36 GMT  
		Size: 66.2 MB (66234261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6862d896ee6f4f6633a8358a24f10f96698f55d9a83e7d4e45e3a2e5289c7ae8`  
		Last Modified: Thu, 15 Jan 2026 19:32:40 GMT  
		Size: 89.9 MB (89858894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fd402dbe928e14f69063c85f23dc6c9bbceb27e04cff93cac6dc77cf1a8f6be`  
		Last Modified: Thu, 15 Jan 2026 19:32:08 GMT  
		Size: 58.9 MB (58871754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:667055a163071452916474c596e487aab89587ef03245f692c4e3d2fb7f0d648`  
		Last Modified: Thu, 15 Jan 2026 19:32:38 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:144c252a99bf6a1b9e340bca0a2f98e4c51322e823a5d925ea61c9c807e9b029
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10503716 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c421ae974a7af846b9581f6eb9c3d77c0451146566517dd843877d1ef23f629`

```dockerfile
```

-	Layers:
	-	`sha256:5a352a577219391c8972d7caaa8a36125b6652f51cb51ac688b49fce1e69a7b9`  
		Last Modified: Thu, 15 Jan 2026 19:32:38 GMT  
		Size: 10.5 MB (10475955 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ceab98223378b13107de09f94459c61005efa6f62cddfcf0127d23a13549fd13`  
		Last Modified: Thu, 15 Jan 2026 19:32:37 GMT  
		Size: 27.8 KB (27761 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:bookworm` - linux; mips64le

```console
$ docker pull golang@sha256:f49ab1bd4f10a29db5addaf55136d10cefd9b240f2553a21373f8f00fd3506a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **262.3 MB (262284479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1ed3958199c0f4a8c9930b3937a8bfbdb9da27da450e634669cb784dd7e91ba`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1768176000'
# Tue, 13 Jan 2026 16:17:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 21:21:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 22:42:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 19:33:52 GMT
ENV GOLANG_VERSION=1.25.6
# Thu, 15 Jan 2026 19:33:52 GMT
ENV GOTOOLCHAIN=local
# Thu, 15 Jan 2026 19:33:52 GMT
ENV GOPATH=/go
# Thu, 15 Jan 2026 19:33:52 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 15 Jan 2026 19:33:52 GMT
COPY /target/ / # buildkit
# Thu, 15 Jan 2026 19:34:05 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Thu, 15 Jan 2026 19:34:06 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:b4c94e33bcdbce9a62a95be51a6e5f8ed2efc653e4be8f8f6722aa13d9d65461`  
		Last Modified: Tue, 13 Jan 2026 00:40:12 GMT  
		Size: 48.8 MB (48763393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df3ebdc0d40ea56bd8ca0e23bf6a7db8ca22ab77cacf0ba126e24eb42d35c708`  
		Last Modified: Tue, 13 Jan 2026 16:17:52 GMT  
		Size: 23.6 MB (23614652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8ee435e05dd9c53ddee45b81a8f55939374cd926a0e00239c752bb0832a5f8b`  
		Last Modified: Tue, 13 Jan 2026 21:22:59 GMT  
		Size: 63.3 MB (63309962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:659edd573efc55ccb964dda4fd8e0b2b02903c5753a704b10ec114e6a6fa5f32`  
		Last Modified: Tue, 13 Jan 2026 22:44:42 GMT  
		Size: 70.0 MB (70021799 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23b0400b5590e7fd7237d1225e0e47e6e763d192b132b6948f11a5446ebd37c3`  
		Last Modified: Thu, 15 Jan 2026 19:35:44 GMT  
		Size: 56.6 MB (56574515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04fd1f6047cc8072073792326b5b21badb078d245c83d8173ebbebe9ad6556a0`  
		Last Modified: Thu, 15 Jan 2026 19:35:38 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:08e9f2f70f9173eae9a4e9a4846d505e9c6133939c48e654a39e93a241bdee3f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.7 KB (27654 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28451948111c8ed874d77f66ff9f23da491425679b6a46838a25730f5d037987`

```dockerfile
```

-	Layers:
	-	`sha256:0747dafc38fae97d41bc64e8c09ce9c8e4a93e29d59718d614d78b552e9ac000`  
		Last Modified: Thu, 15 Jan 2026 19:35:38 GMT  
		Size: 27.7 KB (27654 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:bookworm` - linux; ppc64le

```console
$ docker pull golang@sha256:3b9873e6c4b2723741c92a7d144af325016d009e6aa1e7d30eb95bfd6a4d63b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **296.4 MB (296408181 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35124ab37ac0630c089fcd26a9860180357d33f5c201e033d64dfd82e33c3a0b`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1768176000'
# Tue, 13 Jan 2026 03:34:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 06:37:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 08:53:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 19:31:15 GMT
ENV GOLANG_VERSION=1.25.6
# Thu, 15 Jan 2026 19:31:15 GMT
ENV GOTOOLCHAIN=local
# Thu, 15 Jan 2026 19:31:15 GMT
ENV GOPATH=/go
# Thu, 15 Jan 2026 19:31:15 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 15 Jan 2026 19:31:15 GMT
COPY /target/ / # buildkit
# Thu, 15 Jan 2026 19:32:25 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Thu, 15 Jan 2026 19:32:27 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:7fcf9f2b462d6af06c3ad2420b999e6b092984c4723ebac480c428a5d837d3b7`  
		Last Modified: Tue, 13 Jan 2026 00:40:14 GMT  
		Size: 52.3 MB (52327376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd2769c4ec4b4d67e8059086401477839f8b9d5a5026dd27df50a3c7ce33b9db`  
		Last Modified: Tue, 13 Jan 2026 03:35:30 GMT  
		Size: 25.7 MB (25670703 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba5fcb80ea7d84a82ea96c11045a4f40d0943808d5c5334ea90de2f7ed44f4c4`  
		Last Modified: Tue, 13 Jan 2026 06:38:28 GMT  
		Size: 69.8 MB (69846016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39324acd74abd8d66fc3636cdba0cabcab5132ff369ae8d34e56255bdb262d35`  
		Last Modified: Tue, 13 Jan 2026 08:55:17 GMT  
		Size: 90.4 MB (90428658 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0de1d7ce58974e33ace56f0654af975ba4e29402893e2d90d191005bed4dae95`  
		Last Modified: Thu, 15 Jan 2026 19:32:22 GMT  
		Size: 58.1 MB (58135270 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e0444d9bd6f0b9ba3eaaa9bd81499e0db3b792afbec3d2bf626160d3e07f6b0`  
		Last Modified: Thu, 15 Jan 2026 19:32:58 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:ed2ffa667c433be1c47a5203b870cd726c320175602a1d5de29319df12ea547a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10496723 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a42c7116a534b8f6b6282fb4aef04032c492ac62f465980a8f321856615d5f58`

```dockerfile
```

-	Layers:
	-	`sha256:694dcd24620fe569ecf90d16d9b221c061b032c2a5b72d5494f3c32bd8216156`  
		Last Modified: Thu, 15 Jan 2026 19:32:58 GMT  
		Size: 10.5 MB (10468878 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ca3cd90760a972c440c8b14f97e999f1eda3f7fffaadf8c4ea15b4f9ec9924cf`  
		Last Modified: Thu, 15 Jan 2026 19:32:58 GMT  
		Size: 27.8 KB (27845 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:bookworm` - linux; s390x

```console
$ docker pull golang@sha256:7070b62154032a206b09eda83f2a21ca955842494a51929ca959effa783292f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **263.2 MB (263182108 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb37028f4ef2c59d5f93417ed12bcfaf40f000d1bad6db4d44b6657f35bc134b`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1768176000'
# Tue, 13 Jan 2026 02:09:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 03:14:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 19:29:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 19:31:09 GMT
ENV GOLANG_VERSION=1.25.6
# Thu, 15 Jan 2026 19:31:09 GMT
ENV GOTOOLCHAIN=local
# Thu, 15 Jan 2026 19:31:09 GMT
ENV GOPATH=/go
# Thu, 15 Jan 2026 19:31:09 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 15 Jan 2026 19:31:09 GMT
COPY /target/ / # buildkit
# Thu, 15 Jan 2026 19:31:11 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Thu, 15 Jan 2026 19:31:11 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:533e1723f6efd3a2dac5ef2d710062f1e6292bf061b83d41b908fe862b8922dc`  
		Last Modified: Tue, 13 Jan 2026 00:40:05 GMT  
		Size: 47.1 MB (47138430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8133db08df54d1100dff2f0259f057251959db22c09d939ae558af001aa8088c`  
		Last Modified: Tue, 13 Jan 2026 02:09:58 GMT  
		Size: 24.0 MB (24032491 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fb4cc23aeea1b258f198103e8c2d450f82da1d5de8a3eb227ed2969f60d97c4`  
		Last Modified: Tue, 13 Jan 2026 03:15:23 GMT  
		Size: 63.5 MB (63501276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55ce02e4e54b6659021d8edf907aa6accb7169b9308bca9679853b9c58e085f8`  
		Last Modified: Thu, 15 Jan 2026 19:30:28 GMT  
		Size: 69.0 MB (69018581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bb26ceadf9d37827849921e4f034b2107b0a7ec09f97f2b6301929ee5e50569`  
		Last Modified: Thu, 15 Jan 2026 19:31:35 GMT  
		Size: 59.5 MB (59491172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d01c198a231d715a6d738b947ff9114b411651b6e067517a5bd732361c52aba0`  
		Last Modified: Thu, 15 Jan 2026 19:31:39 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:bd522ea958a9c9a38d402d8bfdf94126edf5ac16f6ec272a563c80baacf0e726
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 MB (10355938 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd33f00de3c8e788ed733e2ec6c79c4e10a36d84025235bc9e37dab30c238cd7`

```dockerfile
```

-	Layers:
	-	`sha256:b8e05ecff641ee17914644ae20fa36a4a08dbb210a10cf659c45a5fce01e3366`  
		Last Modified: Thu, 15 Jan 2026 19:31:40 GMT  
		Size: 10.3 MB (10328141 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c8f3f46b9a5d73081fb7a63cf68d7180e2ae17a1dce4ba032944469a95737b90`  
		Last Modified: Thu, 15 Jan 2026 19:31:39 GMT  
		Size: 27.8 KB (27797 bytes)  
		MIME: application/vnd.in-toto+json
