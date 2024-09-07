## `golang:alpine3.20`

```console
$ docker pull golang@sha256:fbc3a217775ee3ec2328077ad4f3681bbc2c4a812d63cc8c857c827f1e8e971f
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

### `golang:alpine3.20` - unknown; unknown

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

### `golang:alpine3.20` - linux; arm variant v6

```console
$ docker pull golang@sha256:3e3c8988558a9495fe6dfd8e96171d4f233ab0d155ba39f334e1c84605b2be59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.8 MB (75799875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d21ff18263488b322be7703d7f3cedaf3a24e397fdd6a39c284976deb556a26b`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 05 Sep 2024 16:50:05 GMT
ADD file:faa3509308d5524875c6afec4d4d1a357118aa1587e5485eca63c2907b37d968 in / 
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
	-	`sha256:97964a4b92f04f720ed681b3ec62b071ced94b08b57765c612866e77a71ec087`  
		Last Modified: Fri, 06 Sep 2024 22:49:47 GMT  
		Size: 3.4 MB (3366506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57b15e82573debca2fd0fd40f07ac032fefe7f9180bd45f4f9cf2c2afde7d486`  
		Last Modified: Sat, 07 Sep 2024 02:30:42 GMT  
		Size: 291.8 KB (291766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4760cff10c149b56676c77cd8760221949ab26672a37406e0c3c20879d3fb9ee`  
		Last Modified: Thu, 05 Sep 2024 22:04:17 GMT  
		Size: 72.1 MB (72141445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eefcd773902327cc973f87108a7dbad1ced56f254b294682398e2579e442d394`  
		Last Modified: Sat, 07 Sep 2024 02:30:42 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:alpine3.20` - unknown; unknown

```console
$ docker pull golang@sha256:24e9d184d7dc3fba13b197f10084f43e94ce5c0f2360ebea921eb87c8f0c18af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.8 KB (25752 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5db855a3b7ab546d88416d8f0a0e0ef808ae40d103fae7f6fedf6f817ddd266`

```dockerfile
```

-	Layers:
	-	`sha256:5505977179bf7a4f05a523ef2f942ef3ca0a4a4052c10f1fd0b8946b35dfd85c`  
		Last Modified: Sat, 07 Sep 2024 02:30:42 GMT  
		Size: 25.8 KB (25752 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:alpine3.20` - linux; arm variant v7

```console
$ docker pull golang@sha256:b64f829de854714e26ba2b6c0d29dbcb787393eb4f249767662c19d12dbb368e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.5 MB (75528063 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4fdc1d7c0d8c486e4fd112c7a75c6beae4d70842344aedd0d5e248ee47b8dc3e`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 05 Sep 2024 16:50:05 GMT
ADD file:8096a7e97160f837a432988b8138ffab07ff212be781f530c8baa2067265d071 in / 
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
	-	`sha256:da2748c71804914f58a58693c998a4885dd24623380daf301f4a1a88185cb4c8`  
		Last Modified: Fri, 06 Sep 2024 22:08:26 GMT  
		Size: 3.1 MB (3095502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:354df8adec1f26ac2f376cb666910440b4b25a704fec8a3d318f7aff11e80108`  
		Last Modified: Sat, 07 Sep 2024 02:43:40 GMT  
		Size: 290.9 KB (290948 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edfeb4cb216a5c9d7c74247031f4f727e785d2b0477ebee2ffd136b94b292ead`  
		Last Modified: Fri, 06 Sep 2024 05:24:37 GMT  
		Size: 72.1 MB (72141455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7584c0dcde22a140ca4f0ebb963966bb02fadf1ee1a0ef41625866f1a4360469`  
		Last Modified: Sat, 07 Sep 2024 02:43:40 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:alpine3.20` - unknown; unknown

```console
$ docker pull golang@sha256:adb40355e80eef4a0ca4720e9fa4814ad6525015a72c114da69b278bfc186eeb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.4 KB (232384 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ac4ae3697394276d400e26fb06153df5d79e3cf1c1b8d0dff2b9339e163e033`

```dockerfile
```

-	Layers:
	-	`sha256:87a074d4d92c076be28fc918688d9d776901cd834c9126950203660dc8744aa8`  
		Last Modified: Sat, 07 Sep 2024 02:43:40 GMT  
		Size: 206.4 KB (206413 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:05b9a160b36087109f6b211b412dcfafa3c49d9770769b8cadef2783324fc13b`  
		Last Modified: Sat, 07 Sep 2024 02:43:40 GMT  
		Size: 26.0 KB (25971 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:alpine3.20` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:779ec1419250e4c96273bab8a7aa4e06f68e8fba0d4928bd6f6d86baa4f7bf82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.0 MB (75005933 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07228514b78b57adcf9b81fa791a62f3003088958e0afcee6fd09f297abb9370`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 05 Sep 2024 16:50:05 GMT
ADD file:ee5bb8409915b11413f44cce4c22fed658aba4fb078a448e08dd4ac9a23581f2 in / 
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
	-	`sha256:cf04c63912e16506c4413937c7f4579018e4bb25c272d989789cfba77b12f951`  
		Last Modified: Fri, 06 Sep 2024 22:44:39 GMT  
		Size: 4.1 MB (4087646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cac1a4b065c9c855fffe18402bb1a7f6f7e3d3c997a5d6efece488ea46d240e`  
		Last Modified: Sat, 07 Sep 2024 05:15:25 GMT  
		Size: 293.5 KB (293502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a355a3cac949bed5cda9c62103ceb0f004727cedcd2a17d7c9836aea1a452fda`  
		Last Modified: Thu, 05 Sep 2024 22:09:14 GMT  
		Size: 70.6 MB (70624628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:391ae752cf17d63466dfc6a65b5ea06393c5e072568fed74b4365617fd9d56df`  
		Last Modified: Sat, 07 Sep 2024 05:15:24 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:alpine3.20` - unknown; unknown

```console
$ docker pull golang@sha256:61cebc6a06905ad0c56150aa41789a182c25986ede7fcfa1704bfb63665b0e4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.7 KB (232676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86c12bf8137cf47251f7a2e6f655368094d365fcbe5b60e01d1b598f568224c1`

```dockerfile
```

-	Layers:
	-	`sha256:eadc62f9006892e061dfc5a14be7db26cadefafa71c19434351425cf8706629e`  
		Last Modified: Sat, 07 Sep 2024 05:15:25 GMT  
		Size: 206.5 KB (206485 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e495fa35722fee7fd75a1fc78ad7a17663f33cdc33702c6790e4559f416ac6df`  
		Last Modified: Sat, 07 Sep 2024 05:15:24 GMT  
		Size: 26.2 KB (26191 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:alpine3.20` - linux; 386

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

### `golang:alpine3.20` - unknown; unknown

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

### `golang:alpine3.20` - linux; ppc64le

```console
$ docker pull golang@sha256:daa09b3102b387aace4cc7cc7284285b6e0d9d809e98515636cbeefde15cbb23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.7 MB (74665563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfaa090736a04657210c02a5ecd03800a9079f78c302aef0d63d4f9dd360d213`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 05 Sep 2024 16:50:05 GMT
ADD file:c1f14e23acaff59e2dc7a11f65f8fdfbed8be1350a135493a06b692ecefb26cc in / 
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
	-	`sha256:b5caf700653f785a3409fb40484075ff91a3a7a84b79ad6a91b165589b35fbc0`  
		Last Modified: Fri, 06 Sep 2024 22:26:38 GMT  
		Size: 3.6 MB (3572419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63f84e45b04d7b25e1e5813237e957c825c0ed033a4dca7930a9882de8427e0e`  
		Last Modified: Sat, 07 Sep 2024 06:52:19 GMT  
		Size: 294.0 KB (294009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7e5b8a4bec9158fc0bc52aa7bb2055ac421fd36de9ea98898a7188751ff7da1`  
		Last Modified: Thu, 05 Sep 2024 23:28:18 GMT  
		Size: 70.8 MB (70798979 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce0412bf96a18e39e4fc65b2d2db5a212a2df1148afaf9c5afd709af8ec7e4ed`  
		Last Modified: Sat, 07 Sep 2024 06:52:19 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:alpine3.20` - unknown; unknown

```console
$ docker pull golang@sha256:a3554fae04a0f57b24af9c462e909358bf01ab77b34552917d4e5b1ae44ca4ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.4 KB (230430 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6cd7ef88ba22129d9ec52e225abd6192a2acc0747b5a98613d0e1bd285d03cdb`

```dockerfile
```

-	Layers:
	-	`sha256:1e8744354eecd90e9b4b32668c603649946d8ed1f307d6e10895b791164545f6`  
		Last Modified: Sat, 07 Sep 2024 06:52:19 GMT  
		Size: 204.5 KB (204521 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cd592907543e9e2a74d6864adb267432a1b7d362156bca614d225de296113082`  
		Last Modified: Sat, 07 Sep 2024 06:52:19 GMT  
		Size: 25.9 KB (25909 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:alpine3.20` - linux; riscv64

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

### `golang:alpine3.20` - unknown; unknown

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

### `golang:alpine3.20` - linux; s390x

```console
$ docker pull golang@sha256:d960fa028af5fd379254f715a12f650647060291d0d2ca5bc51afa8736c22003
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.7 MB (76673688 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12e7e5ed5758e58ae6ca2ea8f5dbf8259d8074ed09ea2869f66269f7a176f189`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 05 Sep 2024 16:50:05 GMT
ADD file:ba2637314e600db5a647501cf1ab287c5f51de1627c13bc1d82aa48925a3dd78 in / 
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
	-	`sha256:df110db6acd600b9ee5ebd7b510779652f96424d3f80321a4e0dcb8a09aa0526`  
		Last Modified: Fri, 06 Sep 2024 22:48:57 GMT  
		Size: 3.5 MB (3461598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f17125b2ca65c3fc030a73292bd9a81e96c5921e35f14f3aa5165a3777ebe8b5`  
		Last Modified: Sat, 07 Sep 2024 02:36:48 GMT  
		Size: 291.9 KB (291892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:492964f2ae9970b6023102de0a48c54b43149da01ab6bb1b356e5cf44a9f6145`  
		Last Modified: Fri, 06 Sep 2024 03:36:46 GMT  
		Size: 72.9 MB (72920040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9e218ce396551667075ff8bb0b2a2d750e4bc6dd58940cd93c2496e86f7784c`  
		Last Modified: Sat, 07 Sep 2024 02:36:48 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:alpine3.20` - unknown; unknown

```console
$ docker pull golang@sha256:ce30eadd53e04858eaf7a1b00123221bae7e894fb7c720c2181827e05541b5ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.3 KB (230269 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8448205d15147160e550bb01b4862d838886d3b6e44d17a6b9581c102188157`

```dockerfile
```

-	Layers:
	-	`sha256:3e07d0d9b872d1ff0b89bd3b8a9596d7b708738fade6dfb5a776c6ed1179151f`  
		Last Modified: Sat, 07 Sep 2024 02:36:48 GMT  
		Size: 204.4 KB (204427 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f8055e2627901d832f872dae577ef87f228879c61456f5ce198ecded28d50803`  
		Last Modified: Sat, 07 Sep 2024 02:36:48 GMT  
		Size: 25.8 KB (25842 bytes)  
		MIME: application/vnd.in-toto+json
