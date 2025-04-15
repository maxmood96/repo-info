## `golang:tip-20250413-alpine`

```console
$ docker pull golang@sha256:f9bb4d01d66b1e1e2c8b827543853199443797251d37e0cfbac1677097d880db
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

### `golang:tip-20250413-alpine` - linux; amd64

```console
$ docker pull golang@sha256:879660ec47778b7568ea9a287240a1ad75fdd7c045db2785a8db5ce15aeafa21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.0 MB (130014373 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8894d66f842e32dbf57dba0ec60791ddf08cf5caf3e1428bb5c5c5ad04761a3`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Mon, 14 Apr 2025 05:23:20 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 14 Apr 2025 05:23:20 GMT
ENV GOTOOLCHAIN=local
# Mon, 14 Apr 2025 05:23:20 GMT
ENV GOPATH=/go
# Mon, 14 Apr 2025 05:23:20 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 14 Apr 2025 05:23:20 GMT
COPY /target/ / # buildkit
# Mon, 14 Apr 2025 05:23:20 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 14 Apr 2025 05:23:20 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 12:05:35 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58644e3cde527c27f9a962c71e1d97662d217fb89d7e8f560c003187e290d315`  
		Last Modified: Mon, 14 Apr 2025 21:51:13 GMT  
		Size: 294.9 KB (294893 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:013504ab5187d636f1901fcb4a6eeb2b2ad7ca1cea03792606973678944bf0e4`  
		Last Modified: Mon, 14 Apr 2025 21:51:15 GMT  
		Size: 126.1 MB (126077078 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa82bd5311d1a511adedf74731a6762273c854b167e515ff8824cb87803f6292`  
		Last Modified: Mon, 14 Apr 2025 21:51:13 GMT  
		Size: 123.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20250413-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:5d06abd22c98ad54cfcbe7ebdd62e300a234381388c1ed1e342150d95eceb45f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.9 KB (236940 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87710bd95751025a0d71ac8516c41ce86543d331ff460733e3492df92973317f`

```dockerfile
```

-	Layers:
	-	`sha256:3bc6016a37b2c385c53d8c10d978d10f715e2785e0de1c1bcc57cc4e18f3a629`  
		Last Modified: Mon, 14 Apr 2025 21:51:13 GMT  
		Size: 211.8 KB (211799 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c4e03c414f45effbdf164354197917885a7e2fe6696523584105e69c5a8685cf`  
		Last Modified: Mon, 14 Apr 2025 21:51:13 GMT  
		Size: 25.1 KB (25141 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20250413-alpine` - linux; arm variant v6

```console
$ docker pull golang@sha256:456457729a4f7139d57f888599271a5f35f0c7b76b63d102c76a75400479fe03
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.1 MB (125109608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93d9199d22e90545cffb54f05f1df17beb6c7ad859456d5040f23e8576a988d3`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armhf.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Mon, 14 Apr 2025 05:23:20 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 14 Apr 2025 05:23:20 GMT
ENV GOTOOLCHAIN=local
# Mon, 14 Apr 2025 05:23:20 GMT
ENV GOPATH=/go
# Mon, 14 Apr 2025 05:23:20 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 14 Apr 2025 05:23:20 GMT
COPY /target/ / # buildkit
# Mon, 14 Apr 2025 05:23:20 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 14 Apr 2025 05:23:20 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:76099982f06682e28a60c3b774ef20931d07b0a2f551203484e633d8c0361ee7`  
		Last Modified: Fri, 14 Feb 2025 18:28:03 GMT  
		Size: 3.4 MB (3364731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e200e7ad5e2f13ee1ee5c295f12b94fa96417ce036e2a8026a7db4231fdba9a2`  
		Last Modified: Fri, 14 Feb 2025 22:09:20 GMT  
		Size: 296.3 KB (296252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7cffecbc4190b385d992c43c7b7bf1ec5302a806b008514d4f342fbde55db8c`  
		Last Modified: Mon, 14 Apr 2025 21:51:36 GMT  
		Size: 121.4 MB (121448468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54a5fd9fd8623b4e0ed54804499cc51f60d9af3d36714ee038ff8e6c802ca766`  
		Last Modified: Mon, 14 Apr 2025 21:51:32 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20250413-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:5360e64ab0af9559f2814173f0fc768a84545c38564a4a71e4c808d367132db6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.1 KB (25051 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:556abbe686cc4e0510fe9c090eba81f0530a47e7d12c5a402b3c438fbb411dce`

```dockerfile
```

-	Layers:
	-	`sha256:9fe032a2eb09ed03cbd99d2f9978aee439c546df52cd8a9dc3b7616a53a166d9`  
		Last Modified: Mon, 14 Apr 2025 21:51:32 GMT  
		Size: 25.1 KB (25051 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20250413-alpine` - linux; arm variant v7

```console
$ docker pull golang@sha256:36d9bd9487f543375da205a3c05c5f8c843567586abbddce45b4ade2ea20d0a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.5 MB (124501557 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:237910b6a3ed35b55d6f63eaaeb4d3b30f54ec4bed9d04bcec0e6764533b3e1a`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armv7.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Mon, 14 Apr 2025 05:23:20 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 14 Apr 2025 05:23:20 GMT
ENV GOTOOLCHAIN=local
# Mon, 14 Apr 2025 05:23:20 GMT
ENV GOPATH=/go
# Mon, 14 Apr 2025 05:23:20 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 14 Apr 2025 05:23:20 GMT
COPY /target/ / # buildkit
# Mon, 14 Apr 2025 05:23:20 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 14 Apr 2025 05:23:20 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:85f3b18f9f5a8655db86c6dfb02bb01011ffef63d10a173843c5c65c3e9137b7`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.1 MB (3098123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a77833ee7d3adeaa883db3f960686c769232a931d3442cfcc8bb6a4790098520`  
		Last Modified: Fri, 14 Feb 2025 21:47:46 GMT  
		Size: 295.2 KB (295199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e131e20eff5d97e9796f801f5335249fcb3b27557a67cdb1b0533cbc32974fff`  
		Last Modified: Mon, 14 Apr 2025 21:52:15 GMT  
		Size: 121.1 MB (121108078 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94f2430a647b02853ce03361d84c110b8095b84e1a57608a1bec4e695aafa77a`  
		Last Modified: Mon, 14 Apr 2025 21:59:17 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20250413-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:9c0f3f9d7f76ad26b99ce57c86fcefa68c705c1ef2bd8585d4d67b31c707c47b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **237.1 KB (237061 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:799704823725c65a6d3bb31338f947490f909086fbf5c9cc5be17cd280138c74`

```dockerfile
```

-	Layers:
	-	`sha256:76ac582c753ca968643fe62e5bc1c07eb3586319b3c2484b6e4353ee04655f38`  
		Last Modified: Mon, 14 Apr 2025 21:59:17 GMT  
		Size: 211.8 KB (211795 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9bf494ddc00ae64a18acbeef6dd731aaf3cf606b1f0337867f43ff1d2fb7190f`  
		Last Modified: Mon, 14 Apr 2025 21:59:17 GMT  
		Size: 25.3 KB (25266 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20250413-alpine` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:b2ee71a5a5b8891736f7ce93440e4c8e7a37e90c66501fb46c354ac7006cc6a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.1 MB (123060735 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de51a8468cb2f508631b12a7e930bbd8886cadf1ed68b02ccf8a4452afc7e6b8`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Mon, 14 Apr 2025 05:23:20 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 14 Apr 2025 05:23:20 GMT
ENV GOTOOLCHAIN=local
# Mon, 14 Apr 2025 05:23:20 GMT
ENV GOPATH=/go
# Mon, 14 Apr 2025 05:23:20 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 14 Apr 2025 05:23:20 GMT
COPY /target/ / # buildkit
# Mon, 14 Apr 2025 05:23:20 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 14 Apr 2025 05:23:20 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 12:05:33 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b785d572112487c9c64a58663acce46f9fb0896716bd7f1542c938cc5d7af07`  
		Last Modified: Mon, 14 Apr 2025 21:54:40 GMT  
		Size: 297.9 KB (297860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05b206f4f1851ae209ce8b8172ce5c71a21bf857b5a5fc8341f94dabec27aaed`  
		Last Modified: Mon, 14 Apr 2025 21:49:56 GMT  
		Size: 118.8 MB (118769688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac9bc03d0f58375499ca3031b560566a133650c54ac1d39b9f597c270b19c447`  
		Last Modified: Mon, 14 Apr 2025 21:54:40 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20250413-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:19ba48c6c7386e984e31fd8f81070fa2f5fd745723f4ef9739ab87c466d3563c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **237.2 KB (237157 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac07de6ec3d35c89de39535b349a3109ac7c2110f1b75b2562b2bbefc840f55b`

```dockerfile
```

-	Layers:
	-	`sha256:8c7ed250683d79f9528afa9cf0dd311130f67a46466922982a023424a44eba8b`  
		Last Modified: Mon, 14 Apr 2025 21:54:40 GMT  
		Size: 211.9 KB (211855 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:11c7e7aece0e2e309cd6fc11d349a22f4c9e705ce3850a7ec081c386eea6d65e`  
		Last Modified: Mon, 14 Apr 2025 21:54:39 GMT  
		Size: 25.3 KB (25302 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20250413-alpine` - linux; 386

```console
$ docker pull golang@sha256:8a411760ebb501a157df8342e6ec661b9e646cfd4fea13f634650d006e81130b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.0 MB (128009371 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:358de74a8bc8b47c9c69f84147af687e24113563211904c9fcfde0a345f49368`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Mon, 14 Apr 2025 05:23:20 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 14 Apr 2025 05:23:20 GMT
ENV GOTOOLCHAIN=local
# Mon, 14 Apr 2025 05:23:20 GMT
ENV GOPATH=/go
# Mon, 14 Apr 2025 05:23:20 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 14 Apr 2025 05:23:20 GMT
COPY /target/ / # buildkit
# Mon, 14 Apr 2025 05:23:20 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 14 Apr 2025 05:23:20 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:69aa61ccf55e5bf8e7a069b89e8afb42b4f3443b3785868795af8046d810d608`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.5 MB (3463623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed92faf13c831cc3f0b73ca4b0bdcd95c7ac902591d9127e7490c6673b68cf99`  
		Last Modified: Mon, 14 Apr 2025 21:51:53 GMT  
		Size: 295.6 KB (295587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82a1236535bef233193363d469e87ef11dfa5b282a53e3685fad2f41147bdd6d`  
		Last Modified: Mon, 14 Apr 2025 21:51:51 GMT  
		Size: 124.3 MB (124250003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e62c0809e56c8b3d9079862560e203e1b2416dd1526be2d52e5401fe3532eed`  
		Last Modified: Mon, 14 Apr 2025 21:51:53 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20250413-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:77764e8fb38946595711f73fbf42765ee9987d53a41023e0886bf6aaf75d32ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.8 KB (236833 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38c4b8781d9b0b01a83bd79c7428452522e5b0f8786dd58f820ebb322cabc561`

```dockerfile
```

-	Layers:
	-	`sha256:891aa6009c01cb030882f3e28dfa69a6995701b8ff574ccad7141eac69e2e874`  
		Last Modified: Mon, 14 Apr 2025 21:51:53 GMT  
		Size: 211.7 KB (211734 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a4c2033ec1547ee144e912ef1367fd39aec0b2e2400d3ab9d3de53476c961363`  
		Last Modified: Mon, 14 Apr 2025 21:51:53 GMT  
		Size: 25.1 KB (25099 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20250413-alpine` - linux; ppc64le

```console
$ docker pull golang@sha256:363bb665a353eb87f6ac5a5f1b40792aec26b19f9fa67c70584101daff9208f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.8 MB (124780514 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb206282498107260c383689e63dd01d296ed8d0dd5c37ba2346923ff982010a`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-ppc64le.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Mon, 14 Apr 2025 05:23:20 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 14 Apr 2025 05:23:20 GMT
ENV GOTOOLCHAIN=local
# Mon, 14 Apr 2025 05:23:20 GMT
ENV GOPATH=/go
# Mon, 14 Apr 2025 05:23:20 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 14 Apr 2025 05:23:20 GMT
COPY /target/ / # buildkit
# Mon, 14 Apr 2025 05:23:20 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 14 Apr 2025 05:23:20 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:184b14480d317057da092a0994ad6baf4b2df588108f43969f8fd56f021af2c6`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.6 MB (3574345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c634d4cf55ec6e141d2ba75283fb1b12400db05f7be71416f24292b8f98daec`  
		Last Modified: Mon, 14 Apr 2025 21:55:29 GMT  
		Size: 298.3 KB (298278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9394c4e947a61e9f0edca853e080387bc94a62b435ba7141bd2b21c9acb3149`  
		Last Modified: Mon, 14 Apr 2025 21:52:05 GMT  
		Size: 120.9 MB (120907733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f606731fa71a998944a23d47aee944f96b292363fe910c800599dc7175d49ebd`  
		Last Modified: Mon, 14 Apr 2025 21:55:29 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20250413-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:6e1c81ef877215034dd010cd89884cdfcd8984bc7ae093a20a2f2d5da6bcbd9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.1 KB (235122 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3211ec4566702457e9d18fdc5ca63906d67005cb7c3c3aa2ce09520a5dcd59c7`

```dockerfile
```

-	Layers:
	-	`sha256:98d7985456aa3c533df1e72c472c85cd3705c4a16107184cb7baa0b60f1005ab`  
		Last Modified: Mon, 14 Apr 2025 21:55:29 GMT  
		Size: 209.9 KB (209922 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b4c3a289e7a426905583a114b32be7f2cbeddc6e00d6f94a9d6c39e665372568`  
		Last Modified: Mon, 14 Apr 2025 21:55:29 GMT  
		Size: 25.2 KB (25200 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20250413-alpine` - linux; riscv64

```console
$ docker pull golang@sha256:e976c1afbb2b7801deda34635e7a4a02e8349d4bf1715a62d5549e99f5609e85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.9 MB (124908446 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f588f87fa16867239657460451410f7bb4338633202d64eb52a970ad1d545b3e`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-riscv64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Mon, 14 Apr 2025 05:23:20 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 14 Apr 2025 05:23:20 GMT
ENV GOTOOLCHAIN=local
# Mon, 14 Apr 2025 05:23:20 GMT
ENV GOPATH=/go
# Mon, 14 Apr 2025 05:23:20 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 14 Apr 2025 05:23:20 GMT
COPY /target/ / # buildkit
# Mon, 14 Apr 2025 05:23:20 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 14 Apr 2025 05:23:20 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:7df33f7ad8beb367ac09bdd1b2f220db3ee2bbdda14a6310d1340e5628b5ba88`  
		Last Modified: Fri, 14 Feb 2025 18:56:36 GMT  
		Size: 3.4 MB (3351439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd81befb40433dc7da0b53543acafce5d4aa75d9a2bc5815536bad6b9db1682b`  
		Last Modified: Sun, 16 Feb 2025 05:52:00 GMT  
		Size: 295.3 KB (295346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d0cc7d671cb98f96a9b881e518de5f5b9784e511412b2c2087bc879cb5253c9`  
		Last Modified: Mon, 14 Apr 2025 22:30:40 GMT  
		Size: 121.3 MB (121261504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:428ebc72844d867425e7709c68dcedd17070e7a386604a21dee33e4aae25822f`  
		Last Modified: Mon, 14 Apr 2025 22:30:23 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20250413-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:f12f8d5c6af352e21bcff1b19737982c11c40d988875f7e46d20381b3b78d48c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.1 KB (235118 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9fe8592d0e98e5ad4f037e364cc4435c7141fb01c95f5fe61bbc88f39165ff1`

```dockerfile
```

-	Layers:
	-	`sha256:c6f4ffc6347229baaab6279b1045066ea2dc072aa5d81bdf924aaafb8e56d38e`  
		Last Modified: Mon, 14 Apr 2025 22:30:23 GMT  
		Size: 209.9 KB (209918 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6e814ea46dd50f342e6b2c3224862f3bc9748821ada4fe61eaf186ac56ac2d32`  
		Last Modified: Mon, 14 Apr 2025 22:30:23 GMT  
		Size: 25.2 KB (25200 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20250413-alpine` - linux; s390x

```console
$ docker pull golang@sha256:a19cf3d2680c23140989a64786f08690da8d5e36427f65e7ff7d375e8e77b557
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.1 MB (127094263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11d0dcfe733121c83675fad973a2b0b6bfa928a04cb65aeb4c0e19d5cfa03ece`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-s390x.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Mon, 14 Apr 2025 05:23:20 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 14 Apr 2025 05:23:20 GMT
ENV GOTOOLCHAIN=local
# Mon, 14 Apr 2025 05:23:20 GMT
ENV GOPATH=/go
# Mon, 14 Apr 2025 05:23:20 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 14 Apr 2025 05:23:20 GMT
COPY /target/ / # buildkit
# Mon, 14 Apr 2025 05:23:20 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 14 Apr 2025 05:23:20 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:c1a599607158512214777614f916f8193d29fd34b656d47dfc26314af01e2af4`  
		Last Modified: Fri, 14 Feb 2025 12:05:25 GMT  
		Size: 3.5 MB (3467567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2eef4e818bae24bd18b41ddb9fab07f5996a42edf17784ae06c4953fb5f8fd4a`  
		Last Modified: Mon, 14 Apr 2025 21:55:41 GMT  
		Size: 296.2 KB (296189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b3413729307d44114afade63be5a02a91d2719dffc8bdec785d42f725815b7f`  
		Last Modified: Mon, 14 Apr 2025 21:52:34 GMT  
		Size: 123.3 MB (123330348 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2ca015ef0a7faf8b6c8f6cbf9b82c214d108130c293dece4550a4b44ad88ae6`  
		Last Modified: Mon, 14 Apr 2025 21:55:41 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20250413-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:0ac416673a4cd7dd5860da81e84160b87a9abd81423f52647125a253ec673a2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.0 KB (234990 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4fe064d692ca7dbffc822c3f5146cc42da386661ce0b5f396f65650098c93b1a`

```dockerfile
```

-	Layers:
	-	`sha256:b1aa10a8f74ab6d1ff6c36dc1de80b54b2eb1145467a102db5e29eea4c7a0ce9`  
		Last Modified: Mon, 14 Apr 2025 21:55:41 GMT  
		Size: 209.8 KB (209848 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:775ccb8a27ddc2a95c23489ff63e7950342934c166e365ef7b4a3bbe3e16ed8c`  
		Last Modified: Mon, 14 Apr 2025 21:55:41 GMT  
		Size: 25.1 KB (25142 bytes)  
		MIME: application/vnd.in-toto+json
