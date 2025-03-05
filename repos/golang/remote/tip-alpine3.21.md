## `golang:tip-alpine3.21`

```console
$ docker pull golang@sha256:c3c72c53c324f5c4b48b3918bf98351b0003216710717233d5a7aae539441e48
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
$ docker pull golang@sha256:971bcb8ac959e55af293ed7c4f33877b195bc12476150cfe77ba8650a5bfe079
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.8 MB (133776080 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:845bd9be20e23292e10106f9c988cffe2c184a740dd3f5543531e2249965ef3d`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Mon, 03 Mar 2025 00:23:21 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 03 Mar 2025 00:23:21 GMT
ENV GOTOOLCHAIN=local
# Mon, 03 Mar 2025 00:23:21 GMT
ENV GOPATH=/go
# Mon, 03 Mar 2025 00:23:21 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 03 Mar 2025 00:23:21 GMT
COPY /target/ / # buildkit
# Mon, 03 Mar 2025 00:23:21 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 03 Mar 2025 00:23:21 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 12:05:35 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e36efd1b5103f32cd1c19de62d10844db8b4c3326bfd429655c391d5494e174`  
		Last Modified: Tue, 04 Mar 2025 21:59:39 GMT  
		Size: 294.9 KB (294902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b704ebeab23a12c1391628665925189d800995f90d6bab09fc653f615d683c07`  
		Last Modified: Tue, 04 Mar 2025 00:32:19 GMT  
		Size: 129.8 MB (129838774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:405d920dd57e2283be92339b1cb673e56db05bb14aa6a326a99c1b2eeb40c9bd`  
		Last Modified: Tue, 04 Mar 2025 21:59:39 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.21` - unknown; unknown

```console
$ docker pull golang@sha256:ad1ac0712b0bbc668195d988669d8d13e8ce45e18a00e2bb2c841f5bff24480e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.9 KB (236852 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6243757c3476b311d1a36792e1da905961a1d657b93d2e376ec397d7bfd82ec`

```dockerfile
```

-	Layers:
	-	`sha256:7c4b8de544457458ea600fcf1e44788a6f6614e8c1b035d74af8ecef7c2813de`  
		Last Modified: Tue, 04 Mar 2025 21:59:39 GMT  
		Size: 211.7 KB (211711 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:610aa7dd851d58d118b9fbbc74ee399ccc354288430a18fa5d4050ee90963a08`  
		Last Modified: Tue, 04 Mar 2025 21:59:39 GMT  
		Size: 25.1 KB (25141 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.21` - linux; arm variant v6

```console
$ docker pull golang@sha256:ddacb7c52b4938755f7442e15825b9c4d5d95d2028155a446abfeb09a3ff9d51
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.1 MB (127088104 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51c0724acd83a3ffd24b52efa92d941b31eba3c3024d2e41d7a0abd14864f1b5`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armhf.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Mon, 03 Mar 2025 00:23:21 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 03 Mar 2025 00:23:21 GMT
ENV GOTOOLCHAIN=local
# Mon, 03 Mar 2025 00:23:21 GMT
ENV GOPATH=/go
# Mon, 03 Mar 2025 00:23:21 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 03 Mar 2025 00:23:21 GMT
COPY /target/ / # buildkit
# Mon, 03 Mar 2025 00:23:21 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 03 Mar 2025 00:23:21 GMT
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
	-	`sha256:908353bf334c8298bf4221ed4995e78c699ff58f6af7b91fa91bb0e60c060533`  
		Last Modified: Tue, 04 Mar 2025 00:32:51 GMT  
		Size: 123.4 MB (123426962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9789bd79a8a44315da3ea2deb4fb152663b3fa99a2a9dd3c5fbb9a0cc6b7d50`  
		Last Modified: Tue, 04 Mar 2025 00:32:48 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.21` - unknown; unknown

```console
$ docker pull golang@sha256:0149965e535077e0069f02f5bc3fa0f5d3c0a23aaae45ee751244444c2843ce5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.1 KB (25051 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4fa38664129e6d6177cc53098372081ae94c1c951c1a4552ce243035bb00eec5`

```dockerfile
```

-	Layers:
	-	`sha256:dde804e6c8ab3638933a48c55a24b213cef80e8aaf50278ce621fe86bd2a0baf`  
		Last Modified: Tue, 04 Mar 2025 21:57:27 GMT  
		Size: 25.1 KB (25051 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.21` - linux; arm variant v7

```console
$ docker pull golang@sha256:6064f23cb816cbe5c3596084dfd90e8501294fa7b5c196f94ec054a94a2f9375
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.5 MB (126481028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a22c398e01f3de662a56279af12fe2d298075c5121c338cfd3a5889cf2266fc`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armv7.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Mon, 03 Mar 2025 00:23:21 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 03 Mar 2025 00:23:21 GMT
ENV GOTOOLCHAIN=local
# Mon, 03 Mar 2025 00:23:21 GMT
ENV GOPATH=/go
# Mon, 03 Mar 2025 00:23:21 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 03 Mar 2025 00:23:21 GMT
COPY /target/ / # buildkit
# Mon, 03 Mar 2025 00:23:21 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 03 Mar 2025 00:23:21 GMT
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
	-	`sha256:c66a4732c96edfeab450050a70f02b158342482c6f2a5dcf7aeba30aac7fcc17`  
		Last Modified: Tue, 04 Mar 2025 00:33:46 GMT  
		Size: 123.1 MB (123087551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25fc9b219f7aaa3bb21c2bb52a936877902bf0cb2b32e7740ae12a4c1cc30ae8`  
		Last Modified: Tue, 04 Mar 2025 00:40:46 GMT  
		Size: 123.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.21` - unknown; unknown

```console
$ docker pull golang@sha256:84e0e9ae43f90d4c2e3a611183344537815a44dda0e1190a2eadac64447fd818
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **237.0 KB (236973 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:849c99364c5f1828524c6849f61bfbcaf3742434245cd789f989ba8a0c26d835`

```dockerfile
```

-	Layers:
	-	`sha256:a3a1ef72e5ced296d1b8e1325b3c28fd98e9d6d67490cc2736cea5f7ef2b97c7`  
		Last Modified: Tue, 04 Mar 2025 22:18:25 GMT  
		Size: 211.7 KB (211707 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ae383ba35f1e328e65638431a9d31e24ecb2e6c1a8fa795c4a73f91939937f8c`  
		Last Modified: Tue, 04 Mar 2025 22:18:24 GMT  
		Size: 25.3 KB (25266 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.21` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:595d546c1ee192c2ef135a3a04fba894dd8b91a4f51c0bb18a34ca7c9c0d2e60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.9 MB (126911613 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a289c18988bc99e35791e2cfd91341d80d22803e75bd1306ef9197a5d4539af`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Mon, 03 Mar 2025 00:23:21 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 03 Mar 2025 00:23:21 GMT
ENV GOTOOLCHAIN=local
# Mon, 03 Mar 2025 00:23:21 GMT
ENV GOPATH=/go
# Mon, 03 Mar 2025 00:23:21 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 03 Mar 2025 00:23:21 GMT
COPY /target/ / # buildkit
# Mon, 03 Mar 2025 00:23:21 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 03 Mar 2025 00:23:21 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 12:05:33 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:037a2359180f5e29bb26ba5ebe6478f9c3cc6fe1fcd38d94f7289b2ab44088bb`  
		Last Modified: Tue, 04 Mar 2025 00:44:39 GMT  
		Size: 297.9 KB (297859 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2fb2f15af0e54e78387b98706e083a5882e5cd46c9ae24a07d9c9a7de13391d`  
		Last Modified: Tue, 04 Mar 2025 00:39:29 GMT  
		Size: 122.6 MB (122620567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ea6a21e259b39626065fd09d4bded2c225a52840b5f4884c29d35260c19aa11`  
		Last Modified: Tue, 04 Mar 2025 00:44:38 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.21` - unknown; unknown

```console
$ docker pull golang@sha256:4fc9c05659ce38ee780eb6903f6e5707eef7a240c753a654b3b61f38b6d0008d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **237.1 KB (237069 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff7d3f0b27e62b3b2a60adb61a18c289acdb39f2b98b9c94dd9b31698398c7e3`

```dockerfile
```

-	Layers:
	-	`sha256:388ba2663f039374e638f713c9ba6f43741d3a4cd10b212de96d992f42d859c9`  
		Last Modified: Tue, 04 Mar 2025 22:22:34 GMT  
		Size: 211.8 KB (211767 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4675bb3ca6d2cd659abfff3deb57611873b96cfad0ec7717ef1e800e8b5ba093`  
		Last Modified: Tue, 04 Mar 2025 22:22:34 GMT  
		Size: 25.3 KB (25302 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.21` - linux; 386

```console
$ docker pull golang@sha256:f480b9a6f1e9dd55f290223323d037c070ae88aa7cf597e92b98e07ee362ab36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.2 MB (130217598 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:144633d2aa8cdf337f29d00cf2c021b42e21e30c8a7b83220bc659582a3f833e`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Mon, 03 Mar 2025 00:23:21 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 03 Mar 2025 00:23:21 GMT
ENV GOTOOLCHAIN=local
# Mon, 03 Mar 2025 00:23:21 GMT
ENV GOPATH=/go
# Mon, 03 Mar 2025 00:23:21 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 03 Mar 2025 00:23:21 GMT
COPY /target/ / # buildkit
# Mon, 03 Mar 2025 00:23:21 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 03 Mar 2025 00:23:21 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:69aa61ccf55e5bf8e7a069b89e8afb42b4f3443b3785868795af8046d810d608`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.5 MB (3463623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56bfbf57e5908110ffb37dddd092791502a80a972e92de3ef1fb21011485367a`  
		Last Modified: Tue, 04 Mar 2025 21:59:37 GMT  
		Size: 295.6 KB (295587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc05ee2fc954345b4dc36b55c348df7ba176cd1d037dcc0fd8ba6eedfb02eea9`  
		Last Modified: Tue, 04 Mar 2025 00:32:40 GMT  
		Size: 126.5 MB (126458230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d143596eef274a5ce2c9396ac9617a12663b4bc91102fe3673ce14f8d1d42cc2`  
		Last Modified: Tue, 04 Mar 2025 21:59:37 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.21` - unknown; unknown

```console
$ docker pull golang@sha256:001ec8bd2d6c372861b83036035c6ba6ec1145d37e31c502abe92f35a14564b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.7 KB (236745 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3a72b2416113794c30f8a17ff9433be880a68603374b99c8c49909ff5f7a5fb`

```dockerfile
```

-	Layers:
	-	`sha256:4fdac6465c29fd280bac47f5416924d48473249a0295c345d4eb0fd5c890c71e`  
		Last Modified: Tue, 04 Mar 2025 21:59:37 GMT  
		Size: 211.6 KB (211646 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cb031d87b13117b20bb6c3e3ad51d5ced227328a5b0669d420723cab9344d1ce`  
		Last Modified: Tue, 04 Mar 2025 21:59:37 GMT  
		Size: 25.1 KB (25099 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.21` - linux; ppc64le

```console
$ docker pull golang@sha256:f63da2987c7bb4f20abc18ab746ed17723c945a7924356a3ccbe948a2b959b0c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.9 MB (128866862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe47e9e1fe1c6b1e8e9a19562265053837b898f4755d357247078f9610740937`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-ppc64le.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Mon, 03 Mar 2025 00:23:21 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 03 Mar 2025 00:23:21 GMT
ENV GOTOOLCHAIN=local
# Mon, 03 Mar 2025 00:23:21 GMT
ENV GOPATH=/go
# Mon, 03 Mar 2025 00:23:21 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 03 Mar 2025 00:23:21 GMT
COPY /target/ / # buildkit
# Mon, 03 Mar 2025 00:23:21 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 03 Mar 2025 00:23:21 GMT
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
	-	`sha256:de94f4e3ebdd3654e0bb93d6ee292377b5f63d04585b0ae2f0dcd851ba62d914`  
		Last Modified: Tue, 04 Mar 2025 00:33:04 GMT  
		Size: 125.0 MB (124994092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a678d28207883375c058c9288bcf0b70c2b1b7e662fa9a55b2fb63421fa15708`  
		Last Modified: Tue, 04 Mar 2025 00:46:42 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.21` - unknown; unknown

```console
$ docker pull golang@sha256:87ce494d8614a9c9f7eda351a3e7e2f9d956bf76e21cd14721ce0fbaabcd8a1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.0 KB (235034 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c223a92ba07746996280ff0e618314a4f9fc319bbff5c34b28563975d3167fa`

```dockerfile
```

-	Layers:
	-	`sha256:5655f1a1f75718b5371631fc79d0b6f61878c0c36bb1980ef88a3d73241aabea`  
		Last Modified: Tue, 04 Mar 2025 22:02:01 GMT  
		Size: 209.8 KB (209834 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a47412f2510c645a6fb6d136d5d8560184fb856b7bb68e8aa40df18c21374bb4`  
		Last Modified: Tue, 04 Mar 2025 22:02:01 GMT  
		Size: 25.2 KB (25200 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.21` - linux; riscv64

```console
$ docker pull golang@sha256:2860b0ca5c564ee1d8cca4ca626159c0e3fea709821d179957309df1c2aec20b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.1 MB (129051401 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56440b7d066796505e6221cc84402380ef514c78dc15c81158a961cef7e011e0`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-riscv64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Mon, 03 Mar 2025 00:23:21 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 03 Mar 2025 00:23:21 GMT
ENV GOTOOLCHAIN=local
# Mon, 03 Mar 2025 00:23:21 GMT
ENV GOPATH=/go
# Mon, 03 Mar 2025 00:23:21 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 03 Mar 2025 00:23:21 GMT
COPY /target/ / # buildkit
# Mon, 03 Mar 2025 00:23:21 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 03 Mar 2025 00:23:21 GMT
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
	-	`sha256:6c633f7fa993ac4c1efa563a24885fa8695e4a2df8b8a5fd4fd881545bdcea50`  
		Last Modified: Tue, 04 Mar 2025 01:10:32 GMT  
		Size: 125.4 MB (125404458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:affc3b97254978143db5289bd57e618dcde12ef46ed59f6580ce6c3f0ab37348`  
		Last Modified: Tue, 04 Mar 2025 01:10:14 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.21` - unknown; unknown

```console
$ docker pull golang@sha256:0527dce41a72fade62a46dca9f8c31b864c4a6b6c5041b7a5da71df8fa1718a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.0 KB (235029 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26dda1ffcb66f547cffc021bae1d7eceed5c9488b2d6196512555ec68ea0db87`

```dockerfile
```

-	Layers:
	-	`sha256:13f68545798ef0ec8ef46bec6d8680880b7b7d2a97fb0ed80b77a34d5b4ffeab`  
		Last Modified: Tue, 04 Mar 2025 22:34:40 GMT  
		Size: 209.8 KB (209830 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1599e6ef646ff971baa0fc9bb18b4ed9c76d7d63d858ce1967703efbca8a95c1`  
		Last Modified: Tue, 04 Mar 2025 22:34:40 GMT  
		Size: 25.2 KB (25199 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.21` - linux; s390x

```console
$ docker pull golang@sha256:4c8928d9017e8e476746c114db161859ef8cf78fa87d4a1db41b81cf1c63ed75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.1 MB (131120932 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79c4f1ae953837956061816661b42860b0a3a5410da692bcf4e4ecc6f1c1b59c`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-s390x.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Mon, 03 Mar 2025 00:23:21 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 03 Mar 2025 00:23:21 GMT
ENV GOTOOLCHAIN=local
# Mon, 03 Mar 2025 00:23:21 GMT
ENV GOPATH=/go
# Mon, 03 Mar 2025 00:23:21 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 03 Mar 2025 00:23:21 GMT
COPY /target/ / # buildkit
# Mon, 03 Mar 2025 00:23:21 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 03 Mar 2025 00:23:21 GMT
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
	-	`sha256:1a90f174e12bc58df6074c85a9d3459219dd43fe7d642ba33065f9e29227fef9`  
		Last Modified: Tue, 04 Mar 2025 00:32:29 GMT  
		Size: 127.4 MB (127357030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eae6538755f1e4663396a17bca440b577b1ff9c8c2e091616575c4e0787bfff8`  
		Last Modified: Tue, 04 Mar 2025 00:35:22 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.21` - unknown; unknown

```console
$ docker pull golang@sha256:df391c0ddc6e5a1818af524c5c411866e5cf4737472549fd12885291b6ccdbf2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.9 KB (234902 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:029052ab67480b90898a479956303f2576a02c0ffb9a3fd30966cdfb453571cf`

```dockerfile
```

-	Layers:
	-	`sha256:b7de76fbaf2e4a604c3b29d03024d0025fd9b4913160bcdce47cd1a0b7bda500`  
		Last Modified: Tue, 04 Mar 2025 22:00:01 GMT  
		Size: 209.8 KB (209760 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6b74c021497b4b5cd90fc7e2b72e14d768f7133e5de662e9330efbd0ac496a90`  
		Last Modified: Tue, 04 Mar 2025 22:00:01 GMT  
		Size: 25.1 KB (25142 bytes)  
		MIME: application/vnd.in-toto+json
