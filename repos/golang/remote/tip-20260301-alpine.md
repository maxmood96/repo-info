## `golang:tip-20260301-alpine`

```console
$ docker pull golang@sha256:7fd9099ec62ccbcb3d3f6de353bbdd0a59e029170be371d9321ccf523a81ad02
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

### `golang:tip-20260301-alpine` - linux; amd64

```console
$ docker pull golang@sha256:6f5993d6e1fa66a080409be95898805f55f162b9778ef590963e3a5c495312cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.8 MB (97761392 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9daa1c23f717c3e3fe7e54e0c6ad6ac2e14d718db8f7c2b1e256e447263144b9`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Mon, 02 Mar 2026 22:02:13 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 02 Mar 2026 22:04:00 GMT
ENV GOTOOLCHAIN=local
# Mon, 02 Mar 2026 22:04:00 GMT
ENV GOPATH=/go
# Mon, 02 Mar 2026 22:04:00 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 02 Mar 2026 22:04:00 GMT
COPY /target/ / # buildkit
# Mon, 02 Mar 2026 22:04:02 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 02 Mar 2026 22:04:02 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:485614ebb5a8525f92bec9a31f4abb4390ff973fa188a368494b980893460ca5`  
		Last Modified: Mon, 02 Mar 2026 22:04:16 GMT  
		Size: 296.1 KB (296067 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:689a8c664b692c42c224e696026ec9ec2afa2556b09a298fb5881d3823f0c6dd`  
		Last Modified: Mon, 02 Mar 2026 22:02:43 GMT  
		Size: 93.6 MB (93603346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f983253bdb1fceb5277c914ed9f945e0b916fb7ac08522cedb693e73a3a0114d`  
		Last Modified: Mon, 02 Mar 2026 22:04:16 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20260301-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:e084947f5cdd6efb1810a30de6ee0858995e3b99876b013ef2aa7ad60a6145c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.7 KB (220696 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9390d45e69496cdec9a97a80e9145acf50851287327138adcdb0fbc7a76f8f56`

```dockerfile
```

-	Layers:
	-	`sha256:4d18156bfbaf5fa761b1c1297efb9d7268b5609a5922e00b573167d153d17c05`  
		Last Modified: Mon, 02 Mar 2026 22:04:17 GMT  
		Size: 195.6 KB (195601 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:07b46a4779b727f986481900dd0c8057393480c824028b7184645b443d920311`  
		Last Modified: Mon, 02 Mar 2026 22:04:17 GMT  
		Size: 25.1 KB (25095 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20260301-alpine` - linux; arm variant v6

```console
$ docker pull golang@sha256:ade4e1706c8606e29e227ad18a64f8226dade74692bd3502f1dfafada839f0a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.8 MB (93837842 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dacf7e6f3244040445e7e863fff944c890bce72d7f23d2676a645ec21605e715`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:52 GMT
ADD alpine-minirootfs-3.23.3-armhf.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:52 GMT
CMD ["/bin/sh"]
# Mon, 02 Mar 2026 22:01:45 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 02 Mar 2026 22:04:37 GMT
ENV GOTOOLCHAIN=local
# Mon, 02 Mar 2026 22:04:37 GMT
ENV GOPATH=/go
# Mon, 02 Mar 2026 22:04:37 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 02 Mar 2026 22:04:37 GMT
COPY /target/ / # buildkit
# Mon, 02 Mar 2026 22:04:40 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 02 Mar 2026 22:04:40 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:f067a9ad7b3a4e3b687105344f6ad0934a0623c4359c2d841a3d4fab27e26060`  
		Last Modified: Wed, 28 Jan 2026 01:17:56 GMT  
		Size: 3.6 MB (3569821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fae5570d8a03ac3adc2e70b5be911f3adc27f24d57be8c5028af1a8ddeff1b2`  
		Last Modified: Mon, 02 Mar 2026 22:04:51 GMT  
		Size: 297.3 KB (297259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3f75482abeb648b9189b3f4696db6444fed715bf37c369ca85b2202c497f7c6`  
		Last Modified: Mon, 02 Mar 2026 22:04:54 GMT  
		Size: 90.0 MB (89970604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d98a1ff156191fa2afa31672d3f5ab3d4af676e3686ddc6577ae4f56fc1169e4`  
		Last Modified: Mon, 02 Mar 2026 22:04:51 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20260301-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:26c019ba9d5ad48ee4b14522497f371db961f227ca9e786d95747629e596be86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.0 KB (25008 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29d626d1d03b63e7a238ec191acadf13984b266476e17dd5fe60940d0277e3c5`

```dockerfile
```

-	Layers:
	-	`sha256:421fe4a6f23d63a826161585c6be65ec089794ccbcfbd1d0bdf51134c3ce1d15`  
		Last Modified: Mon, 02 Mar 2026 22:04:51 GMT  
		Size: 25.0 KB (25008 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20260301-alpine` - linux; arm variant v7

```console
$ docker pull golang@sha256:48b9255253a83a9e5221b4b8f65b64c8d42ac719ffc7cc9ef917b020b2c0fb40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.3 MB (93274731 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8efd30039322b48ed66e5afd6650c4a78a25615593f6287fe92bf1344b0d8c5a`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:44 GMT
ADD alpine-minirootfs-3.23.3-armv7.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:44 GMT
CMD ["/bin/sh"]
# Mon, 02 Mar 2026 22:01:27 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 02 Mar 2026 22:04:14 GMT
ENV GOTOOLCHAIN=local
# Mon, 02 Mar 2026 22:04:14 GMT
ENV GOPATH=/go
# Mon, 02 Mar 2026 22:04:14 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 02 Mar 2026 22:04:14 GMT
COPY /target/ / # buildkit
# Mon, 02 Mar 2026 22:04:17 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 02 Mar 2026 22:04:17 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:7ed661450d9b41ba25f81f6ef8649bb379f47471d21c4898a8a6a3e11b819220`  
		Last Modified: Wed, 28 Jan 2026 01:18:50 GMT  
		Size: 3.3 MB (3281724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17af8d714c0c589a2709199577d3f6d249bebe679632d7a71bd150e04bb9cf32`  
		Last Modified: Mon, 02 Mar 2026 22:04:32 GMT  
		Size: 296.2 KB (296186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75d47f42e49b5b1824f0c700b4d521593aedaa7278226bf8d2c8c937a0110183`  
		Last Modified: Mon, 02 Mar 2026 22:04:34 GMT  
		Size: 89.7 MB (89696663 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7dd442abee36e5454eccc40d266c336f14e09ab7078eb1b98b84b7d67868d4a`  
		Last Modified: Mon, 02 Mar 2026 22:04:32 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20260301-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:a5544b542aa2c4dd80fb352a4e2ec8cbd1e77a38be33ddf873668a8d5cd398ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.2 KB (220194 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72fccacfcd62666fd297952f5787d4a936a5f26524d312b308fb7043a60f79f6`

```dockerfile
```

-	Layers:
	-	`sha256:096b2e96f90878220d95da0c8298195cc22bc7567e2d7fe5823e20caf0e9933a`  
		Last Modified: Mon, 02 Mar 2026 22:04:32 GMT  
		Size: 195.0 KB (194971 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c530c5672bfce42d192521ea9bd481d0a69229338c66c8b0db0438da6f277a85`  
		Last Modified: Mon, 02 Mar 2026 22:04:32 GMT  
		Size: 25.2 KB (25223 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20260301-alpine` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:cfffbaa6ffd773b9fb929dce331ae6792108489b48547e604eaa55de18b0ee57
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.3 MB (93280919 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99979fb9135a40534e6f826a79344692d8ff85beb9b84d252e18bdb15bcd31bc`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Mon, 02 Mar 2026 22:05:22 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 02 Mar 2026 22:07:29 GMT
ENV GOTOOLCHAIN=local
# Mon, 02 Mar 2026 22:07:29 GMT
ENV GOPATH=/go
# Mon, 02 Mar 2026 22:07:29 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 02 Mar 2026 22:07:29 GMT
COPY /target/ / # buildkit
# Mon, 02 Mar 2026 22:07:31 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 02 Mar 2026 22:07:31 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:848488b1fcdd92a322d790a2b3725263067ad279397811e5dfe6a26f636dc250`  
		Last Modified: Mon, 02 Mar 2026 22:07:45 GMT  
		Size: 298.8 KB (298840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e982fdcb72c3ad1cca7a139b473ea3951042395bd4cf7fbdb4f775c24a9b551`  
		Last Modified: Mon, 02 Mar 2026 22:03:07 GMT  
		Size: 88.8 MB (88784830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33e29515d59891c9c47108dd3cccfd7baaf0e51799216075e4b68aded001ac65`  
		Last Modified: Mon, 02 Mar 2026 22:07:45 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20260301-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:61cb6aa00a97ae558edaecf97cced52e7bd297ac9e42357021c365f9304425e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.3 KB (220262 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3bf17ca17fa886e6a1ce5656e0967c8bd901c1de029d69451dc94ebcab68047`

```dockerfile
```

-	Layers:
	-	`sha256:5e0d375025bf74b8e11c96062f9a47c07a58503be3ea4203c29f39102f90b9b9`  
		Last Modified: Mon, 02 Mar 2026 22:07:46 GMT  
		Size: 195.0 KB (195007 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:48964319eca790c0d82d85e306671290b664fe2b1840bf392c1ceac98b5ef4b7`  
		Last Modified: Mon, 02 Mar 2026 22:07:45 GMT  
		Size: 25.3 KB (25255 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20260301-alpine` - linux; 386

```console
$ docker pull golang@sha256:d050612eb2edd6831255c48afa69f20155885925c2a1754b2db3bea168660180
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.4 MB (95432750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebcc4387d17d9d61e1122a4f44e609e9d9caca133e3d3fcb732bd944e09b8829`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:11 GMT
ADD alpine-minirootfs-3.23.3-x86.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:11 GMT
CMD ["/bin/sh"]
# Mon, 02 Mar 2026 22:02:30 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 02 Mar 2026 22:04:27 GMT
ENV GOTOOLCHAIN=local
# Mon, 02 Mar 2026 22:04:27 GMT
ENV GOPATH=/go
# Mon, 02 Mar 2026 22:04:27 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 02 Mar 2026 22:04:27 GMT
COPY /target/ / # buildkit
# Mon, 02 Mar 2026 22:04:29 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 02 Mar 2026 22:04:29 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:18bdec7eea78464ecf9b88f4ec630eaeb694ea1c0101ecd9c20eda20c9065e23`  
		Last Modified: Wed, 28 Jan 2026 01:18:16 GMT  
		Size: 3.7 MB (3686998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7c69ead3e5918521ee26d25517dcf594170f4ecfe52a1017f84fca91e98a308`  
		Last Modified: Mon, 02 Mar 2026 22:04:42 GMT  
		Size: 296.7 KB (296672 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:862b2140e9f06d205b6b5af3fcc14f26b13013365f22129c2ff99cb48ee34776`  
		Last Modified: Mon, 02 Mar 2026 22:04:44 GMT  
		Size: 91.4 MB (91448922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2afb62f7eb54817d1fa981f899537df52c644a0dab1d0253af9042c27e3d55ef`  
		Last Modified: Mon, 02 Mar 2026 22:04:42 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20260301-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:070465f9f268bfabd615c7ea0edc13bd638558d13f5207bd1466ca1adb2b87ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.6 KB (220612 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2dc2aed1f3d12b169517ca0af89b26220124972fc0c93a7e2cc26a00cf54323c`

```dockerfile
```

-	Layers:
	-	`sha256:512018f1812cfcdaa027755f6f0d124c384ad21b747ef7c2f2b93728b8c72749`  
		Last Modified: Mon, 02 Mar 2026 22:04:42 GMT  
		Size: 195.6 KB (195560 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:65df7c7198f1d4b17d4a9dfc4d4debd7bd306fb106e14471e7688c44a5c9a75e`  
		Last Modified: Mon, 02 Mar 2026 22:04:42 GMT  
		Size: 25.1 KB (25052 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20260301-alpine` - linux; ppc64le

```console
$ docker pull golang@sha256:0acea32c30e436fdb460209b21dc7945b0f266f12b86394a6faa3259ae891da8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.4 MB (94444952 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29940a10f867dba312d9eee81d29ad4962aebb8567f768c09dca64e6be50c64a`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:01 GMT
ADD alpine-minirootfs-3.23.3-ppc64le.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:01 GMT
CMD ["/bin/sh"]
# Mon, 02 Mar 2026 22:09:48 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 02 Mar 2026 22:04:07 GMT
ENV GOTOOLCHAIN=local
# Mon, 02 Mar 2026 22:04:07 GMT
ENV GOPATH=/go
# Mon, 02 Mar 2026 22:04:07 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 02 Mar 2026 22:04:07 GMT
COPY /target/ / # buildkit
# Mon, 02 Mar 2026 22:09:52 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 02 Mar 2026 22:09:53 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:532f7d227cfd697fe6a6f7bfe8c0cc7baa9d99d3d41d50d9b6394fdb6322f4aa`  
		Last Modified: Wed, 28 Jan 2026 01:17:23 GMT  
		Size: 3.8 MB (3829643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0cb5fdbb9c11366be51e10e8824e559071421ad10b7e267e74f44b9bd836d8f`  
		Last Modified: Mon, 02 Mar 2026 22:10:16 GMT  
		Size: 299.3 KB (299264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abcc3a57b0d1a4c549275152be846eeab1e4bfda9d363982944775991fe15219`  
		Last Modified: Mon, 02 Mar 2026 22:05:31 GMT  
		Size: 90.3 MB (90315888 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a5afc3b138ef9484393109202b2818e7784b1de3534297a734c85d94081d350`  
		Last Modified: Mon, 02 Mar 2026 22:10:16 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20260301-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:34750f5aa58cad573d1651f5856e318391b81798ee3bd46798cd412f4f72d473
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.0 KB (219980 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f5632ce7c7c2ccc276bd08bf2d69759965b153737982e529c1bdf6ff0389d48`

```dockerfile
```

-	Layers:
	-	`sha256:5b4238acceab13dd70476566e9cab60c16646c24771da4a2ad6f6300e78624b0`  
		Last Modified: Mon, 02 Mar 2026 22:10:16 GMT  
		Size: 195.0 KB (195000 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0c7a2a88979840b1b29cf28fad84160f2198730f2e1f005ff3b7d0326cddf479`  
		Last Modified: Mon, 02 Mar 2026 22:10:16 GMT  
		Size: 25.0 KB (24980 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20260301-alpine` - linux; riscv64

```console
$ docker pull golang@sha256:f0e4a23199a592dd3428ed6c3090ea2d13206430eeb0a698fb5cd3ea1416b5d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.7 MB (94671229 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de09f60e610690098f2063cdbc0376f394627bdd2ca2f67e441469faf7ebd555`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 03:47:28 GMT
ADD alpine-minirootfs-3.23.3-riscv64.tar.gz / # buildkit
# Wed, 28 Jan 2026 03:47:28 GMT
CMD ["/bin/sh"]
# Thu, 29 Jan 2026 19:12:20 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 03 Mar 2026 09:03:40 GMT
ENV GOTOOLCHAIN=local
# Tue, 03 Mar 2026 09:03:40 GMT
ENV GOPATH=/go
# Tue, 03 Mar 2026 09:03:40 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Mar 2026 09:03:40 GMT
COPY /target/ / # buildkit
# Tue, 03 Mar 2026 09:48:55 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 03 Mar 2026 09:48:55 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:9da5d16b2a566416844fd0c62fa81165037aa0b7f154a5c1f58f06412739471c`  
		Last Modified: Wed, 28 Jan 2026 03:48:00 GMT  
		Size: 3.6 MB (3585287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31f6a28a44ff91c18ab295ffef6822bbaccafe002bd1f4a117c179d363e86328`  
		Last Modified: Thu, 29 Jan 2026 19:14:45 GMT  
		Size: 296.5 KB (296505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7550964df09cbec6e16da50f25098e25826ade610bf4557ad9371e12e9ced3d4`  
		Last Modified: Tue, 03 Mar 2026 09:10:27 GMT  
		Size: 90.8 MB (90789282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93f5fe7459f6e5ec96422d64bc34224ea1462997cc7ece5b80198709dfece29e`  
		Last Modified: Tue, 03 Mar 2026 09:50:08 GMT  
		Size: 123.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20260301-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:eeff79b5e51d88271321826a6b9f959674d590f77e6c82e24e1b46c0f33e41ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.1 KB (220149 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:269564b4cc219c29c21cf1c60791f6198340c44cf76f7597fd7bf5cd474212c4`

```dockerfile
```

-	Layers:
	-	`sha256:5da39d6eeff6b6e55f51eadd665d49269e1fc49b60a5c32d2c042e1ffaa6b087`  
		Last Modified: Tue, 03 Mar 2026 09:50:08 GMT  
		Size: 195.0 KB (194996 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8404d855e2bc1325b3d0f28a0fa74e71ecfe6a8a6978c2cc00700c85f9d972c0`  
		Last Modified: Tue, 03 Mar 2026 09:50:08 GMT  
		Size: 25.2 KB (25153 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20260301-alpine` - linux; s390x

```console
$ docker pull golang@sha256:7bce242a48a662fda548f578d26850081da1de457cfd7c4b188d651b80029fd2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.8 MB (96825225 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd07e6d9f7e24d7aaaa2340d2cf4c04db81f9a909514b5e95db680f291b66be5`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:06 GMT
ADD alpine-minirootfs-3.23.3-s390x.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:06 GMT
CMD ["/bin/sh"]
# Mon, 09 Feb 2026 20:00:18 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 02 Mar 2026 22:04:23 GMT
ENV GOTOOLCHAIN=local
# Mon, 02 Mar 2026 22:04:23 GMT
ENV GOPATH=/go
# Mon, 02 Mar 2026 22:04:23 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 02 Mar 2026 22:04:23 GMT
COPY /target/ / # buildkit
# Mon, 02 Mar 2026 22:04:25 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 02 Mar 2026 22:04:25 GMT
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
	-	`sha256:bfb2d3098d11b942b930d9b88ef8d2b13e42c10d7ccd12c5e317467f410cfa58`  
		Last Modified: Mon, 02 Mar 2026 22:04:29 GMT  
		Size: 92.8 MB (92802560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c03b9335d95cac58de30af4485b43f787d240b693c234dbf5e6ab219c90bee0b`  
		Last Modified: Mon, 02 Mar 2026 22:04:41 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20260301-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:643e5274f5789c3acde9246e2121ae36bf6069900baad848e72d98dae5ab7482
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.9 KB (219872 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b1f4f23de9a7f5df954d518e40ee9f5051de2529c236277a7ff8ccd2d77864e`

```dockerfile
```

-	Layers:
	-	`sha256:296aaa761d5b84966388938a6883609ee57fba771fd6e8da10d7a13c437e58f1`  
		Last Modified: Mon, 02 Mar 2026 22:04:50 GMT  
		Size: 194.9 KB (194950 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:36df20d03bfde0ff0e4f94cc3b3294bfea742da35d1dd58b23bb2be1173828b5`  
		Last Modified: Mon, 02 Mar 2026 22:04:50 GMT  
		Size: 24.9 KB (24922 bytes)  
		MIME: application/vnd.in-toto+json
