## `golang:tip-alpine`

```console
$ docker pull golang@sha256:ca3180a610e9cdc7b561b11bf605eef1a511ecc23ceb68d005f7cb8f4d86538a
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

### `golang:tip-alpine` - linux; amd64

```console
$ docker pull golang@sha256:e49cb5607622ed591a5385446e02dde80a150a8e68e1f64b979b203eaff33227
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.7 MB (101693394 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc1f4b477d3ad8274e8aa2617fc94762245b365163ede37055dbfb3724306e4e`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Thu, 07 May 2026 17:43:28 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Thu, 07 May 2026 17:45:19 GMT
ENV GOTOOLCHAIN=local
# Thu, 07 May 2026 17:45:19 GMT
ENV GOPATH=/go
# Thu, 07 May 2026 17:45:19 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 07 May 2026 17:45:19 GMT
COPY /target/ / # buildkit
# Thu, 07 May 2026 17:45:22 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Thu, 07 May 2026 17:45:22 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ada98c097b6244785457a4820d0c6ff3aeb8bfb38e51bbceca4bba3e1fc8e448`  
		Last Modified: Thu, 07 May 2026 17:45:36 GMT  
		Size: 290.2 KB (290238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e32be2e0f5add9aa550a86f2638e1a5bddb598fef09f796f2626b736ae1c11c9`  
		Last Modified: Tue, 05 May 2026 23:04:31 GMT  
		Size: 97.5 MB (97538809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c99e1b92b356e29ecac9571c34c4905b5ff2fdba07c55242d418ca6ef2372fa`  
		Last Modified: Thu, 07 May 2026 17:45:36 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:95087e788140462ad5d501688f38127708e0ba8ff1889a0dd30578bda926de5c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.7 KB (218743 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64822506b97048b37e64ba0c042175b4846f2581850e1d23d5828d5203d136a2`

```dockerfile
```

-	Layers:
	-	`sha256:662636089b3fb15e4ad92cf537647f199087272478bf967d85f5bf447dbdc71f`  
		Last Modified: Thu, 07 May 2026 17:45:36 GMT  
		Size: 193.6 KB (193648 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f630f6d4f5cb4b2b3847530f1c99b061f8ae934ce186ee51d6f0bbbdeb7bde07`  
		Last Modified: Thu, 07 May 2026 17:45:36 GMT  
		Size: 25.1 KB (25095 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine` - linux; arm variant v6

```console
$ docker pull golang@sha256:94ca64a52f2886f63de101b494b9355b047b64583e56ffeab21a251c62c234fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.5 MB (97525169 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d89e2290ff1c84da9dfacbcc0becd31d963f3ac1cefb4a18288665f55f8707f7`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:02:13 GMT
ADD alpine-minirootfs-3.23.4-armhf.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:02:13 GMT
CMD ["/bin/sh"]
# Thu, 07 May 2026 18:09:15 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Thu, 07 May 2026 18:12:16 GMT
ENV GOTOOLCHAIN=local
# Thu, 07 May 2026 18:12:16 GMT
ENV GOPATH=/go
# Thu, 07 May 2026 18:12:16 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 07 May 2026 18:12:16 GMT
COPY /target/ / # buildkit
# Thu, 07 May 2026 18:12:19 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Thu, 07 May 2026 18:12:19 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:c9cf8ef099e6e20ca4c7a2ae5b731a4beff960c0ffb88dd64fd6cdfdfe04839d`  
		Last Modified: Wed, 15 Apr 2026 20:02:17 GMT  
		Size: 3.6 MB (3571863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32b094299be28abdd3e736a40544a315c61dda87d50be16c53de56eddb798855`  
		Last Modified: Thu, 07 May 2026 18:12:31 GMT  
		Size: 291.0 KB (291022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63da960de4dc7ce914df12e6e4e0869a4439909a8959fdba48a5cd0d07b76f40`  
		Last Modified: Tue, 05 May 2026 23:04:58 GMT  
		Size: 93.7 MB (93662126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43872dc020a1959a5443171915c1b446f4d3672c868fc530d0d920471f04d168`  
		Last Modified: Thu, 07 May 2026 18:12:31 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:688f89cb61d47a6d3ec185de572f7eb01868af7ef85e102a2dbd84d88591c64f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.0 KB (25008 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eebcf5f61a48faf54bd7cc2aac154c5f3e52f0b4bfb68a126df29eb1b36e7634`

```dockerfile
```

-	Layers:
	-	`sha256:2e40137f9ebddf3be4e514e1ce196badb08c8efd439b376f605f2fd8182f044d`  
		Last Modified: Thu, 07 May 2026 18:12:31 GMT  
		Size: 25.0 KB (25008 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine` - linux; arm variant v7

```console
$ docker pull golang@sha256:cc8c1277f587898a8bba776522c5288736aca2d14216444adce586ff52622f7e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.0 MB (96952472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3910a390818c250c487787722bffcc55735ab163489447297c322a6b9b8a8d93`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:47 GMT
ADD alpine-minirootfs-3.23.4-armv7.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:47 GMT
CMD ["/bin/sh"]
# Thu, 07 May 2026 18:16:53 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Thu, 07 May 2026 18:19:51 GMT
ENV GOTOOLCHAIN=local
# Thu, 07 May 2026 18:19:51 GMT
ENV GOPATH=/go
# Thu, 07 May 2026 18:19:51 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 07 May 2026 18:19:51 GMT
COPY /target/ / # buildkit
# Thu, 07 May 2026 18:19:54 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Thu, 07 May 2026 18:19:54 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:c160e404c59d6d30c66a0d74bbd17337f178f5d898a9908e18c71ce3bbe28c99`  
		Last Modified: Wed, 15 Apr 2026 20:01:53 GMT  
		Size: 3.3 MB (3283123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cb2038f0ebca967dec70336afb7293a57a4516020010d3a1e02589de6eefff4`  
		Last Modified: Thu, 07 May 2026 18:20:09 GMT  
		Size: 290.2 KB (290161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7124712ceb426f7d5ea56fbdf12ab02ae56c25941c6892b6e8ce38b9f03ee67d`  
		Last Modified: Tue, 05 May 2026 23:09:06 GMT  
		Size: 93.4 MB (93379030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a04accd5d53cbd1296b768a23ead99dd46063b0d1fbea522194898362270a9e`  
		Last Modified: Thu, 07 May 2026 18:20:09 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:968471ff4098738ad59b47103bd0e5d09dc4c724db423252a3badd75db15d17f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.2 KB (218241 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b170ab1cb7d6ecec71c24bb5b51772d0b646e41bd39645ec2ec164802755aff`

```dockerfile
```

-	Layers:
	-	`sha256:b2d6e1685dad4ea47260c48a286390e7aefca182e4eef337cf3bd25a8901a30c`  
		Last Modified: Thu, 07 May 2026 18:20:09 GMT  
		Size: 193.0 KB (193018 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e460e620a04960de29c80feb35c377ca8dbcdc002f0ae4a1e80f493586ca8522`  
		Last Modified: Thu, 07 May 2026 18:20:09 GMT  
		Size: 25.2 KB (25223 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:c1a13ad7025ff4de60755ac99bb943ebdfde0c100c2600a6dd1d1dcf5bad85b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.7 MB (96735244 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d2715e5b77e8e3e3aea6de8d3e11da98559cf941746cabab8ec0794201ac2f0`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:25 GMT
ADD alpine-minirootfs-3.23.4-aarch64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:25 GMT
CMD ["/bin/sh"]
# Thu, 07 May 2026 17:55:26 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Thu, 07 May 2026 17:57:16 GMT
ENV GOTOOLCHAIN=local
# Thu, 07 May 2026 17:57:16 GMT
ENV GOPATH=/go
# Thu, 07 May 2026 17:57:16 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 07 May 2026 17:57:16 GMT
COPY /target/ / # buildkit
# Thu, 07 May 2026 17:57:19 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Thu, 07 May 2026 17:57:19 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:d17f077ada118cc762df373ff803592abf2dfa3ddafaa7381e364dd27a88fca7`  
		Last Modified: Wed, 15 Apr 2026 20:01:32 GMT  
		Size: 4.2 MB (4199870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c702cf311ac0593497cd64601a6694d9d6fd9c7260a76f37f4070c0b3b99e346`  
		Last Modified: Thu, 07 May 2026 17:57:34 GMT  
		Size: 292.9 KB (292854 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e310d7048cbd083a777980fa032397ddcbb87e03b5b4b31ddec2b7fa305c5ce5`  
		Last Modified: Tue, 05 May 2026 23:04:45 GMT  
		Size: 92.2 MB (92242363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13c0eb2d2b473cb5ce7047eb0339c019c4a76b63297e566197f0de73506355b6`  
		Last Modified: Thu, 07 May 2026 17:57:33 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:adc8758fd1774f992c3518647a2e2af10a1a67c842af645351d1738281e82708
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.3 KB (218309 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18066cb62738642aba4823c5c0a576988a14512c3b6ebefdacb420ae0b545dbb`

```dockerfile
```

-	Layers:
	-	`sha256:1906951b1dccbc54e02d0cc46494a2112e2e04a6cf7f0a84bce78d6ac2a95ac9`  
		Last Modified: Thu, 07 May 2026 17:57:34 GMT  
		Size: 193.1 KB (193054 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f5e820153247fe7e8aa686d726f1c8cfa0a51f0806e07355e6683af6591ec349`  
		Last Modified: Thu, 07 May 2026 17:57:34 GMT  
		Size: 25.3 KB (25255 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine` - linux; 386

```console
$ docker pull golang@sha256:58a1bbdb0df34c3bb2957a3d07edd519b024c3cc8867a2670972a2fccb55e806
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.3 MB (99261068 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8880622a8fee11a492e327177861af9c541ef49b1234abd60f2313fa59ffff09`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 15 Apr 2026 21:33:20 GMT
ADD alpine-minirootfs-3.23.4-x86.tar.gz / # buildkit
# Wed, 15 Apr 2026 21:33:20 GMT
CMD ["/bin/sh"]
# Thu, 07 May 2026 17:41:51 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Thu, 07 May 2026 17:44:06 GMT
ENV GOTOOLCHAIN=local
# Thu, 07 May 2026 17:44:06 GMT
ENV GOPATH=/go
# Thu, 07 May 2026 17:44:06 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 07 May 2026 17:44:06 GMT
COPY /target/ / # buildkit
# Thu, 07 May 2026 17:44:08 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Thu, 07 May 2026 17:44:09 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:1cf9b6fc5889fdc0b6b22dd2afeea78c7c7985e06a8208c77dc71888bcf17f12`  
		Last Modified: Wed, 15 Apr 2026 21:33:25 GMT  
		Size: 3.7 MB (3690446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49f4d853c9aca2c5a115515b8534abfdf613463558ad55cb01eae36624496416`  
		Last Modified: Thu, 07 May 2026 17:44:22 GMT  
		Size: 290.6 KB (290635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:044b12f480be5869cc9862686abcdcfb3464484b704815a3a70c6077d05037bb`  
		Last Modified: Tue, 05 May 2026 23:01:30 GMT  
		Size: 95.3 MB (95279830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7156dd1b5c694064bb291af4ddfc950b0cec9b347407b964dff8564e0effb6c`  
		Last Modified: Thu, 07 May 2026 17:44:22 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:69bf8ae369352bf4e51e93f858c6a4d84f7de976ea08b3375d415a457e9a6804
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.7 KB (218659 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4552ff2668e0014c86ff0f0ada27534eabc028524c613982e7c1755553682dc0`

```dockerfile
```

-	Layers:
	-	`sha256:a9f820482b0512efe7cc613703a01f925394b26fe1276cdc745b6a828bb04148`  
		Last Modified: Thu, 07 May 2026 17:44:22 GMT  
		Size: 193.6 KB (193607 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:24b487f3a8bc39635b2b8889ad6520bf9bdc8d690e3d9f32fef3ff874cf72d37`  
		Last Modified: Thu, 07 May 2026 17:44:22 GMT  
		Size: 25.1 KB (25052 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine` - linux; ppc64le

```console
$ docker pull golang@sha256:484f1a36371ea59bdb6427972cad9188937fc442413858ffab99fdbc697dde8d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.3 MB (98253128 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e15f2724dbe418fcd3ad5b0ff4e6612bb8000761693b55a1a6558aa04aeef334`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:00:31 GMT
ADD alpine-minirootfs-3.23.4-ppc64le.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:00:31 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 21:07:27 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 05 May 2026 23:40:06 GMT
ENV GOTOOLCHAIN=local
# Tue, 05 May 2026 23:40:06 GMT
ENV GOPATH=/go
# Tue, 05 May 2026 23:40:06 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 May 2026 23:40:06 GMT
COPY /target/ / # buildkit
# Tue, 05 May 2026 23:45:31 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 05 May 2026 23:45:32 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:f14c55dbf69723970b011b8f4e3d231f8c307d6db3c80dafa55949ab7d3ea6d2`  
		Last Modified: Wed, 15 Apr 2026 20:00:46 GMT  
		Size: 3.8 MB (3830929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b7ccd49384e7556733dfe66ba3c21432bf16a2524fd3822010b69719728c426`  
		Last Modified: Wed, 15 Apr 2026 21:07:48 GMT  
		Size: 293.4 KB (293365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df66d548befa9f03e6fb22cc6385677d9c13ab71d11ae10a9cbc0d2e3d0efc16`  
		Last Modified: Tue, 05 May 2026 23:41:42 GMT  
		Size: 94.1 MB (94128677 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:894b6c3f959c1e1b9aa7c63f88fde53d04f37f9f02c93c51254f8b556b82efbf`  
		Last Modified: Tue, 05 May 2026 23:45:50 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:77b4de094993cc305c0c602c56507572fc84e5b9e49f72c650be0b4ab55b6964
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.2 KB (218200 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02600e98a72aabbfcdee0b306143ff374c629aa4df1c5affdae6dddb04023647`

```dockerfile
```

-	Layers:
	-	`sha256:bae13537c04d4688dc316bfe671fcc957fdf3f5d2f675333d85caea63ad2e449`  
		Last Modified: Tue, 05 May 2026 23:45:50 GMT  
		Size: 193.0 KB (193047 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9a06c5c24d2733e2c72748ab5dba1ca55d2ed9b20243c373daa72341c4a3b1fb`  
		Last Modified: Tue, 05 May 2026 23:45:50 GMT  
		Size: 25.2 KB (25153 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine` - linux; riscv64

```console
$ docker pull golang@sha256:f50591ceedc17e91202de785bfd0b3da54140572e665120f218c5773fc9acec9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.5 MB (98499805 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5cdda1d83fcc16aaaf6d855f97ff56a8588997568a1147d76260eefdbfbbfa8b`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:30:47 GMT
ADD alpine-minirootfs-3.23.4-riscv64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:30:47 GMT
CMD ["/bin/sh"]
# Thu, 16 Apr 2026 16:18:44 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Wed, 06 May 2026 06:45:06 GMT
ENV GOTOOLCHAIN=local
# Wed, 06 May 2026 06:45:06 GMT
ENV GOPATH=/go
# Wed, 06 May 2026 06:45:06 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 May 2026 06:45:06 GMT
COPY /target/ / # buildkit
# Wed, 06 May 2026 15:37:51 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 06 May 2026 15:37:52 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:352acc3ce0e18a8eecba8cebabbfac8f5d264e89513a883c1566d91d15491462`  
		Last Modified: Wed, 15 Apr 2026 20:31:19 GMT  
		Size: 3.6 MB (3587662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a3257359d78e33ee12c186b4248dac6627cb8e26d6fd747ad8f46ed2b4fb8e1`  
		Last Modified: Thu, 16 Apr 2026 16:19:53 GMT  
		Size: 290.6 KB (290553 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d3d77dd072bbe9d4ad01204d701c796e83867bd2e370f7f50879f12652b55ef`  
		Last Modified: Wed, 06 May 2026 06:52:06 GMT  
		Size: 94.6 MB (94621433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d2685a543d8e19f4540f989404f33eaff795aa991d2490bb9efb7ad43c0478f`  
		Last Modified: Wed, 06 May 2026 15:39:09 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:d79f92d7afb6294b9f8a097036c4af8d86c5664bf492b708264475ec0381c94b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **217.4 KB (217401 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:621e2b238e50a1b037158b0e0b2fd4983675600fc8825ae4ec93fb464c040ffc`

```dockerfile
```

-	Layers:
	-	`sha256:a94f66683a915508fc85b8c815a4cf11e67d687bc6cd3c8ec60bfbb207f9c1fe`  
		Last Modified: Wed, 06 May 2026 15:39:09 GMT  
		Size: 193.0 KB (193043 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9ef7f69a2261aa357441a25f3951cf3d1a9e47ee6c14b4a58eda44b59bc2bcf8`  
		Last Modified: Wed, 06 May 2026 15:39:09 GMT  
		Size: 24.4 KB (24358 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine` - linux; s390x

```console
$ docker pull golang@sha256:3943b227636ce29e265ade5de746cc282b11a90100c0be2db2414211d2206d74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **100.1 MB (100123430 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:606f2d9899d192940f768435bf7fd6a298e80589021b4a9e550fd4b527bab82c`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:00:34 GMT
ADD alpine-minirootfs-3.23.4-s390x.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:00:34 GMT
CMD ["/bin/sh"]
# Mon, 04 May 2026 19:09:07 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 05 May 2026 23:58:52 GMT
ENV GOTOOLCHAIN=local
# Tue, 05 May 2026 23:58:52 GMT
ENV GOPATH=/go
# Tue, 05 May 2026 23:58:52 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 May 2026 23:58:52 GMT
COPY /target/ / # buildkit
# Wed, 06 May 2026 00:02:25 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 06 May 2026 00:02:26 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:13188190f2c53fa4e825ed24ee94f77177787a7ddde7687d5fadb7431f136a37`  
		Last Modified: Wed, 15 Apr 2026 20:00:44 GMT  
		Size: 3.7 MB (3726532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67bb85227a6d474422f642a20f11c0f9c523b2abb74d9032c4b7170dedd36bf4`  
		Last Modified: Mon, 04 May 2026 19:09:22 GMT  
		Size: 291.1 KB (291150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d2604867f1d33ea36e2647b9da201fb796e01f541d58d01f7899b6b2cfc20d4`  
		Last Modified: Wed, 06 May 2026 00:00:26 GMT  
		Size: 96.1 MB (96105590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:408687b1ac63739dd51dd03d8ab863924e6486ee0257b1cff6b296fec41833c9`  
		Last Modified: Wed, 06 May 2026 00:02:50 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:ba13d2c3bbc168de33bd282efba3409533334790a872354e8f9a5d5508a69e02
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.8 KB (218840 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9c6e34286248b9d1ef9d95b18d0bf6d3a642934a7a7fc15784563cf52b01d2b`

```dockerfile
```

-	Layers:
	-	`sha256:88db71d503356143315306011db63eac38e3b8db9d85021c5330d35b722573db`  
		Last Modified: Wed, 06 May 2026 00:02:50 GMT  
		Size: 193.7 KB (193745 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0a4901c9d706c71e92859974edd0a2a46ade27775429518b0173ca55238c130d`  
		Last Modified: Wed, 06 May 2026 00:02:50 GMT  
		Size: 25.1 KB (25095 bytes)  
		MIME: application/vnd.in-toto+json
