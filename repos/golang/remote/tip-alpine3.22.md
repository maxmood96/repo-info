## `golang:tip-alpine3.22`

```console
$ docker pull golang@sha256:7d8e00eb0a892b98e6a9ad1f4e624618cc206fa76f3b388ea13c311e1fdb9538
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
$ docker pull golang@sha256:5abed323ca134d5ab60c782e04e5bf8a6b5535ef08c3e72955749a87f5c660d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.0 MB (105977216 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05cc8c9f4d7f9640e9ccf594228f0db1ef37aa21be5e389235c92ce80b68e267`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:02 GMT
ADD alpine-minirootfs-3.22.4-x86_64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:02 GMT
CMD ["/bin/sh"]
# Wed, 27 May 2026 00:20:15 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Wed, 27 May 2026 00:22:28 GMT
ENV GOTOOLCHAIN=local
# Wed, 27 May 2026 00:22:28 GMT
ENV GOPATH=/go
# Wed, 27 May 2026 00:22:28 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 27 May 2026 00:22:28 GMT
COPY /target/ / # buildkit
# Wed, 27 May 2026 00:22:30 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 27 May 2026 00:22:30 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:84f5eff04246b56d48d1ed6cbd82d6bc7e53f7e790db6a467f92571c69f3289e`  
		Last Modified: Thu, 16 Apr 2026 23:53:07 GMT  
		Size: 3.8 MB (3808189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04f5f04dbd3ecd0bb2379b1159cddea9bd3670da0ed3554ee9b8c72c4d9533b2`  
		Last Modified: Wed, 27 May 2026 00:22:45 GMT  
		Size: 289.5 KB (289451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77da848857ba8d560346623b29060265d568e3fd544a353c4d3226bc71f30e13`  
		Last Modified: Wed, 27 May 2026 00:22:37 GMT  
		Size: 101.9 MB (101879418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db5fc5738bf5f93e78d90917e770b94b392670880115a596a737cf94b21d62d2`  
		Last Modified: Wed, 27 May 2026 00:22:45 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.22` - unknown; unknown

```console
$ docker pull golang@sha256:3dacc1afbeafa1d4adf6443e94eb8ba96430f0204fa68d08e1a10134ffc59984
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.8 KB (218766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d77d52f96f22eb861ff402584c9425eecb2405843a2c24cfd0ff48fe3042732a`

```dockerfile
```

-	Layers:
	-	`sha256:c9d10616a4838f9c7f81b719d831551a7ca7e0d48d037de961c34b60d16c1597`  
		Last Modified: Wed, 27 May 2026 00:22:45 GMT  
		Size: 194.3 KB (194297 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a52ac05336dd7d55e06c6dda148444e0ce40595a8960cc94ff37b2fab5f8dd4b`  
		Last Modified: Wed, 27 May 2026 00:22:46 GMT  
		Size: 24.5 KB (24469 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.22` - linux; arm variant v6

```console
$ docker pull golang@sha256:986e5885773ecb42c119f79b3d1ceff064be5544fdfde73d05eac191a4585bff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.7 MB (101683345 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb65e11f796369e56d50189a8e077fb16546e9a3809201c9ffd5c9e02851304f`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:27 GMT
ADD alpine-minirootfs-3.22.4-armhf.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:27 GMT
CMD ["/bin/sh"]
# Wed, 27 May 2026 00:18:25 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Wed, 27 May 2026 00:21:29 GMT
ENV GOTOOLCHAIN=local
# Wed, 27 May 2026 00:21:29 GMT
ENV GOPATH=/go
# Wed, 27 May 2026 00:21:29 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 27 May 2026 00:21:29 GMT
COPY /target/ / # buildkit
# Wed, 27 May 2026 00:21:32 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 27 May 2026 00:21:32 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:08c654e9a4409dbbeb5faba9659360f33dbc6f7a6d79ebebe08f57d22a1b76fc`  
		Last Modified: Thu, 16 Apr 2026 23:53:31 GMT  
		Size: 3.5 MB (3507383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea683e76f993ac1504cdf6d16b26983cf45cb3fc6bcb7de1fa2fe92b4c8ddd98`  
		Last Modified: Wed, 27 May 2026 00:21:44 GMT  
		Size: 290.3 KB (290338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79cbc47c6937efdcec813236fc1a43a8627a2f5ce2335f3ef2107a3510692211`  
		Last Modified: Wed, 27 May 2026 00:21:39 GMT  
		Size: 97.9 MB (97885466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f8bd362ab127b978b9534afd6d9064f1ff711f8d3a23896d3ba02aa4403eaca`  
		Last Modified: Wed, 27 May 2026 00:21:44 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.22` - unknown; unknown

```console
$ docker pull golang@sha256:5e9c4d3776b5ec2c977e4e5fe4728ae5d117303ccb264e2a3e749641a94fade1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.4 KB (24362 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29790a39ba995241a071be3ab1988de84a7f9002390034741daa013b8890933f`

```dockerfile
```

-	Layers:
	-	`sha256:005e327188180a16381640eeb36319d8b2785a401d07d862d66ee490fa9bba8c`  
		Last Modified: Wed, 27 May 2026 00:21:44 GMT  
		Size: 24.4 KB (24362 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.22` - linux; arm variant v7

```console
$ docker pull golang@sha256:ebbb55651d7102e2a671bda57b94c6335efbdfa4ec9ebd1cfc845b176d189a3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.1 MB (101090310 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48c0fbb8d821a94b2b0eabc77d5cc43cb2961eddba6b0b94083712cef7853c6c`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 16 Apr 2026 23:54:02 GMT
ADD alpine-minirootfs-3.22.4-armv7.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:54:02 GMT
CMD ["/bin/sh"]
# Wed, 27 May 2026 00:18:17 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Wed, 27 May 2026 00:21:22 GMT
ENV GOTOOLCHAIN=local
# Wed, 27 May 2026 00:21:22 GMT
ENV GOPATH=/go
# Wed, 27 May 2026 00:21:22 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 27 May 2026 00:21:22 GMT
COPY /target/ / # buildkit
# Wed, 27 May 2026 00:21:25 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 27 May 2026 00:21:25 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:99e8c7f1cf08d3156a369084c1a1fd745878aa29f4a0f55d73e953b93f0b7a93`  
		Last Modified: Thu, 16 Apr 2026 23:54:07 GMT  
		Size: 3.2 MB (3225830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d578118b60477ddfe6214fb6194fa77b2b4b0711152423d968990a04f0a38040`  
		Last Modified: Wed, 27 May 2026 00:21:41 GMT  
		Size: 289.5 KB (289517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10970b698e6007676a0ddc85a9b7bd9dc803ec199aba70539ca19e2e26b490dc`  
		Last Modified: Wed, 27 May 2026 00:21:38 GMT  
		Size: 97.6 MB (97574805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3774f783d34e31ba300409f896ac966873cdcfe28d003ab2595fb53565e9842`  
		Last Modified: Wed, 27 May 2026 00:21:40 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.22` - unknown; unknown

```console
$ docker pull golang@sha256:042c9f02c4a8fe156f6be3cc501aad8a0b7d65f93869b5e94d2163c0f37d6c7e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.9 KB (218878 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:697d640d9ef852da9ade785992f7865c46495d75e93a5a2f46fbaf9daf5b72cb`

```dockerfile
```

-	Layers:
	-	`sha256:262f7d0b32d29b76e448489700d980800865df7f7f7424c85356f3fca11d1dd6`  
		Last Modified: Wed, 27 May 2026 00:21:41 GMT  
		Size: 194.3 KB (194301 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:06a4ba82b47a7cb900de48a418a97013d681132380886c950f221485a132ee92`  
		Last Modified: Wed, 27 May 2026 00:21:41 GMT  
		Size: 24.6 KB (24577 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.22` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:4ce4b03ba35d32b8b02c709cdeb77788f63ca124cbc95fa192e8167f60976cd0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **100.7 MB (100748514 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd3b765e1f1782ff504da27d5deeec6b8dc80d504307d47b9bbe208ddb36f481`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:00 GMT
ADD alpine-minirootfs-3.22.4-aarch64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:00 GMT
CMD ["/bin/sh"]
# Wed, 27 May 2026 00:19:23 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Wed, 27 May 2026 00:21:18 GMT
ENV GOTOOLCHAIN=local
# Wed, 27 May 2026 00:21:18 GMT
ENV GOPATH=/go
# Wed, 27 May 2026 00:21:18 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 27 May 2026 00:21:18 GMT
COPY /target/ / # buildkit
# Wed, 27 May 2026 00:21:21 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 27 May 2026 00:21:21 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:58e777220c395c319866c5d73ea32a5ea574bbd12f4eb289b392f584d0cd953e`  
		Last Modified: Thu, 16 Apr 2026 23:53:05 GMT  
		Size: 4.1 MB (4141894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb666b9be0ef142c0832e5dc78e87491f1e184bd18d1c25e49c1835aab16b6fb`  
		Last Modified: Wed, 27 May 2026 00:21:36 GMT  
		Size: 291.9 KB (291898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb11297bd411607a8b57c42b1e75c7973dc6c61df122e261576bba30bd7fe3ac`  
		Last Modified: Wed, 27 May 2026 00:21:40 GMT  
		Size: 96.3 MB (96314565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02c3a745b8bf718261527b15987a59a0301b8df6601c1073a31722c4a6de7dd8`  
		Last Modified: Wed, 27 May 2026 00:21:35 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.22` - unknown; unknown

```console
$ docker pull golang@sha256:5dcdad2c169c32e72d26e7bdc90c272a772adc409c3a754783079ecb8ca9707a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.9 KB (218930 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:987d14d3576f85bbe19624eb884c6af82fe7c0df306c62109d43cd4cd6108092`

```dockerfile
```

-	Layers:
	-	`sha256:faaf66519b4ee593dc139196779756ce96cce40774cafb5e4c80b4ecf996bf35`  
		Last Modified: Wed, 27 May 2026 00:21:36 GMT  
		Size: 194.3 KB (194329 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f2bfec281be3f318b073ee837412804b5b04f4d70c356088ff135a8379afebf5`  
		Last Modified: Wed, 27 May 2026 00:21:36 GMT  
		Size: 24.6 KB (24601 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.22` - linux; 386

```console
$ docker pull golang@sha256:57ba5bf3662c0666d8cc27f6e2573040473b7db1fb77b6b30d3658e9d45747b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.5 MB (103518893 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0acfed0a7334b69b0fe2de83d85b4617f96861a6a246169f24e0e86b1340fbdd`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 17 Apr 2026 02:42:29 GMT
ADD alpine-minirootfs-3.22.4-x86.tar.gz / # buildkit
# Fri, 17 Apr 2026 02:42:29 GMT
CMD ["/bin/sh"]
# Wed, 27 May 2026 00:26:05 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Wed, 27 May 2026 00:28:15 GMT
ENV GOTOOLCHAIN=local
# Wed, 27 May 2026 00:28:15 GMT
ENV GOPATH=/go
# Wed, 27 May 2026 00:28:15 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 27 May 2026 00:28:15 GMT
COPY /target/ / # buildkit
# Wed, 27 May 2026 00:28:17 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 27 May 2026 00:28:17 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:481dba1f7704181ddc1e2b499675e9651a93f972d4cd141a4933d44622cdc88a`  
		Last Modified: Fri, 17 Apr 2026 02:42:34 GMT  
		Size: 3.6 MB (3624721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb5efa6b83f1accfe73fbceeeee46dfe97db228f215e036c107804180bb969fb`  
		Last Modified: Wed, 27 May 2026 00:28:31 GMT  
		Size: 289.9 KB (289938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:849d403214e905076ef37eb9bf9b81fdb084f9e69d1847d3cf7505e9a15c9cfa`  
		Last Modified: Wed, 27 May 2026 00:23:45 GMT  
		Size: 99.6 MB (99604078 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e60c972c3eccc0c5136280259131ff7e2205a0b92d7b6f29017732fc0ffb323c`  
		Last Modified: Wed, 27 May 2026 00:28:31 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.22` - unknown; unknown

```console
$ docker pull golang@sha256:5be0894271ec1fa91e6c8a92a2e3a75bd58145d358b66ba0e42f423b7081db19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.7 KB (218698 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d38fbf8db700d791e3b5818a05ad81506d013b8ed30ed36424ca9ea089146fe5`

```dockerfile
```

-	Layers:
	-	`sha256:c564e2d74081b93606ee77cc4e98855bb61543d1ba8baf591caa81c7579eb65e`  
		Last Modified: Wed, 27 May 2026 00:28:31 GMT  
		Size: 194.3 KB (194266 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6434e612d854d7dc7923e5a44f32f41fb6f1393258c38ae1b698f6fe211d5585`  
		Last Modified: Wed, 27 May 2026 00:28:31 GMT  
		Size: 24.4 KB (24432 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.22` - linux; ppc64le

```console
$ docker pull golang@sha256:f7786bbbb0fb06699b365fc87f327f84eda85d211f37ee886f58558e035c8316
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.3 MB (102273320 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbc59b1d2ddc20871c900fe7ea08775014a70e3bee03bc0486b7bdd82ad916da`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 17 Apr 2026 00:00:29 GMT
ADD alpine-minirootfs-3.22.4-ppc64le.tar.gz / # buildkit
# Fri, 17 Apr 2026 00:00:29 GMT
CMD ["/bin/sh"]
# Tue, 12 May 2026 00:47:18 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Wed, 27 May 2026 00:33:54 GMT
ENV GOTOOLCHAIN=local
# Wed, 27 May 2026 00:33:54 GMT
ENV GOPATH=/go
# Wed, 27 May 2026 00:33:54 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 27 May 2026 00:33:54 GMT
COPY /target/ / # buildkit
# Wed, 27 May 2026 00:39:09 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 27 May 2026 00:39:09 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:9d65ab042d46bde09babe9a9587237000067c332d24fd9ca516fea7bdfb77c80`  
		Last Modified: Fri, 17 Apr 2026 00:00:38 GMT  
		Size: 3.7 MB (3736656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d055a7b346c3415d127540993e10eb9dc227fd9e62b3fc2e8282889925f98c6`  
		Last Modified: Tue, 12 May 2026 00:47:45 GMT  
		Size: 292.4 KB (292435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b5d83b0a2acae5776f1d36a1951e6d604ad7e905260707ce03d30294ae6c508`  
		Last Modified: Wed, 27 May 2026 00:34:56 GMT  
		Size: 98.2 MB (98244071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d9c88a643e4dfe99136db49eb90aab4b4a838d7acc28ef2ab29eb3f0bbfecb6`  
		Last Modified: Wed, 27 May 2026 00:39:26 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.22` - unknown; unknown

```console
$ docker pull golang@sha256:ce4b9f59dc1067a7d4e51d4fbc532aa41aeab129281cbf4d9b60000b6c4fb39a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **216.9 KB (216895 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7dccebe7b776f7072c711f786ac7e417af11b337d91ffbe2765ba73db4067e3`

```dockerfile
```

-	Layers:
	-	`sha256:1905315157ea540f74ab848dc0d67178f61998c86a9e0ff646973efecc7a1c56`  
		Last Modified: Wed, 27 May 2026 00:39:27 GMT  
		Size: 192.4 KB (192384 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:10f99c2aea158fafcf738cb23f2349f77b8c621b9d24a149218428ea9aec9f3d`  
		Last Modified: Wed, 27 May 2026 00:39:27 GMT  
		Size: 24.5 KB (24511 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.22` - linux; riscv64

```console
$ docker pull golang@sha256:054ccdac2ddee9a8c07955ac47d1cd87e8a5060fd2320706aefd591ae2384005
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.0 MB (102973269 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b3118c7e8ba3950e4049f63397ebfcc68f040a7afc4a335b922cdacb3d67756`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 17 Apr 2026 07:18:45 GMT
ADD alpine-minirootfs-3.22.4-riscv64.tar.gz / # buildkit
# Fri, 17 Apr 2026 07:18:45 GMT
CMD ["/bin/sh"]
# Tue, 28 Apr 2026 01:45:46 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Thu, 28 May 2026 11:35:46 GMT
ENV GOTOOLCHAIN=local
# Thu, 28 May 2026 11:35:46 GMT
ENV GOPATH=/go
# Thu, 28 May 2026 11:35:46 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 28 May 2026 11:35:46 GMT
COPY /target/ / # buildkit
# Thu, 28 May 2026 11:36:04 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Thu, 28 May 2026 11:36:04 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:fbc07c8b85a3c60e503ffd0cbe3e1b3947fd65764784e1bd9d943ac21097cce7`  
		Last Modified: Fri, 17 Apr 2026 07:19:08 GMT  
		Size: 3.5 MB (3520880 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0e48325e06ab8f03302d19014bd8681498f11993eba6b2fa96b633d7c283c8e`  
		Last Modified: Tue, 28 Apr 2026 02:26:34 GMT  
		Size: 289.8 KB (289807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9ba57acf5ba3d18b7eb9e4286139141d4a6480c2e9b8f4fd881334e86e5e1a9`  
		Last Modified: Thu, 28 May 2026 11:39:26 GMT  
		Size: 99.2 MB (99162424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:795892d6f12a429d3b0e36731748a7b9154d470881b4072746a1e0e22e70609f`  
		Last Modified: Thu, 28 May 2026 11:39:11 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.22` - unknown; unknown

```console
$ docker pull golang@sha256:57e8f5d08ecb8e1c745325027457a2d2b68e48d9217631f6c0b323518a487917
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **216.9 KB (216891 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9a75cae907bdc842cb9ed613cc9f1c3c573ddd90a6a0e934ffc33e05d132dba`

```dockerfile
```

-	Layers:
	-	`sha256:3f384adbfcaf495b09ebf99a354d833dc74820ede5be05b08115c6370367eacd`  
		Last Modified: Thu, 28 May 2026 11:39:11 GMT  
		Size: 192.4 KB (192380 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:05f83fdb52e76bc370fac045ed71dc939532bac1b737a5a0242ce0672effc851`  
		Last Modified: Thu, 28 May 2026 11:39:11 GMT  
		Size: 24.5 KB (24511 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.22` - linux; s390x

```console
$ docker pull golang@sha256:051063b87c6da88b00d66d7435ab45ebe738b0f8cb1f925d69a68b50b1c8b184
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.2 MB (104238055 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6e7b7b605bad50821477b0ff88bae78a92eb9bb69789652abdc6f7be8385314`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:56 GMT
ADD alpine-minirootfs-3.22.4-s390x.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:56 GMT
CMD ["/bin/sh"]
# Wed, 27 May 2026 00:28:08 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Wed, 27 May 2026 00:27:03 GMT
ENV GOTOOLCHAIN=local
# Wed, 27 May 2026 00:27:03 GMT
ENV GOPATH=/go
# Wed, 27 May 2026 00:27:03 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 27 May 2026 00:27:03 GMT
COPY /target/ / # buildkit
# Wed, 27 May 2026 00:28:11 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 27 May 2026 00:28:11 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:54b429821fc7436a26fe07d9038b86e2bef4ef3bf03e43e9ae5e91ab8e4b37a9`  
		Last Modified: Thu, 16 Apr 2026 23:54:12 GMT  
		Size: 3.7 MB (3653873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:251656ff89630003b238e926932e3d25d0db9520f1a14583afdcc79ac57a832f`  
		Last Modified: Wed, 27 May 2026 00:28:40 GMT  
		Size: 290.5 KB (290467 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:def8ca56de94c50983811539154fa57356ce10e9aa7caf4558fbf0aca8e494c9`  
		Last Modified: Wed, 27 May 2026 00:28:25 GMT  
		Size: 100.3 MB (100293557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7518919fde9c2f7d5d340006f0155f478bb19ade7a6dab5c70185dd2f8d020af`  
		Last Modified: Wed, 27 May 2026 00:28:40 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.22` - unknown; unknown

```console
$ docker pull golang@sha256:392c7ca1dcdf8b1f8c09aa00f88919b5ebc5cf90397c2c313d295494af2abe27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **217.4 KB (217389 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d836730c7823d9af66b39129d893eab603eec826f427b2c2615ff9814061cb7`

```dockerfile
```

-	Layers:
	-	`sha256:c5cc2beae840c95a460ce75acd5e74310a7006e684fbff4989b93a3b29a6ebe7`  
		Last Modified: Wed, 27 May 2026 00:28:40 GMT  
		Size: 193.1 KB (193094 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6dedff32972cf5c46cd3ccb029b4ab5c3bee1785c07e9351c49d4187e51d310c`  
		Last Modified: Wed, 27 May 2026 00:28:40 GMT  
		Size: 24.3 KB (24295 bytes)  
		MIME: application/vnd.in-toto+json
