## `golang:tip-20260418-bookworm`

```console
$ docker pull golang@sha256:4ba3bb764845529d7fa92ef99ff9b98ca7c955b9a14733fb451a63987a72e9a2
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

### `golang:tip-20260418-bookworm` - linux; amd64

```console
$ docker pull golang@sha256:bff07a83a2dbdb5d731f778ea1c643f7759dd08871be99b982d0080b6c0b2d41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **326.7 MB (326710121 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4682b80827c2f3058b7c3537cd82d7749b20319c0f0e45e38892b5638e945fe`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1776729600'
# Wed, 22 Apr 2026 05:00:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 05:12:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 07:16:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 07:18:03 GMT
ENV GOTOOLCHAIN=local
# Wed, 22 Apr 2026 07:18:03 GMT
ENV GOPATH=/go
# Wed, 22 Apr 2026 07:18:03 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 07:18:03 GMT
COPY /target/ / # buildkit
# Wed, 22 Apr 2026 07:18:05 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 22 Apr 2026 07:18:05 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:db53381ee51f9e43304e236099ba097ae1b33ae41a8007e0b6319992eb55fd00`  
		Last Modified: Wed, 22 Apr 2026 00:15:45 GMT  
		Size: 48.5 MB (48488628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5203b2bfeff92b72e816dc6cbb1f16856f0cd592e521e3c0cfa195a78fe180e`  
		Last Modified: Wed, 22 Apr 2026 05:01:15 GMT  
		Size: 24.0 MB (24042234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fcda2b4d7993820b00c5488d173051e76d01ba6b85620617ba77001b0f9e2fa`  
		Last Modified: Wed, 22 Apr 2026 05:12:28 GMT  
		Size: 64.4 MB (64396988 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1705f32c4a8f635296d63c6e0995bbdbadc96e4e1e89e67afaadc9463807bafd`  
		Last Modified: Wed, 22 Apr 2026 07:18:31 GMT  
		Size: 92.4 MB (92448709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9e9800fe1d00fbf93fa3af2c224e36eef8eb15b87c8b6fcb13141f73eb2f1ed`  
		Last Modified: Mon, 20 Apr 2026 17:41:31 GMT  
		Size: 97.3 MB (97333404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59a16129eae031be33cdbaa4f6400a28f9869912c4b7085ef9c431f9e0dac6f0`  
		Last Modified: Wed, 22 Apr 2026 07:18:28 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20260418-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:f7368144c9ef391c92c6a346fac5885591e225c590b5ab0eb640d73a3607e2a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10525419 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8bd7a10e55485caa5b209cf528e7bd62cdf9433ff4d91428eb5da90f85aa8a3`

```dockerfile
```

-	Layers:
	-	`sha256:31d8cbe10e84d963b8829de1ecc774818c38b59f909240e6be22bd423d0e2351`  
		Last Modified: Wed, 22 Apr 2026 07:18:29 GMT  
		Size: 10.5 MB (10497033 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:26f47a967b8d4aeb7d74eee19d48f25b6084a96937d66911d7390e258421e284`  
		Last Modified: Wed, 22 Apr 2026 07:18:28 GMT  
		Size: 28.4 KB (28386 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20260418-bookworm` - linux; arm variant v7

```console
$ docker pull golang@sha256:c8f3419bccec4f99fb4b861927020289214684f4d403b6fdaa404a5586800a68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **285.3 MB (285274565 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:586919609d66f7d4d202a8eb86436d76421dfcdb48b42648c01158a6078d8cfe`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1776729600'
# Wed, 22 Apr 2026 02:18:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 03:52:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 05:18:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 05:21:08 GMT
ENV GOTOOLCHAIN=local
# Wed, 22 Apr 2026 05:21:08 GMT
ENV GOPATH=/go
# Wed, 22 Apr 2026 05:21:08 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 05:21:08 GMT
COPY /target/ / # buildkit
# Wed, 22 Apr 2026 05:21:10 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 22 Apr 2026 05:21:11 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:a78e7b2123c5c35e65ee1cc17df0d11c1db8ab3c4fe80b457270c2d9ae5003b1`  
		Last Modified: Wed, 22 Apr 2026 00:16:29 GMT  
		Size: 44.2 MB (44207655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:218160481dc948cfbf943718a4363de6a3663997f19a965c7b86136ac3e28f30`  
		Last Modified: Wed, 22 Apr 2026 02:18:15 GMT  
		Size: 21.9 MB (21946340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3960cd47ab70e092f1d1162d4a33a761e2cfa64e09c3ca3118416ced1e6f99de`  
		Last Modified: Wed, 22 Apr 2026 03:52:25 GMT  
		Size: 59.7 MB (59652860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e02024d7a65cf0d89b82c9345aa490094390ad4f0557726b9b7b3894307b9880`  
		Last Modified: Wed, 22 Apr 2026 05:21:35 GMT  
		Size: 66.3 MB (66305373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e42fcfd73df1c3c4e864c147debb0154bf1e1c38912174f3d52a47a654a9641`  
		Last Modified: Mon, 20 Apr 2026 17:43:22 GMT  
		Size: 93.2 MB (93162179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fb94b97e6e92863520d53baf2e775a278822ac76ddffe3e5de716799cc6243a`  
		Last Modified: Wed, 22 Apr 2026 05:21:33 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20260418-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:bbc417ce1151af1c8d38b1b1713f1ad439ba2ec2996aaea7adb9aa078b950f47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10332227 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99165211a8777c630222fda280a624a290612482aae7fca153712fef4b581907`

```dockerfile
```

-	Layers:
	-	`sha256:8c1a6a4325ac1c97de4456e353bf1b58ab707a36d30e729150f18edb59eac758`  
		Last Modified: Wed, 22 Apr 2026 05:21:33 GMT  
		Size: 10.3 MB (10303729 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9b766353f539c4d07862459355c3710fd7e56b39e7450e0953a433e408930187`  
		Last Modified: Wed, 22 Apr 2026 05:21:33 GMT  
		Size: 28.5 KB (28498 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20260418-bookworm` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:db7a3b3efcf4d077a41c5198aa1ea66b8b013e62c72aca858eb24ad04a97cb22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **315.0 MB (315004205 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5c504c9d4581478f19b52cb84d9a0ffc4c9a011c59dc4a428029af2e20dec00`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1776729600'
# Wed, 22 Apr 2026 01:42:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 02:32:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 04:18:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 04:19:59 GMT
ENV GOTOOLCHAIN=local
# Wed, 22 Apr 2026 04:19:59 GMT
ENV GOPATH=/go
# Wed, 22 Apr 2026 04:19:59 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 04:19:59 GMT
COPY /target/ / # buildkit
# Wed, 22 Apr 2026 04:20:01 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 22 Apr 2026 04:20:02 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:30de66f8fdafab67e88d876087f571a693a1a6c4cf0abc29efbf88ea878e0d29`  
		Last Modified: Wed, 22 Apr 2026 00:15:43 GMT  
		Size: 48.4 MB (48373071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bb7bd28fbdfe678a7f45878b7b1c07dbbc0fa7753b0312aa8fd049667a9e137`  
		Last Modified: Wed, 22 Apr 2026 01:43:06 GMT  
		Size: 23.6 MB (23609423 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:599d07e8492bcee46202f5eae3e3010a470acc5139840e6d14556aefa3fc355f`  
		Last Modified: Wed, 22 Apr 2026 02:32:24 GMT  
		Size: 64.5 MB (64479606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5fb534e886bf427ac371d8c2d457637ed5a24fef53b45d473e69597dc521290`  
		Last Modified: Wed, 22 Apr 2026 04:20:26 GMT  
		Size: 86.5 MB (86521317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d9da8d3894800a39f60fbfd67e48a2654efcedecf176b3e40f1e07ab0291557`  
		Last Modified: Mon, 20 Apr 2026 17:41:33 GMT  
		Size: 92.0 MB (92020630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e97ed993f2c6eedd38c78ec30463409995f762b07a9ba4bf32f4f22af067097`  
		Last Modified: Wed, 22 Apr 2026 04:20:24 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20260418-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:5ce630a7107476e0800847098cde83b3024cead44248040a996ddb53820d4c07
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10553379 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4939b64d00c1108fc9e2359b7dbee3347606fb9f814e02158a1db3c8b94c508`

```dockerfile
```

-	Layers:
	-	`sha256:fb59289dd7152fb74027a11c004b53dedd5ff74869871dae6f32edbed23c48b5`  
		Last Modified: Wed, 22 Apr 2026 04:20:25 GMT  
		Size: 10.5 MB (10524857 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:197a5797c7aa500d820d26ce1c11d5c930648436228c8495484fc225342cce28`  
		Last Modified: Wed, 22 Apr 2026 04:20:24 GMT  
		Size: 28.5 KB (28522 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20260418-bookworm` - linux; 386

```console
$ docker pull golang@sha256:553a10a544f43276947aef81b8698e5613502975a8d82fd04a8c51b48b92adf4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **325.5 MB (325532475 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba188887f4620917134baf7f9412c1e4ef7cda998848fba4b0dbe79d3a88732a`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1776729600'
# Wed, 22 Apr 2026 01:42:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 05:02:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 09:11:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 09:13:48 GMT
ENV GOTOOLCHAIN=local
# Wed, 22 Apr 2026 09:13:48 GMT
ENV GOPATH=/go
# Wed, 22 Apr 2026 09:13:48 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 09:13:48 GMT
COPY /target/ / # buildkit
# Wed, 22 Apr 2026 09:13:51 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 22 Apr 2026 09:13:51 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:1f607c56991d572a9c9e62692330777522b959fe17a14367be35d12959214fa4`  
		Last Modified: Wed, 22 Apr 2026 00:16:17 GMT  
		Size: 49.5 MB (49477718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5d771f6f5a1356deff0c1540de8894e5249a2f8c97ba7961a41235129f48c60`  
		Last Modified: Wed, 22 Apr 2026 01:42:30 GMT  
		Size: 24.9 MB (24875723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2dd81f3dc271c0572c6da562bcce13d5c0a8f379729949fde98b0b1e57ca2e4c`  
		Last Modified: Wed, 22 Apr 2026 05:02:53 GMT  
		Size: 66.2 MB (66235084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a2cb5e997a4d3f30aaca23323d98b07bb9ec20b90f60fa781350c3ece628635`  
		Last Modified: Wed, 22 Apr 2026 09:14:15 GMT  
		Size: 89.9 MB (89871281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a0ee3233bce23292707dea9900b4db989f25efd70edf364d9cfceefc1e3441c`  
		Last Modified: Mon, 20 Apr 2026 17:42:46 GMT  
		Size: 95.1 MB (95072511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6532007f1ec4452e76574fffa9a28d541f2a25feb521383bf2c9163d583e8df`  
		Last Modified: Wed, 22 Apr 2026 09:14:12 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20260418-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:92142ae94b7494fcb2f10799132168b9b97b4359f8b7394beb793d45582f7993
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10504966 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21edf1729f68a51f30160bb0a05bac491c0c5020eda3a15d22576578d505e6fb`

```dockerfile
```

-	Layers:
	-	`sha256:5c225880dc506f443f9afa83e096bfd1ce2699c207c2a8276bc29f88f5e89af8`  
		Last Modified: Wed, 22 Apr 2026 09:14:13 GMT  
		Size: 10.5 MB (10476613 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ceb251687b03b5c574b70f99d31e945c236de92e4c156adc612fae3223b8f1a7`  
		Last Modified: Wed, 22 Apr 2026 09:14:12 GMT  
		Size: 28.4 KB (28353 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20260418-bookworm` - linux; mips64le

```console
$ docker pull golang@sha256:4b2f111fc919134cc980212a8705b54e7aeebc78d2a44d7b603920d377af601f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **296.7 MB (296684259 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a81e50138bd8424a2f04948de90eb399aab3c3ae3f62326ed1af930270899188`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 15:01:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 20:27:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 21:52:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 20 Apr 2026 18:01:39 GMT
ENV GOTOOLCHAIN=local
# Mon, 20 Apr 2026 18:01:39 GMT
ENV GOPATH=/go
# Mon, 20 Apr 2026 18:01:39 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 20 Apr 2026 18:01:39 GMT
COPY /target/ / # buildkit
# Mon, 20 Apr 2026 18:01:54 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 20 Apr 2026 18:01:56 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:7a9b4a7963b008240d9a254ca4fd1193c938bed0a9c6fe9c04630f13b1a17a44`  
		Last Modified: Tue, 07 Apr 2026 00:09:37 GMT  
		Size: 48.8 MB (48782593 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5370b42611bdad35bb24b3e5a6a342f00eb8523dc8562b7babeca6f19608f4c`  
		Last Modified: Tue, 07 Apr 2026 15:01:37 GMT  
		Size: 23.6 MB (23615262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df968e8deea10f7e740272ffa34126abe9d9673e41bbeb7f3f0d785055e19a4d`  
		Last Modified: Tue, 07 Apr 2026 20:28:18 GMT  
		Size: 63.3 MB (63310060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35cf83c0e933a4e8a498aae736ebf10a823fd9ecc755d47233e566e941c9893a`  
		Last Modified: Tue, 07 Apr 2026 21:54:45 GMT  
		Size: 70.1 MB (70051233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d97d132c4cd2477f08383bdb25847164f9927a3e74753805edac12b4cb96c73`  
		Last Modified: Mon, 20 Apr 2026 18:03:53 GMT  
		Size: 90.9 MB (90924954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:960bc4521c730013fe19bf0192469d48d0f76651d21fefe84993706488c12b1b`  
		Last Modified: Mon, 20 Apr 2026 18:03:44 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20260418-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:e3f711c00deb2ee5af06bb0bffceeca595836423e20ee1c4748a1e48db5ff3b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.2 KB (28240 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfa0790ece22e1755db8dd1df63bf9c45c6210e7a1f70b1663eb08bd0c1e9ba8`

```dockerfile
```

-	Layers:
	-	`sha256:898a9c17b9ebe7d66a4d6cc8ff2fba036980ecc54c060e861cb70d9b8f63ae87`  
		Last Modified: Mon, 20 Apr 2026 18:03:44 GMT  
		Size: 28.2 KB (28240 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20260418-bookworm` - linux; ppc64le

```console
$ docker pull golang@sha256:f6b2bbd8e56a34283df84cdc3625ea6e69a2128d5cde4f19f01931c05275bdc6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **332.2 MB (332189765 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad7c2dbc1c9667a411c6501c9e684c3f24c0be04f3311d646c3c5dc752337143`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 04:21:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 09:50:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 18:22:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 20 Apr 2026 17:41:28 GMT
ENV GOTOOLCHAIN=local
# Mon, 20 Apr 2026 17:41:28 GMT
ENV GOPATH=/go
# Mon, 20 Apr 2026 17:41:28 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 20 Apr 2026 17:41:28 GMT
COPY /target/ / # buildkit
# Mon, 20 Apr 2026 17:41:34 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 20 Apr 2026 17:41:35 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:6b775f7ad22043f8bb75d535d8a1279e43453a08a4a9e6a0b48c020c9b387079`  
		Last Modified: Tue, 07 Apr 2026 00:09:43 GMT  
		Size: 52.3 MB (52336938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04a522a501745b6503b15f6badc6170d6fa2321f26576c47b363acd8cb21b2ee`  
		Last Modified: Tue, 07 Apr 2026 04:21:54 GMT  
		Size: 25.7 MB (25671577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f98ce990098f8650217504a159d9031cc264dd29e8af85f749d78eacc319c5a`  
		Last Modified: Tue, 07 Apr 2026 09:51:25 GMT  
		Size: 69.8 MB (69846122 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3f67f0a7bc2638109117ec62f84bf4d06b91348ec6d8486011aaadaa5f42f65`  
		Last Modified: Tue, 07 Apr 2026 18:22:57 GMT  
		Size: 90.5 MB (90462415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88f72075717c40f723c05a62a7b4daebee738f45ad2854cdb0f9f31a6113d444`  
		Last Modified: Mon, 20 Apr 2026 17:42:34 GMT  
		Size: 93.9 MB (93872555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88efcabef6e283d5bcc78bb9abfc58b745bff2a831e6eb81d3934de39ad4fc63`  
		Last Modified: Mon, 20 Apr 2026 17:42:32 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20260418-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:b257830361dbaaa4e20a51df708340943edd76348f581547aa9fba6c03ffaf6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10497950 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29a02418715350b53dd1093608245c97af0473616d3f0ab9d95d1197ebf5d6e3`

```dockerfile
```

-	Layers:
	-	`sha256:b7ab6ec7c895b0149d80daab238264aa3a54dc147123389430828974ffd12446`  
		Last Modified: Mon, 20 Apr 2026 17:42:32 GMT  
		Size: 10.5 MB (10469518 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9649b64ee7d21b941e87bac7c925a4b4b19f24fb3f9ab0d0100a99cdbc21a1c5`  
		Last Modified: Mon, 20 Apr 2026 17:42:32 GMT  
		Size: 28.4 KB (28432 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20260418-bookworm` - linux; s390x

```console
$ docker pull golang@sha256:f34813ca7a6d4d1c40aa02b927122bc365d63ac18ee3ab8b96046f633d2725fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **299.6 MB (299592364 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4ceb2e05a2961df6ff00c60eb3d0ec2cb25f5379554a8bb22b1f3bce0698838`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1776729600'
# Wed, 22 Apr 2026 02:31:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 04:20:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 05:15:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 20 Apr 2026 17:48:01 GMT
ENV GOTOOLCHAIN=local
# Mon, 20 Apr 2026 17:48:01 GMT
ENV GOPATH=/go
# Mon, 20 Apr 2026 17:48:01 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 20 Apr 2026 17:48:01 GMT
COPY /target/ / # buildkit
# Wed, 22 Apr 2026 08:07:42 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 22 Apr 2026 08:07:42 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:65a8acd2327b0f3316fe8707ebd5c99b15e79306d4eca71f3e635588795ae2bb`  
		Last Modified: Wed, 22 Apr 2026 00:15:31 GMT  
		Size: 47.1 MB (47147970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac385f32c2d6e9209dd9f8ada378863aba00921ac3815f399e84f802ea5ce36e`  
		Last Modified: Wed, 22 Apr 2026 02:32:03 GMT  
		Size: 24.0 MB (24036363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8df5494ce4223646f47cc2e95923748571f15dc98fdcd0c46696a358fa2128f`  
		Last Modified: Wed, 22 Apr 2026 04:20:41 GMT  
		Size: 63.5 MB (63500148 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19e2e233398719d67abe7b980a5a64b8651711b1f4668cbf06d0a24e66339470`  
		Last Modified: Wed, 22 Apr 2026 05:16:02 GMT  
		Size: 69.1 MB (69055274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dc40b99896e610d7e8bfd78ceac0447cbdeee9aed83f1c52c72fd167c0ef6be`  
		Last Modified: Mon, 20 Apr 2026 17:47:23 GMT  
		Size: 95.9 MB (95852451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ba8730de5b88215a499b0103c2d729a22a8b3f46db89daccc3d057a43e33d72`  
		Last Modified: Wed, 22 Apr 2026 08:08:12 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20260418-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:e9a70f885aa8b4fd424076a9aa3675c89816f5deaf5658e85a8572c2c808ad62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 MB (10357925 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b779bf6ecce04a51edca535fca0736bf7a03813b6de37b0857e5eb4f00f0b84`

```dockerfile
```

-	Layers:
	-	`sha256:5ef4e66358e4c7c7fbd0fc0e1406e546646ae48cc74d77e79d60d9a14ce89994`  
		Last Modified: Wed, 22 Apr 2026 08:08:12 GMT  
		Size: 10.3 MB (10329539 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5fe806a8f75bdebac0f5b102046b22ccdeb7699d3d1b5ae44782d4c1e334f6a8`  
		Last Modified: Wed, 22 Apr 2026 08:08:12 GMT  
		Size: 28.4 KB (28386 bytes)  
		MIME: application/vnd.in-toto+json
