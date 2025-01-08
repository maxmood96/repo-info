## `golang:alpine`

```console
$ docker pull golang@sha256:13aaa4b92fd4dc81683816b4b62041442e9f685deeb848897ce78c5e2fb03af7
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

### `golang:alpine` - linux; amd64

```console
$ docker pull golang@sha256:fe60376abcd2ed517529818a5ebccc2b4493fa9c19d6f69c45deaddf3b738e72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.0 MB (77963340 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b942bd2d3be3bdde1cc7e0f92601d3e896468f7ef7f3292c2bb254408efc019`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 05 Dec 2024 13:15:10 GMT
ADD alpine-minirootfs-3.21.1-x86_64.tar.gz / # buildkit
# Thu, 05 Dec 2024 13:15:10 GMT
CMD ["/bin/sh"]
# Thu, 05 Dec 2024 13:15:10 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Thu, 05 Dec 2024 13:15:10 GMT
ENV GOLANG_VERSION=1.23.4
# Thu, 05 Dec 2024 13:15:10 GMT
ENV GOTOOLCHAIN=local
# Thu, 05 Dec 2024 13:15:10 GMT
ENV GOPATH=/go
# Thu, 05 Dec 2024 13:15:10 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Dec 2024 13:15:10 GMT
COPY /target/ / # buildkit
# Thu, 05 Dec 2024 13:15:10 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Thu, 05 Dec 2024 13:15:10 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:245043d9199c263f869fc0558f43f7cb98bbc92acdd5def1b4f690adc0ac7807`  
		Last Modified: Mon, 06 Jan 2025 21:44:42 GMT  
		Size: 3.6 MB (3636222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc6424b1ac7ca9a6947ed9bcab469cb2bf68c5fbf964e8c10d909839089d61b9`  
		Last Modified: Tue, 07 Jan 2025 03:32:01 GMT  
		Size: 279.5 KB (279511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06f05ace1117d62b655e04f6f73c83617e3e0febc38681dbedf58f477dd0658c`  
		Last Modified: Tue, 03 Dec 2024 22:28:52 GMT  
		Size: 74.0 MB (74047449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:546fcad2f4c942e8f5c89f28f20aeece4a42768677bc8a5c34be5f3b055451b1`  
		Last Modified: Tue, 07 Jan 2025 03:32:01 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:alpine` - unknown; unknown

```console
$ docker pull golang@sha256:e5a43e31851ab97f3c50422e0266e552a63d09f8066f429810f4e385d8e28617
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **237.2 KB (237169 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4470c1a34d478b81d87fb1b53176306fcf3843a2c4fdff066b479ad95d7967c5`

```dockerfile
```

-	Layers:
	-	`sha256:ebc26847062e9f3ce61fb4af8b88fb7af2da1a048c9dd425d20a104bd73c1066`  
		Last Modified: Tue, 07 Jan 2025 03:32:01 GMT  
		Size: 211.1 KB (211099 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:25620488ea611b3b88ef7b453d79510663c85ebefc79b074e06b3e4bfed4f312`  
		Last Modified: Tue, 07 Jan 2025 03:32:01 GMT  
		Size: 26.1 KB (26070 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:alpine` - linux; arm variant v6

```console
$ docker pull golang@sha256:44b0ea55bc37ad9be4c76547d198f042db35bbab06567408496d2a95c0c41b78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.8 MB (75840069 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5277f0bd3213adaea19209ad4bda299b3b6e890274561a7b764ee7ad80d0e7d9`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 05 Dec 2024 13:15:10 GMT
ADD alpine-minirootfs-3.21.1-armhf.tar.gz / # buildkit
# Thu, 05 Dec 2024 13:15:10 GMT
CMD ["/bin/sh"]
# Thu, 05 Dec 2024 13:15:10 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Thu, 05 Dec 2024 13:15:10 GMT
ENV GOLANG_VERSION=1.23.4
# Thu, 05 Dec 2024 13:15:10 GMT
ENV GOTOOLCHAIN=local
# Thu, 05 Dec 2024 13:15:10 GMT
ENV GOPATH=/go
# Thu, 05 Dec 2024 13:15:10 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Dec 2024 13:15:10 GMT
COPY /target/ / # buildkit
# Thu, 05 Dec 2024 13:15:10 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Thu, 05 Dec 2024 13:15:10 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:31d4a7f5d4e2c1fd6b13116c69b324d9255a249ba92b63cd7d98924ec5438675`  
		Last Modified: Tue, 07 Jan 2025 02:29:34 GMT  
		Size: 3.4 MB (3361034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7a1a066ba01319a2a413a4b4e8495e18954e397883b57ded903afa9d7bd4a5d`  
		Last Modified: Tue, 07 Jan 2025 06:42:03 GMT  
		Size: 280.3 KB (280338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:569843b3031b27806b4332ef906025ac81fe5ab3623a61a6d2306598bfd512bf`  
		Last Modified: Tue, 03 Dec 2024 22:28:55 GMT  
		Size: 72.2 MB (72198540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ebea862779beea11632cde3c61e56e19cb6930299b2552c6df6997a3571ab9a`  
		Last Modified: Tue, 07 Jan 2025 06:51:08 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:alpine` - unknown; unknown

```console
$ docker pull golang@sha256:007d38dfb24d5ba7b58e3ed9619f0dc6ae6fd97e11024a8c84106723dfcacd3e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.0 KB (25989 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef18837a97260be0b3aa5e20262d99a1ef2c040608cf84357d68bf208ec047e7`

```dockerfile
```

-	Layers:
	-	`sha256:382e00a4910f83f02f985da7acc0fadf2bc690d9a047c778e02c20bc2c5ff00f`  
		Last Modified: Tue, 07 Jan 2025 06:51:08 GMT  
		Size: 26.0 KB (25989 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:alpine` - linux; arm variant v7

```console
$ docker pull golang@sha256:35a36708c8521e46cf9ab4a4fdb4fe5c28e82ef92bdfc983af2cf43d1c4b6eed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.6 MB (75571342 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7f388b186c7decd9f217a7b1c609aff505e82d94721ebce0b884f8b8f7a8196`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 05 Dec 2024 13:15:10 GMT
ADD alpine-minirootfs-3.21.1-armv7.tar.gz / # buildkit
# Thu, 05 Dec 2024 13:15:10 GMT
CMD ["/bin/sh"]
# Thu, 05 Dec 2024 13:15:10 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Thu, 05 Dec 2024 13:15:10 GMT
ENV GOLANG_VERSION=1.23.4
# Thu, 05 Dec 2024 13:15:10 GMT
ENV GOTOOLCHAIN=local
# Thu, 05 Dec 2024 13:15:10 GMT
ENV GOPATH=/go
# Thu, 05 Dec 2024 13:15:10 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Dec 2024 13:15:10 GMT
COPY /target/ / # buildkit
# Thu, 05 Dec 2024 13:15:10 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Thu, 05 Dec 2024 13:15:10 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:fa398bd1707194d783a6221bb60ba630f074222cdc0f4b6a05d9167d6e9c4a9f`  
		Last Modified: Tue, 07 Jan 2025 02:55:27 GMT  
		Size: 3.1 MB (3093241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53369145b61506ac256a77458c81613de9e873072eb9392b09431243ceb0de89`  
		Last Modified: Tue, 07 Jan 2025 06:19:28 GMT  
		Size: 279.5 KB (279502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af30004a6a0d94684e60c07bbc44989294b76634fe7cc182dfb2140b1e8c877d`  
		Last Modified: Wed, 04 Dec 2024 07:17:17 GMT  
		Size: 72.2 MB (72198441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6561ec16937062682fc905da97ac87d7995da2ae63b956b444ff9aa4deaed4aa`  
		Last Modified: Tue, 07 Jan 2025 06:40:06 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:alpine` - unknown; unknown

```console
$ docker pull golang@sha256:91b537b0e35e8fcd82d10521ed57a6a09a87305f9bb8ff9e3b6eb94b22a01bdc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **237.3 KB (237335 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f83ae81a3762a42293dd1566ec5aace9f110487fb4e2f2b4c33837062321c4f`

```dockerfile
```

-	Layers:
	-	`sha256:85e578ad3e3c3a5a18d24f15bc51ba98d484007f194b7bc974db44e1198650d5`  
		Last Modified: Tue, 07 Jan 2025 06:40:06 GMT  
		Size: 211.1 KB (211131 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:130a711d429e1e21abcf02c19e36b5ef058760531893e1362b7228734a27b698`  
		Size: 26.2 KB (26204 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:alpine` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:3f136f23fb55a02192c17387f6b7365c0861c254799776d6f385a2c35666c9ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.9 MB (74938275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b3cbcf5e4be13f76804219f4a2558c7d1cdc038f327008b1a29ac689652cf8e`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 05 Dec 2024 13:15:10 GMT
ADD alpine-minirootfs-3.21.1-aarch64.tar.gz / # buildkit
# Thu, 05 Dec 2024 13:15:10 GMT
CMD ["/bin/sh"]
# Thu, 05 Dec 2024 13:15:10 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Thu, 05 Dec 2024 13:15:10 GMT
ENV GOLANG_VERSION=1.23.4
# Thu, 05 Dec 2024 13:15:10 GMT
ENV GOTOOLCHAIN=local
# Thu, 05 Dec 2024 13:15:10 GMT
ENV GOPATH=/go
# Thu, 05 Dec 2024 13:15:10 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Dec 2024 13:15:10 GMT
COPY /target/ / # buildkit
# Thu, 05 Dec 2024 13:15:10 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Thu, 05 Dec 2024 13:15:10 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:707c94c90c597447ce10a36c9b56355c1cc67d0cf593a592daeb419d99a30d85`  
		Last Modified: Tue, 07 Jan 2025 03:02:50 GMT  
		Size: 4.0 MB (3983007 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:712339dc7afde33ea8162a86ca2a257bb3cf6faa8436da4b8d6f01a8dad2e745`  
		Last Modified: Tue, 07 Jan 2025 07:09:01 GMT  
		Size: 281.7 KB (281695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39f8f326b04424eb2027d1f0e3255fe568d71a5567f894a08cd86605ebe51c58`  
		Last Modified: Wed, 04 Dec 2024 01:41:07 GMT  
		Size: 70.7 MB (70673417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6a812228022cb57d695c9ddbd69ffabca8127d521e2d91cfa31e72aa27984f9`  
		Last Modified: Tue, 07 Jan 2025 07:42:30 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:alpine` - unknown; unknown

```console
$ docker pull golang@sha256:ad17c2f689edb6d285b25662706436f879ffdc48a19e337baa802554c539753f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **237.5 KB (237454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0076abe4993e3d6fdf0d36f6eda48c9d35703a4699f83be1a7fcf8f2f1e284f`

```dockerfile
```

-	Layers:
	-	`sha256:9aa3cc31fbabae19ea5ed15885b922d42d07f6f06139aa1e91805c5b7a9fb788`  
		Last Modified: Tue, 07 Jan 2025 07:42:30 GMT  
		Size: 211.2 KB (211203 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7e94b00735a54f4839c6368be2a7326834f691f8d8a26ba582cfd94fa0d81e98`  
		Last Modified: Tue, 07 Jan 2025 07:42:30 GMT  
		Size: 26.3 KB (26251 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:alpine` - linux; 386

```console
$ docker pull golang@sha256:96be875c9c430c3e8ed285230072fc0e9ead1389cb573cc3676e3338d01d5632
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.7 MB (75651484 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfa8e515a035c704fcb533bfadfb9c5e53d36ee3857fb0a6cb344b76cda7c332`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 05 Dec 2024 13:15:10 GMT
ADD alpine-minirootfs-3.21.1-x86.tar.gz / # buildkit
# Thu, 05 Dec 2024 13:15:10 GMT
CMD ["/bin/sh"]
# Thu, 05 Dec 2024 13:15:10 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Thu, 05 Dec 2024 13:15:10 GMT
ENV GOLANG_VERSION=1.23.4
# Thu, 05 Dec 2024 13:15:10 GMT
ENV GOTOOLCHAIN=local
# Thu, 05 Dec 2024 13:15:10 GMT
ENV GOPATH=/go
# Thu, 05 Dec 2024 13:15:10 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Dec 2024 13:15:10 GMT
COPY /target/ / # buildkit
# Thu, 05 Dec 2024 13:15:10 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Thu, 05 Dec 2024 13:15:10 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:1b51cef20fac755ea70acf005c7461407387b0deae88500e38a1982868469f7a`  
		Last Modified: Wed, 08 Jan 2025 03:05:41 GMT  
		Size: 3.5 MB (3458271 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:964c7b1819af1853b1bd285178b7a8829ee44e54400125caa6a793308f54ade4`  
		Last Modified: Tue, 07 Jan 2025 03:15:38 GMT  
		Size: 279.9 KB (279933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:253ee978a239d9a54a2ed89c291f3c5c0ee5f67c1dc8c9ff24b239116398d826`  
		Size: 71.9 MB (71913121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:197dbf92ce21fa8b249db6463b8ef0ad828cdb7a435914186dd6581fc4ef04e8`  
		Last Modified: Tue, 07 Jan 2025 03:15:38 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:alpine` - unknown; unknown

```console
$ docker pull golang@sha256:9a2611d6610cd0f7ae8c419720c24213616ed87df6db110afa0de08f3aab6d3b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **237.0 KB (237032 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:072fe11fa5e3aa5260cc9ab062b8e22981789c3feb0bc3b3100c9588281091cb`

```dockerfile
```

-	Layers:
	-	`sha256:6a70fdf5b4bd63d4a58836b51348bb9e21b4c3b14b1e226cd83da446a578be21`  
		Last Modified: Tue, 07 Jan 2025 03:15:38 GMT  
		Size: 211.0 KB (211018 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e79722654d1c65f358c2da3a5985f524be54147df04343464e2ac82cda845faa`  
		Last Modified: Tue, 07 Jan 2025 03:15:38 GMT  
		Size: 26.0 KB (26014 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:alpine` - linux; ppc64le

```console
$ docker pull golang@sha256:66c115f3009a2074ec952a196a0b0268c6f464e920958c3784f08f83c5d9208f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.7 MB (74689552 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd0996a60579acb876803b0b5fe03167f138fd639350adc43c854cc45d548ce1`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 05 Dec 2024 13:15:10 GMT
ADD alpine-minirootfs-3.21.1-ppc64le.tar.gz / # buildkit
# Thu, 05 Dec 2024 13:15:10 GMT
CMD ["/bin/sh"]
# Thu, 05 Dec 2024 13:15:10 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Thu, 05 Dec 2024 13:15:10 GMT
ENV GOLANG_VERSION=1.23.4
# Thu, 05 Dec 2024 13:15:10 GMT
ENV GOTOOLCHAIN=local
# Thu, 05 Dec 2024 13:15:10 GMT
ENV GOPATH=/go
# Thu, 05 Dec 2024 13:15:10 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Dec 2024 13:15:10 GMT
COPY /target/ / # buildkit
# Thu, 05 Dec 2024 13:15:10 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Thu, 05 Dec 2024 13:15:10 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:9207393f0daad55cddbc775f55edde5baecdca9e0441c9c1f627f2394d28b7c3`  
		Last Modified: Tue, 07 Jan 2025 02:32:05 GMT  
		Size: 3.6 MB (3567745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60799cfa64278921df2cb5022a9b2506e24511fba4464615a66b4483fdd67cc1`  
		Last Modified: Tue, 07 Jan 2025 06:12:41 GMT  
		Size: 282.1 KB (282104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b834890572191b3d66e6bd561aad556f3c52e760e67fe9e31f02ad3d5139f55e`  
		Size: 70.8 MB (70839544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4ad8679b9cc6f5e34066fc27fb4803d6bbd854dc561f9100e2178abf74a4d94`  
		Last Modified: Tue, 07 Jan 2025 06:35:29 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:alpine` - unknown; unknown

```console
$ docker pull golang@sha256:3c99cadb25dbcf175c455172b18f26e0e2e458be91ca6ef323c3f84a2d7c624e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.4 KB (235384 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b37d05bdb5d89cb27ebd7f5dbd425dc69e1a613164ad3ccb8c4365f23f82b296`

```dockerfile
```

-	Layers:
	-	`sha256:38e6f483d1249326c614d8f068b2d29604644259203a4c1fb8045082268cd9c9`  
		Last Modified: Tue, 07 Jan 2025 06:35:29 GMT  
		Size: 209.2 KB (209242 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5f27ec41fd068d402479964dd074ef79e32142704e71daaf547fd7f2f1b845ca`  
		Last Modified: Tue, 07 Jan 2025 06:35:29 GMT  
		Size: 26.1 KB (26142 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:alpine` - linux; riscv64

```console
$ docker pull golang@sha256:d0c6727dbc30a2607ca6d2a2865f84540175514bcc1c67ca7b077d112d419588
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.9 MB (74894739 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3472ea1ace70f7c20da92ff09529851e73049bc71a9cab6489a49e6980dc73a5`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-riscv64.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
CMD ["/bin/sh"]
# Thu, 05 Dec 2024 13:15:10 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Thu, 05 Dec 2024 13:15:10 GMT
ENV GOLANG_VERSION=1.23.4
# Thu, 05 Dec 2024 13:15:10 GMT
ENV GOTOOLCHAIN=local
# Thu, 05 Dec 2024 13:15:10 GMT
ENV GOPATH=/go
# Thu, 05 Dec 2024 13:15:10 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Dec 2024 13:15:10 GMT
COPY /target/ / # buildkit
# Thu, 05 Dec 2024 13:15:10 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Thu, 05 Dec 2024 13:15:10 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:a6d4526e72329f3572a607f27b44cacf8e150856b24a0178c889732b00471eb3`  
		Last Modified: Thu, 05 Dec 2024 22:19:03 GMT  
		Size: 3.4 MB (3354022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:352d2aed11821bec39048fd95800ed8324f4ffbc936cc77681114832e36fdb97`  
		Last Modified: Fri, 06 Dec 2024 22:31:00 GMT  
		Size: 299.6 KB (299638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c56ea5001679e325e9959f4e49e737d7b5d8a17fc575fd3810ab4495a88e73ee`  
		Size: 71.2 MB (71240920 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:823549eb5d032cbe32b843ae14c0e8e8d506cd24122a9b9045affc7d74afd63c`  
		Last Modified: Fri, 06 Dec 2024 22:31:00 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:alpine` - unknown; unknown

```console
$ docker pull golang@sha256:ab8a215ebbe9109b3dd7ac2ba0f93446269f445eaddf6a1393941555246a8e33
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **242.6 KB (242625 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6bb1b5d5e78dd696161d40f1ab9a887c0e424459247d04447ca732e3e2bf546a`

```dockerfile
```

-	Layers:
	-	`sha256:c259a8b951cab2cb0cbacf058261f8e90b6d97cef540e87ed0dd96b3e161e330`  
		Last Modified: Fri, 06 Dec 2024 22:31:00 GMT  
		Size: 216.5 KB (216483 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0e964aef05d43cc899631079a5cde222cdda9e9eee56df6e4f185e5c40f420be`  
		Last Modified: Fri, 06 Dec 2024 22:31:00 GMT  
		Size: 26.1 KB (26142 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:alpine` - linux; s390x

```console
$ docker pull golang@sha256:ad7c4815b182d216d4b53c14585a240f85cca478e3139e421c67baea4bf24351
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.7 MB (76709920 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fdf31e8bb68a98f83594e1733bd3fa0afb3a2bbef79c0fdbcfef8b51d7a6a336`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 05 Dec 2024 13:15:10 GMT
ADD alpine-minirootfs-3.21.1-s390x.tar.gz / # buildkit
# Thu, 05 Dec 2024 13:15:10 GMT
CMD ["/bin/sh"]
# Thu, 05 Dec 2024 13:15:10 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Thu, 05 Dec 2024 13:15:10 GMT
ENV GOLANG_VERSION=1.23.4
# Thu, 05 Dec 2024 13:15:10 GMT
ENV GOTOOLCHAIN=local
# Thu, 05 Dec 2024 13:15:10 GMT
ENV GOPATH=/go
# Thu, 05 Dec 2024 13:15:10 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Dec 2024 13:15:10 GMT
COPY /target/ / # buildkit
# Thu, 05 Dec 2024 13:15:10 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Thu, 05 Dec 2024 13:15:10 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:93a724ed1843277c272a09a7779ca31a802938fe3a88142df42e291e0dc759c3`  
		Last Modified: Tue, 07 Jan 2025 02:32:17 GMT  
		Size: 3.5 MB (3459449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c80aba2f3c52b257c2a9bd1f1926ff778f3cdf5ace50a9adf1eaed5a22d7a96`  
		Last Modified: Tue, 07 Jan 2025 06:18:07 GMT  
		Size: 280.5 KB (280499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1eab153b4468df7f657167533fa78804e60b235edee0f04ec5dcc52a35b056da`  
		Last Modified: Tue, 03 Dec 2024 22:40:01 GMT  
		Size: 73.0 MB (72969813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:622fe77d690492837a240ee7b24f5d03b4d27862a8a43c77ebf0ff4c1540e355`  
		Last Modified: Tue, 07 Jan 2025 06:41:31 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:alpine` - unknown; unknown

```console
$ docker pull golang@sha256:c479c78227e36a9427220c809e9e04d2e413a16354adc712d545d3df13c95666
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.2 KB (235218 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:962627267e4d9328316248152ee946597ea03d4cdb264f7b9ba718e5a31ed8b2`

```dockerfile
```

-	Layers:
	-	`sha256:1da95dac1b27d9e9351c6f4786168154f37c2f3c6fbd601e96a5310830c09eb4`  
		Last Modified: Tue, 07 Jan 2025 06:41:31 GMT  
		Size: 209.1 KB (209148 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:be1c9e9e78e2c7d9a94d43ac1cc30d40a27165e711bbe54b2a3356e6c4efe00a`  
		Last Modified: Wed, 08 Jan 2025 01:33:52 GMT  
		Size: 26.1 KB (26070 bytes)  
		MIME: application/vnd.in-toto+json
