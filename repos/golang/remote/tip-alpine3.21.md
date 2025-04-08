## `golang:tip-alpine3.21`

```console
$ docker pull golang@sha256:29186d7f5323ae87a8a13f1d1686e6d44f12879fa50c46d59b6937b2e2e3a5c2
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

### `golang:tip-alpine3.21` - linux; amd64

```console
$ docker pull golang@sha256:ad161e200505446fec057d8488d46d130aa227dcc02406e362b3cea84ff59939
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.0 MB (129983126 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ce09adc64dae0f4e67f5f9c2790baa25e4ac1617c047f5cf0eb3eb56e6bc75a`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Mon, 07 Apr 2025 05:23:21 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 07 Apr 2025 05:23:21 GMT
ENV GOTOOLCHAIN=local
# Mon, 07 Apr 2025 05:23:21 GMT
ENV GOPATH=/go
# Mon, 07 Apr 2025 05:23:21 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 07 Apr 2025 05:23:21 GMT
COPY /target/ / # buildkit
# Mon, 07 Apr 2025 05:23:21 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 07 Apr 2025 05:23:21 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 12:05:35 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e7542d01728964e647042c6ef7ce624e99ab47593a288bac60da39d5fd94275`  
		Last Modified: Mon, 07 Apr 2025 22:40:54 GMT  
		Size: 294.9 KB (294904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8dc044b4e18e8d70a1ecc203412289673855869397177339cdff79099bda4d2f`  
		Last Modified: Mon, 07 Apr 2025 22:40:51 GMT  
		Size: 126.0 MB (126045817 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1221d9b26ab21dad2fd9def1a27b8f2555a5f707945336cd3266328c8206de9e`  
		Last Modified: Mon, 07 Apr 2025 22:40:54 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.21` - unknown; unknown

```console
$ docker pull golang@sha256:6a4dc13bd3329ef7310792f6f74fb56bb7e0176d8ea6f96a4ef6b46ae9f8c56b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.9 KB (236941 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb6b514604e353bd270eb59de851d3eb0f36e62bb62afbc1ec3ade8259d81956`

```dockerfile
```

-	Layers:
	-	`sha256:df1b061216966d3b7a573a3605aceba6f5c49f4d575fcd3070fa957864f1c186`  
		Last Modified: Mon, 07 Apr 2025 22:40:54 GMT  
		Size: 211.8 KB (211799 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9427cadb6fcffc2535d4eaedd519dd72bcb9b6107a721449bb0e859482f9f999`  
		Last Modified: Mon, 07 Apr 2025 22:40:54 GMT  
		Size: 25.1 KB (25142 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.21` - linux; arm variant v6

```console
$ docker pull golang@sha256:100d10fbe8d2e4eddbc76ed5bdde27f991def6831e4681e4bd8fd529c058971d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.1 MB (125059813 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d659266e4c14b3e63a65d3846f5f95a3e5554563acc22a2810a11a4acedb2bee`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armhf.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Mon, 07 Apr 2025 05:23:21 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 07 Apr 2025 05:23:21 GMT
ENV GOTOOLCHAIN=local
# Mon, 07 Apr 2025 05:23:21 GMT
ENV GOPATH=/go
# Mon, 07 Apr 2025 05:23:21 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 07 Apr 2025 05:23:21 GMT
COPY /target/ / # buildkit
# Mon, 07 Apr 2025 05:23:21 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 07 Apr 2025 05:23:21 GMT
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
	-	`sha256:c7ff3e9e2bbaf23651bef493610b7f08b4463a41f86bea34a435953aaa3e899b`  
		Last Modified: Mon, 07 Apr 2025 22:50:24 GMT  
		Size: 121.4 MB (121398671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4858cf27ff5883ea4d2ca580de44110790f95e3309cbecbf7739d15f3f2225a1`  
		Last Modified: Mon, 07 Apr 2025 22:50:20 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.21` - unknown; unknown

```console
$ docker pull golang@sha256:d762b20e869fc434ccb7581724b102ddb6d2be661d91b424a67d07132fb35b56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.1 KB (25050 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a72fc5a9c4d26316d1eced712ae082649aff1039a944bc3d44e42b398be0ef5`

```dockerfile
```

-	Layers:
	-	`sha256:2b9053232448b11977b0257c6fb4d141c875abdf07987a9951130fd12c216a5e`  
		Last Modified: Mon, 07 Apr 2025 22:50:20 GMT  
		Size: 25.1 KB (25050 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.21` - linux; arm variant v7

```console
$ docker pull golang@sha256:d7f3a1466b376bb807a3e0dbc0e0f90bc0d2597fb35ccf2978a98324cb12f7b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.5 MB (124454371 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f56f148a6f65b31c773abd3acaf1071897acd3d57143a319bb00c80e17be6abb`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armv7.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Mon, 07 Apr 2025 05:23:21 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 07 Apr 2025 05:23:21 GMT
ENV GOTOOLCHAIN=local
# Mon, 07 Apr 2025 05:23:21 GMT
ENV GOPATH=/go
# Mon, 07 Apr 2025 05:23:21 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 07 Apr 2025 05:23:21 GMT
COPY /target/ / # buildkit
# Mon, 07 Apr 2025 05:23:21 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 07 Apr 2025 05:23:21 GMT
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
	-	`sha256:3d1290dc10baba6632fd5e083ce70494036c9bdcaeb42c9719e7ebc2bbe45fe3`  
		Last Modified: Mon, 07 Apr 2025 22:57:05 GMT  
		Size: 121.1 MB (121060891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac8cfc40e31b408f9aea6835f57c50bccef91691d4a2121f7a836e7ef876e359`  
		Last Modified: Mon, 07 Apr 2025 23:03:25 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.21` - unknown; unknown

```console
$ docker pull golang@sha256:0a39543d2bd758d269d554fde36318d2522115e4bf823d3b3fb1143f49bc2661
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **237.1 KB (237061 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:183a6eee2004cdc9f01c3ca6e1b7cafd21a96b7987682ade41a1b9cf832ad208`

```dockerfile
```

-	Layers:
	-	`sha256:2d815230a07c1dcff9b5a86e92b29e9a42984b0314336d832364f81c5543ae27`  
		Last Modified: Mon, 07 Apr 2025 23:03:25 GMT  
		Size: 211.8 KB (211795 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7b805c81e88178f92effba36befc3a7674f687bf41bd31ee9d94953067b211d5`  
		Last Modified: Mon, 07 Apr 2025 23:03:25 GMT  
		Size: 25.3 KB (25266 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.21` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:5f8f8397fb0371a7587afd4b55961b3c759ed2fb2af5e065eb0229d1a09bf214
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.0 MB (123034781 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f9cc87838f96e94d469e245f38ef6082b14d5bf85d208b438d3e76ffcac89af`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Mon, 07 Apr 2025 05:23:21 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 07 Apr 2025 05:23:21 GMT
ENV GOTOOLCHAIN=local
# Mon, 07 Apr 2025 05:23:21 GMT
ENV GOPATH=/go
# Mon, 07 Apr 2025 05:23:21 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 07 Apr 2025 05:23:21 GMT
COPY /target/ / # buildkit
# Mon, 07 Apr 2025 05:23:21 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 07 Apr 2025 05:23:21 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 12:05:33 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26e33b27c9b76515e1154a131a67e2f0fe88ba9e9bc48a1a704c790a0561e068`  
		Last Modified: Mon, 24 Mar 2025 21:29:27 GMT  
		Size: 297.9 KB (297871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52c040252f366631b10d12c85c56edda99c15cbe025d4e4abe3b2a7e0736ae53`  
		Last Modified: Mon, 07 Apr 2025 22:45:10 GMT  
		Size: 118.7 MB (118743723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17b0a022a3d36b86d68e539defa5a070f341d42c538c9495ff8d1cd63011e730`  
		Last Modified: Mon, 07 Apr 2025 22:49:16 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.21` - unknown; unknown

```console
$ docker pull golang@sha256:96b8d4b62bb7bdd3251fa0288c5cc9b44d222f780d9e9d49cf4ef4d1f2155656
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **237.2 KB (237157 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32271ea4f4c205274cb17f4b880d3d6ba06106038f1a490488e0e5db9698b413`

```dockerfile
```

-	Layers:
	-	`sha256:385707ff04e4f9789fc0de95f542acb2d74817695499dd2c558071591c77cc90`  
		Last Modified: Mon, 07 Apr 2025 22:49:16 GMT  
		Size: 211.9 KB (211855 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:049ed530bd64c510873386b8b09998395c3bbf653c3397ddb63ad5bc93b3c67f`  
		Last Modified: Mon, 07 Apr 2025 22:49:15 GMT  
		Size: 25.3 KB (25302 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.21` - linux; 386

```console
$ docker pull golang@sha256:43041a97dfc463d95a108f60e6a9511f46d16e5e0fdfbe9d555fc9a61b8c0a8b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.0 MB (127954683 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9032a83c479c67b7634d404f53843e967fb300e2dc5d1e77c97d0981513051d4`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Mon, 07 Apr 2025 05:23:21 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 07 Apr 2025 05:23:21 GMT
ENV GOTOOLCHAIN=local
# Mon, 07 Apr 2025 05:23:21 GMT
ENV GOPATH=/go
# Mon, 07 Apr 2025 05:23:21 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 07 Apr 2025 05:23:21 GMT
COPY /target/ / # buildkit
# Mon, 07 Apr 2025 05:23:21 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 07 Apr 2025 05:23:21 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:69aa61ccf55e5bf8e7a069b89e8afb42b4f3443b3785868795af8046d810d608`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.5 MB (3463623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a32ea710cde6f1b194f7c76bdb8abac3dcfb8bf3efa656755b4db4164f4a1c5`  
		Last Modified: Mon, 07 Apr 2025 22:41:18 GMT  
		Size: 295.6 KB (295597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ae3c30c1a3e04c667c09570d32c4fdc5fb10965c2ae3c7c8d16fb2e127e055f`  
		Last Modified: Mon, 07 Apr 2025 22:41:19 GMT  
		Size: 124.2 MB (124195306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1f7deb47928bf25e65ebcd787cbe718eddcaf094b95a3f42a0f706d1563d6b5`  
		Last Modified: Mon, 07 Apr 2025 22:41:18 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.21` - unknown; unknown

```console
$ docker pull golang@sha256:8b5b922269302e4365083219fc24f736c776638d4670ffb0f7a776c4e39bdd72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.8 KB (236833 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:938fd9043d11ad688edb4379960ade524a76439894de77a9a01851ee8a79d2c7`

```dockerfile
```

-	Layers:
	-	`sha256:aeeb5194df158db043c01c2cda7c8aa1ed9926ec7248c18ef63dacf522309e60`  
		Last Modified: Mon, 07 Apr 2025 22:41:18 GMT  
		Size: 211.7 KB (211734 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:786504a38614774d76b83289637e03dc2c08e17bf5e53d37b79c07e062cc04ca`  
		Last Modified: Mon, 07 Apr 2025 22:41:18 GMT  
		Size: 25.1 KB (25099 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.21` - linux; ppc64le

```console
$ docker pull golang@sha256:6e154199fdfb6d06c9bf795b6a39ff3b6c983496fa87f3e5a143876e7a9ff058
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.7 MB (124737181 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e78c7f5b4567d4130079081b46ad8918c955bfae1a70679d9e0876c11f12f6fc`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-ppc64le.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Mon, 07 Apr 2025 05:23:21 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 07 Apr 2025 05:23:21 GMT
ENV GOTOOLCHAIN=local
# Mon, 07 Apr 2025 05:23:21 GMT
ENV GOPATH=/go
# Mon, 07 Apr 2025 05:23:21 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 07 Apr 2025 05:23:21 GMT
COPY /target/ / # buildkit
# Mon, 07 Apr 2025 05:23:21 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 07 Apr 2025 05:23:21 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:184b14480d317057da092a0994ad6baf4b2df588108f43969f8fd56f021af2c6`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.6 MB (3574345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c27442ea8b4dc6fdf584c0b30a8e1943de4b659fd7ec220499d43ff5c7d4c1c8`  
		Last Modified: Mon, 24 Mar 2025 21:48:27 GMT  
		Size: 298.3 KB (298274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ff7c926c5215703e9cc5f378e25970c1665c6647a6d87c93d8dedc53c595868`  
		Last Modified: Mon, 07 Apr 2025 22:42:14 GMT  
		Size: 120.9 MB (120864404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fdf075dacdf518cd51cd52529804587fb15cab4e6c64abaa2022e30f67031cf`  
		Last Modified: Mon, 07 Apr 2025 22:45:37 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.21` - unknown; unknown

```console
$ docker pull golang@sha256:3165388aad09b0463096e344348033071cdc54e07b970357da4e83ebd12d0bde
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.1 KB (235122 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3616bda8aff7c256a5809d24d085f7c4c7315b4ae8095a13e5ba4552fed4ec8`

```dockerfile
```

-	Layers:
	-	`sha256:85febdb793e8b0bd217c098d05d47d50bb54a1f25bc9bb0272bb788a1a04adb2`  
		Last Modified: Mon, 07 Apr 2025 22:45:37 GMT  
		Size: 209.9 KB (209922 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5a1495ebbbbc83b89a743b50760c5707d1f2fbadc24b6a77a1f9dfb19d61eb1d`  
		Last Modified: Mon, 07 Apr 2025 22:45:37 GMT  
		Size: 25.2 KB (25200 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.21` - linux; riscv64

```console
$ docker pull golang@sha256:aa484345537aad95c04fb16f9e82b93ee44f108cb6b033483551bf2a0476c947
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.9 MB (124862938 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d45c64871a3e5f3850a27cac3c400a93af84bde93ce3f501bd8e91a324a5c5f`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-riscv64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Mon, 07 Apr 2025 05:23:21 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 07 Apr 2025 05:23:21 GMT
ENV GOTOOLCHAIN=local
# Mon, 07 Apr 2025 05:23:21 GMT
ENV GOPATH=/go
# Mon, 07 Apr 2025 05:23:21 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 07 Apr 2025 05:23:21 GMT
COPY /target/ / # buildkit
# Mon, 07 Apr 2025 05:23:21 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 07 Apr 2025 05:23:21 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:7df33f7ad8beb367ac09bdd1b2f220db3ee2bbdda14a6310d1340e5628b5ba88`  
		Last Modified: Fri, 14 Feb 2025 18:56:36 GMT  
		Size: 3.4 MB (3351439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd81befb40433dc7da0b53543acafce5d4aa75d9a2bc5815536bad6b9db1682b`  
		Last Modified: Sun, 16 Feb 2025 05:52:00 GMT  
		Size: 295.3 KB (295346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0915774cce7d1e6c7d80a450b11f0a26babf55a35c0c3099e39033a85a5bb45b`  
		Last Modified: Mon, 07 Apr 2025 23:27:36 GMT  
		Size: 121.2 MB (121215995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca41435e4d963379edda4bf4f24a7ec6ea06fc9f5eb661cefaba5e5990ea68f3`  
		Last Modified: Mon, 07 Apr 2025 23:27:19 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.21` - unknown; unknown

```console
$ docker pull golang@sha256:f1fb1d9a9c8274273a4c378a4ce5ed74d12c036bd72dbd042e5acfef901c41c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.1 KB (235118 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e57054a8718f2145906e1ea95c96a375264aef70207fc6a82be4f5b72258d72`

```dockerfile
```

-	Layers:
	-	`sha256:fed540f878086b46fe4d6b2f4bdd959da9c711fb00b41ef280eeca41a602ccd0`  
		Last Modified: Mon, 07 Apr 2025 23:27:19 GMT  
		Size: 209.9 KB (209918 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:03742589b89bd40b348db0f7d4fc0065ee0b536c6360336884831fe1989bdf44`  
		Last Modified: Mon, 07 Apr 2025 23:27:19 GMT  
		Size: 25.2 KB (25200 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.21` - linux; s390x

```console
$ docker pull golang@sha256:2004ac0c0132b6046d804f4abb815262e9d5ceebcad86d7626866c51f7c179f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.1 MB (127070350 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65abb867882fdf54985c215d67a9f6c82e2ab0e5bad15cba49180c3100050ee4`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-s390x.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Mon, 07 Apr 2025 05:23:21 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 07 Apr 2025 05:23:21 GMT
ENV GOTOOLCHAIN=local
# Mon, 07 Apr 2025 05:23:21 GMT
ENV GOPATH=/go
# Mon, 07 Apr 2025 05:23:21 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 07 Apr 2025 05:23:21 GMT
COPY /target/ / # buildkit
# Mon, 07 Apr 2025 05:23:21 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 07 Apr 2025 05:23:21 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:c1a599607158512214777614f916f8193d29fd34b656d47dfc26314af01e2af4`  
		Last Modified: Fri, 14 Feb 2025 12:05:25 GMT  
		Size: 3.5 MB (3467567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be80be2c55902add1c4b1f14066b1b4da724beaa2e355b53f8dd45b4887d9b9c`  
		Last Modified: Mon, 24 Mar 2025 21:26:52 GMT  
		Size: 296.2 KB (296183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:422ac8743b3d8d2ff96125eac5437f0e522f00570e50d835f0fcd015b8c6cee0`  
		Last Modified: Mon, 07 Apr 2025 22:47:48 GMT  
		Size: 123.3 MB (123306442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:466d804e7be99ad62a1d04e982f84d83b30ceb1b062a7f127c23e9b635f1789e`  
		Last Modified: Mon, 07 Apr 2025 22:50:54 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.21` - unknown; unknown

```console
$ docker pull golang@sha256:f9883cefa6bb3993c9fed160d48002b9613b0532f9f3d38777284c2795dd588c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.0 KB (234988 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ad983503b06be604e325d00dee6137c6f1140a5e3f7d8a76c137927761e1c0d`

```dockerfile
```

-	Layers:
	-	`sha256:ae2523fa9ef9068853878d8689a9756b82cd16c3d0045df22dbdc9c22477b2d2`  
		Last Modified: Mon, 07 Apr 2025 22:50:54 GMT  
		Size: 209.8 KB (209848 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3d12c6978d922a3783e183b37e7dbc23b9a6f640550e0dc3f60a7d244c9aebfa`  
		Last Modified: Mon, 07 Apr 2025 22:50:54 GMT  
		Size: 25.1 KB (25140 bytes)  
		MIME: application/vnd.in-toto+json
