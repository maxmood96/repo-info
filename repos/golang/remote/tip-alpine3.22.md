## `golang:tip-alpine3.22`

```console
$ docker pull golang@sha256:6bfa26feb2f6864331794e62c84b3d52f84f93849fd7feb15ceb728058a2aedc
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
$ docker pull golang@sha256:23896edb50a717e40dec51d85aebbdfe8da0a59ebe26ae8d45b4a4bcf91aed8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.2 MB (87205874 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d081f96461ebba9824c6346f66363d02447801ce9065406d52f0381a75f04f06`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Mon, 25 Aug 2025 05:23:19 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 25 Aug 2025 05:23:19 GMT
ENV GOTOOLCHAIN=local
# Mon, 25 Aug 2025 05:23:19 GMT
ENV GOPATH=/go
# Mon, 25 Aug 2025 05:23:19 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 25 Aug 2025 05:23:19 GMT
COPY /target/ / # buildkit
# Mon, 25 Aug 2025 05:23:19 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 25 Aug 2025 05:23:19 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:9824c27679d3b27c5e1cb00a73adb6f4f8d556994111c12db3c5d61a0c843df8`  
		Last Modified: Tue, 15 Jul 2025 19:00:01 GMT  
		Size: 3.8 MB (3799689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9e71ab178a9b051972780ce56aaadba9695f986abc5c0f20ae604d0be3a7119`  
		Last Modified: Mon, 25 Aug 2025 21:10:07 GMT  
		Size: 282.4 KB (282439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d550b0c36e09ff5790a4933d03a35b9476508e0154ee793c00f79de3ac387e9f`  
		Last Modified: Mon, 25 Aug 2025 21:00:15 GMT  
		Size: 83.1 MB (83123589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a68f886345db6f2729fcb39a9a98aa8708e2f3a01583014c0e5f58b95d4e6a20`  
		Last Modified: Mon, 25 Aug 2025 21:10:08 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.22` - unknown; unknown

```console
$ docker pull golang@sha256:34e2dcce0d94a9a9f7ecff1eb990abfcb716673d5ff1cbf10c707c203286d939
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **216.7 KB (216665 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d36a956570bce0ca6ec6cff522735c7424a2019b26b3013fcff1cb8ba7a843a`

```dockerfile
```

-	Layers:
	-	`sha256:86c11dc4b24cc746f12eb81a47832a8dd4a85cb72d034a0e974d661e3b38c6da`  
		Last Modified: Mon, 25 Aug 2025 23:23:52 GMT  
		Size: 191.5 KB (191527 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:04262e6960e631bbb252224c9cc920e551ca7410a591da9c3692f41a421a3db8`  
		Last Modified: Mon, 25 Aug 2025 23:23:53 GMT  
		Size: 25.1 KB (25138 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.22` - linux; arm variant v6

```console
$ docker pull golang@sha256:11299e4a154932113810a60328013680c53010977978b741a74612bafcf612f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.2 MB (84182505 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af9232ca4836138f85e0fc5403fe91cf26adaf82dae84bb581e223e603177570`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-armhf.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Mon, 25 Aug 2025 05:23:19 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 25 Aug 2025 05:23:19 GMT
ENV GOTOOLCHAIN=local
# Mon, 25 Aug 2025 05:23:19 GMT
ENV GOPATH=/go
# Mon, 25 Aug 2025 05:23:19 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 25 Aug 2025 05:23:19 GMT
COPY /target/ / # buildkit
# Mon, 25 Aug 2025 05:23:19 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 25 Aug 2025 05:23:19 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:06bab5e847c5674d6ec26b342cc11d7a051a6a231e5db8a955d57bc9f4ab5595`  
		Last Modified: Tue, 15 Jul 2025 18:59:34 GMT  
		Size: 3.5 MB (3500910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33f95cea4c439fb384d1bd6927f75cd3bde82d7a5909bb38cec72c9923ca463a`  
		Last Modified: Tue, 15 Jul 2025 22:55:40 GMT  
		Size: 283.3 KB (283329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd98b83e5330c143d00b2c8248b06ddea895a2afbc3fa4a33290659882f6ffde`  
		Last Modified: Mon, 25 Aug 2025 20:59:45 GMT  
		Size: 80.4 MB (80398108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03bc7f2b963d77e35a6b6d2857f45462649991de13e4fedc1b4cb763013a8483`  
		Last Modified: Mon, 25 Aug 2025 20:59:49 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.22` - unknown; unknown

```console
$ docker pull golang@sha256:7c1e81e8f323a47bee459749149b1b231359577db299c824bcc7afeca08f537d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.0 KB (25047 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17310eae16bd2076562a24dcd7c16ff319089a020f4f042136eded94ccbc6bfb`

```dockerfile
```

-	Layers:
	-	`sha256:6844194d51f2d6277bc0e58bee3ebb5edb8e44f2897677c46060c48fcc35949e`  
		Last Modified: Mon, 25 Aug 2025 23:23:57 GMT  
		Size: 25.0 KB (25047 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.22` - linux; arm variant v7

```console
$ docker pull golang@sha256:947351ff22f27e8a0fbfda5e944a959b8b67e52d8a9bc1c7b5a2e1587433e85e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.7 MB (83659832 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6fba38b4119e2944d9acb8d6917a2b09d38c8ed378c91b55e2e36bb8b2f0f3c0`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-armv7.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Mon, 25 Aug 2025 05:23:19 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 25 Aug 2025 05:23:19 GMT
ENV GOTOOLCHAIN=local
# Mon, 25 Aug 2025 05:23:19 GMT
ENV GOPATH=/go
# Mon, 25 Aug 2025 05:23:19 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 25 Aug 2025 05:23:19 GMT
COPY /target/ / # buildkit
# Mon, 25 Aug 2025 05:23:19 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 25 Aug 2025 05:23:19 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:5ee064f8764b09a64829b58705219a88e0b13243f7f403d66ac0c639640426a5`  
		Last Modified: Tue, 15 Jul 2025 19:04:18 GMT  
		Size: 3.2 MB (3219038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74d1c7cd6f49363bcd6156bb689087c0a4e1624bb6497290e03e589310895c3e`  
		Last Modified: Tue, 15 Jul 2025 23:00:53 GMT  
		Size: 282.5 KB (282485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b7bbceab697cd612c9df9f47bcc80c06c8d22159be94df3795ecdee732a36e0`  
		Last Modified: Mon, 25 Aug 2025 21:33:11 GMT  
		Size: 80.2 MB (80158151 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0bd7ec1ca8d948ab444092a8639c440ccc3483ab9827427a707bb9ae88608eb`  
		Last Modified: Mon, 25 Aug 2025 21:39:13 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.22` - unknown; unknown

```console
$ docker pull golang@sha256:2ccd13eda719ce91a05df8836f97fd1373569a1b4c152f458781ee03817f0232
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **216.8 KB (216811 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:925000e93766b3be9ea93d5086e9904c0f2da85b53d14539c8795359c35b362f`

```dockerfile
```

-	Layers:
	-	`sha256:2a1823c601af5f5048bd1d5f41d7c48cf9046666e967b1a4b0a27d6451e229db`  
		Last Modified: Mon, 25 Aug 2025 23:24:00 GMT  
		Size: 191.5 KB (191549 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c891ca65c0a2c7db6d9ce69f7d398c677c862844202b771645e1afe3c397d239`  
		Last Modified: Mon, 25 Aug 2025 23:24:02 GMT  
		Size: 25.3 KB (25262 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.22` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:c8c35bdb8fcb3f86bfb5f9ab34199f2839d52a03407a4c08267ff428de98314a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.5 MB (83533986 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:665d4792e8d36b249abfae7ff18ae1ac5120a7eae97f5e4fcb586646425d9e38`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-aarch64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Mon, 25 Aug 2025 05:23:19 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 25 Aug 2025 05:23:19 GMT
ENV GOTOOLCHAIN=local
# Mon, 25 Aug 2025 05:23:19 GMT
ENV GOPATH=/go
# Mon, 25 Aug 2025 05:23:19 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 25 Aug 2025 05:23:19 GMT
COPY /target/ / # buildkit
# Mon, 25 Aug 2025 05:23:19 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 25 Aug 2025 05:23:19 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:6e174226ea690ced550e5641249a412cdbefd2d09871f3e64ab52137a54ba606`  
		Last Modified: Tue, 15 Jul 2025 18:59:50 GMT  
		Size: 4.1 MB (4130750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d6e0c986dc92724f88716366774abec9cec3d3a68fb39a938496715d1f61a3f`  
		Last Modified: Mon, 18 Aug 2025 22:17:40 GMT  
		Size: 284.7 KB (284708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9eee5969e4377d6381f91daec759a184ca62e8181048bb70f3b9df717a06ab4a`  
		Last Modified: Mon, 25 Aug 2025 21:23:21 GMT  
		Size: 79.1 MB (79118369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff850caa48112e8f31534d8592d26d14558976a10787a44873c6cb2fd8826b9b`  
		Last Modified: Mon, 25 Aug 2025 21:27:47 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.22` - unknown; unknown

```console
$ docker pull golang@sha256:726f2821eb1b6baee5e011fa0a8747e443414d22cb3c3f4995b886435da669cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **216.9 KB (216881 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df51b13ff75917ff5de634cf6951a3967c60176ba936fdf5265a1be47f8ad047`

```dockerfile
```

-	Layers:
	-	`sha256:905494054f154fb9d8901a34acf8c5d1bd0d0f8363ea0f39e4406fa38f7c5de4`  
		Last Modified: Mon, 25 Aug 2025 23:24:05 GMT  
		Size: 191.6 KB (191583 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7d3ad18b95cffa537c18fb1b50eaa8af9cb7c9b1f2b2812b23b08be89a2ebe38`  
		Last Modified: Mon, 25 Aug 2025 23:24:06 GMT  
		Size: 25.3 KB (25298 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.22` - linux; 386

```console
$ docker pull golang@sha256:a385c089125410f475433f4f24d471441322b064935102287fe6210939acfe46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.7 MB (85659319 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d85a9402ec0306f1c0b86b2fd66535d817671bbe6849f0e6d230a64f86e23a7`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-x86.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Mon, 25 Aug 2025 05:23:19 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 25 Aug 2025 05:23:19 GMT
ENV GOTOOLCHAIN=local
# Mon, 25 Aug 2025 05:23:19 GMT
ENV GOPATH=/go
# Mon, 25 Aug 2025 05:23:19 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 25 Aug 2025 05:23:19 GMT
COPY /target/ / # buildkit
# Mon, 25 Aug 2025 05:23:19 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 25 Aug 2025 05:23:19 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:a55f2fb89da4caae0d783c0045a67446dee9bbd977fecb44db9e1231550fa888`  
		Last Modified: Tue, 15 Jul 2025 19:04:11 GMT  
		Size: 3.6 MB (3615006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae39603b8b954ab3a1e128477545eb64eaaa25918c295991c2190561fb351304`  
		Last Modified: Mon, 25 Aug 2025 20:59:54 GMT  
		Size: 282.9 KB (282930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed00e4afa60c0f083e905e3cb9e3fb29568be047d47ced8ca60d1231e5101266`  
		Last Modified: Mon, 25 Aug 2025 21:00:07 GMT  
		Size: 81.8 MB (81761224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af82c9483079a93cc5b28a62ea9885cc298b593a653bf0c7b643105843bc8a5c`  
		Last Modified: Mon, 25 Aug 2025 20:59:54 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.22` - unknown; unknown

```console
$ docker pull golang@sha256:636d8732565c393d89a21d230e6006357f9ce3b8f0026c6a3e3b106598d0d0a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **216.6 KB (216582 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4beaa51fe86952c23a6a6666ef174e8fd6fb3b59803b86f87c270b7972cc2faf`

```dockerfile
```

-	Layers:
	-	`sha256:f198eb2a3815c22495a35cb656dd906de427361c3871b9d7f6889b3c899108b8`  
		Last Modified: Mon, 25 Aug 2025 23:24:11 GMT  
		Size: 191.5 KB (191488 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1ece1273e7e386cb577dc1fdcc8a6cab15c3862674afb971c4592e61c3d24bc7`  
		Last Modified: Mon, 25 Aug 2025 23:24:12 GMT  
		Size: 25.1 KB (25094 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.22` - linux; ppc64le

```console
$ docker pull golang@sha256:99f86f11a079d5f0286c128f538690f9e7d78120e50b0feef374550e76118075
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.5 MB (84489232 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a52ac819b4cb09558e5e633e5ab4845169c3e40d0de58a701a3a7e609cdfc8e1`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-ppc64le.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Mon, 25 Aug 2025 05:23:19 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 25 Aug 2025 05:23:19 GMT
ENV GOTOOLCHAIN=local
# Mon, 25 Aug 2025 05:23:19 GMT
ENV GOPATH=/go
# Mon, 25 Aug 2025 05:23:19 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 25 Aug 2025 05:23:19 GMT
COPY /target/ / # buildkit
# Mon, 25 Aug 2025 05:23:19 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 25 Aug 2025 05:23:19 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:b762f678859bfa5c3948b5f1b04959aa43c8aba88e2389e281413d303d62a7e3`  
		Last Modified: Tue, 15 Jul 2025 18:59:53 GMT  
		Size: 3.7 MB (3727111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0afe3e6d4a1713a75edf1789d38233b2e8d48f54cebae5e9d0789eb1af52023b`  
		Last Modified: Mon, 28 Jul 2025 20:30:54 GMT  
		Size: 285.1 KB (285114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f497bb9c72f47bbbcc0dbb56c1882627096799f2972f4f6a666d6c33790ad02`  
		Last Modified: Mon, 25 Aug 2025 21:29:02 GMT  
		Size: 80.5 MB (80476849 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8a5c6071d7fabcb815879dde06f981bce1a4308c247b38e77d5c3ee60a7b81a`  
		Last Modified: Mon, 25 Aug 2025 21:49:57 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.22` - unknown; unknown

```console
$ docker pull golang@sha256:2ecfd5a30b9b5556d67bc136f48b5c32aa40974fb138a0df6ac79a72bee5d833
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **214.8 KB (214820 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83acb3b48024637f4d9aa1fa1a97ad6d8b4ecba97b6ca065fa4e5d03100e600e`

```dockerfile
```

-	Layers:
	-	`sha256:8397ee7f5e8eaec8e9e4435a14b541528964a930dbf69e1c3428f87016aaea93`  
		Last Modified: Mon, 25 Aug 2025 23:24:16 GMT  
		Size: 189.6 KB (189624 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c03d2e7aeaa657b5cfe0fc977af8e97862817a3d0e62ae3cfb8637eed5b4483d`  
		Last Modified: Mon, 25 Aug 2025 23:24:17 GMT  
		Size: 25.2 KB (25196 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.22` - linux; riscv64

```console
$ docker pull golang@sha256:d042fe8af67c6d299a1d8d87748db9ffd8b5212b7c84058dbe49e52a0585b221
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.3 MB (84338837 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0b828ef95e61f895dbb22e2906f344c055d0353184eeca86a792415bfd240df`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-riscv64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Mon, 25 Aug 2025 05:23:19 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 25 Aug 2025 05:23:19 GMT
ENV GOTOOLCHAIN=local
# Mon, 25 Aug 2025 05:23:19 GMT
ENV GOPATH=/go
# Mon, 25 Aug 2025 05:23:19 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 25 Aug 2025 05:23:19 GMT
COPY /target/ / # buildkit
# Mon, 25 Aug 2025 05:23:19 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 25 Aug 2025 05:23:19 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:cbe7080b5783de104ad67ff4595bfa8ae70a597181a84621f51c5ccd084218da`  
		Last Modified: Tue, 15 Jul 2025 19:00:17 GMT  
		Size: 3.5 MB (3512801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31e09396f9703679f1457da8ea8533cdf5f2a459c8f9efa4664152e578880b25`  
		Last Modified: Mon, 21 Jul 2025 22:46:21 GMT  
		Size: 282.8 KB (282780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1ac3adf7235fc0890689e2afe7d90ea2dd292a1a4a374507a33ca8646f6e0ad`  
		Last Modified: Tue, 26 Aug 2025 19:38:12 GMT  
		Size: 80.5 MB (80543098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3668b5e20e255b6cf3866e1ce7ce2bb9bbabd8200331d6588b1c74ae1c9b4f03`  
		Last Modified: Tue, 26 Aug 2025 20:12:02 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.22` - unknown; unknown

```console
$ docker pull golang@sha256:9b530cbfa5530c9eeae4bd9caed69cc2122cd2ab42f7233f747ff57fa2a8953c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **214.8 KB (214816 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b456d3d4872434972447ecc8bf493878ccc9e36ed74723fa4d8cdd8f74a3317`

```dockerfile
```

-	Layers:
	-	`sha256:dc2256704419894f6251881ec58604390726a634637ee96bf5fc67f604a93845`  
		Last Modified: Tue, 26 Aug 2025 23:23:35 GMT  
		Size: 189.6 KB (189620 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9ba499ad9c88a9146cfb9cef41e0cb83cc0c0431b939e6a1428ee102047a1239`  
		Last Modified: Tue, 26 Aug 2025 23:23:36 GMT  
		Size: 25.2 KB (25196 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.22` - linux; s390x

```console
$ docker pull golang@sha256:43179f0451810b916d4a0e1afabf734770cf117e307a987835a4dfbfdf588731
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.6 MB (85613923 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c3e47109ce94f595ec10b72a9635408f2d01cf02ab4a7bf6139b7bb00ce76ac`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-s390x.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Mon, 25 Aug 2025 05:23:19 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 25 Aug 2025 05:23:19 GMT
ENV GOTOOLCHAIN=local
# Mon, 25 Aug 2025 05:23:19 GMT
ENV GOPATH=/go
# Mon, 25 Aug 2025 05:23:19 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 25 Aug 2025 05:23:19 GMT
COPY /target/ / # buildkit
# Mon, 25 Aug 2025 05:23:19 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 25 Aug 2025 05:23:19 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:5d29754ce036967079405405a04a54a7d3f8ba85e0057b6bdda3d03aa59c8361`  
		Last Modified: Tue, 15 Jul 2025 19:00:06 GMT  
		Size: 3.6 MB (3644971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cef24d483efe8f2b1053cb578dbafbffab2dfd6a644764474184fb805fc872f3`  
		Last Modified: Mon, 28 Jul 2025 20:31:35 GMT  
		Size: 283.5 KB (283470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4bb0635d2e248956f88a4462ee973445c0bd3979670795027980550063343c5`  
		Last Modified: Mon, 25 Aug 2025 21:46:03 GMT  
		Size: 81.7 MB (81685324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e26b5e15cea26bfba3d806b305de0e048ed58f73c6c7fbfccf118149635cc72a`  
		Last Modified: Mon, 25 Aug 2025 21:52:54 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.22` - unknown; unknown

```console
$ docker pull golang@sha256:dc50af86fc91919aad11b3f5166f550f61e7c5b4ac48d62baf5bde048ba0b2d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **214.7 KB (214714 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3df7b02b1cb904c52424d2f577ea0dff59654d22d5e02edc4a57445fb06b988`

```dockerfile
```

-	Layers:
	-	`sha256:aa8b03892fb0e78eee48e31ffa68a60c8cadc32553474c81197e2e73786f2721`  
		Last Modified: Mon, 25 Aug 2025 23:24:22 GMT  
		Size: 189.6 KB (189576 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2662e12a48a27fd6fe7002c85b493cfb4f5be545e91631b9065ee793dceffddf`  
		Last Modified: Mon, 25 Aug 2025 23:24:23 GMT  
		Size: 25.1 KB (25138 bytes)  
		MIME: application/vnd.in-toto+json
