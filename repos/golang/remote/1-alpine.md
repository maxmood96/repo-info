## `golang:1-alpine`

```console
$ docker pull golang@sha256:f591145352ef7cd7d7e2b4e1d4a6fd4dd2ac72c405b689d6e8147339105a9e3a
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

### `golang:1-alpine` - linux; amd64

```console
$ docker pull golang@sha256:3058c543b93017c20123f4ffe8ca779c88ade0102361ab9a290bf7d590360fc4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.9 MB (77918127 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5ada884192f173018fcb39688bd70545669ab105941231067ea5dbed4ac6914`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 05 Sep 2024 16:50:05 GMT
ADD file:5758b97d8301c84a204a6e516241275d785a7cade40b2fb99f01fe122482e283 in / 
# Thu, 05 Sep 2024 16:50:05 GMT
CMD ["/bin/sh"]
# Thu, 05 Sep 2024 16:50:05 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Thu, 05 Sep 2024 16:50:05 GMT
ENV GOLANG_VERSION=1.23.1
# Thu, 05 Sep 2024 16:50:05 GMT
ENV GOTOOLCHAIN=local
# Thu, 05 Sep 2024 16:50:05 GMT
ENV GOPATH=/go
# Thu, 05 Sep 2024 16:50:05 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Sep 2024 16:50:05 GMT
COPY /target/ / # buildkit
# Thu, 05 Sep 2024 16:50:05 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Thu, 05 Sep 2024 16:50:05 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:43c4264eed91be63b206e17d93e75256a6097070ce643c5e8f0379998b44f170`  
		Last Modified: Fri, 06 Sep 2024 22:20:39 GMT  
		Size: 3.6 MB (3623807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab19dfae90efdd651c37b568f750d129c6d7c47d3a902982eefcd7c6567ccd5d`  
		Last Modified: Fri, 06 Sep 2024 23:19:44 GMT  
		Size: 290.9 KB (290879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7bff916ab0c126c9d943f0c481a905f402e00f206a89248f257ef90beaabbd8`  
		Last Modified: Thu, 05 Sep 2024 22:02:55 GMT  
		Size: 74.0 MB (74003284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78cee99375e3e0bb16a7bcb00218932b90225708c1a53e97b98b5230fe87b86a`  
		Last Modified: Fri, 06 Sep 2024 23:19:44 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:d400e811eaad76f5297f099791a4003a2958e853b91281093b4a6521ccf12003
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.2 KB (232224 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9b242e9bf917ea82d5bc0e66eae8d36dcaaf6c3f59177ef827f4a822600c145`

```dockerfile
```

-	Layers:
	-	`sha256:2ebcf6e5543f9138695d9ecb93ea03121f91657b8b9788627dd2b36e31a9fa20`  
		Last Modified: Fri, 06 Sep 2024 23:19:44 GMT  
		Size: 206.4 KB (206381 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:89ddafe4638d3cd7c1b54abc5170475638e0e513e939fddbaa27ff4c49a0fa07`  
		Last Modified: Fri, 06 Sep 2024 23:19:44 GMT  
		Size: 25.8 KB (25843 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-alpine` - linux; arm variant v6

```console
$ docker pull golang@sha256:21ba56c1b75ddd2ac5faaf7f4a74073cf1575f6c354a1ed2d540ee916cbe1d7a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.8 MB (75798574 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59411d37ae7349ec6468e015f6224c2fb965a2ea9b402669a920e6e937d2d8a9`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Mon, 22 Jul 2024 21:49:18 GMT
ADD file:85f927c1895bee1d0b095b2905c8d47ada8773f13e03fd4a201f718103ef7958 in / 
# Mon, 22 Jul 2024 21:49:19 GMT
CMD ["/bin/sh"]
# Thu, 05 Sep 2024 16:50:05 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Thu, 05 Sep 2024 16:50:05 GMT
ENV GOLANG_VERSION=1.23.1
# Thu, 05 Sep 2024 16:50:05 GMT
ENV GOTOOLCHAIN=local
# Thu, 05 Sep 2024 16:50:05 GMT
ENV GOPATH=/go
# Thu, 05 Sep 2024 16:50:05 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Sep 2024 16:50:05 GMT
COPY /target/ / # buildkit
# Thu, 05 Sep 2024 16:50:05 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Thu, 05 Sep 2024 16:50:05 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:ae2458422e4465e718700cd0c5970c709804ded4caa7b7f317eada5d16878e29`  
		Last Modified: Mon, 22 Jul 2024 21:49:42 GMT  
		Size: 3.4 MB (3365189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ccab56a7828fccbfbf3c5386b666669245e0d8f93e53acce7ed8222093ae62a`  
		Last Modified: Tue, 06 Aug 2024 23:54:15 GMT  
		Size: 291.8 KB (291782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4760cff10c149b56676c77cd8760221949ab26672a37406e0c3c20879d3fb9ee`  
		Last Modified: Thu, 05 Sep 2024 22:04:17 GMT  
		Size: 72.1 MB (72141445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e22287b6c39781bc06f8c45ae700de060397443c6f29fc2d6a7ba6884b4c9ce9`  
		Last Modified: Thu, 05 Sep 2024 22:04:15 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:975104239cbf1bbc29e1205c506966a068f6bd74a3e15a43e8e38a0597855b46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.8 KB (25751 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d345b59e6030d1c1ca5f4f9cc6cd4c5626f9d6c67a861ebf8cb85afae066f9c0`

```dockerfile
```

-	Layers:
	-	`sha256:52439b6f97d525dfc32f1f1e584d9432d6867cfc7f22c7af525f475aea2ac5cd`  
		Last Modified: Thu, 05 Sep 2024 22:04:15 GMT  
		Size: 25.8 KB (25751 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-alpine` - linux; arm variant v7

```console
$ docker pull golang@sha256:f8ce72191624e063a9fa0421dc3b82d38dca43a2d24346c59098dcf52bcf57a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.5 MB (75527526 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a829a7f639b1f95187ed6a59cd85444bc7dcd533fc446188fd304bd1ff640532`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Mon, 22 Jul 2024 21:59:47 GMT
ADD file:816da1ff7b962e1f52c650dfd66caeb2b88f3ab9fadc249c30f86ebe5372538c in / 
# Mon, 22 Jul 2024 21:59:47 GMT
CMD ["/bin/sh"]
# Thu, 05 Sep 2024 16:50:05 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Thu, 05 Sep 2024 16:50:05 GMT
ENV GOLANG_VERSION=1.23.1
# Thu, 05 Sep 2024 16:50:05 GMT
ENV GOTOOLCHAIN=local
# Thu, 05 Sep 2024 16:50:05 GMT
ENV GOPATH=/go
# Thu, 05 Sep 2024 16:50:05 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Sep 2024 16:50:05 GMT
COPY /target/ / # buildkit
# Thu, 05 Sep 2024 16:50:05 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Thu, 05 Sep 2024 16:50:05 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:9c6652a37da7fb600faac56897745bdde89a4f9bd260a082b6bf4a0d173b5906`  
		Last Modified: Mon, 22 Jul 2024 22:00:23 GMT  
		Size: 3.1 MB (3094960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76c7318d3e5485ead98a8a7ffd1815df0d57c2d4e91ee5f14b79d688de1ab2cd`  
		Last Modified: Wed, 07 Aug 2024 00:10:33 GMT  
		Size: 291.0 KB (290953 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edfeb4cb216a5c9d7c74247031f4f727e785d2b0477ebee2ffd136b94b292ead`  
		Last Modified: Fri, 06 Sep 2024 05:24:37 GMT  
		Size: 72.1 MB (72141455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:395f35611c65051451cf75f39e2d9a49e9010f0effb4c064fce1256a935a5553`  
		Last Modified: Fri, 06 Sep 2024 05:26:28 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:b4055da7e4c31f34477f6f342c503711a4c75e836032748b98bf66663957535b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.4 KB (232384 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79987410dc8ed6d75c77ac721a3368db805f81c764472dfe4790c554f167afb3`

```dockerfile
```

-	Layers:
	-	`sha256:8fe723ac89f89b2ae4ecc93a4beb83957a14de68b164e1f62c1ae0b5596b53bc`  
		Last Modified: Fri, 06 Sep 2024 05:26:28 GMT  
		Size: 206.4 KB (206413 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7e439fa58ba2a7232c6b3981bfe742d6beb4ee9bc79ef76acb69fa53511985bc`  
		Last Modified: Fri, 06 Sep 2024 05:26:28 GMT  
		Size: 26.0 KB (25971 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-alpine` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:7fc061b0c4e48920ba7fcd84e5eae946a6e9937727d6e192a09d8bf03542bdc8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.0 MB (75005234 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f13809c9794d3de14c9ea280a2300bbeedc8ca8fa20d48ff4a9260fac55a8de`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Mon, 22 Jul 2024 21:44:13 GMT
ADD file:a71f7e9bc66668361f88637c724c44deeb2774ec268ff0a68bd99014c8a02a84 in / 
# Mon, 22 Jul 2024 21:44:13 GMT
CMD ["/bin/sh"]
# Thu, 05 Sep 2024 16:50:05 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Thu, 05 Sep 2024 16:50:05 GMT
ENV GOLANG_VERSION=1.23.1
# Thu, 05 Sep 2024 16:50:05 GMT
ENV GOTOOLCHAIN=local
# Thu, 05 Sep 2024 16:50:05 GMT
ENV GOPATH=/go
# Thu, 05 Sep 2024 16:50:05 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Sep 2024 16:50:05 GMT
COPY /target/ / # buildkit
# Thu, 05 Sep 2024 16:50:05 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Thu, 05 Sep 2024 16:50:05 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:690e87867337b8441990047e169b892933e9006bdbcbed52ab7a356945477a4d`  
		Last Modified: Mon, 22 Jul 2024 21:44:38 GMT  
		Size: 4.1 MB (4086934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:171883aaf475f5dea5723bb43248d9cf3f3c3a7cf5927947a8bed4836bbccb62`  
		Last Modified: Tue, 06 Aug 2024 22:57:38 GMT  
		Size: 293.5 KB (293514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a355a3cac949bed5cda9c62103ceb0f004727cedcd2a17d7c9836aea1a452fda`  
		Last Modified: Thu, 05 Sep 2024 22:09:14 GMT  
		Size: 70.6 MB (70624628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c4c388ac50a370dc35feaa3a853b83dcb24a72d0a707d496c4a22a28459169b`  
		Last Modified: Thu, 05 Sep 2024 22:10:34 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:fc735f58073f047ddadf65ceb85b28d9e67ad96eb4c38edccb946f4ced6cd0f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.7 KB (232675 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a07a3039db662d04bcf17a205de826b1114b725f48eb57286f27e87ada92b17`

```dockerfile
```

-	Layers:
	-	`sha256:20aaaaa18690b93d72ed7d25fef434c5d8ab9184fcc10bf0a16b2f4ac2b2109c`  
		Last Modified: Thu, 05 Sep 2024 22:10:34 GMT  
		Size: 206.5 KB (206485 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cfd492b0a135e5002afee92a36e8d80532d9f52c438af7575d199377a550f09a`  
		Last Modified: Thu, 05 Sep 2024 22:10:34 GMT  
		Size: 26.2 KB (26190 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-alpine` - linux; 386

```console
$ docker pull golang@sha256:bdf2cf7673ae407996f6186a9f2a83899b8da8608417474ff246b65fe382d2cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.6 MB (75616852 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84690c6ef2f132feeda40ae8005b0ffcc1596f90240f481a29673f788b31f52f`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 05 Sep 2024 16:50:05 GMT
ADD file:00e6c22c1917031dd97c411814ae384c25a7f2bb91890494a73ea34f3c168453 in / 
# Thu, 05 Sep 2024 16:50:05 GMT
CMD ["/bin/sh"]
# Thu, 05 Sep 2024 16:50:05 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Thu, 05 Sep 2024 16:50:05 GMT
ENV GOLANG_VERSION=1.23.1
# Thu, 05 Sep 2024 16:50:05 GMT
ENV GOTOOLCHAIN=local
# Thu, 05 Sep 2024 16:50:05 GMT
ENV GOPATH=/go
# Thu, 05 Sep 2024 16:50:05 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Sep 2024 16:50:05 GMT
COPY /target/ / # buildkit
# Thu, 05 Sep 2024 16:50:05 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Thu, 05 Sep 2024 16:50:05 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:2689ac6c14fd48d5dbd1df1dd2d317f177e131f689c1a010922edcd778518efd`  
		Last Modified: Fri, 06 Sep 2024 22:41:47 GMT  
		Size: 3.5 MB (3469165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf3e05a548be191c2de1cd649a4090f8efdb1c141179f3be32b687ba44ae68fc`  
		Last Modified: Fri, 06 Sep 2024 23:19:56 GMT  
		Size: 291.3 KB (291347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ead5944571d35e19fa81ca655e6b7753cdb3e37418aa683e0c2a9c169e5d7256`  
		Last Modified: Thu, 05 Sep 2024 22:02:55 GMT  
		Size: 71.9 MB (71856183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b2539057123fdd6db415c39df2771e88fde56c52485b05dccf7f2d211fcf0d0`  
		Last Modified: Fri, 06 Sep 2024 23:19:56 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:25841bc3f2fdf90adbb0857619cb9a5f7bd82f47503cf87ffa61a2be040ae4c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.1 KB (232090 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36c83006013a12482863350cc793fb7c566014ac795000ae5a5c298d6f086879`

```dockerfile
```

-	Layers:
	-	`sha256:59c5c18d79b29f2155d093761033b7d6eb27f460ab94041f24834e93de9ad630`  
		Last Modified: Fri, 06 Sep 2024 23:19:56 GMT  
		Size: 206.3 KB (206300 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fec3a313b7aec1e86ca621de5373d33ef23b9fcf99d07802ebdb470c7f587726`  
		Last Modified: Fri, 06 Sep 2024 23:19:56 GMT  
		Size: 25.8 KB (25790 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-alpine` - linux; ppc64le

```console
$ docker pull golang@sha256:39347415071d1928a0d74e66c48e088ec17cb849b86e73b00d842abf53782374
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.7 MB (74664725 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:600026d3d397e3a8930126b2a3f2d187962164d25aa7dfcefb3a0d70ff320bf8`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Mon, 22 Jul 2024 21:26:21 GMT
ADD file:9fcad21b83b7efd6ef267ba714c3ef5a8d4d2064a0bdf528cbb17d0c3388f03f in / 
# Mon, 22 Jul 2024 21:26:22 GMT
CMD ["/bin/sh"]
# Thu, 05 Sep 2024 16:50:05 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Thu, 05 Sep 2024 16:50:05 GMT
ENV GOLANG_VERSION=1.23.1
# Thu, 05 Sep 2024 16:50:05 GMT
ENV GOTOOLCHAIN=local
# Thu, 05 Sep 2024 16:50:05 GMT
ENV GOPATH=/go
# Thu, 05 Sep 2024 16:50:05 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Sep 2024 16:50:05 GMT
COPY /target/ / # buildkit
# Thu, 05 Sep 2024 16:50:05 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Thu, 05 Sep 2024 16:50:05 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:6e59b4988c495782a5b0c8f8d6698931851c16c5c0fc5ef09cbb0637ade56e36`  
		Last Modified: Mon, 22 Jul 2024 21:26:52 GMT  
		Size: 3.6 MB (3571555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3799a78dfbed4f51d46b0331c523ca613f2dab716b4caeac0e3c3fc3a052197`  
		Last Modified: Tue, 06 Aug 2024 22:59:30 GMT  
		Size: 294.0 KB (294033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7e5b8a4bec9158fc0bc52aa7bb2055ac421fd36de9ea98898a7188751ff7da1`  
		Last Modified: Thu, 05 Sep 2024 23:28:18 GMT  
		Size: 70.8 MB (70798979 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d5c10e69f7968bd8d5885bdaf07e68b7afa75ce90fffa9fe4d32cb4d438c0e3`  
		Last Modified: Thu, 05 Sep 2024 23:30:23 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:9dcbe1a994dcec19c1469ad331312ab5b62ee6e0a8f03ba680885602b829dd17
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.4 KB (230430 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f551a4baa5c721a63867adc2ea1d1d831a321200ea604a5c84a57be23238ca0a`

```dockerfile
```

-	Layers:
	-	`sha256:0b8a2688d62243cbf5a3816fa0d2312297b19351c23db8f5ca88d011c2a7e6f0`  
		Last Modified: Thu, 05 Sep 2024 23:30:23 GMT  
		Size: 204.5 KB (204521 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7983645047b008cec189de04f17afb3f94b6c7a5efc98112fcaf6099b1a1b26d`  
		Last Modified: Thu, 05 Sep 2024 23:30:23 GMT  
		Size: 25.9 KB (25909 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-alpine` - linux; riscv64

```console
$ docker pull golang@sha256:2797caafaa40b9040ba7314875ed1bdd0b6a6bb5646580ee04bca4f0a0e29ab2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.9 MB (74857465 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:690cab9ef4f4cbd5e3bd3bc8ce8faaa394cbd0c84ebec95e5377a9daf141e340`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Mon, 22 Jul 2024 22:21:00 GMT
ADD file:cdf7088bbd70519f0f5d7b4249df34386e40f0194752f45842b3d85f2d331cf5 in / 
# Mon, 22 Jul 2024 22:21:00 GMT
CMD ["/bin/sh"]
# Thu, 05 Sep 2024 16:50:05 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Thu, 05 Sep 2024 16:50:05 GMT
ENV GOLANG_VERSION=1.23.1
# Thu, 05 Sep 2024 16:50:05 GMT
ENV GOTOOLCHAIN=local
# Thu, 05 Sep 2024 16:50:05 GMT
ENV GOPATH=/go
# Thu, 05 Sep 2024 16:50:05 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Sep 2024 16:50:05 GMT
COPY /target/ / # buildkit
# Thu, 05 Sep 2024 16:50:05 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Thu, 05 Sep 2024 16:50:05 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:faf447acae27573624c0613a79c4bcf1f9bc46d29f523140352abfd3f7691282`  
		Last Modified: Mon, 22 Jul 2024 22:21:18 GMT  
		Size: 3.4 MB (3370673 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32a571abf33b31d34423d7fdec7f124b736d3b8c4bf672ec686abf087f11f88a`  
		Last Modified: Tue, 06 Aug 2024 23:01:07 GMT  
		Size: 291.7 KB (291678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1b1852d94a6ac6376ee4ed6f339c1eb58a4860dffbd2cad412e5fde061f7a8a`  
		Last Modified: Thu, 05 Sep 2024 22:12:22 GMT  
		Size: 71.2 MB (71194956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb41d3f95d7bfee8796f3138f2257e25451d15309654ff43edd936bf6486bfeb`  
		Last Modified: Thu, 05 Sep 2024 22:12:12 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:4778507df7a4f5e235ebcc7f1bfd3070c3811fd35a3094148d88b970e6edac41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.4 KB (230426 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5fc48c099332b3cfc5c1f489868f57ad5f09677a352624feb1793c790f2d7c6c`

```dockerfile
```

-	Layers:
	-	`sha256:6f664305c56f0a9e8144715ddb349f33c3d4ccced76e1c0cce4128ef04513cae`  
		Last Modified: Thu, 05 Sep 2024 22:12:12 GMT  
		Size: 204.5 KB (204517 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dccdcd967dec291b92256f9a3a0e42931e1e6428b426a6216462c37b46a4d6c4`  
		Last Modified: Thu, 05 Sep 2024 22:12:12 GMT  
		Size: 25.9 KB (25909 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-alpine` - linux; s390x

```console
$ docker pull golang@sha256:8acf02849195eab7d04cfc91c2fb12b95689d81ccee6c3c7d1cfe0bd309a2277
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.7 MB (76673159 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:275606194e5fdb0d4d2a05ecf11ceac92613dde511aef1db1aa660d070cec3b2`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Mon, 22 Jul 2024 21:50:06 GMT
ADD file:63d382fb7a431c57868274a368a659bde32a60ae0cd05c8af34c3d6a57066a77 in / 
# Mon, 22 Jul 2024 21:50:07 GMT
CMD ["/bin/sh"]
# Thu, 05 Sep 2024 16:50:05 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Thu, 05 Sep 2024 16:50:05 GMT
ENV GOLANG_VERSION=1.23.1
# Thu, 05 Sep 2024 16:50:05 GMT
ENV GOTOOLCHAIN=local
# Thu, 05 Sep 2024 16:50:05 GMT
ENV GOPATH=/go
# Thu, 05 Sep 2024 16:50:05 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Sep 2024 16:50:05 GMT
COPY /target/ / # buildkit
# Thu, 05 Sep 2024 16:50:05 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Thu, 05 Sep 2024 16:50:05 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:834c666d55eae0e308600077be061a01680e7cd02b579be887d9469075f0d943`  
		Last Modified: Mon, 22 Jul 2024 21:51:06 GMT  
		Size: 3.5 MB (3461066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c6788457dbf91cadbba73a988a85659e72114e2e2870cccbfd281b6df34fa4c`  
		Last Modified: Fri, 06 Sep 2024 03:38:43 GMT  
		Size: 291.9 KB (291895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:492964f2ae9970b6023102de0a48c54b43149da01ab6bb1b356e5cf44a9f6145`  
		Last Modified: Fri, 06 Sep 2024 03:36:46 GMT  
		Size: 72.9 MB (72920040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd68f05b1514447d9c567f54b39e237313ba8f9aca4aaa04837c58e09059d3d7`  
		Last Modified: Fri, 06 Sep 2024 03:38:43 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:f112b19c00a23d14d494006afe2050186fd32f45f93dfcadbace681c002dcace
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.3 KB (230270 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81d7aebd8488456222d064c038ee4e9036ca5e1a24997bb0d68515a6fc6e928d`

```dockerfile
```

-	Layers:
	-	`sha256:3013aebc7a0b8c98b976d72591ad464b64bf4297a1937682a43ddc9447d81c28`  
		Last Modified: Fri, 06 Sep 2024 03:38:43 GMT  
		Size: 204.4 KB (204427 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:56dbe5bb99afa5a9caa6abcf8c51163e27b562909fede39c346752a3c58f6098`  
		Last Modified: Fri, 06 Sep 2024 03:38:43 GMT  
		Size: 25.8 KB (25843 bytes)  
		MIME: application/vnd.in-toto+json
