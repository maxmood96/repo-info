## `golang:tip-20251128-alpine`

```console
$ docker pull golang@sha256:7fc43152074c03426e3e625b5efcc53e034fd611342a13980279e69a9d79e1fa
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

### `golang:tip-20251128-alpine` - linux; amd64

```console
$ docker pull golang@sha256:c5b73161739c9b6f92e6f4f8403b51523b7649c0fbda1fb3a73bb60c4e3ca04f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.3 MB (98268784 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b1d0ba8c053183d44a2dc763eb5191f5bfb047c51000ed7f96a0046dfcb4c1e`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 03 Dec 2025 19:30:18 GMT
ADD alpine-minirootfs-3.23.0-x86_64.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:30:18 GMT
CMD ["/bin/sh"]
# Thu, 04 Dec 2025 01:06:11 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Thu, 04 Dec 2025 01:08:03 GMT
ENV GOTOOLCHAIN=local
# Thu, 04 Dec 2025 01:08:03 GMT
ENV GOPATH=/go
# Thu, 04 Dec 2025 01:08:03 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Dec 2025 01:08:03 GMT
COPY /target/ / # buildkit
# Thu, 04 Dec 2025 01:08:05 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Thu, 04 Dec 2025 01:08:05 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:014e56e613968f73cce0858124ca5fbc601d7888099969a4eea69f31dcd71a53`  
		Last Modified: Wed, 03 Dec 2025 19:30:44 GMT  
		Size: 3.9 MB (3859315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cca7d25f1ca5f66d1b956daa0950a4de851602c86ba2812bdb5958091ee7aff7`  
		Last Modified: Thu, 04 Dec 2025 01:08:25 GMT  
		Size: 296.1 KB (296079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9da39c78191c9be13a8adf6d46ca789532fb58292a09979c1057608fd7cf7b31`  
		Last Modified: Mon, 01 Dec 2025 23:57:34 GMT  
		Size: 94.1 MB (94113232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3385dca4d1d17ff150d198e24f4ee0f0b2a64534161379ed67a63e758ef95d97`  
		Last Modified: Thu, 04 Dec 2025 01:08:24 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20251128-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:9116d6d7c7dd6a50dacc119ee7739067ec92aa21ac768218321badf6590fcd76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.7 KB (220698 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22897ea54b1850a25d21eb7b185f4e3909af7361690c1cde64fa292a91fefa57`

```dockerfile
```

-	Layers:
	-	`sha256:2536837bfaa6cc263e7982b73e70e3a6ab7bdc79d07846f5f9cb516427218111`  
		Last Modified: Thu, 04 Dec 2025 03:25:08 GMT  
		Size: 195.6 KB (195603 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:da1d9860593c9affde0f5146d51f9d06017b83c8573c917261df4ed761596e1f`  
		Last Modified: Thu, 04 Dec 2025 03:25:09 GMT  
		Size: 25.1 KB (25095 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20251128-alpine` - linux; arm variant v6

```console
$ docker pull golang@sha256:004553dee039f21834d7bf8c29d28791d94d03e79b7a8f347b3031a9389cbf74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.3 MB (94343778 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0de825db5280cc24cefa678d92b0986cc797c18675a210b9036edc2e3d5660b2`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 03 Dec 2025 19:30:25 GMT
ADD alpine-minirootfs-3.23.0-armhf.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:30:25 GMT
CMD ["/bin/sh"]
# Thu, 04 Dec 2025 01:14:00 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Thu, 04 Dec 2025 01:16:50 GMT
ENV GOTOOLCHAIN=local
# Thu, 04 Dec 2025 01:16:50 GMT
ENV GOPATH=/go
# Thu, 04 Dec 2025 01:16:50 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Dec 2025 01:16:50 GMT
COPY /target/ / # buildkit
# Thu, 04 Dec 2025 01:16:53 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Thu, 04 Dec 2025 01:16:53 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:dd0740468c9e19d93d459e4637a652c4fb8e1012c1adeac2e7311f14dcd210f6`  
		Last Modified: Wed, 03 Dec 2025 19:30:39 GMT  
		Size: 3.6 MB (3567894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca2273dcce6994a082ced43419fe0614bd5a116638d0390d36b107c676b4ef8c`  
		Last Modified: Thu, 04 Dec 2025 01:17:10 GMT  
		Size: 297.3 KB (297269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78cef798cb03bb0097c86699403eb8a58ab2cf9b985080b34f19c3c37355503d`  
		Last Modified: Mon, 01 Dec 2025 23:59:35 GMT  
		Size: 90.5 MB (90478457 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4737ac4d30a7be22051af87b4c0d934ef1370c13ae15469148b9dc8043c0e29a`  
		Last Modified: Thu, 04 Dec 2025 01:17:10 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20251128-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:a066138934074a90f902e698358d826dac172280aabdc25184437fa93ff935ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.0 KB (25008 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81f0fe76bde610cc648691b12937f9aa776bd2a6ed75d1d8e20cf04eda392958`

```dockerfile
```

-	Layers:
	-	`sha256:6382600b166c430124d7060f609ef714c97676db01dde7235e05cf6ea3c32699`  
		Last Modified: Thu, 04 Dec 2025 03:25:12 GMT  
		Size: 25.0 KB (25008 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20251128-alpine` - linux; arm variant v7

```console
$ docker pull golang@sha256:618c3791a801cf20206f71ef792132655466dda6f58dd17c529dafff17babdca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.8 MB (93773149 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:457f4e9d6a11539bbfef108f72a890aff92ad0699eac279fafdd0cc47f953302`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 03 Dec 2025 19:30:51 GMT
ADD alpine-minirootfs-3.23.0-armv7.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:30:51 GMT
CMD ["/bin/sh"]
# Thu, 04 Dec 2025 01:13:37 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Thu, 04 Dec 2025 01:16:17 GMT
ENV GOTOOLCHAIN=local
# Thu, 04 Dec 2025 01:16:17 GMT
ENV GOPATH=/go
# Thu, 04 Dec 2025 01:16:17 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Dec 2025 01:16:17 GMT
COPY /target/ / # buildkit
# Thu, 04 Dec 2025 01:16:20 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Thu, 04 Dec 2025 01:16:20 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:5f34bcd7b3c0108b00e414f3370e9140a1cb6e02ec1caaa14ff2f25408910a24`  
		Last Modified: Wed, 03 Dec 2025 19:31:07 GMT  
		Size: 3.3 MB (3278466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7abc693d885bf364e8b34e42178f64da47e69dd89af6653d0104983dec493d28`  
		Last Modified: Thu, 04 Dec 2025 01:16:39 GMT  
		Size: 296.2 KB (296179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cb1234642b8e59fff163165b022247bc43b3cbce7229072851dbefb3454b51c`  
		Last Modified: Mon, 01 Dec 2025 23:59:32 GMT  
		Size: 90.2 MB (90198345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a3c542828a51e53ce31c2a6e9a19336e8a2254876e74c660a647e4f06ec846f`  
		Last Modified: Thu, 04 Dec 2025 01:16:44 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20251128-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:4b77526bfe55d3ab7ba755a320bc5211058e0edd59bf55897cc49f5cc93e2c4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.2 KB (220196 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:010349a4533a8eb9c7ecd61394ff4b9593529c0d48bc0bb649ae41728eca33da`

```dockerfile
```

-	Layers:
	-	`sha256:02a846507cba888c7727e9fea11832b42bea8f19971b0e0979deaf3f4be196b4`  
		Last Modified: Thu, 04 Dec 2025 03:25:16 GMT  
		Size: 195.0 KB (194973 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:178c27770aa22f4d82d615fda2406e5528c5c0a061824babf236fffcc6cbd750`  
		Last Modified: Thu, 04 Dec 2025 03:25:16 GMT  
		Size: 25.2 KB (25223 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20251128-alpine` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:6e6efe296859e029040574d6a90354696589778a5b40461a2a335494f0110f39
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.7 MB (93705576 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72eeae3d30a329ddabf375daf13d1de325a4bbc2ff57906559dec02bd50f68a3`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 03 Dec 2025 19:30:17 GMT
ADD alpine-minirootfs-3.23.0-aarch64.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:30:17 GMT
CMD ["/bin/sh"]
# Thu, 04 Dec 2025 01:05:04 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Thu, 04 Dec 2025 01:06:45 GMT
ENV GOTOOLCHAIN=local
# Thu, 04 Dec 2025 01:06:45 GMT
ENV GOPATH=/go
# Thu, 04 Dec 2025 01:06:45 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Dec 2025 01:06:45 GMT
COPY /target/ / # buildkit
# Thu, 04 Dec 2025 01:06:48 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Thu, 04 Dec 2025 01:06:48 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:0bd713040ebbdef7247f70b0753f8fb2f410e8eb358e95af409a8412b9847d78`  
		Last Modified: Wed, 03 Dec 2025 19:30:49 GMT  
		Size: 4.2 MB (4195200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b146eabfc1d80e1a2a60ebc6496ddc6b01317278a074627090af68251d8208a`  
		Last Modified: Thu, 04 Dec 2025 01:07:20 GMT  
		Size: 298.8 KB (298812 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de5ad4011b8323fe08610380aae994bb765f6965dfc1e0886815c89502e86415`  
		Last Modified: Mon, 01 Dec 2025 23:57:41 GMT  
		Size: 89.2 MB (89211407 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ecd9192de60c4c1bfcffb23f5c4c56acedab81bde65c505b9e1befde1c169de`  
		Last Modified: Thu, 04 Dec 2025 01:07:20 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20251128-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:f57fcb6b1942af0e8bbe1502ef1551aad41484206e6ac4443e9c66ddbbeda7f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.3 KB (220264 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:359feb83678727c1d1fd90d93fb449d73d426ba317a78e9c2378a6cbbc0e3769`

```dockerfile
```

-	Layers:
	-	`sha256:1b81414018b40a318037c23046441704f76b01017102ec995221ed94ab31b13c`  
		Last Modified: Thu, 04 Dec 2025 03:25:19 GMT  
		Size: 195.0 KB (195009 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b75f15809f2f90c778760052e785e110f234b89e09b77eebd59ad02c79200ed5`  
		Last Modified: Thu, 04 Dec 2025 03:25:20 GMT  
		Size: 25.3 KB (25255 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20251128-alpine` - linux; 386

```console
$ docker pull golang@sha256:58b35a98229640ee17b930bc5526454a24c833cf219ccbc7c3c50232556e2d8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.0 MB (96011081 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de09b602a77a53aba2dd3056964bdf56dd5e4654f7c6b9f4b25b86807204d8b9`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 03 Dec 2025 19:30:18 GMT
ADD alpine-minirootfs-3.23.0-x86.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:30:18 GMT
CMD ["/bin/sh"]
# Thu, 04 Dec 2025 01:08:41 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Thu, 04 Dec 2025 01:10:49 GMT
ENV GOTOOLCHAIN=local
# Thu, 04 Dec 2025 01:10:49 GMT
ENV GOPATH=/go
# Thu, 04 Dec 2025 01:10:49 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Dec 2025 01:10:49 GMT
COPY /target/ / # buildkit
# Thu, 04 Dec 2025 01:10:51 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Thu, 04 Dec 2025 01:10:51 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:3527b4f952d5950d8caa74dc0d1759215000f2f0a195344f0239c7e2805fe2fc`  
		Last Modified: Wed, 03 Dec 2025 19:30:41 GMT  
		Size: 3.7 MB (3685856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6ed78a91c31c3fdd738d645d1c11b00d822026fd48c1c21e63e55917a481da1`  
		Last Modified: Thu, 04 Dec 2025 01:11:13 GMT  
		Size: 296.7 KB (296661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a64bdcb75a4ff23e4aa0af6e0121aa066fd65b3acbe84f5a324aa319fab9e281`  
		Last Modified: Tue, 02 Dec 2025 00:00:09 GMT  
		Size: 92.0 MB (92028405 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:598b5c81717447f80aace627d38b84400d84af0d83cdf52858a2f19179f77551`  
		Last Modified: Thu, 04 Dec 2025 01:11:14 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20251128-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:14da573515f9bb4694770eb982fc028023fede8f7ecd6bf0a9f5d3ce41740db3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.6 KB (220614 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8643b8b1b0aab0dffe79db74f6e75a39df28952808628d17d27bae418cc6cf73`

```dockerfile
```

-	Layers:
	-	`sha256:82d5deffc23412d632dfafa7864578e6400de653654d5e3b3370d4b8b6377ab4`  
		Last Modified: Thu, 04 Dec 2025 03:25:23 GMT  
		Size: 195.6 KB (195562 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:242c64b29d5dbb0a0b7de545dd9d53d95c8424ae505b5dfdffc2758b31f14e4c`  
		Last Modified: Thu, 04 Dec 2025 03:25:24 GMT  
		Size: 25.1 KB (25052 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20251128-alpine` - linux; ppc64le

```console
$ docker pull golang@sha256:7dd6b50c282abe79a330545dae679b08e08ebe00c81dc69861f1fe39e77af500
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.9 MB (94867551 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a80e831dc3b9bbb72bc7570534488eb5d5c6d1333ea58103a9695d1d4b3b101d`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 03 Dec 2025 19:29:24 GMT
ADD alpine-minirootfs-3.23.0-ppc64le.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:29:24 GMT
CMD ["/bin/sh"]
# Thu, 04 Dec 2025 00:32:26 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 02 Dec 2025 02:50:37 GMT
ENV GOTOOLCHAIN=local
# Tue, 02 Dec 2025 02:50:37 GMT
ENV GOPATH=/go
# Tue, 02 Dec 2025 02:50:37 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Dec 2025 02:50:37 GMT
COPY /target/ / # buildkit
# Thu, 04 Dec 2025 01:39:09 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Thu, 04 Dec 2025 01:39:10 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:bebb36295c11d2d52cd92944b382c4aa60dce148b63090816248052f38358488`  
		Last Modified: Wed, 03 Dec 2025 19:29:52 GMT  
		Size: 3.8 MB (3827017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c46fe31eb99c053ebac4e4c6c1a45a59669d0a894f8d034aa0117e8363cd3e5b`  
		Last Modified: Thu, 04 Dec 2025 00:33:51 GMT  
		Size: 299.2 KB (299245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:060ee4242807d5eec61fa095a5c2f00f155044d9c099f2f96b9280a66eec7ef6`  
		Last Modified: Tue, 02 Dec 2025 02:52:27 GMT  
		Size: 90.7 MB (90741131 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ac53bd081f76ffe942f6e8a6b6385cefac39232908099a7ddf66797c09270c6`  
		Last Modified: Thu, 04 Dec 2025 02:09:04 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20251128-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:85238f5a3fb7c2bfc395c7977aa99a964b9ec018bcef8abe8299b29b83f1bb01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.2 KB (220155 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0979b9b1ba3b8bb4d065248c01eaf31ce481443c1a707e313873c61472372777`

```dockerfile
```

-	Layers:
	-	`sha256:d1ef97aff24db68ad207aedcdfeb1b8b1b2b4d5c5e5a1f12e0a7ce2abc0fcd65`  
		Last Modified: Thu, 04 Dec 2025 03:25:27 GMT  
		Size: 195.0 KB (195002 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:03136d574c36afd1d65e40737ea0ace47a9f8beb9920b4b922ba50b1b03c0c07`  
		Last Modified: Thu, 04 Dec 2025 03:25:28 GMT  
		Size: 25.2 KB (25153 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20251128-alpine` - linux; riscv64

```console
$ docker pull golang@sha256:eacc821e419f56b3ef42de901406191091704e0e488a8d49b2f2abe540735399
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.3 MB (95259260 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50ae7fe00d9b82753f833d29b4fac44542845d24af4ee960b445d8a13210498c`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 03 Dec 2025 19:29:39 GMT
ADD alpine-minirootfs-3.23.0-riscv64.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:29:39 GMT
CMD ["/bin/sh"]
# Thu, 04 Dec 2025 00:32:33 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 02 Dec 2025 14:37:11 GMT
ENV GOTOOLCHAIN=local
# Tue, 02 Dec 2025 14:37:11 GMT
ENV GOPATH=/go
# Tue, 02 Dec 2025 14:37:11 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Dec 2025 14:37:11 GMT
COPY /target/ / # buildkit
# Thu, 04 Dec 2025 23:22:43 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Thu, 04 Dec 2025 23:22:43 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:9929557817a4c85b33d6dbeb491f7396ef32added7e77de7ac1b644ed0975313`  
		Last Modified: Wed, 03 Dec 2025 19:30:17 GMT  
		Size: 3.6 MB (3583519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ee2260aaa09ba7162340fe5926c0fe305f447e406ba4020d7a84ed8048186cd`  
		Last Modified: Thu, 04 Dec 2025 00:35:11 GMT  
		Size: 296.5 KB (296503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab3dee934585ab74409616bca59b39f30d113b18941a71d91f5e16fd83b3d954`  
		Last Modified: Tue, 02 Dec 2025 14:44:57 GMT  
		Size: 91.4 MB (91379080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bf432bf6ab057b1b5c970884bde5d2c15ef96bd962d89e2973eca40340df0a2`  
		Last Modified: Thu, 04 Dec 2025 23:24:06 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20251128-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:16b053ac9a5b11a89a43ac86fe3e39efd64cce204fc78c2284d2ee9634b1c1fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.2 KB (220151 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:216fb7ab95c11b296d6716aa25037f64cbe64e61901b964104238a5ef03185ca`

```dockerfile
```

-	Layers:
	-	`sha256:871070051ccf56db88fd0c54c8dfcdd7894f190882873f80ec1609ee8449f148`  
		Last Modified: Fri, 05 Dec 2025 00:23:24 GMT  
		Size: 195.0 KB (194998 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9bf81196f21764474b0807fcf64ecfb322b320910088c7e20417f60033988ea8`  
		Last Modified: Fri, 05 Dec 2025 00:23:25 GMT  
		Size: 25.2 KB (25153 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20251128-alpine` - linux; s390x

```console
$ docker pull golang@sha256:9e73aadb173f2a04efb362f8139d3a2ed0caddd1fb82505658b881fc4d31814c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.3 MB (97307425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4ccd42c20005622754217c00318d067d431d9349768e13c6fdb8259e8e07537`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 03 Dec 2025 19:29:31 GMT
ADD alpine-minirootfs-3.23.0-s390x.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:29:31 GMT
CMD ["/bin/sh"]
# Thu, 04 Dec 2025 00:33:08 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 02 Dec 2025 00:24:38 GMT
ENV GOTOOLCHAIN=local
# Tue, 02 Dec 2025 00:24:38 GMT
ENV GOPATH=/go
# Tue, 02 Dec 2025 00:24:38 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Dec 2025 00:24:38 GMT
COPY /target/ / # buildkit
# Thu, 04 Dec 2025 01:29:19 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Thu, 04 Dec 2025 01:29:19 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:c7cee97a7811b4965924727bdc0a2333d48e3c6b4064a9c8867d48607fa0fc16`  
		Last Modified: Wed, 03 Dec 2025 19:30:00 GMT  
		Size: 3.7 MB (3723810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d25c90685dce29b188b5f808186e13517aabb2fb913b72d7b196b20a0850dbc`  
		Last Modified: Thu, 04 Dec 2025 00:34:26 GMT  
		Size: 297.2 KB (297183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d587a6ce9332cd64ade4d6449590e6112812b54bfc350eb8b57100babd31c208`  
		Last Modified: Tue, 02 Dec 2025 00:25:52 GMT  
		Size: 93.3 MB (93286276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f61153fc7d4eed0260e1d9f6612fe642e8fc51150a49e52fbae184c3d6e66010`  
		Last Modified: Thu, 04 Dec 2025 01:30:03 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20251128-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:a3a5e81b3c6cc9e61b2fe381aef28c4eb2f785fe0d171e781101eee9e078074f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.0 KB (220046 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0af1b8ca761283f9c0ea327dc7ae9c1b8dd73c5fb9b052f9641e9d1ae4688d8b`

```dockerfile
```

-	Layers:
	-	`sha256:83876f5033dda5261c79470c58083701490f82c991853414edddc32984e23445`  
		Last Modified: Thu, 04 Dec 2025 03:25:32 GMT  
		Size: 195.0 KB (194952 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a62be92eeaa61564ed3495e13921b2ae8fda169ef5d146c78a78a9032edbb0c8`  
		Last Modified: Thu, 04 Dec 2025 03:25:33 GMT  
		Size: 25.1 KB (25094 bytes)  
		MIME: application/vnd.in-toto+json
