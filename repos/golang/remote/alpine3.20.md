## `golang:alpine3.20`

```console
$ docker pull golang@sha256:6a84ccdb73e005d0ee7bfff6066f230612ca9dff3e88e31bfc752523c3a271f8
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

### `golang:alpine3.20` - linux; amd64

```console
$ docker pull golang@sha256:2ac51b3fa7149c38e572f104a60f0a09211f3f2f7bca2e94c04be5bbe4e4ad8b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.0 MB (77968235 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ad11ca62bce49ae9ff6ae96becbc778dd39876f8655cccdabece786866e8ec1`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 03 Dec 2024 19:01:46 GMT
ADD alpine-minirootfs-3.20.5-x86_64.tar.gz / # buildkit
# Tue, 03 Dec 2024 19:01:46 GMT
CMD ["/bin/sh"]
# Tue, 03 Dec 2024 19:01:46 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 03 Dec 2024 19:01:46 GMT
ENV GOLANG_VERSION=1.23.4
# Tue, 03 Dec 2024 19:01:46 GMT
ENV GOTOOLCHAIN=local
# Tue, 03 Dec 2024 19:01:46 GMT
ENV GOPATH=/go
# Tue, 03 Dec 2024 19:01:46 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Dec 2024 19:01:46 GMT
COPY /target/ / # buildkit
# Tue, 03 Dec 2024 19:01:46 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 03 Dec 2024 19:01:46 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:66a3d608f3fa52124f8463e9467f170c784abd549e8216aa45c6960b00b4b79b`  
		Last Modified: Wed, 08 Jan 2025 15:55:45 GMT  
		Size: 3.6 MB (3626260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fbe7652777a557be7320acd6bafa585a401104296826b9790d94fa35f28480d`  
		Last Modified: Wed, 08 Jan 2025 18:15:10 GMT  
		Size: 294.4 KB (294368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06f05ace1117d62b655e04f6f73c83617e3e0febc38681dbedf58f477dd0658c`  
		Last Modified: Tue, 03 Dec 2024 22:28:52 GMT  
		Size: 74.0 MB (74047449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bda4308841a6cc675c32eadc7ca82f1f5916886229ff6efcbc6e0f9015d73c80`  
		Last Modified: Wed, 08 Jan 2025 18:15:10 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:alpine3.20` - unknown; unknown

```console
$ docker pull golang@sha256:fb0c260157e995a1bbc52314a46c2be3928a8df8ccb8cbb92a505c4eabc01ffd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.9 KB (234885 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b951d8ee64cee83d7339ff3a2b999aff540f1ea673b739af0fbfc5c8b3b2859`

```dockerfile
```

-	Layers:
	-	`sha256:26d8cf4328839f7dedcdd885a3e3c3b9490e09e405953011fa9cea54cfebaeac`  
		Last Modified: Wed, 08 Jan 2025 18:15:10 GMT  
		Size: 210.0 KB (210037 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1cf3c2fae0fd7bdf4e2c860732473ce020afb396176dba271b4fa32f77fac283`  
		Last Modified: Wed, 08 Jan 2025 18:15:10 GMT  
		Size: 24.8 KB (24848 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:alpine3.20` - linux; arm variant v6

```console
$ docker pull golang@sha256:371765c69b922c4153105148a7fc90cad3c202ea58e10544778a74c6c8be28c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.9 MB (75865998 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d105d93ca2098a741989c95ebfa6381181dccbf6a66e34a2983f237d4d438f3`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 03 Dec 2024 19:01:46 GMT
ADD alpine-minirootfs-3.20.5-armhf.tar.gz / # buildkit
# Tue, 03 Dec 2024 19:01:46 GMT
CMD ["/bin/sh"]
# Tue, 03 Dec 2024 19:01:46 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 03 Dec 2024 19:01:46 GMT
ENV GOLANG_VERSION=1.23.4
# Tue, 03 Dec 2024 19:01:46 GMT
ENV GOTOOLCHAIN=local
# Tue, 03 Dec 2024 19:01:46 GMT
ENV GOPATH=/go
# Tue, 03 Dec 2024 19:01:46 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Dec 2024 19:01:46 GMT
COPY /target/ / # buildkit
# Tue, 03 Dec 2024 19:01:46 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 03 Dec 2024 19:01:46 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:27a1f2308f194d2c8cfe617a324e0078d055d65032c6c342eae11afb7a8d38c0`  
		Last Modified: Wed, 08 Jan 2025 17:23:56 GMT  
		Size: 3.4 MB (3371473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f69a70656b186536acaa70853744917e9a0b358e5475d451816ac52af6b864bc`  
		Last Modified: Wed, 08 Jan 2025 21:57:17 GMT  
		Size: 295.8 KB (295828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:569843b3031b27806b4332ef906025ac81fe5ab3623a61a6d2306598bfd512bf`  
		Last Modified: Tue, 03 Dec 2024 22:28:55 GMT  
		Size: 72.2 MB (72198540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c486c35fbfbee8e03d7545b2b84ec7403d41d80c0b7da546b890610d47b8d50`  
		Last Modified: Wed, 08 Jan 2025 21:58:05 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:alpine3.20` - unknown; unknown

```console
$ docker pull golang@sha256:ad57f54d95d77dc3358a923ed191fa66531d84c787df85f7687a88b104daeb83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.7 KB (24737 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:074ec47b4bcd10a4379c39c8a91f068bb74256e780904ba5b37d33e5f4767b03`

```dockerfile
```

-	Layers:
	-	`sha256:c38cfa58443fdb847ca35402e448d5a15b22169b2b201313aaa6b41b7dc7be88`  
		Last Modified: Wed, 08 Jan 2025 21:58:05 GMT  
		Size: 24.7 KB (24737 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:alpine3.20` - linux; arm variant v7

```console
$ docker pull golang@sha256:e02b42675ab7b9eca5311884e30a1242c3812fd7cda128dba27cbdc938af2867
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.6 MB (75588871 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3dbc83b1fb8054e9f0b0a68b6bff44a43d34bdd6482637a3e247dfc5d8edb23e`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 03 Dec 2024 19:01:46 GMT
ADD alpine-minirootfs-3.20.5-armv7.tar.gz / # buildkit
# Tue, 03 Dec 2024 19:01:46 GMT
CMD ["/bin/sh"]
# Tue, 03 Dec 2024 19:01:46 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 03 Dec 2024 19:01:46 GMT
ENV GOLANG_VERSION=1.23.4
# Tue, 03 Dec 2024 19:01:46 GMT
ENV GOTOOLCHAIN=local
# Tue, 03 Dec 2024 19:01:46 GMT
ENV GOPATH=/go
# Tue, 03 Dec 2024 19:01:46 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Dec 2024 19:01:46 GMT
COPY /target/ / # buildkit
# Tue, 03 Dec 2024 19:01:46 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 03 Dec 2024 19:01:46 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:c8a32ed454e751770c0976636b8d0d0fccc4f778a2dd26c428067d613be1a299`  
		Last Modified: Wed, 08 Jan 2025 17:34:15 GMT  
		Size: 3.1 MB (3095514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7bf03070cac649166aa1b87cea610615d91250eff95c905990cea3c1d510e67`  
		Last Modified: Wed, 08 Jan 2025 22:34:16 GMT  
		Size: 294.8 KB (294759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af30004a6a0d94684e60c07bbc44989294b76634fe7cc182dfb2140b1e8c877d`  
		Last Modified: Wed, 04 Dec 2024 07:17:17 GMT  
		Size: 72.2 MB (72198441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:524147eef8a9efa3143645376e1ffd9fe20097c93fdbc4b37746f8458b35b112`  
		Last Modified: Wed, 08 Jan 2025 22:35:49 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:alpine3.20` - unknown; unknown

```console
$ docker pull golang@sha256:15bd63323cd82b639491346926d37cc9d8a63fe63df5b9a0e03c63b9b3b39a3f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.0 KB (234989 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a89471d7625d83635201168ced0f3865ff6d1385a3d66578219901e0e472a9f`

```dockerfile
```

-	Layers:
	-	`sha256:352be4eb8ebb0a050d524dd8124b903c4f0874567dd60407fdbc5e8417b2b9e8`  
		Last Modified: Wed, 08 Jan 2025 22:35:49 GMT  
		Size: 210.0 KB (210037 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2ff18526d62f15a060fc7571387a6b0030fc5d02f431b08b5f4e775e3ec87c61`  
		Last Modified: Wed, 08 Jan 2025 22:35:49 GMT  
		Size: 25.0 KB (24952 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:alpine3.20` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:05756aea3084ab432e91c70cc2cd72d46ff8590eef74cd1ebe8555e28f0034a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.1 MB (75061818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d3f8895ac08aafceeba0be6c96c968cea76a9c56a6dd89d4955c1672d18d530`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 03 Dec 2024 19:01:46 GMT
ADD alpine-minirootfs-3.20.5-aarch64.tar.gz / # buildkit
# Tue, 03 Dec 2024 19:01:46 GMT
CMD ["/bin/sh"]
# Tue, 03 Dec 2024 19:01:46 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 03 Dec 2024 19:01:46 GMT
ENV GOLANG_VERSION=1.23.4
# Tue, 03 Dec 2024 19:01:46 GMT
ENV GOTOOLCHAIN=local
# Tue, 03 Dec 2024 19:01:46 GMT
ENV GOPATH=/go
# Tue, 03 Dec 2024 19:01:46 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Dec 2024 19:01:46 GMT
COPY /target/ / # buildkit
# Tue, 03 Dec 2024 19:01:46 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 03 Dec 2024 19:01:46 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:0152682790bba2052e0b7dc52872083c01ea53c598fe87e3fe3eab5f9d4228cb`  
		Last Modified: Wed, 08 Jan 2025 17:24:05 GMT  
		Size: 4.1 MB (4090769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be07219bb1974a1749c2d7ad8e3c5020b1a9e55023216926da79ccd2a39b4eef`  
		Last Modified: Wed, 08 Jan 2025 22:40:18 GMT  
		Size: 297.5 KB (297474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39f8f326b04424eb2027d1f0e3255fe568d71a5567f894a08cd86605ebe51c58`  
		Last Modified: Wed, 04 Dec 2024 01:41:07 GMT  
		Size: 70.7 MB (70673417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:717d10fbda110fc1d40b782baa31672954bcb08f995d44aaa54b47b2e932ea70`  
		Last Modified: Wed, 08 Jan 2025 22:41:10 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:alpine3.20` - unknown; unknown

```console
$ docker pull golang@sha256:b7050b8b6b066df8c75614cb6b6a87669f9a36147d6ee8bc6f51060008c3058a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.1 KB (235077 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01f68905c66948388ad1e0f3c1f853231b05b4d15b8144dce7c5340e7320d2eb`

```dockerfile
```

-	Layers:
	-	`sha256:fb1f3d4b1d789be420e4b628a501d3108853a83f2a9ecc9d3933b0d3e3946444`  
		Last Modified: Wed, 08 Jan 2025 22:41:11 GMT  
		Size: 210.1 KB (210093 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:20fa9d28b0f38cb5f82b79c9146d7893b9063f8a93d256fede59ded17feccb85`  
		Last Modified: Wed, 08 Jan 2025 22:41:10 GMT  
		Size: 25.0 KB (24984 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:alpine3.20` - linux; 386

```console
$ docker pull golang@sha256:c74d222feee45cd904f299da0c484310e396f6690efd4ba309303713e33cecba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.7 MB (75679386 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78ff8f99affb5e517270dc366e25e6041c616cfa3c1536799843e5db0c87d0b5`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 03 Dec 2024 19:01:46 GMT
ADD alpine-minirootfs-3.20.5-x86.tar.gz / # buildkit
# Tue, 03 Dec 2024 19:01:46 GMT
CMD ["/bin/sh"]
# Tue, 03 Dec 2024 19:01:46 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 03 Dec 2024 19:01:46 GMT
ENV GOLANG_VERSION=1.23.4
# Tue, 03 Dec 2024 19:01:46 GMT
ENV GOTOOLCHAIN=local
# Tue, 03 Dec 2024 19:01:46 GMT
ENV GOPATH=/go
# Tue, 03 Dec 2024 19:01:46 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Dec 2024 19:01:46 GMT
COPY /target/ / # buildkit
# Tue, 03 Dec 2024 19:01:46 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 03 Dec 2024 19:01:46 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:6d632fc6244662e41ee3b3f29090684a520e615dc5c282638a7587366dcd4fb9`  
		Last Modified: Wed, 08 Jan 2025 17:23:34 GMT  
		Size: 3.5 MB (3470969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3a3a677255f257a26e3c31092d64b82f7cdc4d9fc0bd977c717324fdeca5854`  
		Last Modified: Wed, 08 Jan 2025 18:11:15 GMT  
		Size: 295.1 KB (295138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:253ee978a239d9a54a2ed89c291f3c5c0ee5f67c1dc8c9ff24b239116398d826`  
		Last Modified: Tue, 03 Dec 2024 22:28:50 GMT  
		Size: 71.9 MB (71913121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccf56cc115cdb8fc5a484278226dbe6ef6b87be542888c4835ad8f524b11e95f`  
		Last Modified: Wed, 08 Jan 2025 18:11:15 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:alpine3.20` - unknown; unknown

```console
$ docker pull golang@sha256:335d874ad36dc9cb5d1cdf5de058f825060f0ecc5a2e61a4f0f24071117b3709
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.8 KB (234790 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf31075a495bcdfcfb403dff0e067d75d9b6674b6b704a700e3ceee7ce213d3b`

```dockerfile
```

-	Layers:
	-	`sha256:53905285757173405e4def6b77ee232e03a33134e48dfaf447b87368e5f88e8e`  
		Last Modified: Wed, 08 Jan 2025 18:11:15 GMT  
		Size: 210.0 KB (209976 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b3137c1ca76bb95d7a96fc48aebb148542b43ff656164866b2f70e5d7796731b`  
		Last Modified: Wed, 08 Jan 2025 18:11:15 GMT  
		Size: 24.8 KB (24814 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:alpine3.20` - linux; ppc64le

```console
$ docker pull golang@sha256:2893870c6108ac14c733c6baa101529e67b7c55546b2027960c0d4b0fbce3c85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.7 MB (74712002 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb2f51be504fbb693c8510363dec9d74d2ad78d437b5e54a5f426f050b77bb65`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 03 Dec 2024 19:01:46 GMT
ADD alpine-minirootfs-3.20.5-ppc64le.tar.gz / # buildkit
# Tue, 03 Dec 2024 19:01:46 GMT
CMD ["/bin/sh"]
# Tue, 03 Dec 2024 19:01:46 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 03 Dec 2024 19:01:46 GMT
ENV GOLANG_VERSION=1.23.4
# Tue, 03 Dec 2024 19:01:46 GMT
ENV GOTOOLCHAIN=local
# Tue, 03 Dec 2024 19:01:46 GMT
ENV GOPATH=/go
# Tue, 03 Dec 2024 19:01:46 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Dec 2024 19:01:46 GMT
COPY /target/ / # buildkit
# Tue, 03 Dec 2024 19:01:46 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 03 Dec 2024 19:01:46 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:3383dff810cd4af0350465f92c0a5f925af062ceac665a36e91384093216a7db`  
		Last Modified: Wed, 08 Jan 2025 17:24:56 GMT  
		Size: 3.6 MB (3574406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:536d34381fd9ad3cee58f53559c0874fc783fd9067870f324d9d4e8f092a0015`  
		Last Modified: Wed, 08 Jan 2025 21:50:14 GMT  
		Size: 297.9 KB (297894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b834890572191b3d66e6bd561aad556f3c52e760e67fe9e31f02ad3d5139f55e`  
		Last Modified: Tue, 03 Dec 2024 23:35:02 GMT  
		Size: 70.8 MB (70839544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a10173039484873ca3979a3698ef22d1edfdf1fb0aeabab8ad8b5abf80e36c0b`  
		Last Modified: Wed, 08 Jan 2025 21:52:09 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:alpine3.20` - unknown; unknown

```console
$ docker pull golang@sha256:1b112ba2ab30f06695782b4f751260f130cfffd8af3ca68f56659372fae15b20
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.1 KB (233054 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4c8d3eff9f95b3df896dfb423baf35f4f7cd3250d2aa858827c42e9cb8f28e5`

```dockerfile
```

-	Layers:
	-	`sha256:82c798d2cd3e7cfe80f6ea1550cd4f38b4de491b184d31084c847759c470afcd`  
		Last Modified: Wed, 08 Jan 2025 21:52:10 GMT  
		Size: 208.2 KB (208156 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0b93cc120096e3e77cd1772474d6d37e70200b8b4b2d49b4a051c076304cb142`  
		Last Modified: Wed, 08 Jan 2025 21:52:09 GMT  
		Size: 24.9 KB (24898 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:alpine3.20` - linux; riscv64

```console
$ docker pull golang@sha256:3ec902a2e97f16c187850ab425fff566be009bc434c4742459beae3ee3925344
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.9 MB (74908449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2532c7131949e4fc997c03dc12ef6d55a3cc83dd5e796b35ea27d2778c90733c`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 03 Dec 2024 19:01:46 GMT
ADD alpine-minirootfs-3.20.5-riscv64.tar.gz / # buildkit
# Tue, 03 Dec 2024 19:01:46 GMT
CMD ["/bin/sh"]
# Tue, 03 Dec 2024 19:01:46 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 03 Dec 2024 19:01:46 GMT
ENV GOLANG_VERSION=1.23.4
# Tue, 03 Dec 2024 19:01:46 GMT
ENV GOTOOLCHAIN=local
# Tue, 03 Dec 2024 19:01:46 GMT
ENV GOPATH=/go
# Tue, 03 Dec 2024 19:01:46 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Dec 2024 19:01:46 GMT
COPY /target/ / # buildkit
# Tue, 03 Dec 2024 19:01:46 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 03 Dec 2024 19:01:46 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:34b7590cc8ea3b21e8c3a0d69270b822d3ba63bc58c6cf0e36c987c95b18eb8d`  
		Last Modified: Wed, 08 Jan 2025 17:49:41 GMT  
		Size: 3.4 MB (3371926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:816c3897a63cf7689a7beab4c1f1af77b6f15050c01df55852c40f878936f63b`  
		Last Modified: Fri, 10 Jan 2025 17:00:34 GMT  
		Size: 295.4 KB (295445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c56ea5001679e325e9959f4e49e737d7b5d8a17fc575fd3810ab4495a88e73ee`  
		Last Modified: Tue, 03 Dec 2024 22:32:57 GMT  
		Size: 71.2 MB (71240920 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91765e269643a82d9c52e463ec9314f16a49e4edf046b093e4c7b6aac5679190`  
		Last Modified: Fri, 10 Jan 2025 17:08:37 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:alpine3.20` - unknown; unknown

```console
$ docker pull golang@sha256:38dff6419dcbd4f04019d2857012a22e064dc63731a9e1a34c6a65c480524389
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.1 KB (233050 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00877f5b82ebb1ff64e2fc73e2f7ad449995adae3815c7215548f7f54346a537`

```dockerfile
```

-	Layers:
	-	`sha256:128f563ab702d4a91d4ef58ae5b620e992b5fed6e2d12bfeb129e1a9465da67d`  
		Last Modified: Fri, 10 Jan 2025 17:08:37 GMT  
		Size: 208.2 KB (208152 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a4236860016b5e79a6e5c914e9da1b219a62eb6432ebe82706224cd4ae96afd0`  
		Last Modified: Fri, 10 Jan 2025 17:08:37 GMT  
		Size: 24.9 KB (24898 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:alpine3.20` - linux; s390x

```console
$ docker pull golang@sha256:3292512039c7184d771ea398098feab1755b7d74083d78579b363e28d80066c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.7 MB (76728991 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c201de3a4571102812dc84f7a0d5eddda2a3d252500c681849b7cc3cc980f37`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 03 Dec 2024 19:01:46 GMT
ADD alpine-minirootfs-3.20.5-s390x.tar.gz / # buildkit
# Tue, 03 Dec 2024 19:01:46 GMT
CMD ["/bin/sh"]
# Tue, 03 Dec 2024 19:01:46 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 03 Dec 2024 19:01:46 GMT
ENV GOLANG_VERSION=1.23.4
# Tue, 03 Dec 2024 19:01:46 GMT
ENV GOTOOLCHAIN=local
# Tue, 03 Dec 2024 19:01:46 GMT
ENV GOPATH=/go
# Tue, 03 Dec 2024 19:01:46 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Dec 2024 19:01:46 GMT
COPY /target/ / # buildkit
# Tue, 03 Dec 2024 19:01:46 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 03 Dec 2024 19:01:46 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:3e71c43ed556c3ed564b517d9141db651f4134655f96c8731767c14c6dedc4d0`  
		Last Modified: Wed, 08 Jan 2025 17:25:57 GMT  
		Size: 3.5 MB (3463322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f27beb3ecfc66a05c4717a47324657a7da44cd7a01b554efb4ced3c7c613a567`  
		Last Modified: Wed, 08 Jan 2025 22:26:47 GMT  
		Size: 295.7 KB (295699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1eab153b4468df7f657167533fa78804e60b235edee0f04ec5dcc52a35b056da`  
		Last Modified: Tue, 03 Dec 2024 22:40:01 GMT  
		Size: 73.0 MB (72969813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8b18bb26d7f919379e3435b72f0bfcde89d64d33f8a4e91239032ce6aea3006`  
		Last Modified: Wed, 08 Jan 2025 22:28:37 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:alpine3.20` - unknown; unknown

```console
$ docker pull golang@sha256:35e5f03a089d697698e74606df1edc9b9cfe6d4a2711b4039fd0334b17849ecf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.9 KB (232936 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc6b2699d0295bfb7961f69a546c23b324d7c277444adf22042eb920d6e567fb`

```dockerfile
```

-	Layers:
	-	`sha256:e866b48bead70393d157cc989081ac8d706f9e9d0c29b2e9a0198d372ca4bf29`  
		Last Modified: Wed, 08 Jan 2025 22:28:37 GMT  
		Size: 208.1 KB (208086 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d3ba11edae9df0347eb1fdc1c41a8bdbac9b9780651a86f54feca84ebf8a2d83`  
		Last Modified: Wed, 08 Jan 2025 22:28:37 GMT  
		Size: 24.9 KB (24850 bytes)  
		MIME: application/vnd.in-toto+json
