## `golang:tip-20260215-alpine`

```console
$ docker pull golang@sha256:4ed73c18637271968ebdafaa3f9459a37f3e5c041771d032bf9e71344976ee96
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

### `golang:tip-20260215-alpine` - linux; amd64

```console
$ docker pull golang@sha256:070c9a71217cdc043a36a7c2acde20e869f5133f53699a8f17a92a04e97e57f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.7 MB (97668442 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:008ebbf1a54257e35c8bf59bf22517d8ba182d4f136f876c596ddca0d6bf24dc`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Tue, 17 Feb 2026 19:29:50 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 17 Feb 2026 19:31:44 GMT
ENV GOTOOLCHAIN=local
# Tue, 17 Feb 2026 19:31:44 GMT
ENV GOPATH=/go
# Tue, 17 Feb 2026 19:31:44 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Feb 2026 19:31:44 GMT
COPY /target/ / # buildkit
# Tue, 17 Feb 2026 19:31:47 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 17 Feb 2026 19:31:47 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cf2fe682e249601d3fb9909280938dffc72de5d53b7332ee9e2e5b90ac17f65`  
		Last Modified: Tue, 17 Feb 2026 19:32:01 GMT  
		Size: 296.1 KB (296083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eab0817763c3e1cf11dc0cf9b1bdc31701d4aef51c361f72a656b7a9a217055a`  
		Last Modified: Tue, 17 Feb 2026 19:31:25 GMT  
		Size: 93.5 MB (93510382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd6fd21c6cc54945b24604bda0d60b109c26e8421efb38310826c06d2e1adaaf`  
		Last Modified: Tue, 17 Feb 2026 19:32:01 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20260215-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:84b86b5ee083d83fc570b6866cb7be8dc1096ff47ba2e3744fc277a1e489332b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.7 KB (220694 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02c257b2c790ce8a097508e44b5e99c62c7062c4a4efa52e4525713ec963c43e`

```dockerfile
```

-	Layers:
	-	`sha256:980f496268e62062b17493042816b04fc1d89b58cc495454f5bcad934a643990`  
		Last Modified: Tue, 17 Feb 2026 19:32:01 GMT  
		Size: 195.6 KB (195601 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3049ac38aeb5672ee10711c388a3639489c3698277728d66b51376344335a759`  
		Last Modified: Tue, 17 Feb 2026 19:32:01 GMT  
		Size: 25.1 KB (25093 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20260215-alpine` - linux; arm variant v6

```console
$ docker pull golang@sha256:1614d46f0081f03358718fb46ac2c2f5b1bdafaf68fac53fedfcc22e70428325
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.8 MB (93752754 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:456c41441eab5f761e2dbd6d9350ead800a9f1ea41abc4d78e65abe0e8e1956b`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:52 GMT
ADD alpine-minirootfs-3.23.3-armhf.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:52 GMT
CMD ["/bin/sh"]
# Tue, 17 Feb 2026 19:26:00 GMT
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
	-	`sha256:f067a9ad7b3a4e3b687105344f6ad0934a0623c4359c2d841a3d4fab27e26060`  
		Last Modified: Wed, 28 Jan 2026 01:17:56 GMT  
		Size: 3.6 MB (3569821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e73ada47d7e7ec1683d3af0d3ce1468db6640a4d22228a5f756128136f19838`  
		Last Modified: Tue, 17 Feb 2026 19:29:04 GMT  
		Size: 297.3 KB (297259 bytes)  
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

### `golang:tip-20260215-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:13563881c746bd08871fa3f38555fb2b25d6b077018d4247a11a12e209ab8710
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.0 KB (25007 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e26f4087671ea5b4f7ea177dd91585dd0e56baa6e86e19e0e4ae8feede8e0d9`

```dockerfile
```

-	Layers:
	-	`sha256:79bd537ddfc4adda875e522b295c08f821ebd96088af2474de3c8cf44053ed59`  
		Last Modified: Tue, 17 Feb 2026 19:29:05 GMT  
		Size: 25.0 KB (25007 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20260215-alpine` - linux; arm variant v7

```console
$ docker pull golang@sha256:b0f935d2028b482bfbde2d427631b5b0a327a749023fd90a248a42f3f2b63e51
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.2 MB (93194375 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dff122b5eadc78b62589901fdbe4262721473999cb787d00f36444006a72540b`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:44 GMT
ADD alpine-minirootfs-3.23.3-armv7.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:44 GMT
CMD ["/bin/sh"]
# Tue, 17 Feb 2026 19:29:18 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 17 Feb 2026 19:32:10 GMT
ENV GOTOOLCHAIN=local
# Tue, 17 Feb 2026 19:32:10 GMT
ENV GOPATH=/go
# Tue, 17 Feb 2026 19:32:10 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Feb 2026 19:32:10 GMT
COPY /target/ / # buildkit
# Tue, 17 Feb 2026 19:32:13 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 17 Feb 2026 19:32:13 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:7ed661450d9b41ba25f81f6ef8649bb379f47471d21c4898a8a6a3e11b819220`  
		Last Modified: Wed, 28 Jan 2026 01:18:50 GMT  
		Size: 3.3 MB (3281724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c79dd4485345904635f8c5fbdf041ce78b8aaef63a1dfb200754f0881b6cf1de`  
		Last Modified: Tue, 17 Feb 2026 19:32:28 GMT  
		Size: 296.2 KB (296193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc8592fb2ab8b68f648f6fdc255c5205f63cba2d9ae66c3ae76aec04ac54577d`  
		Last Modified: Tue, 17 Feb 2026 19:29:44 GMT  
		Size: 89.6 MB (89616301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f449384853e58b4b38efb102691e2fab7a4a83cbccc8c5bcba823fe69b0253a`  
		Last Modified: Tue, 17 Feb 2026 19:32:28 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20260215-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:4b906f9fdf4abe0f522b118b525a91dd21ec5e7db2f260771712db475d9faf4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.2 KB (220194 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a25f44e8d9ba1e160c3c8009568b9199fc21a8a4e85983fa3f4accac79e994b8`

```dockerfile
```

-	Layers:
	-	`sha256:8a07d8d1f9f7deddd64259ec7b7363e5ef2d5ba439f34ba7f128366eb85906c8`  
		Last Modified: Tue, 17 Feb 2026 19:32:28 GMT  
		Size: 195.0 KB (194971 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:019686a54333240a58cc7889e9fa187c4c9d94a771fb295a9b15340a18e1d671`  
		Last Modified: Tue, 17 Feb 2026 19:32:28 GMT  
		Size: 25.2 KB (25223 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20260215-alpine` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:6e836a922400788516c2097e1b26b7868d2e79c633a2cb9aa282e6e3e6da4e3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.2 MB (93179058 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7532b59e747d438664a531aed024fe6b7ea8a39edf480d5ff78c7389f4f87d37`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Tue, 17 Feb 2026 19:27:10 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 17 Feb 2026 19:28:55 GMT
ENV GOTOOLCHAIN=local
# Tue, 17 Feb 2026 19:28:55 GMT
ENV GOPATH=/go
# Tue, 17 Feb 2026 19:28:55 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Feb 2026 19:28:55 GMT
COPY /target/ / # buildkit
# Tue, 17 Feb 2026 19:28:57 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 17 Feb 2026 19:28:57 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75f15c827635a88e44a1302d7f66f0cd9712b9fdb929b0f08c057c7012c8eb9e`  
		Last Modified: Tue, 17 Feb 2026 19:29:12 GMT  
		Size: 298.8 KB (298838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14c4ec7dd3016101f540520ce3287918647d94b478d69d4a817cb7382cffb26d`  
		Last Modified: Tue, 17 Feb 2026 19:29:15 GMT  
		Size: 88.7 MB (88682971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c17e6e47d8ff03e7da88b723f6f4b31aa32c4da9159aa6e594b63db328a090f0`  
		Last Modified: Tue, 17 Feb 2026 19:29:12 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20260215-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:fd396c550c37448df50de1832d5488637e55346e0976c109fb498c124f30affb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.3 KB (220262 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5026e0347309435beea5e0f2fc407ff10bf8c7a147468ee40bd7a16b684dd415`

```dockerfile
```

-	Layers:
	-	`sha256:956a63e0972a67d342335e1ab99853558a20012cc840ac2e16eab32ac88ffe33`  
		Last Modified: Tue, 17 Feb 2026 19:29:12 GMT  
		Size: 195.0 KB (195007 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:43a78c2f896e0b37589dcb973f9baa8535cd837374a04eec14ffc2f9cf3d5ad4`  
		Last Modified: Tue, 17 Feb 2026 19:29:12 GMT  
		Size: 25.3 KB (25255 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20260215-alpine` - linux; 386

```console
$ docker pull golang@sha256:5f3bb0635f288a60489e88f61867a1614d9b2190cdb07cc6a0abf25b71384693
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.4 MB (95398984 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92812c21e31125a74a88f07e8c199a4e2a083ec3c878c23b66bee883cbb219e1`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:11 GMT
ADD alpine-minirootfs-3.23.3-x86.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:11 GMT
CMD ["/bin/sh"]
# Tue, 17 Feb 2026 19:26:53 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 17 Feb 2026 19:29:07 GMT
ENV GOTOOLCHAIN=local
# Tue, 17 Feb 2026 19:29:07 GMT
ENV GOPATH=/go
# Tue, 17 Feb 2026 19:29:07 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Feb 2026 19:29:07 GMT
COPY /target/ / # buildkit
# Tue, 17 Feb 2026 19:29:10 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 17 Feb 2026 19:29:10 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:18bdec7eea78464ecf9b88f4ec630eaeb694ea1c0101ecd9c20eda20c9065e23`  
		Last Modified: Wed, 28 Jan 2026 01:18:16 GMT  
		Size: 3.7 MB (3686998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8106376f2ef4f5e4eeffb5332cfceaf7198018aba253812884f0b8cc72c72af6`  
		Last Modified: Tue, 17 Feb 2026 19:29:24 GMT  
		Size: 296.7 KB (296672 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30233e899defca3f42aa6ad06bb0772f268b46b15c12c0af84227790251579bd`  
		Last Modified: Tue, 17 Feb 2026 19:26:57 GMT  
		Size: 91.4 MB (91415156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:977282e475e5b20d84e9883559785dea30b6a2e61e96b8e8d0bb6d4420ea6324`  
		Last Modified: Tue, 17 Feb 2026 19:29:24 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20260215-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:88b30bac6386cb1aca39bf1df0b1e0bec2fcfd03f70866cb5e7ce307bc0d1d4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.6 KB (220612 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c499a295f29b4711745e971192a2b0fe58f5385494a9b2105092345a6fd605d`

```dockerfile
```

-	Layers:
	-	`sha256:c920f5bbb1cf109cdbab22caa1da85d221c0efad52ae7b0e6bf4ffd9843d978a`  
		Last Modified: Tue, 17 Feb 2026 19:29:24 GMT  
		Size: 195.6 KB (195560 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d44008ea2635366e739ef49afb6bfa8f33af5e5b45fceb27faa0485ed7598ccb`  
		Last Modified: Tue, 17 Feb 2026 19:29:24 GMT  
		Size: 25.1 KB (25052 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20260215-alpine` - linux; ppc64le

```console
$ docker pull golang@sha256:9964d88b023a64b071c04bb2bc8d6e68a095f40e0eeb66337db2fa761a76042e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.3 MB (94338449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93e112658cd69e16b566f1de37a3f2cec63cb53c5a6aa764a0f6aa833bdb512e`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:01 GMT
ADD alpine-minirootfs-3.23.3-ppc64le.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:01 GMT
CMD ["/bin/sh"]
# Mon, 09 Feb 2026 20:32:44 GMT
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
	-	`sha256:532f7d227cfd697fe6a6f7bfe8c0cc7baa9d99d3d41d50d9b6394fdb6322f4aa`  
		Last Modified: Wed, 28 Jan 2026 01:17:23 GMT  
		Size: 3.8 MB (3829643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e528c55315b3e5f2f548755f16a234f2386736177558710d4d0c6eaf02151f69`  
		Last Modified: Mon, 09 Feb 2026 20:33:09 GMT  
		Size: 299.3 KB (299264 bytes)  
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

### `golang:tip-20260215-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:866df0407738fbdc596f097f9a04f74c4e0ae5a43e23235c68978da555273091
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.2 KB (220152 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77684ab2f690ad2bf251c6188780c241302b6a32389b2d12997fa531f64844e3`

```dockerfile
```

-	Layers:
	-	`sha256:2fb63288a29f09bf121c6cc8325413e93af6dc509115283abdb19d1d606ae116`  
		Last Modified: Tue, 17 Feb 2026 19:47:00 GMT  
		Size: 195.0 KB (195000 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:43616ca030fe0786bf5f27d9be8487f2fc7440314af387f47f20a961438454c8`  
		Last Modified: Tue, 17 Feb 2026 19:47:00 GMT  
		Size: 25.2 KB (25152 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20260215-alpine` - linux; riscv64

```console
$ docker pull golang@sha256:845c44f9ea83a2c53f90d46612cd5f95e0c1e5e3a64daa16773d19f7d5357867
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.6 MB (94573096 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7286859aa11ba47154b7adccb5531bcb9f4efb26b92a1ad19cfcc7d858911ac3`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 03:47:28 GMT
ADD alpine-minirootfs-3.23.3-riscv64.tar.gz / # buildkit
# Wed, 28 Jan 2026 03:47:28 GMT
CMD ["/bin/sh"]
# Thu, 29 Jan 2026 19:12:20 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 17 Feb 2026 22:21:24 GMT
ENV GOTOOLCHAIN=local
# Tue, 17 Feb 2026 22:21:24 GMT
ENV GOPATH=/go
# Tue, 17 Feb 2026 22:21:24 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Feb 2026 22:21:24 GMT
COPY /target/ / # buildkit
# Tue, 17 Feb 2026 23:07:21 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 17 Feb 2026 23:07:21 GMT
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
	-	`sha256:746d06a89f8430c7cc24c4e8f4767315a6df68190cd8dd8e473b0861cbc69392`  
		Last Modified: Tue, 17 Feb 2026 22:28:17 GMT  
		Size: 90.7 MB (90691146 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbea6412de5114a9446e334ce60a5dd58d568d81f90aaec1cff4eb2d7c54712c`  
		Last Modified: Tue, 17 Feb 2026 23:08:34 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20260215-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:ed18e2ef55490cad5ac8b40074d826f1664916920bb8022515cf353fdbd1fb0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.1 KB (220149 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57e5f8e74313d3ff7a8270fd73475f1c9bcc721f083e270f9f4d9f45a5324bad`

```dockerfile
```

-	Layers:
	-	`sha256:ee4d14519cec3ff2ba50c4dd2c737fb1558c28b7be7ba75dc2f214445daeceb2`  
		Last Modified: Tue, 17 Feb 2026 23:08:34 GMT  
		Size: 195.0 KB (194996 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:98655f1470ebcf132a8c89f3245f1f29953053e97c12836638e450491f45779c`  
		Last Modified: Tue, 17 Feb 2026 23:08:34 GMT  
		Size: 25.2 KB (25153 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20260215-alpine` - linux; s390x

```console
$ docker pull golang@sha256:26c56ce0484a11ab78a7d609bafb42368dec190cdaf3bdcc3b03114594e90650
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.8 MB (96769396 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b342624de64c9eb0d406c27bf2da0bf8a268e093d45bb6bbde89b2227e729c9a`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:06 GMT
ADD alpine-minirootfs-3.23.3-s390x.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:06 GMT
CMD ["/bin/sh"]
# Mon, 09 Feb 2026 20:00:18 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 17 Feb 2026 19:29:49 GMT
ENV GOTOOLCHAIN=local
# Tue, 17 Feb 2026 19:29:49 GMT
ENV GOPATH=/go
# Tue, 17 Feb 2026 19:29:49 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Feb 2026 19:29:49 GMT
COPY /target/ / # buildkit
# Tue, 17 Feb 2026 19:30:33 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 17 Feb 2026 19:30:33 GMT
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
	-	`sha256:8a6b6bbd9c00c665dfd4909e8016410533856709507819e5042a938a46f4e345`  
		Last Modified: Tue, 17 Feb 2026 19:30:38 GMT  
		Size: 92.7 MB (92746731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7dc0355d1c2afbc08006f2804a7ff0bf33d17c792b7abb6a159b23dbe05b98ed`  
		Last Modified: Tue, 17 Feb 2026 19:31:01 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20260215-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:c7840bf885e2f887d4836f67450e55fe3f7c5058c7bad1752349063db72e9fe1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.9 KB (219872 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e05c91af0a5bf6612c265614afe684632c40cde1a1404f2d91860560fc259157`

```dockerfile
```

-	Layers:
	-	`sha256:b90d8961da3c2e4ccf38d270330fcb73b4ce368e62b174dd62c9efb461ddf13c`  
		Last Modified: Tue, 17 Feb 2026 19:31:01 GMT  
		Size: 194.9 KB (194950 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:89f63491f7afd7f1ff759ff138452d27dde758672f27b2312395352ee07009e3`  
		Last Modified: Tue, 17 Feb 2026 19:31:01 GMT  
		Size: 24.9 KB (24922 bytes)  
		MIME: application/vnd.in-toto+json
