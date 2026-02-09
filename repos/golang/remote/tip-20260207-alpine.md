## `golang:tip-20260207-alpine`

```console
$ docker pull golang@sha256:5a3ab1b3b6d52b79665171a335b29b9e14e6105d07b17691bd91be8cb26932a2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 14
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
	-	linux; s390x
	-	unknown; unknown

### `golang:tip-20260207-alpine` - linux; amd64

```console
$ docker pull golang@sha256:444c3bc400a41b74a9d9c8263b61836a8411412df3b84605a555f86b5273aa48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.6 MB (97620088 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f56afb2770918e130368051af7d1f46aed4711378e8f2b9e74dbdadc42f2e81`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Mon, 09 Feb 2026 20:01:38 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 09 Feb 2026 20:03:27 GMT
ENV GOTOOLCHAIN=local
# Mon, 09 Feb 2026 20:03:27 GMT
ENV GOPATH=/go
# Mon, 09 Feb 2026 20:03:27 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Feb 2026 20:03:27 GMT
COPY /target/ / # buildkit
# Mon, 09 Feb 2026 20:03:29 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 09 Feb 2026 20:03:29 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15680eb92a1cb3b11515684048c41208bda232efe1b30572940ffba139cffacf`  
		Last Modified: Mon, 09 Feb 2026 20:03:43 GMT  
		Size: 296.1 KB (296092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e72ac0d50002cbee1e950896b157d609a44688d9a2715460c4e3c92d9a126868`  
		Last Modified: Mon, 09 Feb 2026 20:03:44 GMT  
		Size: 93.5 MB (93462017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b8851ad447646491f8bdf177c504eb9cf9f7fed22219bb80245af458d33cfe6`  
		Last Modified: Mon, 09 Feb 2026 20:03:43 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20260207-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:7acfbc58b4e0eda4235207a520fdcbecfe8dbbd8e980ad8c08cae7ad0ab4a220
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.7 KB (220695 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:875a22af54d02dcab58a17cca19f1464a440dcd9dd2f2be0098fe1839d47164e`

```dockerfile
```

-	Layers:
	-	`sha256:6323c44f6b20eae94405e3612440020d88b7256393a760ff0878ea8d0bc760c9`  
		Last Modified: Mon, 09 Feb 2026 20:03:43 GMT  
		Size: 195.6 KB (195601 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a433789ad2ea16bf8bce688d02afd8d91e2039f69827bdaf85b63b164a012b44`  
		Last Modified: Mon, 09 Feb 2026 20:03:43 GMT  
		Size: 25.1 KB (25094 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20260207-alpine` - linux; arm variant v6

```console
$ docker pull golang@sha256:a313db9435346198081d89a8069115d5c6f706d85f14a394f5558bfeb1924a25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.7 MB (93718459 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9900bd951c6925dfe3e3d29ef04128092457f0238a875dfe8e4fd9589d2af840`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:52 GMT
ADD alpine-minirootfs-3.23.3-armhf.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:52 GMT
CMD ["/bin/sh"]
# Mon, 09 Feb 2026 19:56:48 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 09 Feb 2026 19:59:35 GMT
ENV GOTOOLCHAIN=local
# Mon, 09 Feb 2026 19:59:35 GMT
ENV GOPATH=/go
# Mon, 09 Feb 2026 19:59:35 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Feb 2026 19:59:35 GMT
COPY /target/ / # buildkit
# Mon, 09 Feb 2026 19:59:38 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 09 Feb 2026 19:59:38 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:f067a9ad7b3a4e3b687105344f6ad0934a0623c4359c2d841a3d4fab27e26060`  
		Last Modified: Wed, 28 Jan 2026 01:17:56 GMT  
		Size: 3.6 MB (3569821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a108c6609f831847f3df82365ef5c075c5a5a9e2b2ef5a99a08ca43720da073d`  
		Last Modified: Mon, 09 Feb 2026 19:59:50 GMT  
		Size: 297.2 KB (297248 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6550e9c000ea8b3f9a2561021188c21d75815b2a08b1c46ce9ef5f7806416b1`  
		Last Modified: Mon, 09 Feb 2026 19:59:57 GMT  
		Size: 89.9 MB (89851231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85ffa0c589ca530ee3394dafa75d7457f422592f8960f354580c20688a932cfb`  
		Last Modified: Mon, 09 Feb 2026 19:59:50 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20260207-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:72e3f4f12308df99a8be36aa7c3d61e01b7192e8c769f1aebab4837625cf2407
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.0 KB (25008 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9045deef7798b3b35cf095a28e137dca7523edb7c325e460f6572d1a20abea00`

```dockerfile
```

-	Layers:
	-	`sha256:564ea7e8c6934e70b7e9e305370d253c3c8c44fec08a28e40c40ca574b10f99a`  
		Last Modified: Mon, 09 Feb 2026 19:59:49 GMT  
		Size: 25.0 KB (25008 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20260207-alpine` - linux; arm variant v7

```console
$ docker pull golang@sha256:b1adc03a8ea38a3180607706e444d8b76c3b6fc92c1bc04358097171184aedfb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.2 MB (93161753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc811cb5eb3b7803e88e20ea5f7f4540e1f71d513a496b9b717db6efbbccb33a`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:44 GMT
ADD alpine-minirootfs-3.23.3-armv7.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:44 GMT
CMD ["/bin/sh"]
# Mon, 09 Feb 2026 19:56:51 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 09 Feb 2026 19:59:34 GMT
ENV GOTOOLCHAIN=local
# Mon, 09 Feb 2026 19:59:34 GMT
ENV GOPATH=/go
# Mon, 09 Feb 2026 19:59:34 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Feb 2026 19:59:34 GMT
COPY /target/ / # buildkit
# Mon, 09 Feb 2026 19:59:37 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 09 Feb 2026 19:59:37 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:7ed661450d9b41ba25f81f6ef8649bb379f47471d21c4898a8a6a3e11b819220`  
		Last Modified: Wed, 28 Jan 2026 01:18:50 GMT  
		Size: 3.3 MB (3281724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32ac6f6516422665ecee90bf59a12726fcf031eed6fd9432c84592481ab49fe8`  
		Last Modified: Mon, 09 Feb 2026 19:59:51 GMT  
		Size: 296.2 KB (296200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b60c394ecd04fc3ba572f8a2c09a22e7e8c913f51a7766b230d8afa0ed0ae01`  
		Last Modified: Mon, 09 Feb 2026 19:59:07 GMT  
		Size: 89.6 MB (89583671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a0928684d23c9ac4b421ac3bf92579580b6b289f70d82913320c859d2f17532`  
		Last Modified: Mon, 09 Feb 2026 19:59:51 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20260207-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:689acf8e518b4cbcde20397171f23adbdba5e1b485329ec0c481cfe743e40ce9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.2 KB (220193 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:745ba0a3cc15cd4c080d915f9eae38b9013d944d0f795a4e2c05a784b4db8de8`

```dockerfile
```

-	Layers:
	-	`sha256:d5b51c43171d60d645b6fe7de020e451bc81b9b4e4e2483efd86270bdc88ced9`  
		Last Modified: Mon, 09 Feb 2026 19:59:51 GMT  
		Size: 195.0 KB (194971 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:636a37cd6446df398c84ed1b7aa5433a6190a25615677033e2dfa81148127cae`  
		Last Modified: Mon, 09 Feb 2026 19:59:51 GMT  
		Size: 25.2 KB (25222 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20260207-alpine` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:d2a039f296911dafae84e3395d0ed9204acc09d3c1e80a104f8762d716d2ff7f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.0 MB (92970199 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:086acd76ae8597ae657b3a2800940e832412ba17c0dc4b7038cdf6ae0c1360a9`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Mon, 09 Feb 2026 20:01:05 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 09 Feb 2026 20:02:51 GMT
ENV GOTOOLCHAIN=local
# Mon, 09 Feb 2026 20:02:51 GMT
ENV GOPATH=/go
# Mon, 09 Feb 2026 20:02:51 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Feb 2026 20:02:51 GMT
COPY /target/ / # buildkit
# Mon, 09 Feb 2026 20:02:53 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 09 Feb 2026 20:02:53 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d12d14a7231e1992e58ac8bcfba32a07498809089e7169a2c8fd23aa7ca37ac`  
		Last Modified: Mon, 09 Feb 2026 20:03:08 GMT  
		Size: 298.8 KB (298831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:700ae6b9569c22fdb680312e3253454dffff750989d3faaa4cebeb6c55de9593`  
		Last Modified: Mon, 09 Feb 2026 20:03:10 GMT  
		Size: 88.5 MB (88474120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:586c8c485d4fac493a4f33d71e1d3345e85f0d2312a09462e202221ff4f33817`  
		Last Modified: Mon, 09 Feb 2026 20:03:08 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20260207-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:f866615c315b5899304d09147bd9bbd63b9f9ca7c879b8c496a9a2aa503f25ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.3 KB (220262 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e67bd7ffb629c476caf287ecadc5ad0785a547a645e6b0b3df3bf546a6a05024`

```dockerfile
```

-	Layers:
	-	`sha256:3b69449c7093271bffdf7bc91d658d45243980ba3f1a52c4ac4cb6a398ad2245`  
		Last Modified: Mon, 09 Feb 2026 20:03:08 GMT  
		Size: 195.0 KB (195007 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:49a223310caf4c5aa971e9ba64585c22ef9597db2101e39c491432aa8784a0c2`  
		Last Modified: Mon, 09 Feb 2026 20:03:08 GMT  
		Size: 25.3 KB (25255 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20260207-alpine` - linux; 386

```console
$ docker pull golang@sha256:31543a46586c0c8340fe043d39af7b3b8e1abd8fbcb5f06f9819d55d8517e0d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.5 MB (95503075 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f90c91b514bfa0354364f9fc0c632662785a80b1366e9a1c3dcdf1d731214dc`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:11 GMT
ADD alpine-minirootfs-3.23.3-x86.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:11 GMT
CMD ["/bin/sh"]
# Mon, 09 Feb 2026 19:58:13 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 09 Feb 2026 20:00:24 GMT
ENV GOTOOLCHAIN=local
# Mon, 09 Feb 2026 20:00:24 GMT
ENV GOPATH=/go
# Mon, 09 Feb 2026 20:00:24 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Feb 2026 20:00:24 GMT
COPY /target/ / # buildkit
# Mon, 09 Feb 2026 20:00:26 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 09 Feb 2026 20:00:26 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:18bdec7eea78464ecf9b88f4ec630eaeb694ea1c0101ecd9c20eda20c9065e23`  
		Last Modified: Wed, 28 Jan 2026 01:18:16 GMT  
		Size: 3.7 MB (3686998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f82712a47aaa93210d10709619098702b761995161926835e8dfb271282ddcb4`  
		Last Modified: Mon, 09 Feb 2026 20:00:41 GMT  
		Size: 296.7 KB (296670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe9eeab623b500684be7941586d4f5950cd5be2f0139f940b2104a8b3b5d40cc`  
		Last Modified: Mon, 09 Feb 2026 19:58:40 GMT  
		Size: 91.5 MB (91519249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:beb7bdc895895261c83907ac020543dccfb9f1e6023dd0bce91335c065ab1392`  
		Last Modified: Mon, 09 Feb 2026 20:00:42 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20260207-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:705c2d6cdaf7d9d5dfacb55e1e14dc588086e0e9f9ec9e9d514c8424fe29b6cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.6 KB (220611 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c02fd652f5f84f66e8c4944ff74d0f941b02468b30ec68c494d21f65445549c`

```dockerfile
```

-	Layers:
	-	`sha256:28483d7773ff00426490ca4db7a4f2a4c85a88e47986cf4008181338fdb7c67a`  
		Last Modified: Mon, 09 Feb 2026 20:00:41 GMT  
		Size: 195.6 KB (195560 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:27c357d2875aa596bba95cc165832980166a10cad0e1c8dadf12b2d88d76cc25`  
		Last Modified: Mon, 09 Feb 2026 20:00:41 GMT  
		Size: 25.1 KB (25051 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20260207-alpine` - linux; ppc64le

```console
$ docker pull golang@sha256:af29af7e6b9b95f09576623783e0a4ff6b7db4eb1e5752a4a9788ea70131777c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.2 MB (94235807 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8296bb08b747239dce7e81c545ee04bedfa00e9d78b334b913b06182125c5c5`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:01 GMT
ADD alpine-minirootfs-3.23.3-ppc64le.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:01 GMT
CMD ["/bin/sh"]
# Mon, 09 Feb 2026 20:32:44 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 09 Feb 2026 20:26:29 GMT
ENV GOTOOLCHAIN=local
# Mon, 09 Feb 2026 20:26:29 GMT
ENV GOPATH=/go
# Mon, 09 Feb 2026 20:26:29 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Feb 2026 20:26:29 GMT
COPY /target/ / # buildkit
# Mon, 09 Feb 2026 20:32:49 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 09 Feb 2026 20:32:49 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:532f7d227cfd697fe6a6f7bfe8c0cc7baa9d99d3d41d50d9b6394fdb6322f4aa`  
		Last Modified: Wed, 28 Jan 2026 01:17:23 GMT  
		Size: 3.8 MB (3829643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e528c55315b3e5f2f548755f16a234f2386736177558710d4d0c6eaf02151f69`  
		Last Modified: Mon, 09 Feb 2026 20:33:09 GMT  
		Size: 299.3 KB (299264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3f34b281626db46d13e5a751b54221f74b1d0be2bfad3701f6dc696782f8809`  
		Last Modified: Mon, 09 Feb 2026 20:28:07 GMT  
		Size: 90.1 MB (90106742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81f548714377fa99256875d446830994ae9f45eca7d78ce095c40e90b6fbae81`  
		Last Modified: Mon, 09 Feb 2026 20:33:09 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20260207-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:d93fd1270d5c580b273230e9eef78dd5bdc1061985560f8f359417ff146fffa5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.2 KB (220153 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89b2725cfc78c5b0c4e86cbe96ab4e369e607b86a99501b6ef89e507ac385702`

```dockerfile
```

-	Layers:
	-	`sha256:c56e218fe1a462997d663520c47761dbe3dcc36972c52fbd6bad18a5c8ad03c5`  
		Last Modified: Mon, 09 Feb 2026 20:33:09 GMT  
		Size: 195.0 KB (195000 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:53b6f9f1a9d87333ef85761707cb6cc51c835511da4f88b0e5dd123d6c1708c3`  
		Last Modified: Mon, 09 Feb 2026 20:33:10 GMT  
		Size: 25.2 KB (25153 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20260207-alpine` - linux; s390x

```console
$ docker pull golang@sha256:e0865e6c21c9afd32618f394cc7b0bf817adba981d038d8d60eda9b0cd8e9141
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.7 MB (96671555 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:635309e194db06dd2c536cef42a0cb6610621a02bf6c6ea7480aa393cc4f351f`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:06 GMT
ADD alpine-minirootfs-3.23.3-s390x.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:06 GMT
CMD ["/bin/sh"]
# Mon, 09 Feb 2026 20:00:18 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 09 Feb 2026 20:00:01 GMT
ENV GOTOOLCHAIN=local
# Mon, 09 Feb 2026 20:00:01 GMT
ENV GOPATH=/go
# Mon, 09 Feb 2026 20:00:01 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Feb 2026 20:00:01 GMT
COPY /target/ / # buildkit
# Mon, 09 Feb 2026 20:00:20 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 09 Feb 2026 20:00:20 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:623c99520afcb8c68e21bd22d3bc252ae348c276fb9c45a79aeccb4caf2b8d9f`  
		Last Modified: Wed, 28 Jan 2026 01:17:15 GMT  
		Size: 3.7 MB (3725333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96012aea906c12635dfd37f261776f274a7fa57e016424f483ebb57edcd7c898`  
		Last Modified: Mon, 09 Feb 2026 20:00:44 GMT  
		Size: 297.2 KB (297174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23b9ec9ce8a3837e5750bcd10b11df694113758518fac79cbd3aa70f831f2db7`  
		Last Modified: Mon, 09 Feb 2026 20:00:45 GMT  
		Size: 92.6 MB (92648889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:928a20c4af2ceae9d1654a1c94327de80dd1489c96dfca1c082be24d1961164e`  
		Last Modified: Mon, 09 Feb 2026 20:00:46 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20260207-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:81e94bdd7df36493320710f6b9e4cfe71e2dc8fdbccac7be692a7abfe9756888
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.9 KB (219872 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:085d2682a1142ddcede65399edb3ec10d30e9306a53f544dcedc81c226b1dc38`

```dockerfile
```

-	Layers:
	-	`sha256:c0a2bf6a422cec2a7037ac44674a7b598c782798cb3464b10c1be4959ce78748`  
		Last Modified: Mon, 09 Feb 2026 20:00:44 GMT  
		Size: 194.9 KB (194950 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:691c4dc88c0c829ce466631e8eb2ad0b527681ac2ff5b4449abcc014465e1ebb`  
		Last Modified: Mon, 09 Feb 2026 20:00:44 GMT  
		Size: 24.9 KB (24922 bytes)  
		MIME: application/vnd.in-toto+json
