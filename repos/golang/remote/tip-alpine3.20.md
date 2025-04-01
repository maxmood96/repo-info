## `golang:tip-alpine3.20`

```console
$ docker pull golang@sha256:89489546c2e961869b710eb6c70e8e0cef04b669df308610cfc10462fde91179
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

### `golang:tip-alpine3.20` - linux; amd64

```console
$ docker pull golang@sha256:81e56d670d218009ca84078b6f3bfe03d04a172ce1c550ac7c6bd29f522ab0c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.0 MB (129978452 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af0ab1c8a32382bd1442e876006f32fa67968ad010724a887b8d5a2de840705f`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:00:07 GMT
ADD alpine-minirootfs-3.20.6-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:00:07 GMT
CMD ["/bin/sh"]
# Mon, 31 Mar 2025 05:23:21 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 31 Mar 2025 05:23:21 GMT
ENV GOTOOLCHAIN=local
# Mon, 31 Mar 2025 05:23:21 GMT
ENV GOPATH=/go
# Mon, 31 Mar 2025 05:23:21 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 31 Mar 2025 05:23:21 GMT
COPY /target/ / # buildkit
# Mon, 31 Mar 2025 05:23:21 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 31 Mar 2025 05:23:21 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:0a9a5dfd008f05ebc27e4790db0709a29e527690c21bcbcd01481eaeb6bb49dc`  
		Last Modified: Fri, 14 Feb 2025 12:05:36 GMT  
		Size: 3.6 MB (3626897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a07c037c9f0be4e67d4a4a8f2b5ab56d8cae9c3030078fbffb4de15f5861b63`  
		Last Modified: Tue, 01 Apr 2025 17:15:50 GMT  
		Size: 294.4 KB (294388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:222cdcf0ac50c31370559153f24cee269e765f93f7d9caa55e2923550ee66d79`  
		Last Modified: Mon, 31 Mar 2025 17:35:08 GMT  
		Size: 126.1 MB (126057009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75550f6815fc7c497aecff38752861c50cecaac2dc4b9938ec0d92267fcb67dd`  
		Last Modified: Tue, 01 Apr 2025 17:15:50 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.20` - unknown; unknown

```console
$ docker pull golang@sha256:1cb3e804ae048dbbbfeb86d662f24407cc5ca11635da35c1ae15641c6c9b3521
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.0 KB (229955 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ef23d01f46502554e5eed92e51d02543a3116562241620fcd888ae45652ad91`

```dockerfile
```

-	Layers:
	-	`sha256:3f160cc670d9031ff6113d3b23890e17972d729b78e35e35c5a2acabfc5075eb`  
		Last Modified: Tue, 01 Apr 2025 17:15:50 GMT  
		Size: 205.4 KB (205443 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fae9be153d6239ab7d868cf8d3b4c9176b94338cc4e43f72dc929ad9cddc55e8`  
		Last Modified: Tue, 01 Apr 2025 17:15:50 GMT  
		Size: 24.5 KB (24512 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.20` - linux; arm variant v6

```console
$ docker pull golang@sha256:412107fdd1e781168795e5140e4b62ece53b9bc11380bdb5f2d25666a5537862
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.0 MB (125000482 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:979a3bbe75e079593ca24835d5494c4fa2e8516b181bafcbf19e09c3c43757a9`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:00:07 GMT
ADD alpine-minirootfs-3.20.6-armhf.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:00:07 GMT
CMD ["/bin/sh"]
# Mon, 31 Mar 2025 05:23:21 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 31 Mar 2025 05:23:21 GMT
ENV GOTOOLCHAIN=local
# Mon, 31 Mar 2025 05:23:21 GMT
ENV GOPATH=/go
# Mon, 31 Mar 2025 05:23:21 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 31 Mar 2025 05:23:21 GMT
COPY /target/ / # buildkit
# Mon, 31 Mar 2025 05:23:21 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 31 Mar 2025 05:23:21 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:c9aedc9d4e47fa9429e5c329420d8a93e16c433e361d0f9281565ed4da3c057e`  
		Last Modified: Fri, 14 Feb 2025 18:28:14 GMT  
		Size: 3.4 MB (3372531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:737183f74dc0d53c3f643812192622c6f3f2d83b37c68a4ca351085678413983`  
		Last Modified: Fri, 14 Feb 2025 22:17:11 GMT  
		Size: 295.8 KB (295833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2f25f8480ec104bb905a90dd4c3c957e03605868c08a66605d9b85e02dc6d17`  
		Last Modified: Mon, 31 Mar 2025 17:34:04 GMT  
		Size: 121.3 MB (121331960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cacc05e8da2989f4344658ebf4923311729581819db1264c3f550c9c1e605026`  
		Last Modified: Mon, 31 Mar 2025 17:37:39 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.20` - unknown; unknown

```console
$ docker pull golang@sha256:2f7afaad913d5fb0eb944e1e604dc3dc576a007673a8bd3b6c57b3d424b71aae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.4 KB (24404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2fcb8bbd971ae22ece238dae521b27b82e636315add584ab1634bc5116e1ae4d`

```dockerfile
```

-	Layers:
	-	`sha256:213aa6b2182e91a7f4c50e01e3b1d00ff74f1e09d7e100473655a2172b53fc5f`  
		Last Modified: Tue, 01 Apr 2025 17:15:57 GMT  
		Size: 24.4 KB (24404 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.20` - linux; arm variant v7

```console
$ docker pull golang@sha256:3ea1f568f8c810f71283ac1ad8a6a673f13ef978f908d3ea49cf0aa6e6bd5c1b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.4 MB (124381379 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c8530f846482529520f9997b6d8290161f03ce4798cb1062283f8578a65ada2`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:00:07 GMT
ADD alpine-minirootfs-3.20.6-armv7.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:00:07 GMT
CMD ["/bin/sh"]
# Mon, 31 Mar 2025 05:23:21 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 31 Mar 2025 05:23:21 GMT
ENV GOTOOLCHAIN=local
# Mon, 31 Mar 2025 05:23:21 GMT
ENV GOPATH=/go
# Mon, 31 Mar 2025 05:23:21 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 31 Mar 2025 05:23:21 GMT
COPY /target/ / # buildkit
# Mon, 31 Mar 2025 05:23:21 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 31 Mar 2025 05:23:21 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:772078ddbdee5be52d429e08f953aaad6715a90d7e4d6496eb1cd4004efa8a95`  
		Last Modified: Fri, 14 Feb 2025 12:05:37 GMT  
		Size: 3.1 MB (3095969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06d221261a6f80d203497a55ccecdc4912512b230fd036ba2df848b8144d67bf`  
		Last Modified: Fri, 14 Feb 2025 22:11:53 GMT  
		Size: 294.8 KB (294754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5df465922d4d37689f205f8db79322885e1b2a4fcb76bc9411e873e87dc4d228`  
		Last Modified: Mon, 31 Mar 2025 19:49:55 GMT  
		Size: 121.0 MB (120990498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b8689641a381b0fed5908a643506c3e52c3b7d50d530c861964cfbcd7d8d5ac`  
		Last Modified: Mon, 31 Mar 2025 19:59:32 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.20` - unknown; unknown

```console
$ docker pull golang@sha256:e9603d72b1e42cbede76791ddbccf74b61034906dc6d9e993fb8b251833b3f6b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.0 KB (229955 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10e9377ff9d13876bc4cd9c14e19948bb78ab14dffdae06d5c433e9a80b8093f`

```dockerfile
```

-	Layers:
	-	`sha256:ba0e902807242e0028d9e49145031806d0222538d243f40294535a9fce36a962`  
		Last Modified: Mon, 31 Mar 2025 19:59:32 GMT  
		Size: 205.3 KB (205335 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7af7bc7c4fd95984e05417558e6d28447e2256cad6f3475333b255621625804b`  
		Last Modified: Mon, 31 Mar 2025 19:59:32 GMT  
		Size: 24.6 KB (24620 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.20` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:5bec84a7bb5ce2c0ea39c4356530378070e7ac54ca67276ceb30e83e448b6929
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.0 MB (122993140 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54f7dd1c30c684a7d5289e6336adcffe7bcad7e949e7d146607e27a31a66f35d`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:00:07 GMT
ADD alpine-minirootfs-3.20.6-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:00:07 GMT
CMD ["/bin/sh"]
# Mon, 31 Mar 2025 05:23:21 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 31 Mar 2025 05:23:21 GMT
ENV GOTOOLCHAIN=local
# Mon, 31 Mar 2025 05:23:21 GMT
ENV GOPATH=/go
# Mon, 31 Mar 2025 05:23:21 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 31 Mar 2025 05:23:21 GMT
COPY /target/ / # buildkit
# Mon, 31 Mar 2025 05:23:21 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 31 Mar 2025 05:23:21 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:94e9d8af22013aabf0edcaf42950c88b0a1350c3a9ce076d61b98a535a673dd9`  
		Last Modified: Fri, 14 Feb 2025 12:05:38 GMT  
		Size: 4.1 MB (4091165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:634366ca850b96a5c7a0780daec3499faf6933b86acc8a8e99b70a5264f8f00e`  
		Last Modified: Mon, 24 Mar 2025 21:31:30 GMT  
		Size: 297.5 KB (297463 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15331666df650886c34693df6448a24027e3a0aedd81057f599d0c56087566f5`  
		Last Modified: Mon, 31 Mar 2025 17:54:53 GMT  
		Size: 118.6 MB (118604354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9f4c94d9a9a2dea00d530c4d98a0b1809dbe775d04a32fad83da59a18b83fe3`  
		Last Modified: Mon, 31 Mar 2025 18:01:36 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.20` - unknown; unknown

```console
$ docker pull golang@sha256:b5d431bb8bfef152bc8f008fb4830c15513438515b85b70f990d3dfc4cececd5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.0 KB (230035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55c41c8b0a8e13c0d8958f890d16576c24973bafa5710238a362767b2a04a805`

```dockerfile
```

-	Layers:
	-	`sha256:cc16ff5613747e34230eb4a105e162539f7ceb6d6ceb8670907be59efed17137`  
		Last Modified: Mon, 31 Mar 2025 18:01:36 GMT  
		Size: 205.4 KB (205387 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9b7f2e87a158517589ecebc0bc8453b436eb313a35ee47cbab2645eabc5b8c76`  
		Last Modified: Mon, 31 Mar 2025 18:01:36 GMT  
		Size: 24.6 KB (24648 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.20` - linux; 386

```console
$ docker pull golang@sha256:8a7a312891ec18e166651911f7ec791bf20e5ba425c1961567f9ca34ee228761
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.9 MB (127913602 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b7feafc611e156f1786e8913a175c06a24e55aba59d87b8022282f8e4e8d398`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:00:07 GMT
ADD alpine-minirootfs-3.20.6-x86.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:00:07 GMT
CMD ["/bin/sh"]
# Mon, 31 Mar 2025 05:23:21 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 31 Mar 2025 05:23:21 GMT
ENV GOTOOLCHAIN=local
# Mon, 31 Mar 2025 05:23:21 GMT
ENV GOPATH=/go
# Mon, 31 Mar 2025 05:23:21 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 31 Mar 2025 05:23:21 GMT
COPY /target/ / # buildkit
# Mon, 31 Mar 2025 05:23:21 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 31 Mar 2025 05:23:21 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:b3d7db73e90671cb6b7925cc878d43a2781451bed256cf0626110f5386cdd4dc`  
		Last Modified: Fri, 14 Feb 2025 12:05:37 GMT  
		Size: 3.5 MB (3471668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecadbd3dba3b499203936442a7826251fb615c16b308c300b045c3d2250f144b`  
		Last Modified: Tue, 01 Apr 2025 17:14:22 GMT  
		Size: 295.1 KB (295139 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c20357d85d18b3e3e63dc269591697947f7bf020ba7021f1f8a7b1b769a804fe`  
		Last Modified: Mon, 31 Mar 2025 17:36:49 GMT  
		Size: 124.1 MB (124146637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36399af668dcad21a5e7ef2072d073a15252859566f65cc34f6eac32d10eb711`  
		Last Modified: Tue, 01 Apr 2025 17:14:21 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.20` - unknown; unknown

```console
$ docker pull golang@sha256:3b862edeb57c23ea0a2b03534c7bf8c2ee7653d02be0c7262465921cb95e1860
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.9 KB (229867 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ab5cf837bf5e7ee8d96b112528f6393af31301f0dcfb3ca3a1d400cf62b7137`

```dockerfile
```

-	Layers:
	-	`sha256:48c0b46d9f6f6822328ce06f588d339663d352505057ac62475b2a5043b05332`  
		Last Modified: Tue, 01 Apr 2025 17:14:22 GMT  
		Size: 205.4 KB (205388 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6c532b1feeff82f84cd618fdc05ec4cf54dd5b05900a67a4c85984643d6d3789`  
		Last Modified: Tue, 01 Apr 2025 17:14:21 GMT  
		Size: 24.5 KB (24479 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.20` - linux; ppc64le

```console
$ docker pull golang@sha256:3afa4de917292e7d91aaa95c7fb5c2149f3e9073574f5b4ebe09c05dd30d1d8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.8 MB (124779026 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60a02c55757661e5ee87a6f4af9c692beb9e3e67f74513eee20a3d297288fe9f`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:00:07 GMT
ADD alpine-minirootfs-3.20.6-ppc64le.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:00:07 GMT
CMD ["/bin/sh"]
# Mon, 31 Mar 2025 05:23:21 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 31 Mar 2025 05:23:21 GMT
ENV GOTOOLCHAIN=local
# Mon, 31 Mar 2025 05:23:21 GMT
ENV GOPATH=/go
# Mon, 31 Mar 2025 05:23:21 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 31 Mar 2025 05:23:21 GMT
COPY /target/ / # buildkit
# Mon, 31 Mar 2025 05:23:21 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 31 Mar 2025 05:23:21 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:c9813c0f5a2f289ea6175876fd973d6d8adcd495da4a23e9273600c8f0a761c5`  
		Last Modified: Fri, 14 Feb 2025 12:05:35 GMT  
		Size: 3.6 MB (3575680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15784993a892df626148136e939e65b594ed2f1456345704a3272ec8fd984c53`  
		Last Modified: Mon, 24 Mar 2025 21:51:53 GMT  
		Size: 297.9 KB (297899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22730901dc3a920565010f112cf1fbaf34e7ad303fd15179e51589258f9c3f8c`  
		Last Modified: Mon, 31 Mar 2025 19:23:49 GMT  
		Size: 120.9 MB (120905289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07db9c3c6f867d55f5e4b3278c694756669d7b8ff7e37c3dcfd46a3fda71aa38`  
		Last Modified: Mon, 31 Mar 2025 19:30:31 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.20` - unknown; unknown

```console
$ docker pull golang@sha256:b881b9306813c68d677aea7c8fb9b77d0466d39ac079bd77003ad56df4020a42
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.0 KB (228024 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43266c4d3184eaf30079907f9347fcf55fffef8a66abed7c894c8b1fbd19b7de`

```dockerfile
```

-	Layers:
	-	`sha256:ea7181d6656be1ca71d35895c22b28a843edf8264193248dfbf8f0da835e3e52`  
		Last Modified: Mon, 31 Mar 2025 19:30:32 GMT  
		Size: 203.5 KB (203466 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:05d4375916672bc40a630c7469d71fb7debc07c4398ef5b43185ff4e843acb0f`  
		Last Modified: Mon, 31 Mar 2025 19:30:31 GMT  
		Size: 24.6 KB (24558 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.20` - linux; riscv64

```console
$ docker pull golang@sha256:bd8eb3202f2946928d0022ad816ee30bd4f24b2399424279df9c64398bb7fa7e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.9 MB (124893080 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f6ef96d3cbd1ce84893cfd94de8355fd31bc0809d21f963c8243386ffad7ff6`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:00:07 GMT
ADD alpine-minirootfs-3.20.6-riscv64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:00:07 GMT
CMD ["/bin/sh"]
# Mon, 31 Mar 2025 05:23:21 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 31 Mar 2025 05:23:21 GMT
ENV GOTOOLCHAIN=local
# Mon, 31 Mar 2025 05:23:21 GMT
ENV GOPATH=/go
# Mon, 31 Mar 2025 05:23:21 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 31 Mar 2025 05:23:21 GMT
COPY /target/ / # buildkit
# Mon, 31 Mar 2025 05:23:21 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 31 Mar 2025 05:23:21 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:69ccf1207daf2e3c381041f63cfe024189987fde3b1e97110475a71eac2581ba`  
		Last Modified: Fri, 14 Feb 2025 18:57:42 GMT  
		Size: 3.4 MB (3373232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12fa0de6a35b9467baeb7b28786dc580aa911bf02b2cc33ac7a44500327139a1`  
		Last Modified: Sun, 16 Feb 2025 06:13:57 GMT  
		Size: 295.4 KB (295446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3dbd81f507685434e2982d239e7e190f14c1b29624821d3f5baf22e4f468fad`  
		Last Modified: Mon, 31 Mar 2025 18:55:03 GMT  
		Size: 121.2 MB (121224244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1aafb050846a37c4ac8dc1c8d206533eafb1e175d3602b54b69b200a1b12bca`  
		Last Modified: Mon, 31 Mar 2025 19:31:38 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.20` - unknown; unknown

```console
$ docker pull golang@sha256:2a30f4e15640c0dec6964ea45b1ab76cda84d1aa0cff6a90fb80ad343ed58b4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.0 KB (228020 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cba581e1a64a702ad7c5668ba17ac52f3af610819ad21e82f38e8ba5d69d7b7d`

```dockerfile
```

-	Layers:
	-	`sha256:31de674d1ac0f4d57eb67780bdf438468126c9285a81b74def18f20ef35811ae`  
		Last Modified: Mon, 31 Mar 2025 19:31:38 GMT  
		Size: 203.5 KB (203462 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3136d0f3d383f215cefa74422bcfbfd068a88caffb1639fa630603b5371165ba`  
		Last Modified: Mon, 31 Mar 2025 19:31:38 GMT  
		Size: 24.6 KB (24558 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.20` - linux; s390x

```console
$ docker pull golang@sha256:bcc6c890163d92d1bcada60318bd8d8c05cd9abd6f0c07c76419ea0a022bc810
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.1 MB (127096624 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:522ec7e7152c326d038158dd974baafa840f8705422ae7562626c959156f5c4e`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:00:07 GMT
ADD alpine-minirootfs-3.20.6-s390x.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:00:07 GMT
CMD ["/bin/sh"]
# Mon, 31 Mar 2025 05:23:21 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 31 Mar 2025 05:23:21 GMT
ENV GOTOOLCHAIN=local
# Mon, 31 Mar 2025 05:23:21 GMT
ENV GOPATH=/go
# Mon, 31 Mar 2025 05:23:21 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 31 Mar 2025 05:23:21 GMT
COPY /target/ / # buildkit
# Mon, 31 Mar 2025 05:23:21 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 31 Mar 2025 05:23:21 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:7c6bf3be7c8016421fb3033e19b6a313f264093e1ac9e77c9f931ade0d61b3f7`  
		Last Modified: Fri, 14 Feb 2025 12:05:38 GMT  
		Size: 3.5 MB (3464123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f378f0ab9f92249cab05739adecf3318eef414f2bb034b8f1580eac04a7de99`  
		Last Modified: Mon, 24 Mar 2025 21:30:12 GMT  
		Size: 295.7 KB (295703 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab9fd359663b603237a3ae91c837b8d5c159e2e6258d720d7dd1b12433408ceb`  
		Last Modified: Mon, 31 Mar 2025 19:12:01 GMT  
		Size: 123.3 MB (123336639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e79ae61764b96043dd461269858efb77c9d8eb7fbc03f3befe8ef6a36094ce0e`  
		Last Modified: Mon, 31 Mar 2025 19:18:01 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.20` - unknown; unknown

```console
$ docker pull golang@sha256:35e3662b76edda95e4ba1b29aa28c1d583dada74c33c65e50abecbcb081cd377
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.9 KB (227915 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d77f7f7be4f70e6e2bffcaf0aca9f45b2f7d544b071aa739a2b12c3c1ff26b98`

```dockerfile
```

-	Layers:
	-	`sha256:d574c1d88b9c69f901494fa38bf646da32a79639aacfbc74ffc95780b600bd84`  
		Last Modified: Mon, 31 Mar 2025 19:18:02 GMT  
		Size: 203.4 KB (203404 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1cf1f29f7df714ced8b40b311ef335906eea0e68a9d260d39de0b4faef5cdaf3`  
		Last Modified: Mon, 31 Mar 2025 19:18:01 GMT  
		Size: 24.5 KB (24511 bytes)  
		MIME: application/vnd.in-toto+json
