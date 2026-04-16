## `golang:tip-alpine`

```console
$ docker pull golang@sha256:fc52e2efd9fa26c0560ea292bff13355e7102363d41862fceb1519c7e3ac613c
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
$ docker pull golang@sha256:c38af0add8828cd12410848ec6d56ca094ba0580971cc2a5cc8653175507bc35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.7 MB (98736535 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7d80668a7f5c30361dd3ac91640edc66d5acb518aa4960cc9ccff1f153aa6aa`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:21:58 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Wed, 15 Apr 2026 21:31:11 GMT
ENV GOTOOLCHAIN=local
# Wed, 15 Apr 2026 21:31:11 GMT
ENV GOPATH=/go
# Wed, 15 Apr 2026 21:31:11 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 21:31:11 GMT
COPY /target/ / # buildkit
# Wed, 15 Apr 2026 21:31:13 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 15 Apr 2026 21:31:13 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cb496381bf96a08576a8320f7ff7202e580d0da89ae78f7abc411f7c21974eb`  
		Last Modified: Wed, 15 Apr 2026 20:22:06 GMT  
		Size: 290.2 KB (290244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ab04cb4a8e454fc7559b5ebb652cf17e60070b889bacf79f9339f14ac23b48e`  
		Last Modified: Tue, 14 Apr 2026 00:01:54 GMT  
		Size: 94.6 MB (94581946 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0147c304824bb4f87a0dbbe8f6f3286a9dfc9e0d5693c47e0318ab0644dcd0bb`  
		Last Modified: Wed, 15 Apr 2026 21:31:29 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:44b3cadea2615d8efab08f02b8e8cffef7213cbcbb2836185cb92347d14383aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.7 KB (218741 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a54c0c15bd0fbeb34485a2eae8f6d55d4c2962dfc801eed7ad61de60cd947289`

```dockerfile
```

-	Layers:
	-	`sha256:0c087269e8063ca7f6d91f39f382da71091900af3e2cd47e680e765a4dc26a20`  
		Last Modified: Wed, 15 Apr 2026 21:31:29 GMT  
		Size: 193.6 KB (193648 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2116804d07f052b47cae556e9683dc6a5388b0502d898431214c4800dd0b80a8`  
		Last Modified: Wed, 15 Apr 2026 21:31:29 GMT  
		Size: 25.1 KB (25093 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine` - linux; arm variant v6

```console
$ docker pull golang@sha256:fc3cbeeb16e893dd1ec2f2845aa83fa0638624be03986a23a0ffadac9838feee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.0 MB (95049895 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18c34346c3bf36d1e64d4cb0bef2f33f5fb3ff245d07f115fc6d5fada7fc1b9f`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:02:13 GMT
ADD alpine-minirootfs-3.23.4-armhf.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:02:13 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 21:22:27 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Wed, 15 Apr 2026 21:25:20 GMT
ENV GOTOOLCHAIN=local
# Wed, 15 Apr 2026 21:25:20 GMT
ENV GOPATH=/go
# Wed, 15 Apr 2026 21:25:20 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 21:25:20 GMT
COPY /target/ / # buildkit
# Wed, 15 Apr 2026 21:25:22 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 15 Apr 2026 21:25:22 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:c9cf8ef099e6e20ca4c7a2ae5b731a4beff960c0ffb88dd64fd6cdfdfe04839d`  
		Last Modified: Wed, 15 Apr 2026 20:02:17 GMT  
		Size: 3.6 MB (3571863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e242a58dfe3d5201571258c75219855bdb953d7e9ff8da9876953a853a5428be`  
		Last Modified: Wed, 15 Apr 2026 21:25:34 GMT  
		Size: 291.0 KB (291016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b805d56aa0bb12df6840037301a097e9d8c991b01763b634df28890710475e8`  
		Last Modified: Tue, 14 Apr 2026 00:07:36 GMT  
		Size: 91.2 MB (91186859 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cca140d3b52b0ee36e4cd6c2555a1fcd55563497bdfaa50c9ff294ac869e135d`  
		Last Modified: Wed, 15 Apr 2026 21:25:34 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:0a497fa80157b37f8250ac292f0f9d305661c89eeacb173cb74ebdbc18c28857
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.0 KB (25008 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe119ac39ea3b86d80771b481e242309321eb9ab2c026903b4402590ed68400d`

```dockerfile
```

-	Layers:
	-	`sha256:ba4d69b4b0440bc256aa32226d99e817edfbb2394d33547690f25356eaf7ae5e`  
		Last Modified: Wed, 15 Apr 2026 21:25:34 GMT  
		Size: 25.0 KB (25008 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine` - linux; arm variant v7

```console
$ docker pull golang@sha256:01e40207c9e903013bd7f61b7b3590b52c66a957c245d6295e37e11d84101be4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.5 MB (94470539 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e26e024c6cbc0c504a2f1ca02172cca93e6a2e2ce9169377486b8a96ae9167b`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:44 GMT
ADD alpine-minirootfs-3.23.3-armv7.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:44 GMT
CMD ["/bin/sh"]
# Mon, 13 Apr 2026 23:59:49 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 14 Apr 2026 00:02:37 GMT
ENV GOTOOLCHAIN=local
# Tue, 14 Apr 2026 00:02:37 GMT
ENV GOPATH=/go
# Tue, 14 Apr 2026 00:02:37 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 14 Apr 2026 00:02:37 GMT
COPY /target/ / # buildkit
# Tue, 14 Apr 2026 00:02:40 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 14 Apr 2026 00:02:40 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:7ed661450d9b41ba25f81f6ef8649bb379f47471d21c4898a8a6a3e11b819220`  
		Last Modified: Wed, 28 Jan 2026 01:18:50 GMT  
		Size: 3.3 MB (3281724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:856713239ba82c603614115de5d12036393ac1b3af1a3916416327488c218f8b`  
		Last Modified: Tue, 14 Apr 2026 00:02:55 GMT  
		Size: 296.2 KB (296187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b5edd4ff2dbd145648193fafaa3d5f04805713affd95a7e7d9d0029f6ec1270`  
		Last Modified: Tue, 14 Apr 2026 00:02:12 GMT  
		Size: 90.9 MB (90892470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d15fdcb2eab20800bb98178f655216e6b920802d462e7dcd954690840ec48de5`  
		Last Modified: Tue, 14 Apr 2026 00:02:55 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:bcaeb0771c9f441b19052c54bae24bf661149417d300100249780d866981e511
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.2 KB (220196 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8baf4a25814c3aa714b9effa66641b7815f464a69c0b8bbb115f2faa1f83e8bf`

```dockerfile
```

-	Layers:
	-	`sha256:9181f5fb089b100cd02e4e79ec4b7ced52fc87986323374febe988ddd2140743`  
		Last Modified: Tue, 14 Apr 2026 00:02:55 GMT  
		Size: 195.0 KB (194973 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c772150995ba67cb6e21e8fc53e64ec020bd7fa84d27ab58b40d67c39fcd8175`  
		Last Modified: Tue, 14 Apr 2026 00:02:55 GMT  
		Size: 25.2 KB (25223 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:27bc9ff6459da3f3a0958bcd50b72272fd58beede0cc9ca1c7e431816c46fc36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.2 MB (94196985 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7092da02a6245fbe177d0540b4ecbfe6e961a16db1c6ad638a947705dcf5ea3`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Tue, 14 Apr 2026 00:01:01 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 14 Apr 2026 00:02:51 GMT
ENV GOTOOLCHAIN=local
# Tue, 14 Apr 2026 00:02:51 GMT
ENV GOPATH=/go
# Tue, 14 Apr 2026 00:02:51 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 14 Apr 2026 00:02:51 GMT
COPY /target/ / # buildkit
# Tue, 14 Apr 2026 00:02:54 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 14 Apr 2026 00:02:54 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10a66febccaa59202c79fd0cad93a2a3fe97088d94b55c57328ba96a85314d00`  
		Last Modified: Tue, 14 Apr 2026 00:03:09 GMT  
		Size: 298.8 KB (298844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca293ee12e748379dfc7e49600a21d46479ed1f62dbf74c0006b5ec77222dadb`  
		Last Modified: Tue, 14 Apr 2026 00:03:08 GMT  
		Size: 89.7 MB (89700892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b86d20277d224950b463fb531b75505b8edf3f004800d74ce888e726b19e5f98`  
		Last Modified: Tue, 14 Apr 2026 00:03:09 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:ea6c85f20c9aa8d91d01d6854d95b1f9740cba48340293450a21712021327759
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.3 KB (220264 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40ddf089aed25231becd707bd2b75c1eb0f08838c8e05902f0b5f3ada11e3cbb`

```dockerfile
```

-	Layers:
	-	`sha256:d4541af589dcae75c45897b7646cc1135697d06552ffb72f52b22e4c88ed8d51`  
		Last Modified: Tue, 14 Apr 2026 00:03:09 GMT  
		Size: 195.0 KB (195009 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:004c764d4eda17eab426f91a95a7b6b7005f8b0b5058bd6915b00bd95295f632`  
		Last Modified: Tue, 14 Apr 2026 00:03:09 GMT  
		Size: 25.3 KB (25255 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine` - linux; 386

```console
$ docker pull golang@sha256:d4514f84ab615d2a8ca6a9c2af67ae8750ed499bb33dbe15ddd9b72cf759469d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.6 MB (96605071 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae3f1ae9df6e8d04300a49f035d267c7d121ff4f61cc23670c3cbd1340656e48`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:11 GMT
ADD alpine-minirootfs-3.23.3-x86.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:11 GMT
CMD ["/bin/sh"]
# Tue, 14 Apr 2026 00:27:38 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 14 Apr 2026 00:29:47 GMT
ENV GOTOOLCHAIN=local
# Tue, 14 Apr 2026 00:29:47 GMT
ENV GOPATH=/go
# Tue, 14 Apr 2026 00:29:47 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 14 Apr 2026 00:29:47 GMT
COPY /target/ / # buildkit
# Tue, 14 Apr 2026 00:29:50 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 14 Apr 2026 00:29:50 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:18bdec7eea78464ecf9b88f4ec630eaeb694ea1c0101ecd9c20eda20c9065e23`  
		Last Modified: Wed, 28 Jan 2026 01:18:16 GMT  
		Size: 3.7 MB (3686998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c41789a52667a201bad29f8ac964e5fe3cc7ad43fe1c1a54a14275e43506ff17`  
		Last Modified: Tue, 14 Apr 2026 00:30:04 GMT  
		Size: 296.7 KB (296657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5aa5425bebab36322e26303eb33424df1802209b7a6b3dc6b986570aca912bfd`  
		Last Modified: Tue, 14 Apr 2026 00:29:28 GMT  
		Size: 92.6 MB (92621258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:faa7def8fe87062e22aecb62213a7899280be79c5a3f154af9ea09e59db1e1b8`  
		Last Modified: Tue, 14 Apr 2026 00:30:03 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:b69fb38fa39d2fcf5c5001ae7d0ab6adf9a2c378fa279c3613b3be008f7fe7e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.6 KB (220613 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c881e914f8d067b70a0e0e6b929622bf8a0590753f3c16c3c440eda36bc46b0`

```dockerfile
```

-	Layers:
	-	`sha256:9218dc56fcf88b3d1a707ffd89fa3f7e34e909b655662a2a9da9e353e5e7a5ab`  
		Last Modified: Tue, 14 Apr 2026 00:30:03 GMT  
		Size: 195.6 KB (195562 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1b7fdae918cdc2527595409a57769723bd6ca084253f5592e1ea0177828eaf18`  
		Last Modified: Tue, 14 Apr 2026 00:30:04 GMT  
		Size: 25.1 KB (25051 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine` - linux; ppc64le

```console
$ docker pull golang@sha256:15b15b2e401c55358691a2dff7fb8bbbaefe4212fea540c6876b8b1a46bd0ee4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.5 MB (95474293 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:095784980447665aa51ec225150dfcf9af5382a393be681a74234a48e33e67c0`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:01 GMT
ADD alpine-minirootfs-3.23.3-ppc64le.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:01 GMT
CMD ["/bin/sh"]
# Tue, 07 Apr 2026 21:28:43 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 14 Apr 2026 00:06:08 GMT
ENV GOTOOLCHAIN=local
# Tue, 14 Apr 2026 00:06:08 GMT
ENV GOPATH=/go
# Tue, 14 Apr 2026 00:06:08 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 14 Apr 2026 00:06:08 GMT
COPY /target/ / # buildkit
# Tue, 14 Apr 2026 00:10:59 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 14 Apr 2026 00:11:00 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:532f7d227cfd697fe6a6f7bfe8c0cc7baa9d99d3d41d50d9b6394fdb6322f4aa`  
		Last Modified: Wed, 28 Jan 2026 01:17:23 GMT  
		Size: 3.8 MB (3829643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c157c37b8ca35f88bf66161b72bc1761ade8e543ac3a14868075a68b5dff95e5`  
		Last Modified: Tue, 07 Apr 2026 21:29:03 GMT  
		Size: 299.3 KB (299270 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0175a2939aed372a8574a3f30ca86be23817fbc044f643da506137d0f0ef397`  
		Last Modified: Tue, 14 Apr 2026 00:07:09 GMT  
		Size: 91.3 MB (91345222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f7243d814747948a2770c2655af70e62e3a11e8a52e658ae1f4c9651594d173`  
		Last Modified: Tue, 14 Apr 2026 00:11:18 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:c278398e234a456e75ad2867f02c107b23aae38a7246b98a9bb3683d0cd55646
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.2 KB (220155 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc83fee6cd2840282e96e62fbb3cfa78b32f4f0db14d9fb3b58e45636d7cec5a`

```dockerfile
```

-	Layers:
	-	`sha256:187d2c68bacaf3b99fc74f45e6a6c650f4242545abf803476ae7f2ac74eff6ab`  
		Last Modified: Tue, 14 Apr 2026 00:11:18 GMT  
		Size: 195.0 KB (195002 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:25273fac301040588c249d0d1a3cfe4f7ed44e2bbad5c3178fe065b52831c91c`  
		Last Modified: Tue, 14 Apr 2026 00:11:18 GMT  
		Size: 25.2 KB (25153 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine` - linux; riscv64

```console
$ docker pull golang@sha256:6c2968e2d480c17c4672c5141f738a09c3c2f498375bfe1f81d5efbb5d7c2002
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.7 MB (95740951 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7eadd83478bb2f0291d8f1773a739906a44c01907bf294d4bce72aa80e633d1`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 03:47:28 GMT
ADD alpine-minirootfs-3.23.3-riscv64.tar.gz / # buildkit
# Wed, 28 Jan 2026 03:47:28 GMT
CMD ["/bin/sh"]
# Tue, 24 Mar 2026 08:51:29 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 14 Apr 2026 10:51:28 GMT
ENV GOTOOLCHAIN=local
# Tue, 14 Apr 2026 10:51:28 GMT
ENV GOPATH=/go
# Tue, 14 Apr 2026 10:51:28 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 14 Apr 2026 10:51:28 GMT
COPY /target/ / # buildkit
# Tue, 14 Apr 2026 11:38:01 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 14 Apr 2026 11:38:01 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:9da5d16b2a566416844fd0c62fa81165037aa0b7f154a5c1f58f06412739471c`  
		Last Modified: Wed, 28 Jan 2026 03:48:00 GMT  
		Size: 3.6 MB (3585287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:653a48053074547bb1f8e43c4e508d8a803d45b52e98210c3539d09ceb870090`  
		Last Modified: Tue, 24 Mar 2026 08:53:11 GMT  
		Size: 296.5 KB (296514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbae07da1d6f03b6754026e98e9959804791bb758eb0115a888df646b9fb60ce`  
		Last Modified: Tue, 14 Apr 2026 10:58:28 GMT  
		Size: 91.9 MB (91858991 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95a163a5346fb71eb2c3c2e585aa64096b4927b04726a1363083d60e7827dd0b`  
		Last Modified: Tue, 14 Apr 2026 11:39:26 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:e5df4eb19900cd106b9b26535438f087100720e153e52ae7ae7891b0743753b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.2 KB (220151 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:618b3d8d94d4882ed10eeb1178b7cba39b1a65e7ac4403b83bda9e9a0a22da06`

```dockerfile
```

-	Layers:
	-	`sha256:8e9f631ea9e828c33f2b48c538bb81b8878186e528b3cb0321a012ca317884d5`  
		Last Modified: Tue, 14 Apr 2026 11:39:26 GMT  
		Size: 195.0 KB (194998 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4ad168a09b1ad231c9722ad618ea6108c9133b9c8f6da801a45e4aa78f5a1774`  
		Last Modified: Tue, 14 Apr 2026 11:39:26 GMT  
		Size: 25.2 KB (25153 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine` - linux; s390x

```console
$ docker pull golang@sha256:301b5a13aa7b569de9768760906ccc250d9d80412fedac49c782bf8eec35498c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.8 MB (97800880 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a995f144a312b9c4ee304fb43ae46475e72357f9d83af34f74e6839b0e5877ce`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:06 GMT
ADD alpine-minirootfs-3.23.3-s390x.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:06 GMT
CMD ["/bin/sh"]
# Tue, 07 Apr 2026 21:13:30 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 14 Apr 2026 00:26:50 GMT
ENV GOTOOLCHAIN=local
# Tue, 14 Apr 2026 00:26:50 GMT
ENV GOPATH=/go
# Tue, 14 Apr 2026 00:26:50 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 14 Apr 2026 00:26:50 GMT
COPY /target/ / # buildkit
# Tue, 14 Apr 2026 00:26:53 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 14 Apr 2026 00:26:53 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:623c99520afcb8c68e21bd22d3bc252ae348c276fb9c45a79aeccb4caf2b8d9f`  
		Last Modified: Wed, 28 Jan 2026 01:17:15 GMT  
		Size: 3.7 MB (3725333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e09b3320db87c0fbe713adce5ff43836b299964a204ab829de72270c3d2d4c3`  
		Last Modified: Tue, 07 Apr 2026 21:14:59 GMT  
		Size: 297.2 KB (297199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f5aaa70187b5fa60b40f4f6aa959f778263834bd8f55472a34e3a940460eef6`  
		Last Modified: Tue, 14 Apr 2026 00:26:59 GMT  
		Size: 93.8 MB (93778190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:112a79760becf704a56e40f0cfc5ae9e29c3fdc00beb0514aebb944d7cd4eaff`  
		Last Modified: Tue, 14 Apr 2026 00:27:19 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:0abb9b5e87bd4c218b3bd47d98df4e8df5c99882dd8736812ba6bdc95c5ede73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.0 KB (220047 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53245cfd0104347b64a285e26bd6db8a0bdbe9fff6a9b919e1f41d9e65d0558f`

```dockerfile
```

-	Layers:
	-	`sha256:6dafb994900e648dd9004675d2f542b9003602937e9b473eb0a70ca78ba00520`  
		Last Modified: Tue, 14 Apr 2026 00:27:19 GMT  
		Size: 195.0 KB (194952 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fcac978892496aac2d0fc96f0529bc721eff5c7f08c416600499ccf4135dd595`  
		Last Modified: Tue, 14 Apr 2026 00:27:19 GMT  
		Size: 25.1 KB (25095 bytes)  
		MIME: application/vnd.in-toto+json
