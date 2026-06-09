## `golang:tip-alpine3.23`

```console
$ docker pull golang@sha256:5bd142232caaae035d0d7dbdb53f5e39a2539cc09d9d25098fc00a1d44120eec
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
$ docker pull golang@sha256:b6fd78c9c531fb2eaa1f10b8607d4839f57427d5eec2103ed686b354fba7e984
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.2 MB (106206958 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:026de684433ba36ee8698cc0e878414abe6febc76a21fc55859151208458272e`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Mon, 08 Jun 2026 22:44:32 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 08 Jun 2026 22:46:43 GMT
ENV GOTOOLCHAIN=local
# Mon, 08 Jun 2026 22:46:43 GMT
ENV GOPATH=/go
# Mon, 08 Jun 2026 22:46:43 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Jun 2026 22:46:43 GMT
COPY /target/ / # buildkit
# Mon, 08 Jun 2026 22:46:46 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 08 Jun 2026 22:46:46 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68cf46e32d963062f7a1a0f2091b0867c33324d648e73cdc7c2ee8d227630153`  
		Last Modified: Mon, 08 Jun 2026 22:47:01 GMT  
		Size: 290.2 KB (290240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9caf2b5917603f564e8b31c080871596acbc699caf5fd0fec4940c836746ec3`  
		Last Modified: Mon, 08 Jun 2026 22:46:13 GMT  
		Size: 102.1 MB (102052370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4aa4a22577fcdcefcc4a76f21a6294bc495108b20b74ade7d0cade362e5247fb`  
		Last Modified: Mon, 08 Jun 2026 22:47:01 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.23` - unknown; unknown

```console
$ docker pull golang@sha256:0f44b14c888bb69037aff26368bd4f50aa49de77c954edc0a76f557f3495535a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.7 KB (218747 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e136cd31f5306d62a611f4c57f4aaefa0c8278d561c981f0c7a9a9b56c9f5736`

```dockerfile
```

-	Layers:
	-	`sha256:339ec8d287b9ef84a29bede3259ae16c144cb60a9d7a64d7839ebc08c1f2f953`  
		Last Modified: Mon, 08 Jun 2026 22:47:01 GMT  
		Size: 193.6 KB (193648 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4019406211a895bf37112c47bfcd4c1b1265affd51af5728d1d404e411d7b1c0`  
		Last Modified: Mon, 08 Jun 2026 22:47:01 GMT  
		Size: 25.1 KB (25099 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.23` - linux; arm variant v6

```console
$ docker pull golang@sha256:0bf647ddc1081a74e9b8869e78461a40934435cd921661acd2d1a357b9dbc862
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.9 MB (101913413 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75a2ae4f8ac637022a0d8afc7b2f39b880f9c066e2cd26889a018afbc22ffdc2`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:02:13 GMT
ADD alpine-minirootfs-3.23.4-armhf.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:02:13 GMT
CMD ["/bin/sh"]
# Mon, 08 Jun 2026 22:43:49 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 08 Jun 2026 22:46:57 GMT
ENV GOTOOLCHAIN=local
# Mon, 08 Jun 2026 22:46:57 GMT
ENV GOPATH=/go
# Mon, 08 Jun 2026 22:46:57 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Jun 2026 22:46:57 GMT
COPY /target/ / # buildkit
# Mon, 08 Jun 2026 22:47:00 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 08 Jun 2026 22:47:00 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:c9cf8ef099e6e20ca4c7a2ae5b731a4beff960c0ffb88dd64fd6cdfdfe04839d`  
		Last Modified: Wed, 15 Apr 2026 20:02:17 GMT  
		Size: 3.6 MB (3571863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:342ff51eabc62a9f61a28c3179f531ea4d52097c839a3e34c5ec3d45ed3b73ef`  
		Last Modified: Mon, 08 Jun 2026 22:47:12 GMT  
		Size: 291.0 KB (291023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04993cb4ea53eb54b934632859a46a3fda346d78f94e5c8c7587a367646e0cf1`  
		Last Modified: Mon, 08 Jun 2026 22:47:15 GMT  
		Size: 98.1 MB (98050368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e1ae59a9f51a6e7aeedea46277178dbeb3ceddd97ebfaa47442f62c348dce67`  
		Last Modified: Mon, 08 Jun 2026 22:47:12 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.23` - unknown; unknown

```console
$ docker pull golang@sha256:344dd3c78482af42d3f875856089073f6844ea5d610e3b8e220074e938f5e5b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.0 KB (25007 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e2b5ee66e4e2658b68f7af0ab13a8d7b98f7188ffc03631b6699e09cd9114cc`

```dockerfile
```

-	Layers:
	-	`sha256:437a42aad4e4f8492f3bcc29a9f6795a6e82dd5f9eb538a5d17b1716d4f55de2`  
		Last Modified: Mon, 08 Jun 2026 22:47:12 GMT  
		Size: 25.0 KB (25007 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.23` - linux; arm variant v7

```console
$ docker pull golang@sha256:bbea604ef54d13d30b03e82bb4c74b26b7257387a1ec990f9b74a0e01826687c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.3 MB (101308479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bcf3511a191027dd32e38e0c117950caae566ceecdb9fec0a79ba961eed7c72f`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:47 GMT
ADD alpine-minirootfs-3.23.4-armv7.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:47 GMT
CMD ["/bin/sh"]
# Mon, 08 Jun 2026 22:44:59 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 08 Jun 2026 22:48:00 GMT
ENV GOTOOLCHAIN=local
# Mon, 08 Jun 2026 22:48:00 GMT
ENV GOPATH=/go
# Mon, 08 Jun 2026 22:48:00 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Jun 2026 22:48:00 GMT
COPY /target/ / # buildkit
# Mon, 08 Jun 2026 22:48:03 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 08 Jun 2026 22:48:03 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:c160e404c59d6d30c66a0d74bbd17337f178f5d898a9908e18c71ce3bbe28c99`  
		Last Modified: Wed, 15 Apr 2026 20:01:53 GMT  
		Size: 3.3 MB (3283123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17c14d3a46a40621b00bfe1dffad82f777cc325db19b6c202e0e1b22d1251410`  
		Last Modified: Mon, 08 Jun 2026 22:48:19 GMT  
		Size: 290.2 KB (290162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6017a74f67fe3bf0e9dc5d0c334ab5929b4a454a86c2f391ecc6e1d3f6697e53`  
		Last Modified: Mon, 08 Jun 2026 22:48:21 GMT  
		Size: 97.7 MB (97735035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64ba330b4764c363a837174ff77f8f0607e763e35f18a210c2d7a0225bf10461`  
		Last Modified: Mon, 08 Jun 2026 22:48:19 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.23` - unknown; unknown

```console
$ docker pull golang@sha256:f1566af720750f3bb1fba07c4197cba3c29b5ba58b1d260cb1c5b85e088e4b60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.2 KB (218241 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d5bbcb0cb98481cae969329f76b399eecc7897824994a4daaf5bd549a48b33c`

```dockerfile
```

-	Layers:
	-	`sha256:647e79086b57089f85863acfebc614c3bc7f83c02f887df9aafaaada62fffea2`  
		Last Modified: Mon, 08 Jun 2026 22:48:19 GMT  
		Size: 193.0 KB (193018 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:640a8dbd8900a48fa7e20bfa6081bf50f3198541bf569fa3b40ec81b825204e5`  
		Last Modified: Mon, 08 Jun 2026 22:48:19 GMT  
		Size: 25.2 KB (25223 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.23` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:a50cf22907fdc107c508ff1e0cc4f0df64963464deded67bd65e207dd0b0c3f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.0 MB (100962295 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3d9da2d0dcebd76b5c2a214aa96dcab1726b835803e87a253121ab5928fe47a`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:25 GMT
ADD alpine-minirootfs-3.23.4-aarch64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:25 GMT
CMD ["/bin/sh"]
# Mon, 08 Jun 2026 22:44:05 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 08 Jun 2026 22:46:07 GMT
ENV GOTOOLCHAIN=local
# Mon, 08 Jun 2026 22:46:07 GMT
ENV GOPATH=/go
# Mon, 08 Jun 2026 22:46:07 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Jun 2026 22:46:07 GMT
COPY /target/ / # buildkit
# Mon, 08 Jun 2026 22:46:10 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 08 Jun 2026 22:46:10 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:d17f077ada118cc762df373ff803592abf2dfa3ddafaa7381e364dd27a88fca7`  
		Last Modified: Wed, 15 Apr 2026 20:01:32 GMT  
		Size: 4.2 MB (4199870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f47c679cacc17068c23aac4b87d00875e8c50e11adfc468cd4b22021b816bba`  
		Last Modified: Mon, 08 Jun 2026 22:46:25 GMT  
		Size: 292.9 KB (292850 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2308f1cb629a8c8fe52b3b591bdcfb51ba3716d584492ccac8858ffd19fbe4d4`  
		Last Modified: Mon, 08 Jun 2026 22:46:27 GMT  
		Size: 96.5 MB (96469417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f066830fb6ddf300c9be989b86e1d1f36facfd51b037c1538ba818f3ed4ab3fc`  
		Last Modified: Mon, 08 Jun 2026 22:46:25 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.23` - unknown; unknown

```console
$ docker pull golang@sha256:f3c435636166876eaa7ca82929454e84fd23297fcae31556e9cd7c893db83d0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.3 KB (218309 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11cd304f8d9e7fb724060bbd468335932cb765a4f0f8cd6dafc1b97139d57d92`

```dockerfile
```

-	Layers:
	-	`sha256:4120943d2bf3cca6ddb12d6113126635f8d6257842e4ebcf418d707daae8139e`  
		Last Modified: Mon, 08 Jun 2026 22:46:25 GMT  
		Size: 193.1 KB (193054 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e0d0d8d1170132b8263f076964cd6aca8227d3e4f6bddfec46f541c25484f44c`  
		Last Modified: Mon, 08 Jun 2026 22:46:25 GMT  
		Size: 25.3 KB (25255 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.23` - linux; 386

```console
$ docker pull golang@sha256:e7bfd75003edfe66a0b998256458c56ad0b119113055133c08056fc3a684bb01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.8 MB (103759257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6feb0cdcd898c38a79dbdd4b8c4b631ac712ca9e2a919f58d40826229687a35`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 15 Apr 2026 21:33:20 GMT
ADD alpine-minirootfs-3.23.4-x86.tar.gz / # buildkit
# Wed, 15 Apr 2026 21:33:20 GMT
CMD ["/bin/sh"]
# Mon, 08 Jun 2026 22:44:52 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 08 Jun 2026 22:47:21 GMT
ENV GOTOOLCHAIN=local
# Mon, 08 Jun 2026 22:47:21 GMT
ENV GOPATH=/go
# Mon, 08 Jun 2026 22:47:21 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Jun 2026 22:47:21 GMT
COPY /target/ / # buildkit
# Mon, 08 Jun 2026 22:47:24 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 08 Jun 2026 22:47:24 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:1cf9b6fc5889fdc0b6b22dd2afeea78c7c7985e06a8208c77dc71888bcf17f12`  
		Last Modified: Wed, 15 Apr 2026 21:33:25 GMT  
		Size: 3.7 MB (3690446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27d7f74632f38064c5d8bf6cb1f22517786c314491e049dc3485afa54cecaa8f`  
		Last Modified: Mon, 08 Jun 2026 22:47:39 GMT  
		Size: 290.6 KB (290644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c856874e83d87ce8611744942560effd5d1e879f3a49a6259f9e0f789a54f9b`  
		Last Modified: Mon, 08 Jun 2026 22:47:42 GMT  
		Size: 99.8 MB (99778009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de67acee086a0a65ff28367857330b93f3e2d77e5818ea23af712b6b1fcf21b0`  
		Last Modified: Mon, 08 Jun 2026 22:47:39 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.23` - unknown; unknown

```console
$ docker pull golang@sha256:f3b688555c498994602bd062fa8a11b100298ba657e72a245b6878abfcbee6b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.7 KB (218659 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6bd399590eab3ed0e43e2382677a803335ac80f67401225e96baf1389e24c55`

```dockerfile
```

-	Layers:
	-	`sha256:95412d8cdfa9bb79f3e01e119ccd554ff08700480f1ee45d9bc68c07731681db`  
		Last Modified: Mon, 08 Jun 2026 22:47:39 GMT  
		Size: 193.6 KB (193607 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ae6b5dc19d9250179ea8b3fee3ce5508a2375924fff0168b0cb0f3afa9572130`  
		Last Modified: Mon, 08 Jun 2026 22:47:39 GMT  
		Size: 25.1 KB (25052 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.23` - linux; ppc64le

```console
$ docker pull golang@sha256:b41247e2cf0d794349b304979fe263a7dcfc97ecb76899b36cf01c329e512ce5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.6 MB (102551747 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69810f59a5538a9a2faf72e698f33032c19b615274f24ada6bb0a83d0339f8dc`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:00:31 GMT
ADD alpine-minirootfs-3.23.4-ppc64le.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:00:31 GMT
CMD ["/bin/sh"]
# Tue, 02 Jun 2026 16:47:20 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 08 Jun 2026 23:06:07 GMT
ENV GOTOOLCHAIN=local
# Mon, 08 Jun 2026 23:06:07 GMT
ENV GOPATH=/go
# Mon, 08 Jun 2026 23:06:07 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Jun 2026 23:06:07 GMT
COPY /target/ / # buildkit
# Mon, 08 Jun 2026 23:11:27 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 08 Jun 2026 23:11:27 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:f14c55dbf69723970b011b8f4e3d231f8c307d6db3c80dafa55949ab7d3ea6d2`  
		Last Modified: Wed, 15 Apr 2026 20:00:46 GMT  
		Size: 3.8 MB (3830929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77dfc45c5906cb105fa1bde6a534e8e48deced0c4556f99056c2f76204caa5c2`  
		Last Modified: Tue, 02 Jun 2026 16:47:39 GMT  
		Size: 293.4 KB (293393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a1d5d0b8da3315c28f7e047d6d8c920d4423531520a738d9dbd717fd24afb93`  
		Last Modified: Mon, 08 Jun 2026 23:07:16 GMT  
		Size: 98.4 MB (98427267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c64ee496197eb7593e189e9c4859af7ef400caff8a3bed29000144ca8e0e2d54`  
		Last Modified: Mon, 08 Jun 2026 23:11:46 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.23` - unknown; unknown

```console
$ docker pull golang@sha256:79dc8eaee496eede5550a1faf2ae2c0d9c87c8ecd774ea7dfc6c98641bbbd6bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.0 KB (218027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f699b17afffa55bd6948454058f4d827a2ef3b8a4dff83df9915c12bf8f3ca5`

```dockerfile
```

-	Layers:
	-	`sha256:64b12a550486ffc62ecb7e1369eb4eebc6b13953e02c1f394fe118bfdaa707a1`  
		Last Modified: Mon, 08 Jun 2026 23:11:47 GMT  
		Size: 193.0 KB (193047 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4dac4d922478f5f9f8ed9541f7c81b638331e1a4a58d42f7e80db0284be23101`  
		Last Modified: Mon, 08 Jun 2026 23:11:47 GMT  
		Size: 25.0 KB (24980 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.23` - linux; riscv64

```console
$ docker pull golang@sha256:404f810c133b06155ec6ce95de59565d3dc11a007d77738e49fa405d312bc075
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.2 MB (103225559 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:beaaaa576c035fe100effb16af051633c50ede2fcacc8ad75ed559735dc606f4`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:30:47 GMT
ADD alpine-minirootfs-3.23.4-riscv64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:30:47 GMT
CMD ["/bin/sh"]
# Thu, 16 Apr 2026 16:18:44 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 09 Jun 2026 06:45:18 GMT
ENV GOTOOLCHAIN=local
# Tue, 09 Jun 2026 06:45:18 GMT
ENV GOPATH=/go
# Tue, 09 Jun 2026 06:45:18 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Jun 2026 06:45:18 GMT
COPY /target/ / # buildkit
# Tue, 09 Jun 2026 07:34:02 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 09 Jun 2026 07:34:02 GMT
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
	-	`sha256:fd5a55eb95001de7bce5a945456836deb24c4f6ef91e17b9ea69478ba20a16a6`  
		Last Modified: Tue, 09 Jun 2026 06:52:30 GMT  
		Size: 99.3 MB (99347186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c23c073a607d8c2239945fff6f9fac6bab2c41f05a801c1a33e71a8a21457e5`  
		Last Modified: Tue, 09 Jun 2026 07:35:20 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.23` - unknown; unknown

```console
$ docker pull golang@sha256:457d58aaab712843470fecdb2bf63db1d0beccdf6275e03a6440ef0c56bd6e77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.2 KB (218196 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:218b23ea318df3bac8e592f0a8e7fb377a09465de6b751ab1ab4b10bdd7ab75f`

```dockerfile
```

-	Layers:
	-	`sha256:aadd954dc619a0ce069d40da074b59f03ec3439cb5e7af74148995b6e15d72fe`  
		Last Modified: Tue, 09 Jun 2026 07:35:20 GMT  
		Size: 193.0 KB (193043 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6e46abe2c38f91d401f6892f8d17570a82c0e027245ce37744c5d9a398854b14`  
		Last Modified: Tue, 09 Jun 2026 07:35:20 GMT  
		Size: 25.2 KB (25153 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.23` - linux; s390x

```console
$ docker pull golang@sha256:dff31ae7bcd5201313a067d8071d5b157328708dace0d415e999658e75356b4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.5 MB (104509085 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de3ad6d2225921d34e932d3ec40abcb006696629b1ae1a069953aa8301549563`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:00:34 GMT
ADD alpine-minirootfs-3.23.4-s390x.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:00:34 GMT
CMD ["/bin/sh"]
# Tue, 02 Jun 2026 16:41:58 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 08 Jun 2026 22:52:26 GMT
ENV GOTOOLCHAIN=local
# Mon, 08 Jun 2026 22:52:26 GMT
ENV GOPATH=/go
# Mon, 08 Jun 2026 22:52:26 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Jun 2026 22:52:26 GMT
COPY /target/ / # buildkit
# Mon, 08 Jun 2026 22:52:33 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 08 Jun 2026 22:52:33 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:13188190f2c53fa4e825ed24ee94f77177787a7ddde7687d5fadb7431f136a37`  
		Last Modified: Wed, 15 Apr 2026 20:00:44 GMT  
		Size: 3.7 MB (3726532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f42ca9f29dfa6d3e969a05d12ba4b1dd9465b2ec31113dd62c26050eb7eeae28`  
		Last Modified: Tue, 02 Jun 2026 16:42:25 GMT  
		Size: 291.2 KB (291162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a56217687aa3cc648280b9c7052cd68f26077339d92dab45c68b721ed5388981`  
		Last Modified: Mon, 08 Jun 2026 22:53:02 GMT  
		Size: 100.5 MB (100491232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fde8fb187d9ed63d6faba6989fc259bab384a0ba821a136e82458d0ab32914f2`  
		Last Modified: Mon, 08 Jun 2026 22:53:00 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.23` - unknown; unknown

```console
$ docker pull golang@sha256:58dfe4f161eaecf25b52428c08f2b777c7818c8b2949a184bfbdfca0573a7ee8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.7 KB (218667 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e3e81b876b73e5f38c320480fec5962d990bf4a38ea5f31029b20d6a03333a3`

```dockerfile
```

-	Layers:
	-	`sha256:6d2a2ad24d37f716b3f65033d24f1a39bed8ca7f849b8c704533dd9d745e55dd`  
		Last Modified: Mon, 08 Jun 2026 22:53:00 GMT  
		Size: 193.7 KB (193745 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:77ac4bac42c789c2ab9f1a5e4be6475b282c6b4ab97a8ed8bfc7e7f294d7c23e`  
		Last Modified: Mon, 08 Jun 2026 22:53:00 GMT  
		Size: 24.9 KB (24922 bytes)  
		MIME: application/vnd.in-toto+json
