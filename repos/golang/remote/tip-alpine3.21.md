## `golang:tip-alpine3.21`

```console
$ docker pull golang@sha256:57ff4371cb41e798006794ff311d629c275bd07c6367a718a5d62af9a71fb39d
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
$ docker pull golang@sha256:ee8f2fd1bc1c58459b298d1dac47f73b64c7c47c83bff391579e79b65902b038
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.5 MB (88533864 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0510b7af469690051d7dea0a0237e9f556510fc6f484b1e71ac8e0ced06ba31f`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Mon, 06 Oct 2025 05:23:19 GMT
ADD alpine-minirootfs-3.21.5-x86_64.tar.gz / # buildkit
# Mon, 06 Oct 2025 05:23:19 GMT
CMD ["/bin/sh"]
# Mon, 06 Oct 2025 05:23:19 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 06 Oct 2025 05:23:19 GMT
ENV GOTOOLCHAIN=local
# Mon, 06 Oct 2025 05:23:19 GMT
ENV GOPATH=/go
# Mon, 06 Oct 2025 05:23:19 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 06 Oct 2025 05:23:19 GMT
COPY /target/ / # buildkit
# Mon, 06 Oct 2025 05:23:19 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 06 Oct 2025 05:23:19 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:f637881d1138581d892d9eb942c56e0ccc7758fe3bdc0f1e6cd66059fdfd8185`  
		Last Modified: Wed, 08 Oct 2025 12:54:09 GMT  
		Size: 3.6 MB (3642569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d01cb87a4b07776e019c3edd7b6cf49bfb6fca564db3893451c7171ff2da5489`  
		Last Modified: Wed, 08 Oct 2025 23:40:04 GMT  
		Size: 291.1 KB (291121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df330a3159ef2a0bf41805e9465d878d806cf4287e8fdd250ddbc3e024a94e45`  
		Last Modified: Mon, 06 Oct 2025 21:03:35 GMT  
		Size: 84.6 MB (84600016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08929cd0a8f49433e1ad9057dbf452952efaa3ce4de04f830d442db3095881da`  
		Last Modified: Wed, 08 Oct 2025 23:40:04 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.21` - unknown; unknown

```console
$ docker pull golang@sha256:e8a55f9c69066c85a333ff0f6be0859f9d8d7d9d9634254188f4429551ea2352
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **217.2 KB (217240 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9eb74fcde650000a52ce1da6756903414a45350ea949ca4dc8fbe4eb187466f`

```dockerfile
```

-	Layers:
	-	`sha256:709069fb51ffc8f4cc3e4a722bf5066b6c68b39a7cda7c1b5cb7b94161a89bc4`  
		Last Modified: Thu, 09 Oct 2025 02:24:21 GMT  
		Size: 192.7 KB (192733 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ba98ce62a598f8bfcab79cd13a4288cffabb38e907085ac0a24859a94a46e46b`  
		Last Modified: Thu, 09 Oct 2025 02:24:22 GMT  
		Size: 24.5 KB (24507 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.21` - linux; arm variant v6

```console
$ docker pull golang@sha256:32eff8a1874ef8a3328a6900518728319087fd87ea11157d8c2692e61971e403
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.0 MB (90991131 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a9865d7c963d1a69549550c399bd470bbbb49dfd5ddf9e7a803fb59f1f5e1fb`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:06:42 GMT
ADD alpine-minirootfs-3.21.5-armhf.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:06:42 GMT
CMD ["/bin/sh"]
# Mon, 13 Oct 2025 05:23:19 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 13 Oct 2025 05:23:19 GMT
ENV GOTOOLCHAIN=local
# Mon, 13 Oct 2025 05:23:19 GMT
ENV GOPATH=/go
# Mon, 13 Oct 2025 05:23:19 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 13 Oct 2025 05:23:19 GMT
COPY /target/ / # buildkit
# Mon, 13 Oct 2025 05:23:19 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 13 Oct 2025 05:23:19 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:f8b30cbd0fab9e5a803578a09c973d18d7450816d914e63e04e5c2edd79f8bee`  
		Last Modified: Wed, 08 Oct 2025 21:00:33 GMT  
		Size: 3.4 MB (3365468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b497dfca13b84f2c425d2ed2b32a24d6982f04a7fada3fe3ab8542ee2e6462dc`  
		Last Modified: Mon, 13 Oct 2025 18:26:31 GMT  
		Size: 292.2 KB (292236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b74301a8b76982b257bb111ec9b6820a6de48153ddc455c61eafa801ef71fcc5`  
		Last Modified: Mon, 13 Oct 2025 20:24:30 GMT  
		Size: 87.3 MB (87333269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48200b34caf57e170fb0ce9eed47f677078af43d1f67e74b0101b6273f48b9d9`  
		Last Modified: Mon, 13 Oct 2025 18:26:31 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.21` - unknown; unknown

```console
$ docker pull golang@sha256:1e08b725608617cd3cb07a9a8a67ec7213420aaf898ef32c8183efbc23073e16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.4 KB (24404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac883ec1629394fb131e876f9b0f7b5cbcf90a911b0ea1641e84237dddbe24ca`

```dockerfile
```

-	Layers:
	-	`sha256:02bbd455c9c1ef8fcf894cce6fce409e17563c88af89f4e930561991bd6b57c5`  
		Last Modified: Mon, 13 Oct 2025 20:24:08 GMT  
		Size: 24.4 KB (24404 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.21` - linux; arm variant v7

```console
$ docker pull golang@sha256:42c0b9b59ccd2810d5a288dd7c189e44801ba904a66a1c1b7600ca1281119f80
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.5 MB (90464414 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8db5945b2baab93c7ae76cf313b49408f8e3a2e6a64dfa0e3073c26e1e82c455`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:06:42 GMT
ADD alpine-minirootfs-3.21.5-armv7.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:06:42 GMT
CMD ["/bin/sh"]
# Mon, 13 Oct 2025 05:23:19 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 13 Oct 2025 05:23:19 GMT
ENV GOTOOLCHAIN=local
# Mon, 13 Oct 2025 05:23:19 GMT
ENV GOPATH=/go
# Mon, 13 Oct 2025 05:23:19 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 13 Oct 2025 05:23:19 GMT
COPY /target/ / # buildkit
# Mon, 13 Oct 2025 05:23:19 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 13 Oct 2025 05:23:19 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:520d06ecc3ba4ec2920319fa6f2cc6bea9a9c1d5a43808c1d2388522c37d7b30`  
		Last Modified: Wed, 08 Oct 2025 16:24:34 GMT  
		Size: 3.1 MB (3098611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4971328e2e10bc8520e9951bd2772256d012bcef2aa6e189325900d3e2232a15`  
		Last Modified: Mon, 13 Oct 2025 18:23:37 GMT  
		Size: 291.1 KB (291146 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:991b3f77f198194af8440022630b5f3555d19874bc1b8dcfcdeb4ff1346ed16b`  
		Last Modified: Mon, 13 Oct 2025 18:23:46 GMT  
		Size: 87.1 MB (87074499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c4800ce785496d6858cfb4b670d7b37ce4e2c27e7abe7509de465899ab709aa`  
		Last Modified: Mon, 13 Oct 2025 18:23:36 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.21` - unknown; unknown

```console
$ docker pull golang@sha256:25be71c6c2b3ba72c2fe0270c0dfa829fbea6aac48e57171b7da0a59264aec5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.8 KB (218829 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d36dd496c0a7b0dfb70d218f6b87c0ec0a7acc383508ccf35ceb753b1227678d`

```dockerfile
```

-	Layers:
	-	`sha256:f6483742aba9d1f40e64ef435466446977cef834448f7256ecbe644830a1d79c`  
		Last Modified: Mon, 13 Oct 2025 20:24:12 GMT  
		Size: 194.2 KB (194209 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:517b9144bfe10b2e881fb0b181c56704022dfae255e3310001dd3649d26390d7`  
		Last Modified: Mon, 13 Oct 2025 20:24:13 GMT  
		Size: 24.6 KB (24620 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.21` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:be28586399ed76981e8b8e5a04c2a13b852c7b18f0f1b7b614add6ea38074708
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.3 MB (90328644 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96af3e1364ea5659e13f9c98118d36f8715ea9f38b0b02a090bb02686a4a19f1`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:06:42 GMT
ADD alpine-minirootfs-3.21.5-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:06:42 GMT
CMD ["/bin/sh"]
# Mon, 13 Oct 2025 05:23:19 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 13 Oct 2025 05:23:19 GMT
ENV GOTOOLCHAIN=local
# Mon, 13 Oct 2025 05:23:19 GMT
ENV GOPATH=/go
# Mon, 13 Oct 2025 05:23:19 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 13 Oct 2025 05:23:19 GMT
COPY /target/ / # buildkit
# Mon, 13 Oct 2025 05:23:19 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 13 Oct 2025 05:23:19 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:c2fe130f4aabc917e559e7eed7d37b0e21ba13b44520101696887ca892e8c63f`  
		Last Modified: Wed, 08 Oct 2025 16:24:46 GMT  
		Size: 4.0 MB (3992353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4d02428876f4df5a7821daa617e79a86b120df69936caaee83c7203fff2b9a9`  
		Last Modified: Mon, 13 Oct 2025 18:27:23 GMT  
		Size: 294.0 KB (294040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:998ad87b7b196d7850da55968ab4ea8d2e74337f796a2dda3e1e502c848906a7`  
		Last Modified: Mon, 13 Oct 2025 18:26:56 GMT  
		Size: 86.0 MB (86042092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0efd6fc2eae8daaf1a57daee760b110c7dd93659116eba7d4b92782ebd739a65`  
		Last Modified: Mon, 13 Oct 2025 18:27:22 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.21` - unknown; unknown

```console
$ docker pull golang@sha256:44eef1b60bc371d2948aa2ebd81256eb81b80e958e7377ca7a1c20d5851a71a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.9 KB (218880 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb617bca5ad84a523e5d9b169218cf9fd615ad85b62bcf5fbe167c03e9bb67cc`

```dockerfile
```

-	Layers:
	-	`sha256:3838acdd02322b5993b05db9606650caa9fa596e604b6234d332cdf762b61895`  
		Last Modified: Mon, 13 Oct 2025 20:24:16 GMT  
		Size: 194.2 KB (194237 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c85e3e264ad73e72aff9dba5ede61914505f95340c5e068f291810f52791d3af`  
		Last Modified: Mon, 13 Oct 2025 20:24:17 GMT  
		Size: 24.6 KB (24643 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.21` - linux; 386

```console
$ docker pull golang@sha256:5fbc64d8d78ca800190621dea0fb5fa22c0bfe3a62175fa0923e0d4c426b6f2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.6 MB (92608544 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:911688c7100f412846f9e8673acc8c73c227184cf16be6076d8486efb8d63638`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:06:42 GMT
ADD alpine-minirootfs-3.21.5-x86.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:06:42 GMT
CMD ["/bin/sh"]
# Mon, 13 Oct 2025 05:23:19 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 13 Oct 2025 05:23:19 GMT
ENV GOTOOLCHAIN=local
# Mon, 13 Oct 2025 05:23:19 GMT
ENV GOPATH=/go
# Mon, 13 Oct 2025 05:23:19 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 13 Oct 2025 05:23:19 GMT
COPY /target/ / # buildkit
# Mon, 13 Oct 2025 05:23:19 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 13 Oct 2025 05:23:19 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:bbedd1c05bb5090fc3fc2356be88d60b2a60937565b56e91fb4be42c5c73d485`  
		Last Modified: Wed, 08 Oct 2025 16:25:36 GMT  
		Size: 3.5 MB (3464704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c15133a8af42d66b8f32565434df595bb0d6eb0a70cab8e0b005300671d34bee`  
		Last Modified: Mon, 13 Oct 2025 18:24:43 GMT  
		Size: 291.6 KB (291586 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffc457dc23d2f2501ae16881398a5b91dd66079c5042a578bb1e723668e7c145`  
		Last Modified: Mon, 13 Oct 2025 21:20:42 GMT  
		Size: 88.9 MB (88852096 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bed1ddf8ee284d766f9ae085752cbeab41374134241f60355dd61905e93f6639`  
		Last Modified: Mon, 13 Oct 2025 18:24:43 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.21` - unknown; unknown

```console
$ docker pull golang@sha256:9235b0d3c8048f471592a96754a12b14f3abfcf8e7e97a1244cca3f2182c1030
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.6 KB (218648 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0490f95e61cbcb4c6f18a2ccc4a884fd634c6cdf99e5b2cb37681453d63d458b`

```dockerfile
```

-	Layers:
	-	`sha256:076e597c82dc845f904ff2834ba1216c76ad57c87562ec5c1fe31fc6ba8bb507`  
		Last Modified: Mon, 13 Oct 2025 20:24:20 GMT  
		Size: 194.2 KB (194174 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c3debc10fe577a243a669e8d463bde7155642dd5c406f506d70d4e1d3871e018`  
		Last Modified: Mon, 13 Oct 2025 20:24:21 GMT  
		Size: 24.5 KB (24474 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.21` - linux; ppc64le

```console
$ docker pull golang@sha256:5fd54bed1fe1e05d73a8a417f5f1528653dd1c80a73c3e4e1756bfb88eadc723
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.3 MB (91310641 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11628b99e1025373c7ed36557d28beb2b93556e3d027bd8a4dad373589a4ffa0`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:06:42 GMT
ADD alpine-minirootfs-3.21.5-ppc64le.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:06:42 GMT
CMD ["/bin/sh"]
# Mon, 13 Oct 2025 05:23:19 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 13 Oct 2025 05:23:19 GMT
ENV GOTOOLCHAIN=local
# Mon, 13 Oct 2025 05:23:19 GMT
ENV GOPATH=/go
# Mon, 13 Oct 2025 05:23:19 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 13 Oct 2025 05:23:19 GMT
COPY /target/ / # buildkit
# Mon, 13 Oct 2025 05:23:19 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 13 Oct 2025 05:23:19 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:e99908f6ead74bb809123fe0d40505509ed6113949496be71629433c6ea3fa1a`  
		Last Modified: Wed, 08 Oct 2025 16:25:03 GMT  
		Size: 3.6 MB (3574075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f73de5935c27bbf53bedf5cf444a1a2d137f0c9fa6be0ac31ba3a0af17a0953`  
		Last Modified: Thu, 09 Oct 2025 03:31:32 GMT  
		Size: 294.5 KB (294519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7fb280635ff73067e450776ffb495ea1ad6245c60020ec72c47db59cab52504`  
		Last Modified: Mon, 13 Oct 2025 18:24:19 GMT  
		Size: 87.4 MB (87441889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1da7f2ed71f20b3640caece799dcbc5bed18b450fa134d2b2710d74b463e3009`  
		Last Modified: Mon, 13 Oct 2025 18:36:24 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.21` - unknown; unknown

```console
$ docker pull golang@sha256:8e39e45920a3baa4367b76d353646b4a1b6b1a9f729fa148a12e4d5d5b7b51dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **216.8 KB (216845 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c43f7eb7577578b719c809c1ca30a51c65b4b8cbb4bc51eacae7fb4e6cdcf668`

```dockerfile
```

-	Layers:
	-	`sha256:b8d1dd3a66e9be6363b55d47eae1da22702e8ac5ae5c96b3e3905d99770283e1`  
		Last Modified: Mon, 13 Oct 2025 20:24:24 GMT  
		Size: 192.3 KB (192292 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:872832e584cb23b7382706f47afb394447710ad9e0e05885cb806dac26126fcf`  
		Last Modified: Mon, 13 Oct 2025 20:24:25 GMT  
		Size: 24.6 KB (24553 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.21` - linux; riscv64

```console
$ docker pull golang@sha256:b44d49674fa37f88377bb5508f3f74ca497108ba2a6e10c07932bf4feb957531
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.9 MB (85876509 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a407f4cd8a0807e138e2e4ac41dc0421c67a543a0993ca2bd7918f852c9e2a5`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Mon, 06 Oct 2025 05:23:19 GMT
ADD alpine-minirootfs-3.21.5-riscv64.tar.gz / # buildkit
# Mon, 06 Oct 2025 05:23:19 GMT
CMD ["/bin/sh"]
# Mon, 06 Oct 2025 05:23:19 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 06 Oct 2025 05:23:19 GMT
ENV GOTOOLCHAIN=local
# Mon, 06 Oct 2025 05:23:19 GMT
ENV GOPATH=/go
# Mon, 06 Oct 2025 05:23:19 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 06 Oct 2025 05:23:19 GMT
COPY /target/ / # buildkit
# Mon, 06 Oct 2025 05:23:19 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 06 Oct 2025 05:23:19 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:f874295bfcd01a87ee99265d45f0786d35242cd9d53bc2744cb330bf3be277f5`  
		Last Modified: Wed, 08 Oct 2025 21:19:05 GMT  
		Size: 3.4 MB (3351001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:611661040751365eafd7f1dfe7a29755674f06b893fdaa0640152a38b160d0dc`  
		Last Modified: Fri, 10 Oct 2025 21:10:14 GMT  
		Size: 291.5 KB (291463 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58fd0ce2ab28438bdf94f05f192ab71a6b801a6c5d6e3d4dc6d664c820e75f2c`  
		Last Modified: Tue, 07 Oct 2025 14:09:36 GMT  
		Size: 82.2 MB (82233887 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:479787beda8a6ceded542985b639242a0e8833b043f77391801f3aad73c480ba`  
		Last Modified: Mon, 13 Oct 2025 09:24:11 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.21` - unknown; unknown

```console
$ docker pull golang@sha256:6dfdf633bf58963bf87ed168799ff404a9f5d806ac5b3d9bcc04d719c49af588
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **215.4 KB (215368 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f6e73c8e175c4e81932175ba064e921ed55968a37bb10702b2e0457bfb6754e`

```dockerfile
```

-	Layers:
	-	`sha256:c2963277f3e75d42dc6cf83ac9932debf5dc570bc2016bf27cbb5aa428f08471`  
		Last Modified: Mon, 13 Oct 2025 11:23:35 GMT  
		Size: 190.8 KB (190814 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e2e62e718dcca99237fc7eadf164d17f69b368b416a125fb392b018a8431182d`  
		Last Modified: Mon, 13 Oct 2025 11:23:36 GMT  
		Size: 24.6 KB (24554 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.21` - linux; s390x

```console
$ docker pull golang@sha256:593980f8c0cf8e25c8eb77090fbd1beab960f49552337a0264066be35a51fb1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.6 MB (92550883 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:154cd86d759fc4ab0191811889423a59c71e2f16f9f189eb94f7804eb6008c1e`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:06:42 GMT
ADD alpine-minirootfs-3.21.5-s390x.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:06:42 GMT
CMD ["/bin/sh"]
# Mon, 13 Oct 2025 05:23:19 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 13 Oct 2025 05:23:19 GMT
ENV GOTOOLCHAIN=local
# Mon, 13 Oct 2025 05:23:19 GMT
ENV GOPATH=/go
# Mon, 13 Oct 2025 05:23:19 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 13 Oct 2025 05:23:19 GMT
COPY /target/ / # buildkit
# Mon, 13 Oct 2025 05:23:19 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 13 Oct 2025 05:23:19 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:9f2ceebb28b6c8480d6ae26501eda06bf0b6029f7c797c80673b95a60276e050`  
		Last Modified: Wed, 08 Oct 2025 16:25:19 GMT  
		Size: 3.5 MB (3466434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3cc4c05838d57ecfe671b31e7400d015d24d81c7ce717be366103b575ebe388`  
		Last Modified: Thu, 09 Oct 2025 07:53:30 GMT  
		Size: 292.1 KB (292099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9327917e2dddfe4111d470e54a510bc92320cf661a5e14b0ac90c62acacad6e`  
		Last Modified: Mon, 13 Oct 2025 18:22:35 GMT  
		Size: 88.8 MB (88792191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0084a4776fd0501b025a217db6c3d016626527946dcd9f9d3ed25b8e77f7cf17`  
		Last Modified: Mon, 13 Oct 2025 18:28:37 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.21` - unknown; unknown

```console
$ docker pull golang@sha256:8dd4d48f030c9221fde6b78b29e267b935d705f4f770dd5e42599a90daaed732
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **216.8 KB (216762 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48e31ee92dbacbbc4175a43d469c3eb06d9ac8e987520ae4f32bf4f685dfe0fd`

```dockerfile
```

-	Layers:
	-	`sha256:f3e92ef87ba623452f2a9ec1b3083b74f6312b75f414440981235b37c0ba7ee7`  
		Last Modified: Mon, 13 Oct 2025 20:24:29 GMT  
		Size: 192.3 KB (192254 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c4ab680574759671d8c1516b66f5486415f27cc07f5f2f121af2d1dc353124a6`  
		Last Modified: Mon, 13 Oct 2025 20:24:30 GMT  
		Size: 24.5 KB (24508 bytes)  
		MIME: application/vnd.in-toto+json
