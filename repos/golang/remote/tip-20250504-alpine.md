## `golang:tip-20250504-alpine`

```console
$ docker pull golang@sha256:cdd1d21d8951e74ad6b2d264ae601b908ca52fe3c461c4295bb791e334cba7d0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `golang:tip-20250504-alpine` - linux; amd64

```console
$ docker pull golang@sha256:cff9b4d1de6118f045b9c3f03dff38d9026034194e3d37ec047abcc3ba5fb156
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.7 MB (130677414 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5aa5a14f595f53e2306501fddcf6214cb5726471eb6288a307c9d2abaa334975`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Mon, 05 May 2025 05:23:20 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 05 May 2025 05:23:20 GMT
ENV GOTOOLCHAIN=local
# Mon, 05 May 2025 05:23:20 GMT
ENV GOPATH=/go
# Mon, 05 May 2025 05:23:20 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 05 May 2025 05:23:20 GMT
COPY /target/ / # buildkit
# Mon, 05 May 2025 05:23:20 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 05 May 2025 05:23:20 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 12:05:35 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f8d3f8ff36034ab30cd65b6532c35a5034bd883589380173f0c782aeaacc5ac`  
		Last Modified: Mon, 05 May 2025 17:32:49 GMT  
		Size: 294.9 KB (294919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f43c76dc6ee2ca1c3cdba208e84ccb4e1c5c0677efaf8a998b57c3e624b57e3`  
		Last Modified: Mon, 05 May 2025 17:32:51 GMT  
		Size: 126.7 MB (126740090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:702c2dba55a7f563423754ea9fdd256a2297df75f9e27a861df85f8576147f0f`  
		Last Modified: Mon, 05 May 2025 17:32:49 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20250504-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:874e518e3420af25a3f3d30a8070a9d60f60bdbd63b70e7529e13ab584bf340c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **237.0 KB (236973 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7858901cb3e43b0caff5a4875107113ded85be189d8fe983e5cfc6da2be59300`

```dockerfile
```

-	Layers:
	-	`sha256:1f822b6a84fcc0d0279da6fa50155a4de78c60378122a1c2b024a83c42d8bc37`  
		Last Modified: Mon, 05 May 2025 17:32:49 GMT  
		Size: 211.8 KB (211831 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0ce40fda45bc1dfbb77b8f96aa0169dcb8c417e69feeb8a8a10f92f4e110f63e`  
		Last Modified: Mon, 05 May 2025 17:32:49 GMT  
		Size: 25.1 KB (25142 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20250504-alpine` - linux; arm variant v6

```console
$ docker pull golang@sha256:ce25ecb89a6d8a86480764587f81ccc4e10d30c888878a2e84f16701a901dcd1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.8 MB (125754292 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4617030c0aed41eb6946affaae453083b70b535ac3db2f975a46c87559625375`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armhf.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Mon, 05 May 2025 05:23:20 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 05 May 2025 05:23:20 GMT
ENV GOTOOLCHAIN=local
# Mon, 05 May 2025 05:23:20 GMT
ENV GOPATH=/go
# Mon, 05 May 2025 05:23:20 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 05 May 2025 05:23:20 GMT
COPY /target/ / # buildkit
# Mon, 05 May 2025 05:23:20 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 05 May 2025 05:23:20 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:76099982f06682e28a60c3b774ef20931d07b0a2f551203484e633d8c0361ee7`  
		Last Modified: Fri, 14 Feb 2025 18:28:03 GMT  
		Size: 3.4 MB (3364731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e200e7ad5e2f13ee1ee5c295f12b94fa96417ce036e2a8026a7db4231fdba9a2`  
		Last Modified: Fri, 14 Feb 2025 22:09:20 GMT  
		Size: 296.3 KB (296252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:120e42f205c7ea79f8572b00a6e58ed770c10091329a9fdb96f1b2f7bbbedac6`  
		Last Modified: Mon, 05 May 2025 17:52:56 GMT  
		Size: 122.1 MB (122093151 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15806a630fc8874d0269d9e8b970447abd8c00577eb5bd0279336f0ce7beb042`  
		Last Modified: Mon, 05 May 2025 17:52:52 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20250504-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:f6b25c9542ed59cf7ee0fd1daa09465f7325877d7819f3b9663234c0bed89103
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.1 KB (25051 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44c6c85de04f8e6b465c54aad7370b5361b19c1825e593dca2eb452dae2c89fa`

```dockerfile
```

-	Layers:
	-	`sha256:6d5e5fb569d52b6ba2ccdd6bb29f891cc97e23875354df3b12f0156791d1f591`  
		Last Modified: Mon, 05 May 2025 17:52:52 GMT  
		Size: 25.1 KB (25051 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20250504-alpine` - linux; arm variant v7

```console
$ docker pull golang@sha256:19739ad1d8e8a87ae51a313e0e1007912aa8cda7fbe6a9bf34e5fd6fedaa9ed1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.2 MB (125158747 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3c5883260a53dec76a379c2066807d415718ea80b840626a160e65fc444095a`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armv7.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Mon, 05 May 2025 05:23:20 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 05 May 2025 05:23:20 GMT
ENV GOTOOLCHAIN=local
# Mon, 05 May 2025 05:23:20 GMT
ENV GOPATH=/go
# Mon, 05 May 2025 05:23:20 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 05 May 2025 05:23:20 GMT
COPY /target/ / # buildkit
# Mon, 05 May 2025 05:23:20 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 05 May 2025 05:23:20 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:85f3b18f9f5a8655db86c6dfb02bb01011ffef63d10a173843c5c65c3e9137b7`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.1 MB (3098123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a77833ee7d3adeaa883db3f960686c769232a931d3442cfcc8bb6a4790098520`  
		Last Modified: Fri, 14 Feb 2025 21:47:46 GMT  
		Size: 295.2 KB (295199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:185f617f5384afe02adfbf4600ef1c02d06ba922d332b58b68dacf2c75505cb9`  
		Last Modified: Mon, 05 May 2025 17:58:33 GMT  
		Size: 121.8 MB (121765268 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0da6b222a222a8fcf112946582d323d765caa56a5df98478a7382b6dd27a0ddb`  
		Last Modified: Mon, 05 May 2025 18:05:53 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20250504-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:f1755cc29d5c7f20df88709f79bbe269729f9350219389f957b96c49b3b83eb5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **237.1 KB (237093 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbce126121b6655ef7f83710319152cb503f17cc4cdb9bd3c6b2aa8f7dda0821`

```dockerfile
```

-	Layers:
	-	`sha256:c9c005e4f7c06d3a0506098830b7c158bb4de35a3859a17c962168940dc4d682`  
		Last Modified: Mon, 05 May 2025 18:05:53 GMT  
		Size: 211.8 KB (211827 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b66d2581c8316c7ac67f5ce157b728f95b1913bf28c9d564aaf3597d623e4782`  
		Last Modified: Mon, 05 May 2025 18:05:53 GMT  
		Size: 25.3 KB (25266 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20250504-alpine` - linux; 386

```console
$ docker pull golang@sha256:8acb40a6848e4fdafeccd8dd55d3bd11def9f8cb0912b56234edc805b9213e7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.9 MB (128899320 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f784a6ac954c5dd03df7d69b0b6f960c4eade9d6f01ce93153f0db7e06d8be1c`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Mon, 05 May 2025 05:23:20 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 05 May 2025 05:23:20 GMT
ENV GOTOOLCHAIN=local
# Mon, 05 May 2025 05:23:20 GMT
ENV GOPATH=/go
# Mon, 05 May 2025 05:23:20 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 05 May 2025 05:23:20 GMT
COPY /target/ / # buildkit
# Mon, 05 May 2025 05:23:20 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 05 May 2025 05:23:20 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:69aa61ccf55e5bf8e7a069b89e8afb42b4f3443b3785868795af8046d810d608`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.5 MB (3463623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd73547b1d12133fde535e00280d6a512a1f053f9c06d84b619d65ebe94bfed5`  
		Last Modified: Mon, 05 May 2025 17:33:34 GMT  
		Size: 295.6 KB (295603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0adf2ac7302cf0e124e19835cb5b85e5efb297232f12a426c19cbe865f7f8c6`  
		Last Modified: Mon, 05 May 2025 17:33:28 GMT  
		Size: 125.1 MB (125139936 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65830431cbad4f29bea005540e46b9c677c1a6cda5b03aba7951f055c14bb285`  
		Last Modified: Mon, 05 May 2025 17:33:34 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20250504-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:58df034fbeab54d983f94de43d6d46ead39d6e6c4cce2689aec1f45458d1d5e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.9 KB (236865 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d6c259bad4e5c2145afe7a604520dcfb24a041de0496f36493cb3ce652dab7c`

```dockerfile
```

-	Layers:
	-	`sha256:e8c00401a3bb369d51bc88762480f9a029161479748c98b9633357366dd9ae69`  
		Last Modified: Mon, 05 May 2025 17:33:34 GMT  
		Size: 211.8 KB (211766 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9ced6009e98427a38a1ac14f8007d4eee517f8ac8f751332e95a8b0482dd0816`  
		Last Modified: Mon, 05 May 2025 17:33:34 GMT  
		Size: 25.1 KB (25099 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20250504-alpine` - linux; ppc64le

```console
$ docker pull golang@sha256:9be92a19092b67de3a070192f46f9503df2344e4d803728c9a4bfaf37dbdb2b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.5 MB (125505138 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:977dc24405798af51e540fca0e72a4fd2b777dc7ffb55af9d9a8404d4be368ba`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-ppc64le.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Mon, 05 May 2025 05:23:20 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 05 May 2025 05:23:20 GMT
ENV GOTOOLCHAIN=local
# Mon, 05 May 2025 05:23:20 GMT
ENV GOPATH=/go
# Mon, 05 May 2025 05:23:20 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 05 May 2025 05:23:20 GMT
COPY /target/ / # buildkit
# Mon, 05 May 2025 05:23:20 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 05 May 2025 05:23:20 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:184b14480d317057da092a0994ad6baf4b2df588108f43969f8fd56f021af2c6`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.6 MB (3574345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38d07c13e49694099e3952065321ca0fc45938d3a118b16ce109a83e147045f6`  
		Last Modified: Mon, 05 May 2025 19:01:05 GMT  
		Size: 298.3 KB (298290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b31ed22752475c6f8926b1f87264c9b47f4ccaebd9fffea12e01e7f160cb5e70`  
		Last Modified: Mon, 05 May 2025 18:58:04 GMT  
		Size: 121.6 MB (121632345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e478a146ac61e77ec63bb5ac7e33448688735fbac73f55133add5c4b4647ae51`  
		Last Modified: Mon, 05 May 2025 19:01:05 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20250504-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:a40685483ff6a5299f8cde924180c855a3a333beb546ca755959d99365ea8501
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.2 KB (235154 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6d960912486af912876b1095ccd77ec006b8fe4405f15ef30edac608e98911f`

```dockerfile
```

-	Layers:
	-	`sha256:535710a79728fc35363bd2279cf79877367cfd8c6da15b4067074302c2e71827`  
		Last Modified: Mon, 05 May 2025 19:01:05 GMT  
		Size: 210.0 KB (209954 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:76c79fae1f675e8a32394504d234a1dc8756f1ca2719dce66322d60d7606dc0e`  
		Last Modified: Mon, 05 May 2025 19:01:05 GMT  
		Size: 25.2 KB (25200 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20250504-alpine` - linux; s390x

```console
$ docker pull golang@sha256:10b26db5f27b8fd1771a56a3c7c3973a1586943bac807862012b5295aa465b33
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.9 MB (127900131 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63f12e39d1bfdd24c815711620cfd030eab0b6128053418756c28e9fd2ed7f6a`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-s390x.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Mon, 05 May 2025 05:23:20 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 05 May 2025 05:23:20 GMT
ENV GOTOOLCHAIN=local
# Mon, 05 May 2025 05:23:20 GMT
ENV GOPATH=/go
# Mon, 05 May 2025 05:23:20 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 05 May 2025 05:23:20 GMT
COPY /target/ / # buildkit
# Mon, 05 May 2025 05:23:20 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 05 May 2025 05:23:20 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:c1a599607158512214777614f916f8193d29fd34b656d47dfc26314af01e2af4`  
		Last Modified: Fri, 14 Feb 2025 12:05:25 GMT  
		Size: 3.5 MB (3467567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bd99af01c56b56dd8b4b638222a30d969ae806a266626016d5a030517f57428`  
		Last Modified: Mon, 05 May 2025 17:56:04 GMT  
		Size: 296.2 KB (296192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4145acb431091c4f38f8aa86656f1534dd86342d379c6569a1f1b1af46cd2b6e`  
		Last Modified: Mon, 05 May 2025 17:53:10 GMT  
		Size: 124.1 MB (124136214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3786f8a070d511ab095d0ac907b0243440e7343d3e8017032c3a8cbe0621a2ef`  
		Last Modified: Mon, 05 May 2025 17:56:04 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20250504-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:f9ce3d6b6534b99db281789a7d87edd104683fc49334c6d64611bed8a4dbc634
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.0 KB (235022 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f28b9b07171797b71a6f92baa019178435ab3fac34ce1c8ef3587e549ea01d5c`

```dockerfile
```

-	Layers:
	-	`sha256:bec92bbcc2d175c6a1cc8b4d0efa649c91ceaab3bfc411ae9dd9973620b124a0`  
		Last Modified: Mon, 05 May 2025 17:56:04 GMT  
		Size: 209.9 KB (209880 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:56f5b10aa438bee4b2abf765568c7a5bb0d886a6083dc108d759b8104ca3461f`  
		Last Modified: Mon, 05 May 2025 17:56:04 GMT  
		Size: 25.1 KB (25142 bytes)  
		MIME: application/vnd.in-toto+json
