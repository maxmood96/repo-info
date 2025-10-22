## `golang:tip-alpine3.21`

```console
$ docker pull golang@sha256:a1c9358df1bd101830e1c633e8ce4845f3cdb8490ce90201f1a41be4fa2f0c2d
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

### `golang:tip-alpine3.21` - linux; amd64

```console
$ docker pull golang@sha256:f1e6e5cc32184ab9aa37f1a917a54eaee12d49584d3e2dc8e3e955ce4d16af4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.5 MB (95469899 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:344ac540bfe00670dfb81f0def88674a05e94cc5495d7e214983da8be5b58823`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:06:42 GMT
ADD alpine-minirootfs-3.21.5-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:06:42 GMT
CMD ["/bin/sh"]
# Mon, 20 Oct 2025 05:23:19 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 20 Oct 2025 05:23:19 GMT
ENV GOTOOLCHAIN=local
# Mon, 20 Oct 2025 05:23:19 GMT
ENV GOPATH=/go
# Mon, 20 Oct 2025 05:23:19 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 20 Oct 2025 05:23:19 GMT
COPY /target/ / # buildkit
# Mon, 20 Oct 2025 05:23:19 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 20 Oct 2025 05:23:19 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:f637881d1138581d892d9eb942c56e0ccc7758fe3bdc0f1e6cd66059fdfd8185`  
		Last Modified: Wed, 08 Oct 2025 12:54:09 GMT  
		Size: 3.6 MB (3642569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbdd56088f5280f14ee6347cd70e4c890a80e73454198a3a61368ba08f362fc0`  
		Last Modified: Tue, 21 Oct 2025 20:16:29 GMT  
		Size: 291.1 KB (291120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1632beb51230c8a4ac1a55d542c14118180abcd1ea545cae9f227132e15b6ab3`  
		Last Modified: Tue, 21 Oct 2025 20:16:37 GMT  
		Size: 91.5 MB (91536053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d1124f20568be58652532499e86fe04f1368b82408f744cd8e73abbcbe456c0`  
		Last Modified: Tue, 21 Oct 2025 20:16:28 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.21` - unknown; unknown

```console
$ docker pull golang@sha256:69194651e2e384fd8476db0125c99d3b146746b6c893f36360fadec43078c141
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.7 KB (218712 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74f58d7096a2e34d4d3c9ace23cffd26082037d4f11d935577be2f7a50d4975b`

```dockerfile
```

-	Layers:
	-	`sha256:d72b504ae49fb1dfc155da9b7f2916d950bc2c2fe35b1579cc267875e45eeeb7`  
		Last Modified: Tue, 21 Oct 2025 23:23:43 GMT  
		Size: 194.2 KB (194205 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:05727c7c86c7da208751814bfb16d413977cbd3ea8bdd9fdb4b3395bb3fe69e5`  
		Last Modified: Tue, 21 Oct 2025 23:23:44 GMT  
		Size: 24.5 KB (24507 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.21` - linux; arm variant v6

```console
$ docker pull golang@sha256:9573b2cbdb0a26b6cdcb02a1eea0353d02e6e67180841118bde3dbe25873e392
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.8 MB (91751350 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b759123bae4a667ef239901f700551b0b7ab95ad7d8af8689252aa52a9aeb592`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:06:42 GMT
ADD alpine-minirootfs-3.21.5-armhf.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:06:42 GMT
CMD ["/bin/sh"]
# Mon, 20 Oct 2025 05:23:19 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 20 Oct 2025 05:23:19 GMT
ENV GOTOOLCHAIN=local
# Mon, 20 Oct 2025 05:23:19 GMT
ENV GOPATH=/go
# Mon, 20 Oct 2025 05:23:19 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 20 Oct 2025 05:23:19 GMT
COPY /target/ / # buildkit
# Mon, 20 Oct 2025 05:23:19 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 20 Oct 2025 05:23:19 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:f8b30cbd0fab9e5a803578a09c973d18d7450816d914e63e04e5c2edd79f8bee`  
		Last Modified: Wed, 08 Oct 2025 21:00:33 GMT  
		Size: 3.4 MB (3365468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:404187866b34203f46537b84220bb13e059d5ac126d1251aa1acc5522a2fe162`  
		Last Modified: Tue, 21 Oct 2025 18:14:31 GMT  
		Size: 292.2 KB (292244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13fca43ea3215bb8b4bd8c9ca4cc0aa81fba4980d0b35ba908d3f70e7a5c22f6`  
		Last Modified: Tue, 21 Oct 2025 18:13:59 GMT  
		Size: 88.1 MB (88093480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:336a4d80b4adcdf27afe4548f7ce00e88c4f5f4234d474ee5fb6bf0a039fba8f`  
		Last Modified: Tue, 21 Oct 2025 18:14:31 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.21` - unknown; unknown

```console
$ docker pull golang@sha256:a3134e187e049588d5b43e0d7d8571d9b10831453c556c2cf49fa67c9f39a405
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.4 KB (24405 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca7bc83987e5300d20cb153dce5229a9cb98f4032210d58e837d769f50faecb0`

```dockerfile
```

-	Layers:
	-	`sha256:76e1b4fed9908f1eee06401af5d0cc0991a984f4be137f51fa1605ac1d90ae35`  
		Last Modified: Tue, 21 Oct 2025 20:23:46 GMT  
		Size: 24.4 KB (24405 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.21` - linux; arm variant v7

```console
$ docker pull golang@sha256:bb5a878e5819a006eb8dcc24243c5e29d312d0a3e0b80fd7927eeed13f4b4070
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.2 MB (91227366 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dec29143ef88d76285236831aebc6d851de68ebd824718d8b427e555144ed37a`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:06:42 GMT
ADD alpine-minirootfs-3.21.5-armv7.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:06:42 GMT
CMD ["/bin/sh"]
# Mon, 20 Oct 2025 05:23:19 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 20 Oct 2025 05:23:19 GMT
ENV GOTOOLCHAIN=local
# Mon, 20 Oct 2025 05:23:19 GMT
ENV GOPATH=/go
# Mon, 20 Oct 2025 05:23:19 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 20 Oct 2025 05:23:19 GMT
COPY /target/ / # buildkit
# Mon, 20 Oct 2025 05:23:19 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 20 Oct 2025 05:23:19 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:520d06ecc3ba4ec2920319fa6f2cc6bea9a9c1d5a43808c1d2388522c37d7b30`  
		Last Modified: Wed, 08 Oct 2025 16:24:34 GMT  
		Size: 3.1 MB (3098611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16dd1bbb650212fc85a0c72a9f33656f2e0ec8c1978c7c6f2429afd922dc6e35`  
		Last Modified: Tue, 21 Oct 2025 18:16:18 GMT  
		Size: 291.1 KB (291140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e37a565b466ff673d6eaad95f7f918df4a47f13ea7ff94f9312bc4a254253fc`  
		Last Modified: Tue, 21 Oct 2025 18:15:25 GMT  
		Size: 87.8 MB (87837459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a92723452a3bea5d58c016adda8d0fa909aa8bfb20fa694d26fbae8fb178d37c`  
		Last Modified: Tue, 21 Oct 2025 18:16:18 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.21` - unknown; unknown

```console
$ docker pull golang@sha256:52e9f64e5f728ab64188ace40fdf5d3cc5ad24d02b2871c81108469eab3bbc7e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.8 KB (218829 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f86f0d69b47492efd521116de81901d64e8a91e2f78f94d3f88feea9742cbfc`

```dockerfile
```

-	Layers:
	-	`sha256:6c8d321927c2a658be29f24d240c72a6aee54b510745d8ebd76883a8a24145cd`  
		Last Modified: Tue, 21 Oct 2025 20:23:49 GMT  
		Size: 194.2 KB (194209 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aa9ba9bd21062e12d5f686bc1cdde4006338d7ecaf49351e3e60c6cc123c0e97`  
		Last Modified: Tue, 21 Oct 2025 20:23:50 GMT  
		Size: 24.6 KB (24620 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.21` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:8a249d9cead20efef0ce479dc58cbea814982a06d68a2b19230c4b236088e86e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.1 MB (91075219 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a67800db7f48f89209e2179913b0bddaa8701c05d4f6f38f964c586b730ccdbb`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:06:42 GMT
ADD alpine-minirootfs-3.21.5-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:06:42 GMT
CMD ["/bin/sh"]
# Mon, 20 Oct 2025 05:23:19 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 20 Oct 2025 05:23:19 GMT
ENV GOTOOLCHAIN=local
# Mon, 20 Oct 2025 05:23:19 GMT
ENV GOPATH=/go
# Mon, 20 Oct 2025 05:23:19 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 20 Oct 2025 05:23:19 GMT
COPY /target/ / # buildkit
# Mon, 20 Oct 2025 05:23:19 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 20 Oct 2025 05:23:19 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:c2fe130f4aabc917e559e7eed7d37b0e21ba13b44520101696887ca892e8c63f`  
		Last Modified: Wed, 08 Oct 2025 16:24:46 GMT  
		Size: 4.0 MB (3992353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c13fc8eb3ee14543d642ca41f64affb3dd6ea68f9f7ecdc431cd21b50d1f44cd`  
		Last Modified: Tue, 21 Oct 2025 18:13:54 GMT  
		Size: 294.0 KB (294029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c596fe60daead99d920e71d2cefb1c0329c841dbd8772728b90e497e3f4f21b`  
		Last Modified: Tue, 21 Oct 2025 18:14:12 GMT  
		Size: 86.8 MB (86788679 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d72fa2872a14f6815045eb3ee186719248f99f07fb17b8c5ad8a3bc71d5ae6fe`  
		Last Modified: Tue, 21 Oct 2025 18:13:54 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.21` - unknown; unknown

```console
$ docker pull golang@sha256:b0af66243e09ad523b904be05c19ba1e101848fd583cdb84e0049487a9ca4c11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.9 KB (218881 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:685f9b97db0d9cc2dff8aa38033304a13224046bd1d9c39028de5749881379f7`

```dockerfile
```

-	Layers:
	-	`sha256:dc7c4857e64681b3351a68bea55d61cff23fdcd06510b7ac85b44a895df62a8a`  
		Last Modified: Tue, 21 Oct 2025 20:23:53 GMT  
		Size: 194.2 KB (194237 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f21ed6f29871cc9360f27d74f208d034f558bf22e41d1bf309f2c992307f1d78`  
		Last Modified: Tue, 21 Oct 2025 20:23:54 GMT  
		Size: 24.6 KB (24644 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.21` - linux; 386

```console
$ docker pull golang@sha256:91b55682ac800beeac41d781ed70051ac5cdf1c5e47708af6ff9997e75936550
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.4 MB (93419762 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:265cc155b2f5e483dd682abd0b99f1b1589cf098f6d5171a0662106e50d00aa1`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:06:42 GMT
ADD alpine-minirootfs-3.21.5-x86.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:06:42 GMT
CMD ["/bin/sh"]
# Mon, 20 Oct 2025 05:23:19 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 20 Oct 2025 05:23:19 GMT
ENV GOTOOLCHAIN=local
# Mon, 20 Oct 2025 05:23:19 GMT
ENV GOPATH=/go
# Mon, 20 Oct 2025 05:23:19 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 20 Oct 2025 05:23:19 GMT
COPY /target/ / # buildkit
# Mon, 20 Oct 2025 05:23:19 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 20 Oct 2025 05:23:19 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:bbedd1c05bb5090fc3fc2356be88d60b2a60937565b56e91fb4be42c5c73d485`  
		Last Modified: Wed, 08 Oct 2025 16:25:36 GMT  
		Size: 3.5 MB (3464704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6754c628489dd091964bb0a428e98e88a4e9c5c58535d823c22f5e7c74702a92`  
		Last Modified: Tue, 21 Oct 2025 18:15:33 GMT  
		Size: 291.6 KB (291583 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f21a8159428f1559d656875bfece2dbae3e195e6c40dc6a160e07432d96a1ef`  
		Last Modified: Tue, 21 Oct 2025 18:13:42 GMT  
		Size: 89.7 MB (89663317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb12cbe987abdacc3137234d0de1d4e4290ca10a2c3e16703655f4d7030195cf`  
		Last Modified: Tue, 21 Oct 2025 18:15:33 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.21` - unknown; unknown

```console
$ docker pull golang@sha256:a1160ac9b14b94b3e2549b2719820776a208b7e06301354ee5ea1751ce06bfde
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.6 KB (218648 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db4d1766b8e31228e5c8a1159335cfc418972996356a18724605a8e2ac5160be`

```dockerfile
```

-	Layers:
	-	`sha256:d7f3ecf73afe387103f95efb9f8aafccdf2109bf864382cfcd741255311f56e7`  
		Last Modified: Tue, 21 Oct 2025 20:23:57 GMT  
		Size: 194.2 KB (194174 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b09fc440a94ce02692ade59d2d9cf15ddfcacb068491b88785b5be4fed2c9fd6`  
		Last Modified: Tue, 21 Oct 2025 20:23:58 GMT  
		Size: 24.5 KB (24474 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.21` - linux; ppc64le

```console
$ docker pull golang@sha256:5fd54bed1fe1e05d73a8a417f5f1528653dd1c80a73c3e4e1756bfb88eadc723
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.3 MB (91310641 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11628b99e1025373c7ed36557d28beb2b93556e3d027bd8a4dad373589a4ffa0`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:06:42 GMT
ADD alpine-minirootfs-3.21.5-ppc64le.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:06:42 GMT
CMD ["/bin/sh"]
# Mon, 13 Oct 2025 05:23:19 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 13 Oct 2025 05:23:19 GMT
ENV GOTOOLCHAIN=local
# Mon, 13 Oct 2025 05:23:19 GMT
ENV GOPATH=/go
# Mon, 13 Oct 2025 05:23:19 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 13 Oct 2025 05:23:19 GMT
COPY /target/ / # buildkit
# Mon, 13 Oct 2025 05:23:19 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 13 Oct 2025 05:23:19 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:e99908f6ead74bb809123fe0d40505509ed6113949496be71629433c6ea3fa1a`  
		Last Modified: Wed, 08 Oct 2025 16:25:03 GMT  
		Size: 3.6 MB (3574075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f73de5935c27bbf53bedf5cf444a1a2d137f0c9fa6be0ac31ba3a0af17a0953`  
		Last Modified: Thu, 09 Oct 2025 03:31:32 GMT  
		Size: 294.5 KB (294519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7fb280635ff73067e450776ffb495ea1ad6245c60020ec72c47db59cab52504`  
		Last Modified: Mon, 13 Oct 2025 18:24:19 GMT  
		Size: 87.4 MB (87441889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1da7f2ed71f20b3640caece799dcbc5bed18b450fa134d2b2710d74b463e3009`  
		Last Modified: Mon, 13 Oct 2025 18:36:24 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.21` - unknown; unknown

```console
$ docker pull golang@sha256:87e556afe6317fe399178117583a95fb0a2e2f0cb94c5b8c014abb9039d3ab22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **216.8 KB (216846 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:120881e88c0c48486e00fca3882ced5d2efbdf38d77d5947aa65d0659035baaa`

```dockerfile
```

-	Layers:
	-	`sha256:6b160ccc6ebe14ab77eb54c17c064bf0d36da06e4b15dc3abb6c4e1ce1c0a17b`  
		Last Modified: Tue, 14 Oct 2025 02:24:57 GMT  
		Size: 192.3 KB (192292 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d06210c3d3c5bcaf0d9d0af9b3a25a76a321ec6b5e4826b755c71e62f69ef6d5`  
		Last Modified: Tue, 14 Oct 2025 02:24:58 GMT  
		Size: 24.6 KB (24554 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.21` - linux; riscv64

```console
$ docker pull golang@sha256:59784092948ce0d042ada0432ab903664cb7f865c8dee585f79e1bb719474e62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.5 MB (91541454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2930cdbad9c6ce1f9ad486d907986a355f9c6bd07cf48c4eb05ee75bf08d9213`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:06:42 GMT
ADD alpine-minirootfs-3.21.5-riscv64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:06:42 GMT
CMD ["/bin/sh"]
# Mon, 13 Oct 2025 05:23:19 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 13 Oct 2025 05:23:19 GMT
ENV GOTOOLCHAIN=local
# Mon, 13 Oct 2025 05:23:19 GMT
ENV GOPATH=/go
# Mon, 13 Oct 2025 05:23:19 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 13 Oct 2025 05:23:19 GMT
COPY /target/ / # buildkit
# Mon, 13 Oct 2025 05:23:19 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 13 Oct 2025 05:23:19 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:f874295bfcd01a87ee99265d45f0786d35242cd9d53bc2744cb330bf3be277f5`  
		Last Modified: Wed, 08 Oct 2025 21:19:05 GMT  
		Size: 3.4 MB (3351001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:611661040751365eafd7f1dfe7a29755674f06b893fdaa0640152a38b160d0dc`  
		Last Modified: Fri, 10 Oct 2025 21:10:14 GMT  
		Size: 291.5 KB (291463 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c2d5d7683a75ce062ee755840019c59bf7ca74ff155b360004efb2f79df7164`  
		Last Modified: Wed, 15 Oct 2025 23:27:21 GMT  
		Size: 87.9 MB (87898833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20047a80afc3f1428c102e7aa3954512498786e69806c60f64c67a81856715d0`  
		Last Modified: Thu, 16 Oct 2025 00:38:12 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.21` - unknown; unknown

```console
$ docker pull golang@sha256:1733ecedaad75ba6b006a41a53b19112a0299b633bdddea6898abddf2dfb0352
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **216.8 KB (216842 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90d33ebb99627a4286068098a0697767e2ec295f96b045a6368086a406ee7aa7`

```dockerfile
```

-	Layers:
	-	`sha256:cd748a15331eed5c5e87de390fd3ec1b9a9d58131d4f8353318776e944327aba`  
		Last Modified: Thu, 16 Oct 2025 02:23:39 GMT  
		Size: 192.3 KB (192288 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9103dcd2219baa296d4396e8139619782710732449066ddb3b3b50654d551d5b`  
		Last Modified: Thu, 16 Oct 2025 02:23:39 GMT  
		Size: 24.6 KB (24554 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.21` - linux; s390x

```console
$ docker pull golang@sha256:593980f8c0cf8e25c8eb77090fbd1beab960f49552337a0264066be35a51fb1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.6 MB (92550883 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:154cd86d759fc4ab0191811889423a59c71e2f16f9f189eb94f7804eb6008c1e`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:06:42 GMT
ADD alpine-minirootfs-3.21.5-s390x.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:06:42 GMT
CMD ["/bin/sh"]
# Mon, 13 Oct 2025 05:23:19 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 13 Oct 2025 05:23:19 GMT
ENV GOTOOLCHAIN=local
# Mon, 13 Oct 2025 05:23:19 GMT
ENV GOPATH=/go
# Mon, 13 Oct 2025 05:23:19 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 13 Oct 2025 05:23:19 GMT
COPY /target/ / # buildkit
# Mon, 13 Oct 2025 05:23:19 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 13 Oct 2025 05:23:19 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:9f2ceebb28b6c8480d6ae26501eda06bf0b6029f7c797c80673b95a60276e050`  
		Last Modified: Wed, 08 Oct 2025 16:25:19 GMT  
		Size: 3.5 MB (3466434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3cc4c05838d57ecfe671b31e7400d015d24d81c7ce717be366103b575ebe388`  
		Last Modified: Thu, 09 Oct 2025 07:53:30 GMT  
		Size: 292.1 KB (292099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9327917e2dddfe4111d470e54a510bc92320cf661a5e14b0ac90c62acacad6e`  
		Last Modified: Mon, 13 Oct 2025 18:22:35 GMT  
		Size: 88.8 MB (88792191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0084a4776fd0501b025a217db6c3d016626527946dcd9f9d3ed25b8e77f7cf17`  
		Last Modified: Mon, 13 Oct 2025 18:28:37 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.21` - unknown; unknown

```console
$ docker pull golang@sha256:4ed9adefa51ff47d8b01616ecb3b7a80d63210b281a02e43e272a3491aa056a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **216.8 KB (216762 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7fec5bb2f6553cee92e9d552adc1627186c04307791d4ee9f9acf9489bd8db4c`

```dockerfile
```

-	Layers:
	-	`sha256:32c507f739c8493412ce9b4d7fdfb02c6b3398fe67f21828bb3cf1ff70db8d47`  
		Last Modified: Tue, 14 Oct 2025 02:25:01 GMT  
		Size: 192.3 KB (192254 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:81307eeaa4eafc86fe7ce735a50eb3c43606db0698df2864031d36e19de8e173`  
		Last Modified: Tue, 14 Oct 2025 02:25:02 GMT  
		Size: 24.5 KB (24508 bytes)  
		MIME: application/vnd.in-toto+json
