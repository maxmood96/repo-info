## `golang:tip-alpine3.22`

```console
$ docker pull golang@sha256:a00afe2cdde9c488deb14f087bcaa0b0624ee47cb83090bd82adfc37a84d2156
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
$ docker pull golang@sha256:295c8cd2299a75c176340f162a5c6e13578efcdd0db583c728f84cd63fbaa7f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.6 MB (83582122 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93c667dc75b86fd6c00386d71900c07c06fffcfd705364b3bd8482d951a17f71`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-armv7.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Mon, 11 Aug 2025 05:23:23 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 11 Aug 2025 05:23:23 GMT
ENV GOTOOLCHAIN=local
# Mon, 11 Aug 2025 05:23:23 GMT
ENV GOPATH=/go
# Mon, 11 Aug 2025 05:23:23 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 11 Aug 2025 05:23:23 GMT
COPY /target/ / # buildkit
# Mon, 11 Aug 2025 05:23:23 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 11 Aug 2025 05:23:23 GMT
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
	-	`sha256:331d10df13da6c65403fe5e3b6a9cc280dde2bb564435b287f2b85119c986cc8`  
		Last Modified: Tue, 12 Aug 2025 19:00:44 GMT  
		Size: 80.1 MB (80080443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:713bce62344bd09c8ee7a7c02bd8a32ccfe9f11897a3cda7215130566e24016c`  
		Last Modified: Tue, 12 Aug 2025 18:05:42 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.22` - unknown; unknown

```console
$ docker pull golang@sha256:bc27276b1b1eb2243e71c2c5ccb04ca790f07418b7c583c1e6a7f10a2d3a481e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **216.8 KB (216811 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9f4fe2f591f3c683675873b1d89ab2e9bd2d3440aa0cb9382a543e40b03b93c`

```dockerfile
```

-	Layers:
	-	`sha256:d91fb4764e1e5b450c61bb48d7d8ed4cb80c504cc49f563d955b3421eb19682d`  
		Last Modified: Thu, 14 Aug 2025 08:23:44 GMT  
		Size: 191.5 KB (191549 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:23b898d1c3d17c9dda304bd8383b3a2d816d419ecc3cee7e355d8ab728fca8de`  
		Last Modified: Thu, 14 Aug 2025 08:23:44 GMT  
		Size: 25.3 KB (25262 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.22` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:7a7dbd9bc36a23c1b72e2f75492b520aa7089a742d77bd73680211f905942a49
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.4 MB (83421030 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:524893b2e66cd6684ebdbbf54ee1887a028d4866e73c1447a3eaa8e5638ffbf0`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-aarch64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Mon, 11 Aug 2025 05:23:23 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 11 Aug 2025 05:23:23 GMT
ENV GOTOOLCHAIN=local
# Mon, 11 Aug 2025 05:23:23 GMT
ENV GOPATH=/go
# Mon, 11 Aug 2025 05:23:23 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 11 Aug 2025 05:23:23 GMT
COPY /target/ / # buildkit
# Mon, 11 Aug 2025 05:23:23 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 11 Aug 2025 05:23:23 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:6e174226ea690ced550e5641249a412cdbefd2d09871f3e64ab52137a54ba606`  
		Last Modified: Tue, 15 Jul 2025 18:59:50 GMT  
		Size: 4.1 MB (4130750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d1a427e917c48b164eae3ec3692b4741f5de528261925d2e5efc62a43e5bfc4`  
		Last Modified: Mon, 28 Jul 2025 20:42:19 GMT  
		Size: 284.7 KB (284709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a87b7cf68665eac7cfd64f5bb944a8b17de913d4de7e1d26ec5a73f422afb207`  
		Last Modified: Tue, 12 Aug 2025 22:36:24 GMT  
		Size: 79.0 MB (79005413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d382007b04729aa9d8b4d0e9a0567518d718e8a3f05c8efad509739b6a2a20e`  
		Last Modified: Tue, 12 Aug 2025 22:36:13 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.22` - unknown; unknown

```console
$ docker pull golang@sha256:ab966047564c1e777c1d36e06e798e4102c7ae24be5b96beaed14d4487d0dc0d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **216.9 KB (216881 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7527fd43b6fd195ff7be967a42ced761ff95c3868c50ed139d02044cac5bafc`

```dockerfile
```

-	Layers:
	-	`sha256:aaccb4efd1c62fd677478d05fe9fc2555418c1a530243eaf3ffe79755ade735f`  
		Last Modified: Thu, 14 Aug 2025 05:24:14 GMT  
		Size: 191.6 KB (191583 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e556f620bd2a6b5686f11eb178694825faee3f4d16a44a0c8f2a9e3d0df01b4c`  
		Last Modified: Thu, 14 Aug 2025 05:24:15 GMT  
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
$ docker pull golang@sha256:da8ff8413c318d9b16d939bd84062b852d0d56372284a7ae85a3894b4deeaaaf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.4 MB (84415417 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b1e1f4e634f8b069f3fb7ca0631fe8acb52bc47953d44533dafdcb430eb9672`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-ppc64le.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Mon, 11 Aug 2025 05:23:23 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 11 Aug 2025 05:23:23 GMT
ENV GOTOOLCHAIN=local
# Mon, 11 Aug 2025 05:23:23 GMT
ENV GOPATH=/go
# Mon, 11 Aug 2025 05:23:23 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 11 Aug 2025 05:23:23 GMT
COPY /target/ / # buildkit
# Mon, 11 Aug 2025 05:23:23 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 11 Aug 2025 05:23:23 GMT
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
	-	`sha256:49d949d12b56c803641dc1ee823fe0b4254f92598b51ea3dd4b12bbfc422e9b7`  
		Last Modified: Tue, 12 Aug 2025 23:22:22 GMT  
		Size: 80.4 MB (80403035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07b48213749a730eeb7aad6b77018ff1acd81481d74db98cd78f4530aae7355b`  
		Last Modified: Tue, 12 Aug 2025 23:22:11 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.22` - unknown; unknown

```console
$ docker pull golang@sha256:323144ca6ab975dcc2a39f0bbb0981a10a1bf9e5c1d378834ff66640993e70df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **214.8 KB (214820 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ed396d7f75a55ca424d7b735c1b4db48a02c6eec32e75f3180324f59140cfb4`

```dockerfile
```

-	Layers:
	-	`sha256:ced42c86f35a893a649623f5bff89f9eb4114b0fa559a4f62d4109c183df11e3`  
		Last Modified: Thu, 14 Aug 2025 08:23:52 GMT  
		Size: 189.6 KB (189624 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f10429f4a263a1c517cce14937bed88ff351b2d5fa979cc79aac42595f369211`  
		Last Modified: Thu, 14 Aug 2025 08:23:52 GMT  
		Size: 25.2 KB (25196 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.22` - linux; riscv64

```console
$ docker pull golang@sha256:918051b43cab56239ba67b660eceb925fa406a17cd991005cc33ea730e468ae8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.3 MB (84262989 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7be3360ed50858a26d6cf4b1474345ac65a1d63724a0195e5a5380aeac08a7e3`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-riscv64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Mon, 11 Aug 2025 05:23:23 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 11 Aug 2025 05:23:23 GMT
ENV GOTOOLCHAIN=local
# Mon, 11 Aug 2025 05:23:23 GMT
ENV GOPATH=/go
# Mon, 11 Aug 2025 05:23:23 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 11 Aug 2025 05:23:23 GMT
COPY /target/ / # buildkit
# Mon, 11 Aug 2025 05:23:23 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 11 Aug 2025 05:23:23 GMT
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
	-	`sha256:913c1159826bb23e5196b06096f2b66ad808c31d84200f35d658ee413af6cd93`  
		Last Modified: Tue, 12 Aug 2025 21:35:10 GMT  
		Size: 80.5 MB (80467250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6936b194b529e582a2ab6897a5f1083b02771be7d4875a94dd8113ff8a067e47`  
		Last Modified: Mon, 18 Aug 2025 09:59:48 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.22` - unknown; unknown

```console
$ docker pull golang@sha256:b3e5abf0f8f3becf170e0de11a4df62efb3bbd2729ff1b84aa6428b06779afbe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **214.8 KB (214815 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a92d1eac478d01bbfbc7f1ae4bd2da5e38e7cf420ede37e64240fa1e99d52c2b`

```dockerfile
```

-	Layers:
	-	`sha256:ea7a80f9408f88e2b298ba0df2019dd64328340f9c24d2fb05108a3ec29f5016`  
		Last Modified: Mon, 18 Aug 2025 11:24:01 GMT  
		Size: 189.6 KB (189620 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0269c8eebbad5cb1f96d998b389cfca908341e09e864ff9fbe3bed50d58aa794`  
		Last Modified: Mon, 18 Aug 2025 11:24:01 GMT  
		Size: 25.2 KB (25195 bytes)  
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
