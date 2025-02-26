## `golang:tip-alpine3.21`

```console
$ docker pull golang@sha256:402ddc10c3fb0bda011be81279f3b1622b6db973fb3db841e24166c42cb78ba3
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
$ docker pull golang@sha256:df2e3581b1a37f4b0a36d1e1d1dc2b970133c7cfeb04c1c2301b7a9f0fc43c81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.7 MB (133681162 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef9b8ececed57db9ffec258346551a17f20ec6c2d50813f1d0d7751100f982c7`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 25 Feb 2025 00:23:21 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 25 Feb 2025 00:23:21 GMT
ENV GOTOOLCHAIN=local
# Tue, 25 Feb 2025 00:23:21 GMT
ENV GOPATH=/go
# Tue, 25 Feb 2025 00:23:21 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 25 Feb 2025 00:23:21 GMT
COPY /target/ / # buildkit
# Tue, 25 Feb 2025 00:23:21 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 25 Feb 2025 00:23:21 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 12:05:35 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a456f40cc3db39c7a85d4b2eb0d9f35fcd2de2caf2657c5573a6294cbbdc60b`  
		Last Modified: Tue, 25 Feb 2025 23:30:39 GMT  
		Size: 294.9 KB (294906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4a93651a1e507b5bd3cfde19fbfc91acf223de81d90d9e07fc812851aad09e7`  
		Last Modified: Tue, 25 Feb 2025 23:30:29 GMT  
		Size: 129.7 MB (129743852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e21ac708b687a75ec5256a21ebaa32f8a9c434450c4c36281d13158d44856834`  
		Last Modified: Tue, 25 Feb 2025 23:30:39 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.21` - unknown; unknown

```console
$ docker pull golang@sha256:e4d20bfd6c7a2e3b250b682fc19a9e9dd1ea8db8187473bf66aede99435885c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.9 KB (236852 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f1b520ac66c2b2ea8f71d38b29be54546e7111eef7f2d48ef1e536e29ded033`

```dockerfile
```

-	Layers:
	-	`sha256:8702e772d74e5523d2da30aabe4d4fc213edc4831d58489d959667675e76abfd`  
		Last Modified: Tue, 25 Feb 2025 23:30:39 GMT  
		Size: 211.7 KB (211711 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dda4e89e0581eda10e8fe23f76a51eaada6ed93b76fd7d8e281b849c71d4a634`  
		Last Modified: Tue, 25 Feb 2025 23:30:39 GMT  
		Size: 25.1 KB (25141 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.21` - linux; arm variant v6

```console
$ docker pull golang@sha256:27f6e6a9ad3a567631e4ad210fd8fc59a3879a8e89a0aec57b305709bc9870d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.0 MB (127023027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a66adebf0298bd88e283ae63b5eef172747e34e5573fc10293401646c48e2e1`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armhf.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 25 Feb 2025 00:23:21 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 25 Feb 2025 00:23:21 GMT
ENV GOTOOLCHAIN=local
# Tue, 25 Feb 2025 00:23:21 GMT
ENV GOPATH=/go
# Tue, 25 Feb 2025 00:23:21 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 25 Feb 2025 00:23:21 GMT
COPY /target/ / # buildkit
# Tue, 25 Feb 2025 00:23:21 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 25 Feb 2025 00:23:21 GMT
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
	-	`sha256:8c10d33f52a0d639e250df7f8e253e1910c94bdaf30d4e34b190895d9f138d27`  
		Last Modified: Tue, 25 Feb 2025 23:31:13 GMT  
		Size: 123.4 MB (123361886 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0112713dd1b34547ad95bcb119226039d815b2c9e7f02d430b3803dbae8b20b`  
		Last Modified: Tue, 25 Feb 2025 23:31:09 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.21` - unknown; unknown

```console
$ docker pull golang@sha256:b3013ec0ebd97494277a2243e52d84d43e4645ed8643d81e489c702e8b44b63c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.1 KB (25051 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:555411e66300a44d4fa70e3a31b3d9925a9a122a915a7df7e52e7b635b216077`

```dockerfile
```

-	Layers:
	-	`sha256:83d338864374fa1f0bb2ff0edeeb9db14d89dff0ae1706e1b983e8dfb6410b46`  
		Last Modified: Tue, 25 Feb 2025 23:31:09 GMT  
		Size: 25.1 KB (25051 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.21` - linux; arm variant v7

```console
$ docker pull golang@sha256:d88f3e8b858d4f7ca57becfd451ed0669a884cb50deee84c0e4c908367ba58ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.4 MB (126428452 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1d85672974a6ba6e9afcd111e8f61a832b886368404d5d3ca284ac32c360855`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armv7.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 25 Feb 2025 00:23:21 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 25 Feb 2025 00:23:21 GMT
ENV GOTOOLCHAIN=local
# Tue, 25 Feb 2025 00:23:21 GMT
ENV GOPATH=/go
# Tue, 25 Feb 2025 00:23:21 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 25 Feb 2025 00:23:21 GMT
COPY /target/ / # buildkit
# Tue, 25 Feb 2025 00:23:21 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 25 Feb 2025 00:23:21 GMT
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
	-	`sha256:cbe77fa27af7b36c34f8f11e6bd2bd4b9ddf9e28c094fdee1cc3b2735243e847`  
		Last Modified: Wed, 26 Feb 2025 02:56:52 GMT  
		Size: 123.0 MB (123034972 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c92484191e5ab354d694462b6b50c640d1e6edb262ffffe14b263241dc1b5e1c`  
		Last Modified: Wed, 26 Feb 2025 04:30:30 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.21` - unknown; unknown

```console
$ docker pull golang@sha256:605aba4e937d4fa69a2d026bb7ae1def8686e416943afe20b5fd4de0d210eb00
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **237.0 KB (236973 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f337b317dc5ebf46d39866fb6a14caf29d0f41242ec124d66a2eacbf8d5dfe14`

```dockerfile
```

-	Layers:
	-	`sha256:04a4ba709ea00b1c162a2719ee5c9ebf8f90af3c6ed4e42338b543a72733ad0e`  
		Last Modified: Wed, 26 Feb 2025 04:30:31 GMT  
		Size: 211.7 KB (211707 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e47c0b47f988e23c8f5758e6d820c0c472f22e930a9ec64e6ebfaf18618a0947`  
		Last Modified: Wed, 26 Feb 2025 04:30:31 GMT  
		Size: 25.3 KB (25266 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.21` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:a695341ba3d00c801889ed14d2ff4994aa7aa16249cec2d914183a06c92c40fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.9 MB (126855798 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb931736a8662ca96f588e145e850d37391a927354b6b3e05ef87137eacf4eab`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 25 Feb 2025 00:23:21 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 25 Feb 2025 00:23:21 GMT
ENV GOTOOLCHAIN=local
# Tue, 25 Feb 2025 00:23:21 GMT
ENV GOPATH=/go
# Tue, 25 Feb 2025 00:23:21 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 25 Feb 2025 00:23:21 GMT
COPY /target/ / # buildkit
# Tue, 25 Feb 2025 00:23:21 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 25 Feb 2025 00:23:21 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 12:05:33 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14aa1d43e92f86dc074668d0ee29a76fd40e91e4c4142a8f0580170417c1a1e6`  
		Last Modified: Fri, 14 Feb 2025 22:23:05 GMT  
		Size: 297.8 KB (297842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37e46df0fcf6e0e573af560112ea65411de1e4c09446bfe2aa5c396181b055ef`  
		Last Modified: Tue, 25 Feb 2025 23:43:25 GMT  
		Size: 122.6 MB (122564769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bd8317a399bf371b684be0cee8df2308161e975cbf5a4ab907e4c8bdd1060e4`  
		Last Modified: Tue, 25 Feb 2025 23:47:27 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.21` - unknown; unknown

```console
$ docker pull golang@sha256:fe7e58c52cf7b590ebdf714738389b18d34f0128c1c7673f344b5687aeec2f4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **237.1 KB (237069 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3742d60cc2efa1ff6ac05ed01f947019551e6740568d1df4d026a530c6c41f61`

```dockerfile
```

-	Layers:
	-	`sha256:a9de522a6ac5f3891bc64e536602e9e26e0a1d11e6746037019bf3988f95d573`  
		Last Modified: Tue, 25 Feb 2025 23:47:27 GMT  
		Size: 211.8 KB (211767 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8d97622bf22c56ab4f3ecc4c8257128c10125c624734bb15cd00192c31e1b0f5`  
		Last Modified: Tue, 25 Feb 2025 23:47:27 GMT  
		Size: 25.3 KB (25302 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.21` - linux; 386

```console
$ docker pull golang@sha256:7f14d64c15b1dbb5ec29fe0030be2331bfe50786b0a19f6d17a45b0b40315c1a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.2 MB (130162161 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05bd0ff1f1448ece9fe3c1af7a415d0866b8577a887bb4a095fbaf5a640705aa`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 25 Feb 2025 00:23:21 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 25 Feb 2025 00:23:21 GMT
ENV GOTOOLCHAIN=local
# Tue, 25 Feb 2025 00:23:21 GMT
ENV GOPATH=/go
# Tue, 25 Feb 2025 00:23:21 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 25 Feb 2025 00:23:21 GMT
COPY /target/ / # buildkit
# Tue, 25 Feb 2025 00:23:21 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 25 Feb 2025 00:23:21 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:69aa61ccf55e5bf8e7a069b89e8afb42b4f3443b3785868795af8046d810d608`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.5 MB (3463623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d5d1bc61dea5af3fbaa7030196474ba363be1de727b216fd99dcca8a913f00a`  
		Last Modified: Tue, 25 Feb 2025 23:30:59 GMT  
		Size: 295.6 KB (295588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8ea1fd7113951d2f0ff9a9824c4749a117ae67be28d96b0ab33e27305a83954`  
		Last Modified: Tue, 25 Feb 2025 23:31:02 GMT  
		Size: 126.4 MB (126402793 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:394b4a6a28e3c9e8a03e765d143aaef564c12d701bae6cca06a993ce3d4c87b2`  
		Last Modified: Tue, 25 Feb 2025 23:30:59 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.21` - unknown; unknown

```console
$ docker pull golang@sha256:023a8074c34938aca1607aca712c49e3aedcf7e9390af1dfaf3dea173461d982
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.7 KB (236745 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbdbd0b214a5d604b4d1a1c8d3193dffd5c8f00c96171e9981c7f3be05239fb8`

```dockerfile
```

-	Layers:
	-	`sha256:d802cbb12c46db181be88afcc9b6b00b608441de7f7b19fe93c93f043929d892`  
		Last Modified: Tue, 25 Feb 2025 23:30:59 GMT  
		Size: 211.6 KB (211646 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c7edd54488dbbdc75272ca942efe5b2943b4c7b92d771761a4ebfa2406e14c73`  
		Last Modified: Tue, 25 Feb 2025 23:30:59 GMT  
		Size: 25.1 KB (25099 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.21` - linux; ppc64le

```console
$ docker pull golang@sha256:5994285ade31f9e9ec49fcd541f58d22ef124e8ae910f8a7df1afb2ea89a10d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.8 MB (128824639 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cfaf3bfd96ffba9d70c86bdea89a9e99d4cab19a926a79b24b36460e3f161117`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-ppc64le.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 25 Feb 2025 00:23:21 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 25 Feb 2025 00:23:21 GMT
ENV GOTOOLCHAIN=local
# Tue, 25 Feb 2025 00:23:21 GMT
ENV GOPATH=/go
# Tue, 25 Feb 2025 00:23:21 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 25 Feb 2025 00:23:21 GMT
COPY /target/ / # buildkit
# Tue, 25 Feb 2025 00:23:21 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 25 Feb 2025 00:23:21 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:184b14480d317057da092a0994ad6baf4b2df588108f43969f8fd56f021af2c6`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.6 MB (3574345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:542036b0f90df8875e93add192346f3bcc8edd586aa34c11a6af80938cb06173`  
		Last Modified: Fri, 14 Feb 2025 21:50:57 GMT  
		Size: 298.3 KB (298267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e0d28a5af7632832dbf0a9896248be932971aba4af06c89b659315ee4a42081`  
		Last Modified: Tue, 25 Feb 2025 23:32:05 GMT  
		Size: 125.0 MB (124951869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58161ad9b71b3eb377d5de90c0e5f230a7601996b72f827b17125ea23725d48e`  
		Last Modified: Tue, 25 Feb 2025 23:35:23 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.21` - unknown; unknown

```console
$ docker pull golang@sha256:032a12e1ebc8c2f2724e422c2bc618d7ff53ada50f147fe1b59194c9c4db7a43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.0 KB (235034 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b268a00556cb7f1ce445d74e372c87ead4c395a5634336f991d39ff8f536fb4`

```dockerfile
```

-	Layers:
	-	`sha256:d9790e1857be1ce69260844d712331d80ea944910c8382a31f191f1b4bedd0ce`  
		Last Modified: Tue, 25 Feb 2025 23:35:23 GMT  
		Size: 209.8 KB (209834 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:de9189d1aa35397fec430309092597af3e22eb42e3bf84ed3531058d0bd0946c`  
		Last Modified: Tue, 25 Feb 2025 23:35:23 GMT  
		Size: 25.2 KB (25200 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.21` - linux; riscv64

```console
$ docker pull golang@sha256:180faf27d9d69513c47932bcee165ef63513694562ef9745d471bddb1469ea1b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.0 MB (128985602 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c52c2169333897e4af1fb2d257881f49f7deaf969c6f41a2ed7eb7ce788b8f35`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-riscv64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 25 Feb 2025 00:23:21 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 25 Feb 2025 00:23:21 GMT
ENV GOTOOLCHAIN=local
# Tue, 25 Feb 2025 00:23:21 GMT
ENV GOPATH=/go
# Tue, 25 Feb 2025 00:23:21 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 25 Feb 2025 00:23:21 GMT
COPY /target/ / # buildkit
# Tue, 25 Feb 2025 00:23:21 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 25 Feb 2025 00:23:21 GMT
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
	-	`sha256:0cd9ffc10fd27eaf00487a985d3d6937522e17c7cdf03f77def367bc29eb78e7`  
		Last Modified: Wed, 26 Feb 2025 00:21:32 GMT  
		Size: 125.3 MB (125338659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bb5f95a560154d26b735eab8b8287e7432a1efe56c37a0b00f225d27eee956e`  
		Last Modified: Wed, 26 Feb 2025 00:21:15 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.21` - unknown; unknown

```console
$ docker pull golang@sha256:e76374dbd2fd9fe7a8f36c776f18ac69f89cbf7bc3105a145bea89fbc55b5458
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.0 KB (235030 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0bf3664d4265969d26640ee7c445ac44ff3cf15cb66481c1f457d5cdfbed4a7f`

```dockerfile
```

-	Layers:
	-	`sha256:fc5d11f3ea4cf959e7467e2c990561500d354e47850ae4ee69d8ba522d58e041`  
		Last Modified: Wed, 26 Feb 2025 00:21:15 GMT  
		Size: 209.8 KB (209830 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ad5f8e80427c2559c8b97e1e3cbc62db15ead3fe7f8690a58a8295a2eeafa925`  
		Last Modified: Wed, 26 Feb 2025 00:21:15 GMT  
		Size: 25.2 KB (25200 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.21` - linux; s390x

```console
$ docker pull golang@sha256:b727bbc8d749cd56f284af88eba4d53628c2e48e8ef5984df5b1c90da443647d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.1 MB (131098645 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:293fb99612f4d3efe7564ced035fb2cc593431884128832fcccb4c7388f3e677`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-s390x.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 25 Feb 2025 00:23:21 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 25 Feb 2025 00:23:21 GMT
ENV GOTOOLCHAIN=local
# Tue, 25 Feb 2025 00:23:21 GMT
ENV GOPATH=/go
# Tue, 25 Feb 2025 00:23:21 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 25 Feb 2025 00:23:21 GMT
COPY /target/ / # buildkit
# Tue, 25 Feb 2025 00:23:21 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 25 Feb 2025 00:23:21 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:c1a599607158512214777614f916f8193d29fd34b656d47dfc26314af01e2af4`  
		Last Modified: Fri, 14 Feb 2025 12:05:25 GMT  
		Size: 3.5 MB (3467567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45367ec7901486a744e83b8e8c40908894d960175ae2dea51903497a09542717`  
		Last Modified: Fri, 14 Feb 2025 22:24:43 GMT  
		Size: 296.2 KB (296178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a0708d6fc70d6c17d917a582922c9c9c869293636d289db2a690696469b90d8`  
		Last Modified: Tue, 25 Feb 2025 23:31:35 GMT  
		Size: 127.3 MB (127334743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56ccbc0d1afb54c1ad9f93ad0dcaafee7088072a86b2d7c4d2d4d21f24fae912`  
		Last Modified: Tue, 25 Feb 2025 23:34:35 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.21` - unknown; unknown

```console
$ docker pull golang@sha256:29674831d3448bc489d7fe6f01c897fb6d16546458cb7e1ab2b48e642e1380e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.9 KB (234902 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79d84449f21af6e93f7703f6dc6626a811e7c34edbbe826feb77fd0ed43fe4dd`

```dockerfile
```

-	Layers:
	-	`sha256:80c1ec42e6989e6e2735f5fd8663475fd8214791649dadbe2832930b25673f2b`  
		Last Modified: Tue, 25 Feb 2025 23:34:35 GMT  
		Size: 209.8 KB (209760 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:313c205043e458f9141138ce5fbe0f869cd7d08b4495b7947067895db7cf883f`  
		Last Modified: Tue, 25 Feb 2025 23:34:35 GMT  
		Size: 25.1 KB (25142 bytes)  
		MIME: application/vnd.in-toto+json
