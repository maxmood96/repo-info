## `golang:tip-alpine3.22`

```console
$ docker pull golang@sha256:4c3cb84908644c1815b13f941c48c400a56e3914192948fe0db064bda10edeba
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
$ docker pull golang@sha256:799a9b4d7bb731807fcd6d03dadd2c687a122b945dc78f4617bd41ec0176dc7e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.6 MB (97606572 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04daf440c7771ca6206a5b8f0dcc809d90a4a218d77575e8659c39380d287e87`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:40 GMT
ADD alpine-minirootfs-3.22.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:40 GMT
CMD ["/bin/sh"]
# Tue, 17 Feb 2026 19:29:09 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 17 Feb 2026 19:31:05 GMT
ENV GOTOOLCHAIN=local
# Tue, 17 Feb 2026 19:31:05 GMT
ENV GOPATH=/go
# Tue, 17 Feb 2026 19:31:05 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Feb 2026 19:31:05 GMT
COPY /target/ / # buildkit
# Tue, 17 Feb 2026 19:31:08 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 17 Feb 2026 19:31:08 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:d49a2dee86fb12766dd648402d010ca105846a41bd58738454e53780d4bb8e97`  
		Last Modified: Wed, 28 Jan 2026 01:18:46 GMT  
		Size: 3.8 MB (3804875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40117826638c20c8d127d176d1e7e02635693aaff63b683c9b97026997d60d9f`  
		Last Modified: Tue, 17 Feb 2026 19:31:23 GMT  
		Size: 291.2 KB (291157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eab0817763c3e1cf11dc0cf9b1bdc31701d4aef51c361f72a656b7a9a217055a`  
		Last Modified: Tue, 17 Feb 2026 19:31:25 GMT  
		Size: 93.5 MB (93510382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28bbe664d72fd6785df9967be372f4bee188672663c87ec819a4f2d6825a91af`  
		Last Modified: Tue, 17 Feb 2026 19:31:23 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.22` - unknown; unknown

```console
$ docker pull golang@sha256:9cac3fdebc13d04fb6fa27bf6f1544415f6e5a68dbff6e2f74167ec29bbc0585
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.4 KB (219447 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6c0f0f76351866733ca2d1cc3484920ebbd148753ac050ec7f85a1c1a7d4bd5`

```dockerfile
```

-	Layers:
	-	`sha256:bf50e018168a952096bb41435d37d4e555242a492864bed3f4c907d501580088`  
		Last Modified: Tue, 17 Feb 2026 19:31:23 GMT  
		Size: 195.0 KB (194982 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:379d4b8442656cf6c0a3344a261729b00e596a1e4f904c063fceececa45372b8`  
		Last Modified: Tue, 17 Feb 2026 19:31:23 GMT  
		Size: 24.5 KB (24465 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.22` - linux; arm variant v6

```console
$ docker pull golang@sha256:9c4ea96c1032f15ee8579e04a99e4b6d76b1b55bd6925acc935e71ddb4722c3c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.7 MB (93683041 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6fc589f1efec0093521a8e50d402e2b83b387d695eab29db31683b1492f83ce`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:06 GMT
ADD alpine-minirootfs-3.22.3-armhf.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:06 GMT
CMD ["/bin/sh"]
# Tue, 17 Feb 2026 19:26:02 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 17 Feb 2026 19:28:50 GMT
ENV GOTOOLCHAIN=local
# Tue, 17 Feb 2026 19:28:50 GMT
ENV GOPATH=/go
# Tue, 17 Feb 2026 19:28:50 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Feb 2026 19:28:50 GMT
COPY /target/ / # buildkit
# Tue, 17 Feb 2026 19:28:53 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 17 Feb 2026 19:28:53 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:835838571e5c80c63481753299e25a9f89f366d8f4a9c1a2043b8fdf98176f17`  
		Last Modified: Wed, 28 Jan 2026 01:18:10 GMT  
		Size: 3.5 MB (3505046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd6701237791d27cafe8e8f9d4c7bfcbac4a5d0be27031f234baf00409cf4d7b`  
		Last Modified: Tue, 17 Feb 2026 19:29:04 GMT  
		Size: 292.3 KB (292321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c849b5502ff1808ed42324acc56715e626b727f24beea5a036b21ffa2f6c3079`  
		Last Modified: Tue, 17 Feb 2026 19:29:06 GMT  
		Size: 89.9 MB (89885516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:724c9a65f9811433cf733e94e1a8c45e5f7ec4e574d479221ab63b51f6399105`  
		Last Modified: Tue, 17 Feb 2026 19:29:04 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.22` - unknown; unknown

```console
$ docker pull golang@sha256:61e4301837fc1195873e9b9c55abb6bacefd93c45b7c28ca1e0a00d85b6b8c06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.4 KB (24362 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03d6531895756155b964392c0476e76613e405e60cff45fcb9434c3af591a127`

```dockerfile
```

-	Layers:
	-	`sha256:7312aecadc4dd499a314f0e6d5a491e3ec1316873c28fa3e01ee78c7b592fa06`  
		Last Modified: Tue, 17 Feb 2026 19:29:04 GMT  
		Size: 24.4 KB (24362 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.22` - linux; arm variant v7

```console
$ docker pull golang@sha256:3ba5b9d67391a7459f8374a20a9f6ab3ef0b13854166a4e5df368f5fd082bbb0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.1 MB (93131291 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:723116fcb1ec629e26faf8dc13f6d0ea39dee6245f03746d25027fd5b7444bfa`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:29 GMT
ADD alpine-minirootfs-3.22.3-armv7.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:29 GMT
CMD ["/bin/sh"]
# Tue, 17 Feb 2026 19:29:53 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 17 Feb 2026 19:29:15 GMT
ENV GOTOOLCHAIN=local
# Tue, 17 Feb 2026 19:29:15 GMT
ENV GOPATH=/go
# Tue, 17 Feb 2026 19:29:15 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Feb 2026 19:29:15 GMT
COPY /target/ / # buildkit
# Tue, 17 Feb 2026 19:32:39 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 17 Feb 2026 19:32:39 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:caca1d0e2f8affe80569328af55c755a8480801c5ee912e55aaa828c8209aa6e`  
		Last Modified: Wed, 28 Jan 2026 01:18:35 GMT  
		Size: 3.2 MB (3223629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7977dbdcc21d6795f22274f24ee39edf9b24cc0a9587d76fea9dfd73f37d26be`  
		Last Modified: Tue, 17 Feb 2026 19:32:45 GMT  
		Size: 291.2 KB (291204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc8592fb2ab8b68f648f6fdc255c5205f63cba2d9ae66c3ae76aec04ac54577d`  
		Last Modified: Tue, 17 Feb 2026 19:29:44 GMT  
		Size: 89.6 MB (89616301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d412846adce3bdfd1e635114d0461d91f2e257ea09bb0d3e989ad99d3e4f6b9f`  
		Last Modified: Tue, 17 Feb 2026 19:32:45 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.22` - unknown; unknown

```console
$ docker pull golang@sha256:0dcc561a23f12cbcc906011b44c6e327fcf382021d28091275281dd9c3139a4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.6 KB (219563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:966638ba5b8b25a09e17562b8fd4c7ed0ec9064bf0d642805e60dfde54a92a54`

```dockerfile
```

-	Layers:
	-	`sha256:e05170bdd28e4b5c8b89ae03eac7b94f64e6be503eab0d30e7081229bce924bd`  
		Last Modified: Tue, 17 Feb 2026 19:32:45 GMT  
		Size: 195.0 KB (194986 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7c27ba6adc00da70196b546a29dcc0ea1476e41246862fce9ad336fe2097e717`  
		Last Modified: Tue, 17 Feb 2026 19:32:45 GMT  
		Size: 24.6 KB (24577 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.22` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:18453c853c96a20be7595446b43c6024ad52b1a3ac5d101e9bbcf49287fa3d9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.1 MB (93116757 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf288ad22278ee53111f957ffbea9fa4d6f039348a1b263636145894a30d56de`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:55 GMT
ADD alpine-minirootfs-3.22.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:55 GMT
CMD ["/bin/sh"]
# Tue, 17 Feb 2026 19:27:15 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 17 Feb 2026 19:29:01 GMT
ENV GOTOOLCHAIN=local
# Tue, 17 Feb 2026 19:29:01 GMT
ENV GOPATH=/go
# Tue, 17 Feb 2026 19:29:01 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Feb 2026 19:29:01 GMT
COPY /target/ / # buildkit
# Tue, 17 Feb 2026 19:29:03 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 17 Feb 2026 19:29:03 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:d741ee1608f399e21c72d05f0f818c348c6801af33aeb83523893d09dc153957`  
		Last Modified: Wed, 28 Jan 2026 01:18:00 GMT  
		Size: 4.1 MB (4139519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b36a86cc792a009963a5e3417a03f665a1bb56b50d1a97bfba82124ae9d192c8`  
		Last Modified: Tue, 17 Feb 2026 19:29:18 GMT  
		Size: 294.1 KB (294109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14c4ec7dd3016101f540520ce3287918647d94b478d69d4a817cb7382cffb26d`  
		Last Modified: Tue, 17 Feb 2026 19:29:15 GMT  
		Size: 88.7 MB (88682971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2a00264817fdcf8f5238e3b8892653cc052e4e1aefd0308ccf9facbab0f6646`  
		Last Modified: Tue, 17 Feb 2026 19:29:18 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.22` - unknown; unknown

```console
$ docker pull golang@sha256:2a1ed718639d3a2b0467721f834ef75d8a2baf51ff6c66fe3bfafc239d5c5ae1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.6 KB (219615 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:753555558a0aff23b82e70ed0d28428c2b61ee307c2c8a2024311e8d843b6d03`

```dockerfile
```

-	Layers:
	-	`sha256:e35575b28cc682904936e7d5585ed7d57eb29db981e18abbaac90a801abb2c3f`  
		Last Modified: Tue, 17 Feb 2026 19:29:18 GMT  
		Size: 195.0 KB (195014 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:57cb6c89d30c435c8245b90bc7daefa09e92c5e48cdc9b47c86673380efd0898`  
		Last Modified: Tue, 17 Feb 2026 19:29:18 GMT  
		Size: 24.6 KB (24601 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.22` - linux; 386

```console
$ docker pull golang@sha256:cac4e3575cee1ec8f244c2d894e120c6b04af4a0bb6ab2130b40460123becb35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.3 MB (95327672 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c808312cf94d0e7c4a9924f65c1b9e8e781d2c4db6bd4cbe43ea459001956885`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:53 GMT
ADD alpine-minirootfs-3.22.3-x86.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:53 GMT
CMD ["/bin/sh"]
# Tue, 17 Feb 2026 19:27:09 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 17 Feb 2026 19:26:28 GMT
ENV GOTOOLCHAIN=local
# Tue, 17 Feb 2026 19:26:28 GMT
ENV GOPATH=/go
# Tue, 17 Feb 2026 19:26:28 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Feb 2026 19:26:28 GMT
COPY /target/ / # buildkit
# Tue, 17 Feb 2026 19:29:05 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 17 Feb 2026 19:29:05 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:757a99eda61f22434071cfbc7a70f9526b63aeb5479a64272982017ee7cd9cfd`  
		Last Modified: Wed, 28 Jan 2026 01:18:59 GMT  
		Size: 3.6 MB (3620732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:091320d5128775275bf70598410ff3a892863a64d12bb82871573589bc84b5fa`  
		Last Modified: Tue, 17 Feb 2026 19:29:11 GMT  
		Size: 291.6 KB (291626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30233e899defca3f42aa6ad06bb0772f268b46b15c12c0af84227790251579bd`  
		Last Modified: Tue, 17 Feb 2026 19:26:57 GMT  
		Size: 91.4 MB (91415156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b41b42a830c9c7594f1342330d3d81536cae6d1f5afa46dddb1907850a25040`  
		Last Modified: Tue, 17 Feb 2026 19:29:10 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.22` - unknown; unknown

```console
$ docker pull golang@sha256:77fc8f0d3eaf48755e3aba446288b6c246374fda07ab78990508d5dd3821ca1a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.4 KB (219381 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d947ddfd048244d86414c096391cc460c0050c5f8b90e0e808b24c4f4fbae50f`

```dockerfile
```

-	Layers:
	-	`sha256:08333544df93da86007cb69d99e991d45fc7405de3c04d0b627ae57adc07889a`  
		Last Modified: Tue, 17 Feb 2026 19:29:10 GMT  
		Size: 195.0 KB (194951 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a90d9bb7a87019b11213deb3c2b41db8ec98a374d54b0a5d923936d8da123064`  
		Last Modified: Tue, 17 Feb 2026 19:29:11 GMT  
		Size: 24.4 KB (24430 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.22` - linux; ppc64le

```console
$ docker pull golang@sha256:a806a5857373543cf95396a015cb0de71a03159c1155850b322de3962551f3cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.2 MB (94238486 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c41c845fcaf4bafd5b0e18f5e9501becf2161cc4cc9c24bb54f52edee41dc4c`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:35 GMT
ADD alpine-minirootfs-3.22.3-ppc64le.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:35 GMT
CMD ["/bin/sh"]
# Mon, 09 Feb 2026 20:32:45 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 17 Feb 2026 19:40:43 GMT
ENV GOTOOLCHAIN=local
# Tue, 17 Feb 2026 19:40:43 GMT
ENV GOPATH=/go
# Tue, 17 Feb 2026 19:40:43 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Feb 2026 19:40:43 GMT
COPY /target/ / # buildkit
# Tue, 17 Feb 2026 19:46:33 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 17 Feb 2026 19:46:36 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:d7b7d5bab08f20b53e85395b2d6e793469e3acdbe8644bd234992524588b440f`  
		Last Modified: Wed, 28 Jan 2026 01:17:44 GMT  
		Size: 3.7 MB (3734297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cc2604b78642af0499cb3a1b9f782035bf72390be0d0d2b55d3e7523ce711e9`  
		Last Modified: Mon, 09 Feb 2026 20:33:09 GMT  
		Size: 294.6 KB (294647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fde41aed2421b1bfa6ecab656c0c906edcbf89b7187c466f56a4a89af6490b6`  
		Last Modified: Tue, 17 Feb 2026 19:42:01 GMT  
		Size: 90.2 MB (90209384 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4af1e46bca926ebb9950d9c408c4e134a54f91931e9e652287e167cdf16e64c`  
		Last Modified: Tue, 17 Feb 2026 19:47:00 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.22` - unknown; unknown

```console
$ docker pull golang@sha256:10ad538498ff91cd68f81d9cc06a194ff4ed3aa997047c9aefdb14a71879bb4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **217.4 KB (217407 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1813e8bc32e0abd2faff7579e9cd91c86eaf682863956ff866423cb0a53c5e5d`

```dockerfile
```

-	Layers:
	-	`sha256:45c68d678d4d06e35474409eac11b7997f8b0e8430614992226e6257f97ce4d2`  
		Last Modified: Tue, 17 Feb 2026 19:47:01 GMT  
		Size: 193.1 KB (193069 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:772a8b0ddf76818ca0b083aa75d61dc4b3cf9f6b358cc91a082e90315e837b19`  
		Last Modified: Tue, 17 Feb 2026 19:47:01 GMT  
		Size: 24.3 KB (24338 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.22` - linux; riscv64

```console
$ docker pull golang@sha256:eadadce120aa03df7c089a46fca9401f923fab0518d4d373dc11149089aae85c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.5 MB (94450510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e50017bca6d51b9211d129aa0ffb5d08f30c307aadd1e57020d25495e4c4de43`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 03:49:43 GMT
ADD alpine-minirootfs-3.22.3-riscv64.tar.gz / # buildkit
# Wed, 28 Jan 2026 03:49:43 GMT
CMD ["/bin/sh"]
# Thu, 29 Jan 2026 19:15:18 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 09 Feb 2026 20:36:19 GMT
ENV GOTOOLCHAIN=local
# Mon, 09 Feb 2026 20:36:19 GMT
ENV GOPATH=/go
# Mon, 09 Feb 2026 20:36:19 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Feb 2026 20:36:19 GMT
COPY /target/ / # buildkit
# Mon, 09 Feb 2026 22:03:11 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 09 Feb 2026 22:03:11 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:15ea87d2370d91334d14e1cb46366adb6a57bbae717f07f8c9f55735cf137f62`  
		Last Modified: Wed, 28 Jan 2026 03:50:15 GMT  
		Size: 3.5 MB (3517422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79dcab0b270d631ffdfee1c090f676984c71b03f87fc76005b512418b2ec110c`  
		Last Modified: Thu, 29 Jan 2026 19:17:49 GMT  
		Size: 291.5 KB (291499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a23894c629a08e6202ce12c965a7b27818d87e5582941a612a4ef5200db7436f`  
		Last Modified: Mon, 09 Feb 2026 20:43:36 GMT  
		Size: 90.6 MB (90641431 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f24082e71ed1fb2a79b992c890a19fc45c509b06ff905118c78ceea7f60be524`  
		Last Modified: Mon, 09 Feb 2026 22:04:34 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.22` - unknown; unknown

```console
$ docker pull golang@sha256:ce9ee12c1aeb4ea21f31e587cc8fb27f5878d803ab2aea92d5a79fbf22869f87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **217.6 KB (217576 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4be5b6c96dc607f9ad680df9b868ee33994ba026092b2beb7b63ea3e5f9e5658`

```dockerfile
```

-	Layers:
	-	`sha256:b45262bcbd6a5ddb4899e596e14126ab0e5fe05b2b71b89e3a746f558eed6409`  
		Last Modified: Tue, 10 Feb 2026 23:52:21 GMT  
		Size: 193.1 KB (193065 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7a52bcf9fe50d73997f62c12d6deaca298f7f48e0f41225a783c1740117e13fd`  
		Last Modified: Tue, 10 Feb 2026 23:52:21 GMT  
		Size: 24.5 KB (24511 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.22` - linux; s390x

```console
$ docker pull golang@sha256:980c89fd77909aa19650df88cab9b93ba1532ac7eaf5e1dec1027dc2e3a484b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.7 MB (96689462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87de41e6d178bda21063d020bbed59935ab4e86cc62e4bf6dbc88fcde856f739`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:06 GMT
ADD alpine-minirootfs-3.22.3-s390x.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:06 GMT
CMD ["/bin/sh"]
# Mon, 09 Feb 2026 20:00:48 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 17 Feb 2026 19:29:54 GMT
ENV GOTOOLCHAIN=local
# Tue, 17 Feb 2026 19:29:54 GMT
ENV GOPATH=/go
# Tue, 17 Feb 2026 19:29:54 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Feb 2026 19:29:54 GMT
COPY /target/ / # buildkit
# Tue, 17 Feb 2026 19:30:05 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 17 Feb 2026 19:30:05 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:dab48b8d1bab09fede3f54264828e67466f10d64acc37d9412190034dbcbf61f`  
		Last Modified: Wed, 28 Jan 2026 01:17:16 GMT  
		Size: 3.7 MB (3650434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76749314be44914af39bd61e306cd10a375855ca5a5abff17bb70e369a7a3426`  
		Last Modified: Mon, 09 Feb 2026 20:01:00 GMT  
		Size: 292.1 KB (292139 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a6b6bbd9c00c665dfd4909e8016410533856709507819e5042a938a46f4e345`  
		Last Modified: Tue, 17 Feb 2026 19:30:38 GMT  
		Size: 92.7 MB (92746731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bcf8ceea3e77cbf9983f3f398442674d716b50e84ed1ba2de1d1096b5bdd16f`  
		Last Modified: Tue, 17 Feb 2026 19:30:36 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.22` - unknown; unknown

```console
$ docker pull golang@sha256:04020ce13780ed9047065822dfe956793d13c46ec68380659ef055c9a8708677
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **217.3 KB (217323 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d100e30a242e399965a19c8e7f657d7b54a314db76be74c1d0cb033a61c5dae6`

```dockerfile
```

-	Layers:
	-	`sha256:a884ae3e4618ca1f156a987b451c514641f6469255b3b6766c26c9c26588d946`  
		Last Modified: Tue, 17 Feb 2026 19:30:36 GMT  
		Size: 193.0 KB (193031 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7dc1d1ca2e7106fc149974f68d0bb71e058a8a33ef30e25a0f293433407053ad`  
		Last Modified: Tue, 17 Feb 2026 19:30:36 GMT  
		Size: 24.3 KB (24292 bytes)  
		MIME: application/vnd.in-toto+json
