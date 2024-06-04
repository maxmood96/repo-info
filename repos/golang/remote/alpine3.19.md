## `golang:alpine3.19`

```console
$ docker pull golang@sha256:65b5d2d0a312fd9ef65551ad7f9cb5db1f209b7517ef6d5625cfd29248bc6c85
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 14
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
	-	linux; s390x
	-	unknown; unknown

### `golang:alpine3.19` - linux; amd64

```console
$ docker pull golang@sha256:0fac882b6c3b63e70986e185670706e8661225b7cf7f4d312ec30e9b109141d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.0 MB (73047332 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:673ded70c0bb26b891504b69e738ead4f8565763eabebb91cc32513cc394ff0c`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:48 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Sat, 27 Jan 2024 00:30:48 GMT
CMD ["/bin/sh"]
# Tue, 04 Jun 2024 19:06:26 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 04 Jun 2024 19:06:26 GMT
ENV GOLANG_VERSION=1.22.4
# Tue, 04 Jun 2024 19:06:26 GMT
ENV GOTOOLCHAIN=local
# Tue, 04 Jun 2024 19:06:26 GMT
ENV GOPATH=/go
# Tue, 04 Jun 2024 19:06:26 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Jun 2024 19:06:26 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Tue, 04 Jun 2024 19:06:26 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 04 Jun 2024 19:06:26 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:4abcf20661432fb2d719aaf90656f55c287f8ca915dc1c92ec14ff61e67fbaf8`  
		Last Modified: Sat, 27 Jan 2024 00:31:24 GMT  
		Size: 3.4 MB (3408729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24cf458f3a1138632ed993cf08d5c5f031ed242f203b379a25a5f0de3f6a9609`  
		Last Modified: Tue, 04 Jun 2024 20:15:54 GMT  
		Size: 292.9 KB (292904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0836633d3ad30840017cbf04f1d30ba523fe7522a3bc7baee3d42dd5c2f876af`  
		Last Modified: Tue, 04 Jun 2024 20:15:55 GMT  
		Size: 69.3 MB (69345542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6ce58a6137d735a9a8110140b4bc183d52e1b1c237d3b8e71c7f3b82bf0aaa4`  
		Last Modified: Tue, 04 Jun 2024 20:15:54 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:alpine3.19` - unknown; unknown

```console
$ docker pull golang@sha256:71af5b2a5f93040b71d901839bd4dba48a1832447b94e66e0940a838ebea168d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.5 KB (22459 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8985caa70f813e240597ade84c01311a6bae375ca91afd0b0682133ed241c9bb`

```dockerfile
```

-	Layers:
	-	`sha256:81261429b8bda4a9d2c2f1e548f48787272aeca6a704666c6bad4efb7b72a3b8`  
		Last Modified: Tue, 04 Jun 2024 20:15:54 GMT  
		Size: 22.5 KB (22459 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:alpine3.19` - linux; arm variant v6

```console
$ docker pull golang@sha256:1be00756e8e00eec7347967d3f4d3e4d4de1f38fb60e614cee945fe25cd62717
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.2 MB (71173211 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f26069c6315ce3976f7e3c883ac041819a95e67e15ffceaa152b80a8926e598`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 26 Jan 2024 23:49:17 GMT
ADD file:99cc37cba14ac64dc4652e46dc671888a0265f90992faa05c32d32e21f89c147 in / 
# Fri, 26 Jan 2024 23:49:17 GMT
CMD ["/bin/sh"]
# Tue, 04 Jun 2024 19:06:26 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 04 Jun 2024 19:06:26 GMT
ENV GOLANG_VERSION=1.22.4
# Tue, 04 Jun 2024 19:06:26 GMT
ENV GOTOOLCHAIN=local
# Tue, 04 Jun 2024 19:06:26 GMT
ENV GOPATH=/go
# Tue, 04 Jun 2024 19:06:26 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Jun 2024 19:06:26 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Tue, 04 Jun 2024 19:06:26 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 04 Jun 2024 19:06:26 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:0dc2e6c0f9ded2daeca96bbf270526d182d2f4267f5c7610c222c05cad6f6b96`  
		Last Modified: Fri, 26 Jan 2024 23:49:40 GMT  
		Size: 3.2 MB (3165396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9038d28e8a5b6b0a997ff1184fba2f3c29383d931838505a29f72ef9314c64f3`  
		Last Modified: Tue, 04 Jun 2024 20:21:15 GMT  
		Size: 294.3 KB (294343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2388fa1f9ceced099ac1af7a1054215236ac4f41428b02ea4d6e98d46f5da9d6`  
		Last Modified: Tue, 04 Jun 2024 20:20:34 GMT  
		Size: 67.7 MB (67713314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9295694e7068dafbf8d4bd92e1e6f95603a11bdf5bba20c300a27fef557b1605`  
		Last Modified: Tue, 04 Jun 2024 20:21:14 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:alpine3.19` - unknown; unknown

```console
$ docker pull golang@sha256:5259417fc966c5c26c0799f96e168a74be5296c4b13a37a54f33c8d106fc9285
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.6 KB (22555 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:097c6f778f7016102a4c5d189e3620fb31452e9bd4130a9c735f13e370a2b881`

```dockerfile
```

-	Layers:
	-	`sha256:84047155a1443cd5ba1b9f6cb99ad1849f6338bb73c5d1c62bf078742b73b0fe`  
		Last Modified: Tue, 04 Jun 2024 20:21:14 GMT  
		Size: 22.6 KB (22555 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:alpine3.19` - linux; arm variant v7

```console
$ docker pull golang@sha256:f9ae7a76e0a9ebeb505722dc10096241e535c3ea746cca125580c727b8619ff2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.9 MB (70925627 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1570b62eee685bf1a5e212c0def4a5cc24ecff5205ce4954d49811e7d4abe627`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Sat, 27 Jan 2024 00:14:54 GMT
ADD file:dca2a738b46ed78f0ccd7e23ba4d4729528feaa423a0ff0ac5c3512bf43b6fae in / 
# Sat, 27 Jan 2024 00:14:54 GMT
CMD ["/bin/sh"]
# Tue, 04 Jun 2024 19:06:26 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 04 Jun 2024 19:06:26 GMT
ENV GOLANG_VERSION=1.22.4
# Tue, 04 Jun 2024 19:06:26 GMT
ENV GOTOOLCHAIN=local
# Tue, 04 Jun 2024 19:06:26 GMT
ENV GOPATH=/go
# Tue, 04 Jun 2024 19:06:26 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Jun 2024 19:06:26 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Tue, 04 Jun 2024 19:06:26 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 04 Jun 2024 19:06:26 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:fda0ff469afd28d9cfbb946e8e0a3c911c591a2691bea62be9187e45a1c50549`  
		Last Modified: Sat, 27 Jan 2024 00:15:27 GMT  
		Size: 2.9 MB (2918899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1561d32e92fb99b99c45c2513bc8e78227d187a0f1db885d85f03506ce4bc8f2`  
		Last Modified: Tue, 04 Jun 2024 20:22:48 GMT  
		Size: 293.2 KB (293179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05f2d60982f3278ca26e0dd4a91fb30e80076051e36da023e58e47681cc2934e`  
		Last Modified: Tue, 04 Jun 2024 20:20:28 GMT  
		Size: 67.7 MB (67713391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d2d497b2d3f829f6f1c67a4ba173e71092767b18eb9919480fbbc3d36445ffb`  
		Last Modified: Tue, 04 Jun 2024 20:22:47 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:alpine3.19` - unknown; unknown

```console
$ docker pull golang@sha256:73b4c1f705cba1bccc183d62604afcd63752653e5c5634d204165529d7cc6bea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.6 KB (22555 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6f72e4ee5b4610aad02ce6699e79982e1dd6642fa7c28bc410bd57f21287862`

```dockerfile
```

-	Layers:
	-	`sha256:7dec0db01bdb1777d3a1398ee209edfbbe071ec03f09df43913844dc916d24aa`  
		Last Modified: Tue, 04 Jun 2024 20:22:48 GMT  
		Size: 22.6 KB (22555 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:alpine3.19` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:f163f4bb1f3b5596b0dd5691d74f9f7839de22687feb0366cac8786c3c231f72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.9 MB (69914361 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e2c0d0559fa0dde1662d019fd01d75d3f3aaba58ffbd44c7594ee6146537572`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:47 GMT
ADD file:d0764a717d1e9d0aff3fa84779b11bfa0afe4430dcb6b46d965b209167639ba0 in / 
# Fri, 26 Jan 2024 23:44:47 GMT
CMD ["/bin/sh"]
# Tue, 04 Jun 2024 19:06:26 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 04 Jun 2024 19:06:26 GMT
ENV GOLANG_VERSION=1.22.4
# Tue, 04 Jun 2024 19:06:26 GMT
ENV GOTOOLCHAIN=local
# Tue, 04 Jun 2024 19:06:26 GMT
ENV GOPATH=/go
# Tue, 04 Jun 2024 19:06:26 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Jun 2024 19:06:26 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Tue, 04 Jun 2024 19:06:26 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 04 Jun 2024 19:06:26 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:bca4290a96390d7a6fc6f2f9929370d06f8dfcacba591c76e3d5c5044e7f420c`  
		Last Modified: Fri, 26 Jan 2024 23:45:19 GMT  
		Size: 3.3 MB (3347715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b615716f2b1f22619df8c7d67ecfbb834bf1ddaa93b879fca55f8e7fe3057877`  
		Last Modified: Tue, 04 Jun 2024 20:21:38 GMT  
		Size: 296.1 KB (296077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45c0d35bf3e901b1024e7abc65a8b1332e085c592b5bdd1d9422364771935e1e`  
		Last Modified: Tue, 04 Jun 2024 20:19:51 GMT  
		Size: 66.3 MB (66270410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9009ef7e7042d86d7340e68c9b8cfe4a8029fd3160c92126e56d55c0f37810d`  
		Last Modified: Tue, 04 Jun 2024 20:21:38 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:alpine3.19` - unknown; unknown

```console
$ docker pull golang@sha256:57e0aef46bc84cf3fc1786ad3a30f9ec32048aa1158272c8209ea931e393b782
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.8 KB (22758 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56f3059d38ef8366e4ce34b8f5d08f1ce4c7ef32c9cdc2dac5c4a91125cf0fb8`

```dockerfile
```

-	Layers:
	-	`sha256:a6018f48148f0a36ac34ef8ca93bed6e721fd019347538bc8afdf91093ea7400`  
		Last Modified: Tue, 04 Jun 2024 20:21:38 GMT  
		Size: 22.8 KB (22758 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:alpine3.19` - linux; 386

```console
$ docker pull golang@sha256:575b87257198a1afb0a9c0792a1237591aeb070d0fe69d40b63fc227e049b373
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.9 MB (70882381 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4aa399a68cb82a7bcef48cd90fda376d2790870246df80e12f7ca0a6d64ac07c`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Sat, 27 Jan 2024 00:38:19 GMT
ADD file:50130ffc87b68d2889c28269d2783e37c42087ce4793108222ad53ed22443a90 in / 
# Sat, 27 Jan 2024 00:38:19 GMT
CMD ["/bin/sh"]
# Tue, 04 Jun 2024 19:06:26 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 04 Jun 2024 19:06:26 GMT
ENV GOLANG_VERSION=1.22.4
# Tue, 04 Jun 2024 19:06:26 GMT
ENV GOTOOLCHAIN=local
# Tue, 04 Jun 2024 19:06:26 GMT
ENV GOPATH=/go
# Tue, 04 Jun 2024 19:06:26 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Jun 2024 19:06:26 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Tue, 04 Jun 2024 19:06:26 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 04 Jun 2024 19:06:26 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:4a0759b5afbffdc507fbb4e32b3a139063c3a5c0829f811973850447f98830ae`  
		Last Modified: Sat, 27 Jan 2024 00:38:47 GMT  
		Size: 3.2 MB (3244089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3acc8db28e36c21728ec789b448597b1e37c8a605af2cc1244ab9b551fa2ebf5`  
		Last Modified: Tue, 04 Jun 2024 20:16:15 GMT  
		Size: 293.6 KB (293585 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b70653b7605bcb6cd6384a2e3f3063531042e198fbb44fc2c8ef4a6292ac9de`  
		Last Modified: Tue, 04 Jun 2024 20:16:17 GMT  
		Size: 67.3 MB (67344549 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37fa49bd8a29fd25e24acb8b8a2e8a0d65d3a7a53e8725185132d84312eae771`  
		Last Modified: Tue, 04 Jun 2024 20:16:15 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:alpine3.19` - unknown; unknown

```console
$ docker pull golang@sha256:df994216819a329ca6ff8907725e898a044675d3e267fc86cc3e5ab18219c579
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.4 KB (22426 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41128cc63e7a02441a0d1152556040fddcf4be0dd5fef9e724b340f61533e60d`

```dockerfile
```

-	Layers:
	-	`sha256:885413bb4b0f2b0f131b9282819fa55cd2c32f0b5a85ce19fa4f6d5bfbcdc5eb`  
		Last Modified: Tue, 04 Jun 2024 20:16:15 GMT  
		Size: 22.4 KB (22426 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:alpine3.19` - linux; ppc64le

```console
$ docker pull golang@sha256:c17fc793ed0eb0105cb3edc5a99b82e6da40fb0c3e4ad08ba3026dbae0d97ca6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.1 MB (70095832 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ae3ce6181675770bc9c7b31f95dadfd89c7df63242b04d1e074d206aa8f10ce`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Sat, 27 Jan 2024 00:27:35 GMT
ADD file:76976bd619bf0c4e63bbd1d1d0a20b224d1f14070cb9be6036c1b7672a7848ba in / 
# Sat, 27 Jan 2024 00:27:35 GMT
CMD ["/bin/sh"]
# Tue, 04 Jun 2024 19:06:26 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 04 Jun 2024 19:06:26 GMT
ENV GOLANG_VERSION=1.22.4
# Tue, 04 Jun 2024 19:06:26 GMT
ENV GOTOOLCHAIN=local
# Tue, 04 Jun 2024 19:06:26 GMT
ENV GOPATH=/go
# Tue, 04 Jun 2024 19:06:26 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Jun 2024 19:06:26 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Tue, 04 Jun 2024 19:06:26 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 04 Jun 2024 19:06:26 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:f4968021da4ff8b74325e5aebf0f9448b44becfdd14df80ecba474e43cc92546`  
		Last Modified: Sat, 27 Jan 2024 00:28:10 GMT  
		Size: 3.4 MB (3358353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee954196fd450a22d40adce9553b889b909e570f99bb480f12fb9009787a392e`  
		Last Modified: Tue, 04 Jun 2024 20:23:05 GMT  
		Size: 296.5 KB (296481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:236cbdc316b6a948ffe0177ed252011a6646360d0cbcf8cbfc819b8774160a29`  
		Last Modified: Tue, 04 Jun 2024 20:19:26 GMT  
		Size: 66.4 MB (66440839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02c9ab2c0dfe2585c9cd51720d5084c9ba1ec17e2bafa9baa9c480621316dae4`  
		Last Modified: Tue, 04 Jun 2024 20:23:05 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:alpine3.19` - unknown; unknown

```console
$ docker pull golang@sha256:02b6461223ae54462725eff3649d01841553e9f32298d879acb843ca4a89c702
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.5 KB (22501 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cb11b6c7ce5b618d325b0e3efdcba97997374894e7a5d4073e873ce89d10e47`

```dockerfile
```

-	Layers:
	-	`sha256:445674fadaf4b38ca8f3ff4a3b8efbf7d3b20d6234fc0cc8b223b59d1c4f4a7b`  
		Last Modified: Tue, 04 Jun 2024 20:23:05 GMT  
		Size: 22.5 KB (22501 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:alpine3.19` - linux; s390x

```console
$ docker pull golang@sha256:b0a14b2a51a8f5668b8c9baa032f1a06cfe4989f083381eb9bc5f2b9afc58672
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.9 MB (71942164 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78b836c4b6a6ef945013b92100fa92b19eec6914e9fb1f64308738ac262c3eed`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Sat, 27 Jan 2024 00:37:52 GMT
ADD file:a3a70231936c63931e39d0cbee91dc800a1f64c713d03da79c5cc7b7d68bde92 in / 
# Sat, 27 Jan 2024 00:37:52 GMT
CMD ["/bin/sh"]
# Tue, 04 Jun 2024 19:06:26 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 04 Jun 2024 19:06:26 GMT
ENV GOLANG_VERSION=1.22.4
# Tue, 04 Jun 2024 19:06:26 GMT
ENV GOTOOLCHAIN=local
# Tue, 04 Jun 2024 19:06:26 GMT
ENV GOPATH=/go
# Tue, 04 Jun 2024 19:06:26 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Jun 2024 19:06:26 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Tue, 04 Jun 2024 19:06:26 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 04 Jun 2024 19:06:26 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:eb8fba61d86413beda3240c40c599041e040e658cd8314e38ee15e67ea57d349`  
		Last Modified: Sat, 27 Jan 2024 00:43:21 GMT  
		Size: 3.2 MB (3242635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80cbc49a779c2292f76433376e1adfaaa1c09734804344d3ea4dc5f5a7331d2f`  
		Last Modified: Tue, 04 Jun 2024 20:26:42 GMT  
		Size: 294.1 KB (294123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7fb824bc24fdc7f4fb089d47d141644e86949635714a893519e6ce56fa54e32`  
		Last Modified: Tue, 04 Jun 2024 20:22:15 GMT  
		Size: 68.4 MB (68405249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36f9858c56983510c560b0faa75d160bf2d7b740b333c0221bd7901035e7da72`  
		Last Modified: Tue, 04 Jun 2024 20:26:42 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:alpine3.19` - unknown; unknown

```console
$ docker pull golang@sha256:d8ff5e63e35b406f77325de00061768c795b9a2f23a5309c1ed79b8ff3275186
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.5 KB (22459 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ad8196a4ec2ba24bfc2ea4bf6e14b9fc660779a68257927443051974b14e796`

```dockerfile
```

-	Layers:
	-	`sha256:71aafe795ab944dd10508187c289f72c527d2df1b72e624879c8390a7be11b16`  
		Last Modified: Tue, 04 Jun 2024 20:26:42 GMT  
		Size: 22.5 KB (22459 bytes)  
		MIME: application/vnd.in-toto+json
