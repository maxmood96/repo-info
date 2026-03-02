## `golang:tip-alpine3.23`

```console
$ docker pull golang@sha256:2587436c6d50d83bcbb5497ba1648c67a36ca05d8fdf335aa185d17677a6dca3
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

### `golang:tip-alpine3.23` - linux; amd64

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

### `golang:tip-alpine3.23` - unknown; unknown

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

### `golang:tip-alpine3.23` - linux; arm variant v6

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

### `golang:tip-alpine3.23` - unknown; unknown

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

### `golang:tip-alpine3.23` - linux; arm variant v7

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

### `golang:tip-alpine3.23` - unknown; unknown

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

### `golang:tip-alpine3.23` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:e5e8e59bb6f129048f28f081e26c01502a657967b5701d3a701978e420418f7f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.2 MB (93222940 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aee8be3a29520cbf9bafacef492ff713f28b54629a9706d44054a8c4c0415b42`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Tue, 24 Feb 2026 19:28:09 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 24 Feb 2026 19:29:55 GMT
ENV GOTOOLCHAIN=local
# Tue, 24 Feb 2026 19:29:55 GMT
ENV GOPATH=/go
# Tue, 24 Feb 2026 19:29:55 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 19:29:55 GMT
COPY /target/ / # buildkit
# Tue, 24 Feb 2026 19:29:58 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 24 Feb 2026 19:29:58 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5498aecd4670288fc9e17a473801304e4726e8320b8f97c3f847f4bd3faa1e0`  
		Last Modified: Tue, 24 Feb 2026 19:30:13 GMT  
		Size: 298.8 KB (298842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c991311643d5ba1266ad32d242c21d958ba93238b33b79d32fc0b23bd2b25b23`  
		Last Modified: Tue, 24 Feb 2026 19:30:15 GMT  
		Size: 88.7 MB (88726849 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5000cf4edba94ee1b2fc6705e1633fabbff67d14fa0ae6ae21966899f0e9ffc3`  
		Last Modified: Tue, 24 Feb 2026 19:30:13 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.23` - unknown; unknown

```console
$ docker pull golang@sha256:df90ce6081e335bbee75bd1598de735ed78293ecd2a02667d248f0d1aaea6edb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.3 KB (220262 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7d1c580c4179b90f9514e625fbefdd35696322cb1579f93ce27aa00b3ecbc97`

```dockerfile
```

-	Layers:
	-	`sha256:453513c4173c57f63e57a29f41ce2f369af80348fea653d891237f353359ac2e`  
		Last Modified: Tue, 24 Feb 2026 19:30:13 GMT  
		Size: 195.0 KB (195007 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9222c2ee22b5ccc29a496fb3065a18aec4c2242fa90e076eb63d56a3f54cd361`  
		Last Modified: Tue, 24 Feb 2026 19:30:13 GMT  
		Size: 25.3 KB (25255 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.23` - linux; 386

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

### `golang:tip-alpine3.23` - unknown; unknown

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

### `golang:tip-alpine3.23` - linux; ppc64le

```console
$ docker pull golang@sha256:9e92dc355ed786b1b9eb8d0340a4e2497c94f939537a93a46999e22a3e731b64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.4 MB (94376969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61a5f97504144277aa03e70dda92e347f876a55d9894995491fb96192d9e35a7`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:01 GMT
ADD alpine-minirootfs-3.23.3-ppc64le.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:01 GMT
CMD ["/bin/sh"]
# Mon, 09 Feb 2026 20:32:44 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 24 Feb 2026 21:37:06 GMT
ENV GOTOOLCHAIN=local
# Tue, 24 Feb 2026 21:37:06 GMT
ENV GOPATH=/go
# Tue, 24 Feb 2026 21:37:06 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 21:37:06 GMT
COPY /target/ / # buildkit
# Tue, 24 Feb 2026 21:37:11 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 24 Feb 2026 21:37:12 GMT
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
	-	`sha256:4cf61cfa0cf71c339b4513ee7439845e2a12d7a655ba1ebeafcd94af8061e69a`  
		Last Modified: Tue, 24 Feb 2026 21:37:48 GMT  
		Size: 90.2 MB (90247905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e737c72bff00ac3d03174c6e41026e6eaa61e164258e0611403b5c43f51b15e`  
		Last Modified: Tue, 24 Feb 2026 21:37:46 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.23` - unknown; unknown

```console
$ docker pull golang@sha256:bb520cc01162652a5c2d381d70d5a2d2f8d82b26d74c1cd5a6ae3f5411349ffa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.2 KB (220151 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74b4837b9baf8cb5d4f81751f726623726683ea4e5f36d6aca1da62b2dbb44f4`

```dockerfile
```

-	Layers:
	-	`sha256:d97c6a47a28c9bf4c47fe7abccad7f79f79da4b07b8b48134bc5b6b4456ff780`  
		Last Modified: Tue, 24 Feb 2026 21:37:46 GMT  
		Size: 195.0 KB (195000 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:54875134a50cb26d64d86d5a9a596e6835c17e456e98d480260c40b60f7199fa`  
		Last Modified: Tue, 24 Feb 2026 21:37:46 GMT  
		Size: 25.2 KB (25151 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.23` - linux; riscv64

```console
$ docker pull golang@sha256:b0359915850ee3695cfa55a83f7256cf22b1c601918ffe91d5d24a72c2dba649
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.6 MB (94612154 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38e831cc3b4de8a7b29e039bee06f8058ee261e505fa1671ba0d2e3323d7d7f6`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 03:47:28 GMT
ADD alpine-minirootfs-3.23.3-riscv64.tar.gz / # buildkit
# Wed, 28 Jan 2026 03:47:28 GMT
CMD ["/bin/sh"]
# Thu, 29 Jan 2026 19:12:20 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 24 Feb 2026 19:48:19 GMT
ENV GOTOOLCHAIN=local
# Tue, 24 Feb 2026 19:48:19 GMT
ENV GOPATH=/go
# Tue, 24 Feb 2026 19:48:19 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 19:48:19 GMT
COPY /target/ / # buildkit
# Tue, 24 Feb 2026 19:48:37 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 24 Feb 2026 19:48:37 GMT
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
	-	`sha256:be5c9add62f2c1974f9d8b2a5b72c3c47a21eb3a147c7469bf123bb66cc26173`  
		Last Modified: Tue, 24 Feb 2026 19:51:42 GMT  
		Size: 90.7 MB (90730204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:357079aecf437f5d3915a4a418edf1e779b208e97afa3f56596b72bdf6c2e5ad`  
		Last Modified: Tue, 24 Feb 2026 19:51:29 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.23` - unknown; unknown

```console
$ docker pull golang@sha256:3260fc697ac4027681d01a5530560fc423a96e223795b73d1c885721f5d66f28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.1 KB (220149 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2653dc91057ce19aa5d6c51ca35f3dbf64669a97ad3f3b04c1b7accba35a5666`

```dockerfile
```

-	Layers:
	-	`sha256:d2f428d9055872d9c610516d34423b398e663991bc3a2b45acb9a9dbac2e7a4a`  
		Last Modified: Tue, 24 Feb 2026 19:51:29 GMT  
		Size: 195.0 KB (194996 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1a595c41deccc147200c5e381179bfafe0ff645a4621bb97f6513a00cd40d0e7`  
		Last Modified: Tue, 24 Feb 2026 19:51:29 GMT  
		Size: 25.2 KB (25153 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.23` - linux; s390x

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

### `golang:tip-alpine3.23` - unknown; unknown

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
