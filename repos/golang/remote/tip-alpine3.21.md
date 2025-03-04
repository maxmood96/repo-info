## `golang:tip-alpine3.21`

```console
$ docker pull golang@sha256:e2f00da0ff048ae85b1b650098985d5511388f5582000a45686acb599c986522
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
$ docker pull golang@sha256:d3feb5c504c03048723a76d0118713b0678f3ce4d865e7869f35dd133ce6a4c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.8 MB (133776083 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07d4334d3d68551e7e009f725a14a3f028a2f1572e500767af8387839cca6395`
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
	-	`sha256:579d1a7be3a9022f3a14514c95c48c6776a056e540ac6a727af8ecc55001dbb0`  
		Last Modified: Tue, 04 Mar 2025 00:32:16 GMT  
		Size: 294.9 KB (294905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b704ebeab23a12c1391628665925189d800995f90d6bab09fc653f615d683c07`  
		Last Modified: Tue, 04 Mar 2025 00:32:19 GMT  
		Size: 129.8 MB (129838774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a89c02bf9e05e03a30e6ff7313f40583f477f1fe0a2df698e3f5ef1bee0541b`  
		Last Modified: Tue, 04 Mar 2025 00:32:16 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.21` - unknown; unknown

```console
$ docker pull golang@sha256:02955d3a9c713158d29c1001243d2c29687fe6c3cf7ef00cc0887a4b5812f651
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.9 KB (236853 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd0b06536d8fdfa607616c815e1201e5e7e37c15237dd274c3d3dd87a0521fed`

```dockerfile
```

-	Layers:
	-	`sha256:31ed5c28b82c453095de7f01a0f74678cba0512e4ad4a3252937f1c0fcbbddcc`  
		Last Modified: Tue, 04 Mar 2025 00:32:16 GMT  
		Size: 211.7 KB (211711 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:31e593743ffc5cbb262ff5f51a874e6ea1611f4515ee205f40d24305045c91d5`  
		Last Modified: Tue, 04 Mar 2025 00:32:16 GMT  
		Size: 25.1 KB (25142 bytes)  
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
$ docker pull golang@sha256:bd6e9b0f287ff17b3d37ed30cf75dc5d27c14e302be5e459d3b0ea6aa19f6f81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.3 KB (24256 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cf33b751f52d5805da9f50b4b028bfbc34d060abe2a7aa6a4c3b3cd2c7c2811`

```dockerfile
```

-	Layers:
	-	`sha256:9e556d9b107e43dc4f29a16b82f15be0caea3a7320b78e6ce5511870e6bce7a6`  
		Last Modified: Tue, 04 Mar 2025 00:32:48 GMT  
		Size: 24.3 KB (24256 bytes)  
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
$ docker pull golang@sha256:595d6bcb3741385cc0b5d60d6e1d37b8f91bf0071f970b10fb1e5e72c914f8d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.2 KB (236178 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a835e796da6e5cfe38fd83b0272ac32c16cd48e8eb93de9eb0b6d759765f3ebd`

```dockerfile
```

-	Layers:
	-	`sha256:13e5c3cb1ba5feaa3f2a27f81d2a654d95bbe175fc62efc9b032286b961034ce`  
		Last Modified: Tue, 04 Mar 2025 00:40:46 GMT  
		Size: 211.7 KB (211707 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2f4e1ba0ed6d678248eabc7c6e0bcadab953eb3c88d7c8bbeff06102d05437f1`  
		Last Modified: Tue, 04 Mar 2025 00:40:46 GMT  
		Size: 24.5 KB (24471 bytes)  
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
$ docker pull golang@sha256:51ffc9e8b8f527cab2c9fa92f57c26a21156452730370037d00512992c211667
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **237.1 KB (237068 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a726dd7c4cfb2cc50b6b8df3ffe86c61b4f3ed4a67f0408482db6162544876d`

```dockerfile
```

-	Layers:
	-	`sha256:23b4a01c2ddd034fa997cae473f9ecf22f909aa6e137c384efa50be6fe5e1ba9`  
		Last Modified: Tue, 04 Mar 2025 00:44:39 GMT  
		Size: 211.8 KB (211767 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:41198135054055156202d401e7cfeedbbd054e8c00582a8126da3ca4234c35b1`  
		Last Modified: Tue, 04 Mar 2025 00:44:38 GMT  
		Size: 25.3 KB (25301 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.21` - linux; 386

```console
$ docker pull golang@sha256:b9c89efa8825c75afa6a74885e1279f21eb2c6d5ef7c1313512bdfd61dd3479d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.2 MB (130217601 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e799f5701ce81bf12c5292e8336dc67fc99a9f8718106130fbe0d88cad62649`
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
	-	`sha256:846cca974ab59749c9e042a2239489cda7d7167cafe6671ff33cbd0aed36da8e`  
		Last Modified: Tue, 04 Mar 2025 00:32:39 GMT  
		Size: 295.6 KB (295590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc05ee2fc954345b4dc36b55c348df7ba176cd1d037dcc0fd8ba6eedfb02eea9`  
		Last Modified: Tue, 04 Mar 2025 00:32:40 GMT  
		Size: 126.5 MB (126458230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b8c38de21f63272e31471f1f8e3c7622d38fce6b6fba680ff05fa83828ce86e`  
		Last Modified: Tue, 04 Mar 2025 00:32:39 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.21` - unknown; unknown

```console
$ docker pull golang@sha256:c1477fdddf6feac5abb48ecb46f1320950d8dc0ac708f3ef72451892217390e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.7 KB (236745 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e30b8526e39f94cce20ca9b03ebe1dbd34ae50f4104f96256b27dce5f2e3a83`

```dockerfile
```

-	Layers:
	-	`sha256:33273442c6615d35f81792fde4d26d3837b77958f20c418decd88060e9fa564c`  
		Last Modified: Tue, 04 Mar 2025 00:32:39 GMT  
		Size: 211.6 KB (211646 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1a46f4c2f5a7de828f2f70f26b8bba26d912b51e0abf7f35601e916385c46ed9`  
		Last Modified: Tue, 04 Mar 2025 00:32:39 GMT  
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
$ docker pull golang@sha256:ad4efcaec11215eab4ef36cfc22ea8c3936cf188a025e20e31a4f4525dc7c456
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.0 KB (235033 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5c0eec32292d9f1bca163bd3a8fc6439951a49e8732cf6a70534331268208f3`

```dockerfile
```

-	Layers:
	-	`sha256:79d04bfe465644e621d708e711efc6393a35f8253f1cab826af0d762102d739c`  
		Last Modified: Tue, 04 Mar 2025 00:46:42 GMT  
		Size: 209.8 KB (209834 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:75f70b65120b5c50310b5bec45c939f718de68a7ef2cf62ab0eca7d2a84e5af1`  
		Last Modified: Tue, 04 Mar 2025 00:46:42 GMT  
		Size: 25.2 KB (25199 bytes)  
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
$ docker pull golang@sha256:971fd60f10b401d14b5d3dd181e7213eca5b22665f5bb45bb48e26d1ec0627fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.9 KB (234902 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed671a88c0c7e40326ee207b2a0e91f67a22360caa1ab04594a007a3dc19448a`

```dockerfile
```

-	Layers:
	-	`sha256:253d739108881a4246f1ddb6f4982e4a61cdaa62c0a8758d9aa838b7b73925c6`  
		Last Modified: Tue, 04 Mar 2025 00:35:22 GMT  
		Size: 209.8 KB (209760 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e2ea5e01d322414eb96b2db4232bb73db9ffcf2a3ff59b1ca57cf6f3dcb5f8bf`  
		Last Modified: Tue, 04 Mar 2025 00:35:22 GMT  
		Size: 25.1 KB (25142 bytes)  
		MIME: application/vnd.in-toto+json
