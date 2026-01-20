## `golang:tip-bookworm`

```console
$ docker pull golang@sha256:063f238313868b8a483555f7e6356e3e77114a1b31805c078e3839c33379e6aa
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

### `golang:tip-bookworm` - linux; amd64

```console
$ docker pull golang@sha256:c637e97d705b9f9eec6a532b9c6b592b2bbcbd25f9fb73a72f07fe0b3bdb2486
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **324.4 MB (324399907 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0771b52d55760ced0210f15b793dd52c38f09f239a9487d8b364171a71797b9`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1768176000'
# Tue, 13 Jan 2026 02:08:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 03:53:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 21:45:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 21:46:53 GMT
ENV GOTOOLCHAIN=local
# Thu, 15 Jan 2026 21:46:53 GMT
ENV GOPATH=/go
# Thu, 15 Jan 2026 21:46:53 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 15 Jan 2026 21:46:53 GMT
COPY /target/ / # buildkit
# Thu, 15 Jan 2026 21:46:56 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Thu, 15 Jan 2026 21:46:56 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:c1be109a62df95316ceac87ea501079f32e17f36b636865a860841b7db06100c`  
		Last Modified: Tue, 13 Jan 2026 00:41:40 GMT  
		Size: 48.5 MB (48481622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64538a062a61add8dc8b290fa69475e8902eb839c497a5f5dcd5a950422e493c`  
		Last Modified: Tue, 13 Jan 2026 02:09:06 GMT  
		Size: 24.0 MB (24036867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd1872fa12cc6b1145803f1a0679ca26cc65fa1b4e0ee389bfb30267594736b6`  
		Last Modified: Tue, 13 Jan 2026 03:53:27 GMT  
		Size: 64.4 MB (64395833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8496047268ad16f553e0f7938bcff2404c8d8507bc25f4970900efe22fc75a22`  
		Last Modified: Thu, 15 Jan 2026 21:47:39 GMT  
		Size: 92.4 MB (92433575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16e09070cc4c8c6b4577469e540a043174ece319f2134af5f8b6f76f4d7806aa`  
		Last Modified: Mon, 12 Jan 2026 20:05:02 GMT  
		Size: 95.1 MB (95051851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87bfac8243c217e10a86b66b4cb79e19daedc44e287de1afc6ea957e8eb7efb1`  
		Last Modified: Thu, 15 Jan 2026 21:47:20 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:32c8bd979a25b5851a6e732e3bf843554d8070fbe5f795670e4b9f950dd247a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10525417 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0bca042008c2132d36aa82b37d831dc1b5189cc43f607d983028282bfc1307f6`

```dockerfile
```

-	Layers:
	-	`sha256:069534586c48554a604afad13629eac74488b1c68f3385620107a032de6de081`  
		Last Modified: Fri, 16 Jan 2026 00:26:54 GMT  
		Size: 10.5 MB (10497031 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:422c099fb9817b749e3a9d06c064cd34a87176eb55c34272c91484c8b74f2f6e`  
		Last Modified: Fri, 16 Jan 2026 00:26:55 GMT  
		Size: 28.4 KB (28386 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-bookworm` - linux; arm variant v7

```console
$ docker pull golang@sha256:435ab926b40ee216c28be8662eddce5817e6940801e8a3025c0a2393dce58006
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **283.2 MB (283215429 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d44107d59ad4e3d83cfddfe9c17613617a11e2ea155b79d3e5e8d69d3e5cbbd`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1768176000'
# Tue, 13 Jan 2026 02:57:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 04:24:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 21:45:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 21:48:09 GMT
ENV GOTOOLCHAIN=local
# Thu, 15 Jan 2026 21:48:09 GMT
ENV GOPATH=/go
# Thu, 15 Jan 2026 21:48:09 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 15 Jan 2026 21:48:09 GMT
COPY /target/ / # buildkit
# Thu, 15 Jan 2026 21:48:12 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Thu, 15 Jan 2026 21:48:12 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:d1f8df344790c402ed8a818bba76e9111f5e212418c662cf0574919edf68933b`  
		Last Modified: Tue, 13 Jan 2026 00:42:02 GMT  
		Size: 44.2 MB (44198845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6b61baedfd715aa7493fd2550daee1914be821a60dd0067158988236109172a`  
		Last Modified: Tue, 13 Jan 2026 02:57:25 GMT  
		Size: 21.9 MB (21941488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a97f9f395cd1e9e02761196527b4253d5246be969781795c278996437891e5cf`  
		Last Modified: Tue, 13 Jan 2026 04:25:03 GMT  
		Size: 59.7 MB (59652006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d4f2f91ec95dfd2a0cdd8c87f4af98c2cbec64995ccc1481d365c43eec7459f`  
		Last Modified: Thu, 15 Jan 2026 21:48:49 GMT  
		Size: 66.3 MB (66288538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb06c5933c094de46d52df9ed5d5962ecacceb10cdc72056e1307b0ee8c18640`  
		Last Modified: Mon, 12 Jan 2026 20:04:24 GMT  
		Size: 91.1 MB (91134394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bd966c6674df05b4c2864508f340bdc284b2503f25e016185af6954891e6eb8`  
		Last Modified: Thu, 15 Jan 2026 21:48:43 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:406ea0d1f663486a3d2ea72317f061af24931ef861411187e579a2afb5957b24
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10332225 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b526cfc5dbd446bd457882301b3b360baa763872b5df0df13635a2f629af362`

```dockerfile
```

-	Layers:
	-	`sha256:6105d2ea886d55a27cf76b90127abb5e3810c9004811bcd7152ac8497abef885`  
		Last Modified: Fri, 16 Jan 2026 00:27:06 GMT  
		Size: 10.3 MB (10303727 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c2098a296f2f3a8f0826182c26d215f3df6a5fd98f5b07c2e450844c974f51a4`  
		Last Modified: Fri, 16 Jan 2026 00:27:15 GMT  
		Size: 28.5 KB (28498 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-bookworm` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:00f045e25a452e80daadbb0d822033227901a370a86ecc4638e0cc050deddc77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **313.1 MB (313094716 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:accd3ee29dfd978175acc1b96cd16f8baf996aba4cb974a78602997b6343cb00`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1768176000'
# Tue, 13 Jan 2026 02:12:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 03:56:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 21:45:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 21:46:48 GMT
ENV GOTOOLCHAIN=local
# Thu, 15 Jan 2026 21:46:48 GMT
ENV GOPATH=/go
# Thu, 15 Jan 2026 21:46:48 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 15 Jan 2026 21:46:48 GMT
COPY /target/ / # buildkit
# Thu, 15 Jan 2026 21:46:51 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Thu, 15 Jan 2026 21:46:51 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:1029f5ddc0d24726f1cefbb8def7a88f8ec819a1fdc4c05ce523011b4b73c72d`  
		Last Modified: Tue, 13 Jan 2026 00:41:34 GMT  
		Size: 48.4 MB (48366072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d72c713ab317dd7f302a6ff5a345af5b61cddc864fca2d96a23e6ef3c90a6657`  
		Last Modified: Tue, 13 Jan 2026 02:12:51 GMT  
		Size: 23.6 MB (23604814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:687ad46596f06c934001fa6d7bea3d1508b0bb616cffb71004efd5bada56884f`  
		Last Modified: Tue, 13 Jan 2026 03:57:17 GMT  
		Size: 64.5 MB (64479462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8143a2dd82c91e357033fbcf687b5908f9e2d1098ed033f94134136db9cd0b87`  
		Last Modified: Thu, 15 Jan 2026 21:47:29 GMT  
		Size: 86.5 MB (86506901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cab7771dc3fd9d6c93b2e8fcd20d3b05cdc987b52c3e09c78b1417acc8931f2`  
		Last Modified: Mon, 12 Jan 2026 20:04:04 GMT  
		Size: 90.1 MB (90137309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08fef95b77f96a351747f5015c9060ceaf7a7806ef3fd52992e5f3c6a66fa644`  
		Last Modified: Thu, 15 Jan 2026 21:47:23 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:3116374b0b348de2f3caff3992a037f8426d2a152a1996180c28c216dcfd31d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10553377 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4669a5d71ca7a60f9a24fd5e5af9978d5310ed605bc8dac20af237b0543120f`

```dockerfile
```

-	Layers:
	-	`sha256:d42e04607d0c3f6bf74fec9bc22505f850c0c79b921bba8aa223342234e5c62c`  
		Last Modified: Thu, 15 Jan 2026 21:47:15 GMT  
		Size: 10.5 MB (10524855 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:af92e2f132569f9519d983a8caaeca10dde3fe429ab14653fa4bc62760f49e6e`  
		Last Modified: Thu, 15 Jan 2026 21:47:14 GMT  
		Size: 28.5 KB (28522 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-bookworm` - linux; 386

```console
$ docker pull golang@sha256:8b9de7b01c9ba2ce0e762adc6f2605458bcf1aff7e5bf24c61b1152c79ef191b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **323.4 MB (323378705 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01ff45bd63b6d04c41b26d8f5f7abdc3796bff11e7e674e18f0e08c932f358a2`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1768176000'
# Tue, 13 Jan 2026 02:02:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 03:03:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 21:45:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 21:48:01 GMT
ENV GOTOOLCHAIN=local
# Thu, 15 Jan 2026 21:48:01 GMT
ENV GOPATH=/go
# Thu, 15 Jan 2026 21:48:01 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 15 Jan 2026 21:48:01 GMT
COPY /target/ / # buildkit
# Thu, 15 Jan 2026 21:48:04 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Thu, 15 Jan 2026 21:48:04 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:2ec54d337d067729b748c8f421e417d2e02e79e9e0caf328deaa1b815a93c883`  
		Last Modified: Tue, 13 Jan 2026 00:41:57 GMT  
		Size: 49.5 MB (49468594 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63ef3b5e8322d4c8e5ca6198e931fb91c384bac3ef8aafd81a71617e9534b7ab`  
		Last Modified: Tue, 13 Jan 2026 02:02:23 GMT  
		Size: 24.9 MB (24871330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20be0f262f5ef3547fc45c5726dd33bf707569fc1cceccb9f87c4f4965c4f9ed`  
		Last Modified: Tue, 13 Jan 2026 03:03:50 GMT  
		Size: 66.2 MB (66234261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef81d0074ee36b51cb0bc8ce5ce6307d8a77c5b2017b987d7ec2e5fe041d8b8f`  
		Last Modified: Thu, 15 Jan 2026 21:48:47 GMT  
		Size: 89.9 MB (89858808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b42b2997976651e9da981a359adb745663b505ba580ded35d1fcd67a84ec5f37`  
		Last Modified: Mon, 12 Jan 2026 20:05:45 GMT  
		Size: 92.9 MB (92945554 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26e73a18eb2a236b41a1c22ca3118d42631a8f022fc9ad4f0941d2d2e77bd8f5`  
		Last Modified: Thu, 15 Jan 2026 21:48:37 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:18566c5b9a0805ac975321e8a8bb15a47d4ce8f73bac9e952ea250034f9e3f28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10504964 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:491ac23e2acaf42c7e62548b2cdf842c84e77a3718d37242e6390866d3f95aea`

```dockerfile
```

-	Layers:
	-	`sha256:75845cf8e2e12a15070e5bad4b417ecaf3c494072d2adc41e9c77c799aa7539f`  
		Last Modified: Thu, 15 Jan 2026 21:48:29 GMT  
		Size: 10.5 MB (10476611 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e20882550652b50a1ab97d41d78902f0256341ecbb36cf86d3500197e1733b86`  
		Last Modified: Fri, 16 Jan 2026 00:27:31 GMT  
		Size: 28.4 KB (28353 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-bookworm` - linux; mips64le

```console
$ docker pull golang@sha256:d412f95124e6c961eeb480e306e7ff68ee3d316c8a1ce163ab2202d469a1422b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **294.5 MB (294519224 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76ec92f88d348c0f7e499bec57d14b19d4692ac2585f140e17e9bfa3557b7966`
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
# Wed, 14 Jan 2026 00:39:31 GMT
ENV GOTOOLCHAIN=local
# Wed, 14 Jan 2026 00:39:31 GMT
ENV GOPATH=/go
# Wed, 14 Jan 2026 00:39:31 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 14 Jan 2026 00:39:31 GMT
COPY /target/ / # buildkit
# Wed, 14 Jan 2026 00:39:48 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 14 Jan 2026 00:39:50 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:b4c94e33bcdbce9a62a95be51a6e5f8ed2efc653e4be8f8f6722aa13d9d65461`  
		Last Modified: Tue, 13 Jan 2026 00:40:28 GMT  
		Size: 48.8 MB (48763393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df3ebdc0d40ea56bd8ca0e23bf6a7db8ca22ab77cacf0ba126e24eb42d35c708`  
		Last Modified: Tue, 13 Jan 2026 16:18:00 GMT  
		Size: 23.6 MB (23614652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8ee435e05dd9c53ddee45b81a8f55939374cd926a0e00239c752bb0832a5f8b`  
		Last Modified: Tue, 13 Jan 2026 21:23:11 GMT  
		Size: 63.3 MB (63309962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:659edd573efc55ccb964dda4fd8e0b2b02903c5753a704b10ec114e6a6fa5f32`  
		Last Modified: Tue, 13 Jan 2026 22:44:55 GMT  
		Size: 70.0 MB (70021799 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a831f31f3ccc6903fefb1751e80553dde8e9c3ac9501ef429ef0c2121806bc98`  
		Last Modified: Mon, 12 Jan 2026 20:25:17 GMT  
		Size: 88.8 MB (88809259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27f9cb6ea0b2bef9627475d702ddf6029ee026c76f56e04ec8aad64f7cad8772`  
		Last Modified: Wed, 14 Jan 2026 00:41:45 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:14b3ccfe0f334423243a94cbf40a1ac507f90a95b847079d62f2a8410759c987
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.2 KB (28240 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a9f84121153c9cf7ae50a25d256cc397aa029297b9005cdbe9b98280b6e1d87`

```dockerfile
```

-	Layers:
	-	`sha256:84db4c9183a14e8fee5c508ff0b6d92f3232ffd9bed9a982208c3cd23f4d836b`  
		Last Modified: Thu, 15 Jan 2026 22:05:50 GMT  
		Size: 28.2 KB (28240 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-bookworm` - linux; ppc64le

```console
$ docker pull golang@sha256:85278c168a623b5225a91d29f3b397380f8d6ff2ecc06198216e077e6f602884
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **330.0 MB (329956831 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb90b26262524eff21441792fd3721b991ff3b2757251f08c7657f43bd676311`
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
# Mon, 12 Jan 2026 20:05:00 GMT
ENV GOTOOLCHAIN=local
# Mon, 12 Jan 2026 20:05:00 GMT
ENV GOPATH=/go
# Mon, 12 Jan 2026 20:05:00 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 12 Jan 2026 20:05:00 GMT
COPY /target/ / # buildkit
# Thu, 15 Jan 2026 21:48:19 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Thu, 15 Jan 2026 21:48:20 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:7fcf9f2b462d6af06c3ad2420b999e6b092984c4723ebac480c428a5d837d3b7`  
		Last Modified: Tue, 13 Jan 2026 00:40:39 GMT  
		Size: 52.3 MB (52327376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd2769c4ec4b4d67e8059086401477839f8b9d5a5026dd27df50a3c7ce33b9db`  
		Last Modified: Tue, 13 Jan 2026 03:35:37 GMT  
		Size: 25.7 MB (25670703 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba5fcb80ea7d84a82ea96c11045a4f40d0943808d5c5334ea90de2f7ed44f4c4`  
		Last Modified: Tue, 13 Jan 2026 06:38:36 GMT  
		Size: 69.8 MB (69846016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39324acd74abd8d66fc3636cdba0cabcab5132ff369ae8d34e56255bdb262d35`  
		Last Modified: Tue, 13 Jan 2026 08:55:35 GMT  
		Size: 90.4 MB (90428658 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80c1f34a163f68379a85adaf1396976b01cd79b6100ad42ff3e6581c97310f7b`  
		Last Modified: Mon, 12 Jan 2026 20:06:22 GMT  
		Size: 91.7 MB (91683920 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b972e99d2941780613d1be4a9f19c36a219d575a1431263bc46718785a30637d`  
		Last Modified: Thu, 15 Jan 2026 21:48:54 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:446a453ad1d3f48799dd4d76441befab726c12729f032bfd17f1417e2294a0f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10497775 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:851aac073a0867f4ca1c6412ee754c311dec7851a50069ea574d62533d876903`

```dockerfile
```

-	Layers:
	-	`sha256:b77e6587fdfe6db14b98ee69cc1c7db60e6161f79a9cee2516ecf6372ea455dd`  
		Last Modified: Fri, 16 Jan 2026 00:27:44 GMT  
		Size: 10.5 MB (10469516 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d548a64a465144f4246a23bdc867dcd554a7d599ed6795c5d6b6c6ddc60705fb`  
		Last Modified: Fri, 16 Jan 2026 00:27:45 GMT  
		Size: 28.3 KB (28259 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-bookworm` - linux; s390x

```console
$ docker pull golang@sha256:e633899e5038fe04af0ca16dd182324f417c2cc67a85d49e22f30e8663152d3c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.9 MB (297920840 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87f8d3e4f9fad38771801bbcbdb08526fc1efa0dd843e72494409beb05bc2f75`
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
# Thu, 15 Jan 2026 21:47:38 GMT
ENV GOTOOLCHAIN=local
# Thu, 15 Jan 2026 21:47:38 GMT
ENV GOPATH=/go
# Thu, 15 Jan 2026 21:47:38 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 15 Jan 2026 21:47:38 GMT
COPY /target/ / # buildkit
# Thu, 15 Jan 2026 21:47:40 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Thu, 15 Jan 2026 21:47:41 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:533e1723f6efd3a2dac5ef2d710062f1e6292bf061b83d41b908fe862b8922dc`  
		Last Modified: Tue, 13 Jan 2026 00:40:26 GMT  
		Size: 47.1 MB (47138430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8133db08df54d1100dff2f0259f057251959db22c09d939ae558af001aa8088c`  
		Last Modified: Tue, 13 Jan 2026 02:10:04 GMT  
		Size: 24.0 MB (24032491 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fb4cc23aeea1b258f198103e8c2d450f82da1d5de8a3eb227ed2969f60d97c4`  
		Last Modified: Tue, 13 Jan 2026 03:15:34 GMT  
		Size: 63.5 MB (63501276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55ce02e4e54b6659021d8edf907aa6accb7169b9308bca9679853b9c58e085f8`  
		Last Modified: Thu, 15 Jan 2026 19:30:28 GMT  
		Size: 69.0 MB (69018581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:560c721b150b3efd4976a8fc9ccaf826512a0d88981fdddc7ad84ff81c3bfa69`  
		Last Modified: Mon, 12 Jan 2026 20:20:29 GMT  
		Size: 94.2 MB (94229904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce08e80ed5de53399c538590a00a3a91dc1fbf943835a79e613301abbba88b36`  
		Last Modified: Thu, 15 Jan 2026 21:48:12 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:7541ed6871ede493b882217f89de1de072f91f4212745c6348aa3c2f227e8dde
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 MB (10357174 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ada16614b756135778cb6e510f2718a59d6c8b13768e76f4784b59d98164e846`

```dockerfile
```

-	Layers:
	-	`sha256:76442c0012d5d7898bcbb016e5d232399d82a5c4cf843602a7f39ed6bd702cc9`  
		Last Modified: Fri, 16 Jan 2026 00:27:59 GMT  
		Size: 10.3 MB (10328789 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a2161fd897cb57eef7a49fec1603586b3f935067f26d84d592e9f41dd83da4dc`  
		Last Modified: Fri, 16 Jan 2026 00:28:00 GMT  
		Size: 28.4 KB (28385 bytes)  
		MIME: application/vnd.in-toto+json
