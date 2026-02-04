## `golang:tip-alpine3.22`

```console
$ docker pull golang@sha256:6ec39f1f0f7834ee235267ee138a168ddcba850cceb4c95f290dd17736d78d72
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
$ docker pull golang@sha256:9eb522cea7a8a47e66704c26aa4c71a0e41dc1f3ba9720e77101c7a660bbdfcb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.4 MB (97429598 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:531b5bb3f54b76f509670793199afb6eca9a0e8a71dfd8ccf94e81771c8999dc`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:40 GMT
ADD alpine-minirootfs-3.22.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:40 GMT
CMD ["/bin/sh"]
# Wed, 04 Feb 2026 17:07:34 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Wed, 04 Feb 2026 17:09:25 GMT
ENV GOTOOLCHAIN=local
# Wed, 04 Feb 2026 17:09:25 GMT
ENV GOPATH=/go
# Wed, 04 Feb 2026 17:09:25 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Feb 2026 17:09:25 GMT
COPY /target/ / # buildkit
# Wed, 04 Feb 2026 17:09:28 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 04 Feb 2026 17:09:28 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:d49a2dee86fb12766dd648402d010ca105846a41bd58738454e53780d4bb8e97`  
		Last Modified: Wed, 28 Jan 2026 01:18:46 GMT  
		Size: 3.8 MB (3804875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd5fd34588c794cfebfb200b7161d1077c3ae21b79a1272f051bd0a537485774`  
		Last Modified: Wed, 04 Feb 2026 17:09:42 GMT  
		Size: 291.2 KB (291157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64ca55bbd490d4f215c5420355c680b71279036da5d7c91d2d678e32c231a9c9`  
		Last Modified: Mon, 02 Feb 2026 19:30:41 GMT  
		Size: 93.3 MB (93333409 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b18272c6ab698f80da913006a8e2c65d9a137b5a02d76db0cbc0adbe6991dcc`  
		Last Modified: Wed, 04 Feb 2026 17:09:42 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.22` - unknown; unknown

```console
$ docker pull golang@sha256:78241b6b43fa733cc46c021cce7415b24a3d3f301baccaaf720d843c9a807d22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.4 KB (219447 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:796f1ff75fa42bd5924cf3734efe81effa59711a7a7a43df9a0811f20e013b15`

```dockerfile
```

-	Layers:
	-	`sha256:8abede245bd2dac3ca52434a7ca51581fd9fa2beee851dbbd4a48ce9289233d3`  
		Last Modified: Wed, 04 Feb 2026 17:09:42 GMT  
		Size: 195.0 KB (194982 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:83ff84abb72e1279ecc3ec652f03c344627f720095b7699300811ffdb92cb30f`  
		Last Modified: Wed, 04 Feb 2026 17:09:42 GMT  
		Size: 24.5 KB (24465 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.22` - linux; arm variant v6

```console
$ docker pull golang@sha256:e24667b67b9564db9eab6717665aaff8c0987d0ed42e8a04d3fbd73372433933
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.6 MB (93553342 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fafc56e7cf6d8273d46c2ebea32d520fb9ed117cbef4a2f4d957fa595132c61c`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:06 GMT
ADD alpine-minirootfs-3.22.3-armhf.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:06 GMT
CMD ["/bin/sh"]
# Wed, 04 Feb 2026 17:07:25 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Wed, 04 Feb 2026 17:10:07 GMT
ENV GOTOOLCHAIN=local
# Wed, 04 Feb 2026 17:10:07 GMT
ENV GOPATH=/go
# Wed, 04 Feb 2026 17:10:07 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Feb 2026 17:10:07 GMT
COPY /target/ / # buildkit
# Wed, 04 Feb 2026 17:10:10 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 04 Feb 2026 17:10:10 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:835838571e5c80c63481753299e25a9f89f366d8f4a9c1a2043b8fdf98176f17`  
		Last Modified: Wed, 28 Jan 2026 01:18:10 GMT  
		Size: 3.5 MB (3505046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8198b2de25a14cc75238c02db65a92ee87385b213103cdbc7789ac4870ea0ff0`  
		Last Modified: Wed, 04 Feb 2026 17:10:22 GMT  
		Size: 292.3 KB (292300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2e0df2db5a6de63ae56b2b7ac54a7918fd9414ba7652c1dadac1bfb31d63c9e`  
		Last Modified: Mon, 02 Feb 2026 19:28:08 GMT  
		Size: 89.8 MB (89755840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9babea0d978f42d991fbef59001b1845447816303f61f9169a609c88ef9cc4d1`  
		Last Modified: Wed, 04 Feb 2026 17:10:21 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.22` - unknown; unknown

```console
$ docker pull golang@sha256:e8e832bc77d1a38daf71c23407c0f64f8223ed8aedf49082e9aa1290aabba665
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.4 KB (24362 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b07c0762ca331171aa06e65fc63564440c14699b9265afc68626a24023329cea`

```dockerfile
```

-	Layers:
	-	`sha256:1055c57699697c76676cb9e712afb1a4b12f805d698638df4a666b33e221ddea`  
		Last Modified: Wed, 04 Feb 2026 17:10:21 GMT  
		Size: 24.4 KB (24362 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.22` - linux; arm variant v7

```console
$ docker pull golang@sha256:c0160657fb144cd241003f44292d6f4aa3d3c9935e3300d3b2b50d77c67bd3ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.0 MB (92991423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d1291a57da57923059822ad94fd17065bb86aafe24caa394c67baa5b0219312`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:29 GMT
ADD alpine-minirootfs-3.22.3-armv7.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:29 GMT
CMD ["/bin/sh"]
# Wed, 04 Feb 2026 17:07:19 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Wed, 04 Feb 2026 17:10:04 GMT
ENV GOTOOLCHAIN=local
# Wed, 04 Feb 2026 17:10:04 GMT
ENV GOPATH=/go
# Wed, 04 Feb 2026 17:10:04 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Feb 2026 17:10:04 GMT
COPY /target/ / # buildkit
# Wed, 04 Feb 2026 17:10:07 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 04 Feb 2026 17:10:07 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:caca1d0e2f8affe80569328af55c755a8480801c5ee912e55aaa828c8209aa6e`  
		Last Modified: Wed, 28 Jan 2026 01:18:35 GMT  
		Size: 3.2 MB (3223629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:701e4c24a87b878cc2df87a6ff3470280276e0002409598dd0beee22e252edea`  
		Last Modified: Wed, 04 Feb 2026 17:10:22 GMT  
		Size: 291.2 KB (291207 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd7c4d8d165092e2ffa5f6928ecd151df0b8f3dc1362c8f59dcd6d9b09df5017`  
		Last Modified: Mon, 02 Feb 2026 19:30:25 GMT  
		Size: 89.5 MB (89476429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40e2a6b9d5594d4e0986fdc30ba1ea15f9eda94817c77eb2087996774ff4e73f`  
		Last Modified: Wed, 04 Feb 2026 17:10:22 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.22` - unknown; unknown

```console
$ docker pull golang@sha256:927ad8aa4d76b1e08419fb4737cea10bb89ed9a6c31f988b56cbee8febaa9afc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.6 KB (219563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09ffed8a24ee6a070b8e12ea664adf045da65d3557683a0dc4bcc44d3f652d44`

```dockerfile
```

-	Layers:
	-	`sha256:c7619f19bcd5e0256f8c931701577d014e6ab4107355053db466eacdc25c2540`  
		Last Modified: Wed, 04 Feb 2026 17:10:22 GMT  
		Size: 195.0 KB (194986 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e68de61557cd2978e1e2cedc1940491fc94fbd768b78a30d8cd08928001b57b6`  
		Last Modified: Wed, 04 Feb 2026 17:10:22 GMT  
		Size: 24.6 KB (24577 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.22` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:c6bac22a8411125a31d2213a3e762ed960c454462640c9eec1af4895b8277194
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.8 MB (92809455 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59008cfa66210eceeb4b836e566a8523cb0e9fc13e7edab1ac28039dfd0fa72d`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:55 GMT
ADD alpine-minirootfs-3.22.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:55 GMT
CMD ["/bin/sh"]
# Wed, 04 Feb 2026 17:04:00 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Wed, 04 Feb 2026 17:09:01 GMT
ENV GOTOOLCHAIN=local
# Wed, 04 Feb 2026 17:09:01 GMT
ENV GOPATH=/go
# Wed, 04 Feb 2026 17:09:01 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Feb 2026 17:09:01 GMT
COPY /target/ / # buildkit
# Wed, 04 Feb 2026 17:09:03 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 04 Feb 2026 17:09:04 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:d741ee1608f399e21c72d05f0f818c348c6801af33aeb83523893d09dc153957`  
		Last Modified: Wed, 28 Jan 2026 01:18:00 GMT  
		Size: 4.1 MB (4139519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e7cf52d53515a275e23abccc27bc5445b17ed89b17cccc17672fed893830fca`  
		Last Modified: Wed, 04 Feb 2026 17:04:43 GMT  
		Size: 294.1 KB (294078 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a6a2a8a6cfc628c3f67b49421d89d0e853e9d214495c3cea23b3d909be150cb`  
		Last Modified: Mon, 02 Feb 2026 19:26:36 GMT  
		Size: 88.4 MB (88375700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88e169e337eb997bab7f2e4e43b5377ce5f1b65f6a4c3f1a75bf61c0e18cfd96`  
		Last Modified: Wed, 04 Feb 2026 17:09:18 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.22` - unknown; unknown

```console
$ docker pull golang@sha256:43fdd08647c647fca08ce55ca4ac86978d9bb690e085ab00e46a07d8dc9f3842
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.6 KB (219615 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45a79d7a78f01e6f1b92d29ea59c9884d3477398acb9430892f758141cf243e8`

```dockerfile
```

-	Layers:
	-	`sha256:4404067ffa6d8799c3bb636e04402c3e7efccfda515598d11f4de04d105ebbd1`  
		Last Modified: Wed, 04 Feb 2026 17:09:18 GMT  
		Size: 195.0 KB (195014 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d92f97f81af1f04b6885309841de0ca9d09994069e08cc5992f579f5abee94c8`  
		Last Modified: Wed, 04 Feb 2026 17:09:18 GMT  
		Size: 24.6 KB (24601 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.22` - linux; 386

```console
$ docker pull golang@sha256:85e7907e50367a2d4691c5fd1434c7ed7655aecac79818cc031fc70f8d6d2ffb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.3 MB (95318749 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8c0aae58c8e60b1bfc65619546f8150377d415b1ea3d4d4d1f6cf91b680ea6b`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:53 GMT
ADD alpine-minirootfs-3.22.3-x86.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:53 GMT
CMD ["/bin/sh"]
# Wed, 04 Feb 2026 17:07:18 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Wed, 04 Feb 2026 17:09:17 GMT
ENV GOTOOLCHAIN=local
# Wed, 04 Feb 2026 17:09:17 GMT
ENV GOPATH=/go
# Wed, 04 Feb 2026 17:09:17 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Feb 2026 17:09:17 GMT
COPY /target/ / # buildkit
# Wed, 04 Feb 2026 17:09:19 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 04 Feb 2026 17:09:19 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:757a99eda61f22434071cfbc7a70f9526b63aeb5479a64272982017ee7cd9cfd`  
		Last Modified: Wed, 28 Jan 2026 01:18:59 GMT  
		Size: 3.6 MB (3620732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e75a2f264a5e902cf57d601fb852e7782a1a23a344a69c20949d7417701a8f0e`  
		Last Modified: Wed, 04 Feb 2026 17:09:32 GMT  
		Size: 291.6 KB (291624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4604cae1ff047094cf665f2719aaf0543d71e670a699786143900320f6ba300`  
		Last Modified: Mon, 02 Feb 2026 19:27:18 GMT  
		Size: 91.4 MB (91406236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:995b19424d6469014b91ad923d025d70e616cee327e7541dc692c4307baab9ce`  
		Last Modified: Wed, 04 Feb 2026 17:09:32 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.22` - unknown; unknown

```console
$ docker pull golang@sha256:b202f2467cf40a8fdfdb9d67246613eb6f5de27d49aa5633db4453bf9585e0d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.4 KB (219383 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4cc07cb83d1a0f31baeab170e5ae452eb539d7625f8309986f6587bce0eaac3e`

```dockerfile
```

-	Layers:
	-	`sha256:0e808ee4a3530a07385b09dac775eda4cc84ad44d0d4ee4f813b521f44a3d3c8`  
		Last Modified: Wed, 04 Feb 2026 17:09:32 GMT  
		Size: 195.0 KB (194951 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5c80f69902449f60aa326937bfb1dc06d2164096dc030c7d1d22b06576d232c3`  
		Last Modified: Wed, 04 Feb 2026 17:09:32 GMT  
		Size: 24.4 KB (24432 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.22` - linux; ppc64le

```console
$ docker pull golang@sha256:9f27881ef64d48192e08d01d5835211ccd735fc949075ccf6eceacb2e522de2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.0 MB (94036393 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77927a02aa2578f6cfdfe0e9fa6361b82e1e9e55418c960db1486428019b5d9c`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:35 GMT
ADD alpine-minirootfs-3.22.3-ppc64le.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:35 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 04:06:40 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 02 Feb 2026 19:27:20 GMT
ENV GOTOOLCHAIN=local
# Mon, 02 Feb 2026 19:27:20 GMT
ENV GOPATH=/go
# Mon, 02 Feb 2026 19:27:20 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 02 Feb 2026 19:27:20 GMT
COPY /target/ / # buildkit
# Mon, 02 Feb 2026 19:32:34 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 02 Feb 2026 19:32:35 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:d7b7d5bab08f20b53e85395b2d6e793469e3acdbe8644bd234992524588b440f`  
		Last Modified: Wed, 28 Jan 2026 01:17:44 GMT  
		Size: 3.7 MB (3734297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e5da64929a546b25e151c7b89cac4fd99dc41033a2fc1973779548ea5121f99`  
		Last Modified: Wed, 28 Jan 2026 04:07:07 GMT  
		Size: 294.6 KB (294573 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14e432b6dca22e637a3a25408001c269ffda0f2c5d9306b2f7174d2a31051778`  
		Last Modified: Mon, 02 Feb 2026 19:28:34 GMT  
		Size: 90.0 MB (90007365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bee5cd9c137bea619e34d92f5c2da5d2d9a445fb38582ee9af5aa8663b51962`  
		Last Modified: Mon, 02 Feb 2026 19:32:49 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.22` - unknown; unknown

```console
$ docker pull golang@sha256:94db9c83b07a0cbe513e8cf8ba1d7fc04e1799f2b022671904eb94c79e46cc81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **217.6 KB (217579 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0321da0a67d40717859b1b1ff8f1cb30864d08af25dd25e99771b0846621bb46`

```dockerfile
```

-	Layers:
	-	`sha256:3d993ec7f2fa5f8919af6f189cb5c07781f777b3e471dc73aca95ccffb8c210e`  
		Last Modified: Wed, 04 Feb 2026 17:53:45 GMT  
		Size: 193.1 KB (193069 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:444282deba027cc0f2ba0f8a37826b4afc87e3c290c7350f9ecbd46d24bd2a41`  
		Last Modified: Wed, 04 Feb 2026 17:53:45 GMT  
		Size: 24.5 KB (24510 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.22` - linux; riscv64

```console
$ docker pull golang@sha256:3ff62abcbe5eceda1b0dfe7fee8355029470a0ba2c3cf4c46e232faad7c0cb37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.4 MB (94366378 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:783fb47f38c8db94687bf53a9f6ec04b721a045bfa26a7cb8610b3a25f1a5262`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 03:49:43 GMT
ADD alpine-minirootfs-3.22.3-riscv64.tar.gz / # buildkit
# Wed, 28 Jan 2026 03:49:43 GMT
CMD ["/bin/sh"]
# Thu, 29 Jan 2026 19:15:18 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 03 Feb 2026 08:03:08 GMT
ENV GOTOOLCHAIN=local
# Tue, 03 Feb 2026 08:03:08 GMT
ENV GOPATH=/go
# Tue, 03 Feb 2026 08:03:08 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Feb 2026 08:03:08 GMT
COPY /target/ / # buildkit
# Tue, 03 Feb 2026 08:43:40 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 03 Feb 2026 08:43:40 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:15ea87d2370d91334d14e1cb46366adb6a57bbae717f07f8c9f55735cf137f62`  
		Last Modified: Wed, 28 Jan 2026 03:50:15 GMT  
		Size: 3.5 MB (3517422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79dcab0b270d631ffdfee1c090f676984c71b03f87fc76005b512418b2ec110c`  
		Last Modified: Thu, 29 Jan 2026 19:17:49 GMT  
		Size: 291.5 KB (291499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc3c8f3022c37addebb7f3bba04877b6aa3acbe5feb276f525d0db506f58caad`  
		Last Modified: Tue, 03 Feb 2026 08:06:29 GMT  
		Size: 90.6 MB (90557299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b778cd0b2a4c3c8e4c3a23411f4ef01ef3e19c5f4068684d7c99ea603a26270`  
		Last Modified: Tue, 03 Feb 2026 08:44:57 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.22` - unknown; unknown

```console
$ docker pull golang@sha256:986f4289cb7437888caa34dc5b51eb527f0268a058cf98f26d2595587609351d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **217.6 KB (217576 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2bfb7bdb7af9197b90b0d71413b27d45466f72a6b8b3edd335f601d086f21abc`

```dockerfile
```

-	Layers:
	-	`sha256:50935fda1c10d08ecb2ceba18269fee75bea6fd7a5c419c040a1eeed4fe39b6d`  
		Last Modified: Tue, 03 Feb 2026 08:44:57 GMT  
		Size: 193.1 KB (193065 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cbf89932344bfb76bfaff09565b544e01409094e6bfede40d411fdc1e8b9ba51`  
		Last Modified: Tue, 03 Feb 2026 08:44:57 GMT  
		Size: 24.5 KB (24511 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.22` - linux; s390x

```console
$ docker pull golang@sha256:fa244d0bfd64a48f66abfc2efd4702a366d5305834c0b86b0ba2742bebd12f4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.5 MB (96513176 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4bd2197ce07de3d06a3367fb680e4d2ca0482d90e8896bacc5f64fb746f31833`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:06 GMT
ADD alpine-minirootfs-3.22.3-s390x.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:06 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 07:11:53 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 02 Feb 2026 19:28:52 GMT
ENV GOTOOLCHAIN=local
# Mon, 02 Feb 2026 19:28:52 GMT
ENV GOPATH=/go
# Mon, 02 Feb 2026 19:28:52 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 02 Feb 2026 19:28:52 GMT
COPY /target/ / # buildkit
# Mon, 02 Feb 2026 19:28:55 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 02 Feb 2026 19:28:55 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:dab48b8d1bab09fede3f54264828e67466f10d64acc37d9412190034dbcbf61f`  
		Last Modified: Wed, 28 Jan 2026 01:17:16 GMT  
		Size: 3.7 MB (3650434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a83b6b4e7826d3ddebd9c48a75091c1c37e104afa456d3507b2ce5beab9301e2`  
		Last Modified: Wed, 28 Jan 2026 07:14:36 GMT  
		Size: 292.1 KB (292142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a7062bfc50107a913a5fd7c0d090af1366da08b74147cf71ec4490488730775`  
		Last Modified: Mon, 02 Feb 2026 19:29:23 GMT  
		Size: 92.6 MB (92570442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a5c96bc5ce39fde8e48af7552ffeafc272c948a63d413ab11c236f84ab96fad`  
		Last Modified: Mon, 02 Feb 2026 19:29:21 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.22` - unknown; unknown

```console
$ docker pull golang@sha256:30bd611697ff249ed1488f8dc415ef6d9cd504ed4685030d18340f4750bdb6bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **217.5 KB (217496 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d72e7de8a009bfbaffc05bcf3fc3607fe4077626793f7d3846c731c866fe8df1`

```dockerfile
```

-	Layers:
	-	`sha256:d91a250493ed610846538c12a4389dc1d72c54304a7536df664813b2d6aee976`  
		Last Modified: Wed, 04 Feb 2026 17:13:11 GMT  
		Size: 193.0 KB (193031 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0484ac84bbceca64ae839b16c98e2515d37440c25cda094232c847dd4107d977`  
		Last Modified: Wed, 04 Feb 2026 17:13:11 GMT  
		Size: 24.5 KB (24465 bytes)  
		MIME: application/vnd.in-toto+json
