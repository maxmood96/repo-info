## `golang:tip-alpine3.22`

```console
$ docker pull golang@sha256:a33da0ed29a2c0d050eb3fd9589f26b385cad259e74c602c3aa2bb54147a34ff
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 16
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
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

### `golang:tip-alpine3.22` - linux; amd64

```console
$ docker pull golang@sha256:af49078d70dc078d6a2d92bc1966c7fa387cc0e0082a30a3cd733a0d4168548f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.2 MB (87216525 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:deb9a34ba57df0c6e30c10f071631d99be20b8aad5b1d27c2de8aa0add7b8de3`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Mon, 18 Aug 2025 05:23:18 GMT
RUN apk add --no-cache ca-certificates # buildkit
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
	-	`sha256:9824c27679d3b27c5e1cb00a73adb6f4f8d556994111c12db3c5d61a0c843df8`  
		Last Modified: Tue, 15 Jul 2025 19:00:01 GMT  
		Size: 3.8 MB (3799689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9797af702a9840f0c0d00f013ea39d09d5950d9b50135994a3b0d2cb0491bf2f`  
		Last Modified: Mon, 18 Aug 2025 18:27:37 GMT  
		Size: 282.4 KB (282450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c981e030468965854d1b7da64b902a546cf410e421543877a0dbcd1eb3b5506d`  
		Last Modified: Mon, 18 Aug 2025 19:09:02 GMT  
		Size: 83.1 MB (83134228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cabd75946b30924a1a9a66b860b19f1cf1b7defdff33eed61a7deebcba3b2230`  
		Last Modified: Mon, 18 Aug 2025 18:27:36 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.22` - unknown; unknown

```console
$ docker pull golang@sha256:fa0d5adad1478d234202aa2e99d90f32f0c3e6ac8f7a039a22205a1e9f7f8332
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **216.7 KB (216664 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e6a02de88c49894769d8d10d3573d9d51d330c817ed4b99d583a4a25c16b2cd`

```dockerfile
```

-	Layers:
	-	`sha256:61bba9ce3d6ebcfe805e0f6872c0c42a11b8db81e3ea008993a7ae88df9b2836`  
		Last Modified: Mon, 18 Aug 2025 20:23:39 GMT  
		Size: 191.5 KB (191527 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f549112e1f611a4a0cc75d5118af5c1d754bf1f8869cd596bfaf61535d41cf5c`  
		Last Modified: Mon, 18 Aug 2025 20:23:39 GMT  
		Size: 25.1 KB (25137 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.22` - linux; arm variant v6

```console
$ docker pull golang@sha256:5176d0eca77035598ee08cb72110398ad1d5e97f3c49bb104e1a8cd57fef9179
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.2 MB (84180083 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87d75adb0f0249c3b88fc3e3aa5e73aa4905ac64b9b0f1466ab5494e21baa1e9`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-armhf.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Mon, 18 Aug 2025 05:23:18 GMT
RUN apk add --no-cache ca-certificates # buildkit
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
	-	`sha256:06bab5e847c5674d6ec26b342cc11d7a051a6a231e5db8a955d57bc9f4ab5595`  
		Last Modified: Tue, 15 Jul 2025 18:59:34 GMT  
		Size: 3.5 MB (3500910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33f95cea4c439fb384d1bd6927f75cd3bde82d7a5909bb38cec72c9923ca463a`  
		Last Modified: Tue, 15 Jul 2025 22:55:40 GMT  
		Size: 283.3 KB (283329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37585a3cefa6eac4cd3e186fb9d4cb0cec0d9885ec6592350e2308f3ede04143`  
		Last Modified: Mon, 18 Aug 2025 18:20:58 GMT  
		Size: 80.4 MB (80395687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3175edf04d702ca2bbd85f6bb32e706dce53512d76094b9182ac75730b642766`  
		Last Modified: Mon, 18 Aug 2025 18:20:40 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.22` - unknown; unknown

```console
$ docker pull golang@sha256:0f9ff80fdb8f6878e546733aa68d5fd135d7a3d530a8f99dd4e2ac3af132f03d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.0 KB (25047 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad42d1d17441f8e6a91af94bb5f5cfc3f5517973d89dcb73a5e75e06a0c29e16`

```dockerfile
```

-	Layers:
	-	`sha256:373bcfc950cffbe8dc99315ed84320cfd17d9f53690e6c8e1eecebe52ad66cac`  
		Last Modified: Mon, 18 Aug 2025 20:23:43 GMT  
		Size: 25.0 KB (25047 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.22` - linux; arm variant v7

```console
$ docker pull golang@sha256:c79718b73b9a53812f6b7fb61f2d7a477d0e67ac786a4f3a5d1b3f04879d5503
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.7 MB (83660457 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ba3ab2b18713eaeb7425fdc456ab4c31f38196b7178773f156e786cbb030085`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-armv7.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Mon, 18 Aug 2025 05:23:18 GMT
RUN apk add --no-cache ca-certificates # buildkit
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
	-	`sha256:5ee064f8764b09a64829b58705219a88e0b13243f7f403d66ac0c639640426a5`  
		Last Modified: Tue, 15 Jul 2025 19:04:18 GMT  
		Size: 3.2 MB (3219038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74d1c7cd6f49363bcd6156bb689087c0a4e1624bb6497290e03e589310895c3e`  
		Last Modified: Tue, 15 Jul 2025 23:00:53 GMT  
		Size: 282.5 KB (282485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65db35adfd1c26b9fd865e957c7ac16cfbd5d2925f26a2f01840bdbea9cb3b72`  
		Last Modified: Mon, 18 Aug 2025 23:18:49 GMT  
		Size: 80.2 MB (80158777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c46ffe1569240072afd05a2ffe8aa216aa2f17353d3165480a641417b6e66bb`  
		Last Modified: Mon, 18 Aug 2025 23:25:03 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.22` - unknown; unknown

```console
$ docker pull golang@sha256:1beb4a30f736606bcf6de102d0a80b934f521cc81f76d0750388330ad0cbe56d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **216.0 KB (216016 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4cf1351eae0ffb2fb50772acbf3b25d1d177ef07501d0fd7edfa30039c0269c9`

```dockerfile
```

-	Layers:
	-	`sha256:664397e5ca1aa0521bbb6cd03ff461be0a29f0c13c9c490b069d2952b6498db4`  
		Last Modified: Tue, 19 Aug 2025 02:23:30 GMT  
		Size: 191.5 KB (191549 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d6b0ee4719439f1dd7eeb2c866fa17393eda2fd3b66a0f1dc39da1d269893dd8`  
		Last Modified: Tue, 19 Aug 2025 02:23:31 GMT  
		Size: 24.5 KB (24467 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.22` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:523e12be97e5037be6163d92c2ff7c99e6bfd755eb834e7520ae4e69733993a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.5 MB (83548239 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4496f4f1121b1d889673beef9876f45b9ec4fedd3d4a1917b0e87246b1963cf2`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-aarch64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Mon, 18 Aug 2025 05:23:18 GMT
RUN apk add --no-cache ca-certificates # buildkit
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
	-	`sha256:6e174226ea690ced550e5641249a412cdbefd2d09871f3e64ab52137a54ba606`  
		Last Modified: Tue, 15 Jul 2025 18:59:50 GMT  
		Size: 4.1 MB (4130750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d6e0c986dc92724f88716366774abec9cec3d3a68fb39a938496715d1f61a3f`  
		Last Modified: Mon, 18 Aug 2025 22:17:40 GMT  
		Size: 284.7 KB (284708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a9a962081772d9ddd06f0164791e2d37e59bd0091e1d2b79d410ab8b218794c`  
		Last Modified: Mon, 18 Aug 2025 22:12:08 GMT  
		Size: 79.1 MB (79132623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c61eb059730cbf7e9110be44bba005979669fc086c38ebcab995b0168969bf1a`  
		Last Modified: Mon, 18 Aug 2025 22:17:39 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.22` - unknown; unknown

```console
$ docker pull golang@sha256:db0c91df58552823cfbb6dc1066f958f3560dacbc8465a1bd7ff3bda6e694fd5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **216.9 KB (216881 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5cf4af91991efeebffa852f4715349c13a90dc2df6441e24ec0527e83ace771e`

```dockerfile
```

-	Layers:
	-	`sha256:9a111c1da5ef15828908d79c495127dc017b1cfc2d2c3f3cf5fd5456838f26cb`  
		Last Modified: Mon, 18 Aug 2025 23:23:32 GMT  
		Size: 191.6 KB (191583 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7c42c1b83da4feb70897a89593bd3ff3ac6b97925241bd7b636b105461133648`  
		Last Modified: Mon, 18 Aug 2025 23:23:33 GMT  
		Size: 25.3 KB (25298 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.22` - linux; 386

```console
$ docker pull golang@sha256:7341b0e6f966318ffeef712c8beda44fe74be5aa418aad7bb98453bf0448e497
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.7 MB (85657183 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc470001c54d7c790e974bab5440e87667f80cd0b8cdcb63940b0394b3fdfb91`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-x86.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Mon, 18 Aug 2025 05:23:18 GMT
RUN apk add --no-cache ca-certificates # buildkit
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
	-	`sha256:a55f2fb89da4caae0d783c0045a67446dee9bbd977fecb44db9e1231550fa888`  
		Last Modified: Tue, 15 Jul 2025 19:04:11 GMT  
		Size: 3.6 MB (3615006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2123a7806e751fcd00082f0b16257ea229488e38d644e91372a1112f2f26ec6`  
		Last Modified: Mon, 18 Aug 2025 18:21:05 GMT  
		Size: 282.9 KB (282925 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82670d3acf9adce43c089b894a11312540a785c816af45b90edbb17d606892e6`  
		Last Modified: Mon, 18 Aug 2025 19:08:00 GMT  
		Size: 81.8 MB (81759095 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:647fa27b0620a638a1a7f596a10592f12bbd39c4d5fd78bacf42b0f427280a7c`  
		Last Modified: Mon, 18 Aug 2025 18:21:05 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.22` - unknown; unknown

```console
$ docker pull golang@sha256:3862b12afad6ca41bb349cbd13f38afda905c053dad5c721504ddd22a85991c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **216.6 KB (216583 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6765e910a932e143dda7dcb3077feb5666178a3bd00d61c67e61a77ecab70744`

```dockerfile
```

-	Layers:
	-	`sha256:10fdcd9fed21e94885a284c51765d1abdaff8fc2546082ca803477c53d3680e5`  
		Last Modified: Mon, 18 Aug 2025 20:23:47 GMT  
		Size: 191.5 KB (191488 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:90dac0b97ccae9bedf84b2a0a32075183e755ec7f31df9a11960a56e812d5684`  
		Last Modified: Mon, 18 Aug 2025 20:23:47 GMT  
		Size: 25.1 KB (25095 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.22` - linux; ppc64le

```console
$ docker pull golang@sha256:e9c881580c54c5c4dacc2a5d11d23f048d88b75f6c01f559089e5f11120f8db3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.5 MB (84493814 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb51077c2d368b3552ebcab7b4a2bfaffc68578b0a043ef1f9a8f0093c261170`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-ppc64le.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Mon, 18 Aug 2025 05:23:18 GMT
RUN apk add --no-cache ca-certificates # buildkit
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
	-	`sha256:b762f678859bfa5c3948b5f1b04959aa43c8aba88e2389e281413d303d62a7e3`  
		Last Modified: Tue, 15 Jul 2025 18:59:53 GMT  
		Size: 3.7 MB (3727111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0afe3e6d4a1713a75edf1789d38233b2e8d48f54cebae5e9d0789eb1af52023b`  
		Last Modified: Mon, 28 Jul 2025 20:30:54 GMT  
		Size: 285.1 KB (285114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d39b86dffb1db621a8fcea400d6f61123247f5d28fb771a6f68ef42e85a595f`  
		Last Modified: Mon, 18 Aug 2025 21:57:49 GMT  
		Size: 80.5 MB (80481431 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d3288bd8921caffaa1863cc993e30b8fa806e13166a157b755826f6db4a9dc7`  
		Last Modified: Mon, 18 Aug 2025 22:05:45 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.22` - unknown; unknown

```console
$ docker pull golang@sha256:1733fc445100907239ea8c8bafaf2960f66b682f12cf75169aaded988e6ce21b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **214.8 KB (214820 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36fa010b473b9263df885a58aa86317166a2c155b26d86fc8c4c6eb382775a60`

```dockerfile
```

-	Layers:
	-	`sha256:fb5ad854ae28e3c6a2c307fe4dc2693555aee4d03cf579c5928ac6b9a344c5d2`  
		Last Modified: Mon, 18 Aug 2025 23:23:39 GMT  
		Size: 189.6 KB (189624 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:933d542b0a1725eefec0aa51aaf187fa410266c3a14b7a27376715f4688d2994`  
		Last Modified: Mon, 18 Aug 2025 23:23:39 GMT  
		Size: 25.2 KB (25196 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.22` - linux; riscv64

```console
$ docker pull golang@sha256:556f4d69f2514b0c6876b647fe0ef3ea5b6d6ec3c1708a1253b8821a49d38e30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.3 MB (84343798 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea9816e5f2be06b2e5061c3cde0f791bb3f0c4bf7dec5106bd8bbf57dbfc3560`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-riscv64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Mon, 18 Aug 2025 05:23:18 GMT
RUN apk add --no-cache ca-certificates # buildkit
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
	-	`sha256:cbe7080b5783de104ad67ff4595bfa8ae70a597181a84621f51c5ccd084218da`  
		Last Modified: Tue, 15 Jul 2025 19:00:17 GMT  
		Size: 3.5 MB (3512801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31e09396f9703679f1457da8ea8533cdf5f2a459c8f9efa4664152e578880b25`  
		Last Modified: Mon, 21 Jul 2025 22:46:21 GMT  
		Size: 282.8 KB (282780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d3a68e6ea4a30742896db2d06e67c3791dcc7f520502dccc3c8999b381c1bb1`  
		Last Modified: Tue, 19 Aug 2025 06:42:06 GMT  
		Size: 80.5 MB (80548060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d839e29480fa3eef84e5924412a20c1973e92b5300fdf80bae666fa05d416eef`  
		Last Modified: Tue, 19 Aug 2025 06:41:59 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.22` - unknown; unknown

```console
$ docker pull golang@sha256:4c219056eb935c579f3e8e804149253f49b52a08e4f4891f434ea0eaaccee08e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **214.0 KB (214021 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42a057fe0eedc6d5e40d063f435bdc284c30ef83008b879ecbdfd571ac7fce64`

```dockerfile
```

-	Layers:
	-	`sha256:4ff667bced560e1f11f03d0c0d3411ce146427e5ab1f1f0a6acd8f716ab91d60`  
		Last Modified: Tue, 19 Aug 2025 08:23:33 GMT  
		Size: 189.6 KB (189620 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b3d6b4fb89ef609661de6127761d87c43ea88caf18ff3237b4aa75d9a316ac19`  
		Last Modified: Tue, 19 Aug 2025 08:23:34 GMT  
		Size: 24.4 KB (24401 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.22` - linux; s390x

```console
$ docker pull golang@sha256:150bb8182d45497569d74fc4a13bdc8ab3b8a2b73c96803a5d08d394fb9f4bb6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.6 MB (85626001 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2424403bd772d0ead7c41f3d06cf90ab3f1f11b2acdf898b4de96d468999a08`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-s390x.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Mon, 18 Aug 2025 05:23:18 GMT
RUN apk add --no-cache ca-certificates # buildkit
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
	-	`sha256:5d29754ce036967079405405a04a54a7d3f8ba85e0057b6bdda3d03aa59c8361`  
		Last Modified: Tue, 15 Jul 2025 19:00:06 GMT  
		Size: 3.6 MB (3644971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cef24d483efe8f2b1053cb578dbafbffab2dfd6a644764474184fb805fc872f3`  
		Last Modified: Mon, 28 Jul 2025 20:31:35 GMT  
		Size: 283.5 KB (283470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3316bff964f9f759871a9216a703323b51e64d4b58eb53b6a858e7831c8cd357`  
		Last Modified: Mon, 18 Aug 2025 18:40:20 GMT  
		Size: 81.7 MB (81697402 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a46149d100c12c2a3952f86d1a80e0cc3b64cb50a79f62b6ef751da1a2bebf7`  
		Last Modified: Mon, 18 Aug 2025 18:52:11 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.22` - unknown; unknown

```console
$ docker pull golang@sha256:72c549fc3b594064f86265609200482d8fd0921c647397631cb342cb9795ab95
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **214.7 KB (214714 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25af2267d8a4ceedb71ff3be28995353de38007216ec2590866a49b23c5f3613`

```dockerfile
```

-	Layers:
	-	`sha256:e938846f0a33a1c22c04768de1db8ec91bf4a3e0fbb519689b97e8afb531342d`  
		Last Modified: Mon, 18 Aug 2025 20:23:51 GMT  
		Size: 189.6 KB (189576 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:03ff378fa42a82ade2330203e1f57dba2a414619a9d6cf28ddeaaccda6e6595f`  
		Last Modified: Mon, 18 Aug 2025 20:23:52 GMT  
		Size: 25.1 KB (25138 bytes)  
		MIME: application/vnd.in-toto+json
